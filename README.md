### Magento2 中文语言包
目前网上有很多Magento2中文语言包，我尝试过各种版本的中文语言包，大多让人感觉翻译生硬，不够本土化。本语言包基于[Crowdin](https://crowdin.com/)网站上[Magento2官方翻译项目](https://crowdin.com/project/magento-2/zh-CN)生成，并参考第三方中文语言包（[Magento2Translations](https://github.com/Magento2Translations/language_zh_hans_cn), [mageplaza](https://github.com/mageplaza/magento-2-chinese-language-pack)）翻译结果，新增部分词条，完善大量的词条翻译。语言包尚存不足之处，我会持续地更新迭代加以完善，同时希望大家一起贡献代码，体验更好的Magento2中文版。

### 安装语言包
**Composer安装**
```
cd <magento2 path>
composer require benheart/magento2_zh_hans_cn:dev-master
php bin/magento cache:clean && php bin/magento setup:static-content:deploy zh_Hans_CN
```
**手动安装**
- [下载 Magento2 中文包](https://github.com/benheart/magento2_zh_hans_cn/archive/master.zip)
- 解压并上传文件到指定目录：\<magento2 path\>/app/i18n/benheart/magento2_zh_hans_cn
- 在Magento2根目录执行命令：
```
php bin/magento cache:clean && php bin/magento setup:static-content:deploy zh_Hans_CN
```
- 登录Magento2管理后台，选择中文语言包：Stores -> Configuration -> General > General -> Locale options -> Chinese (China)
![后台总览](http://i.imgur.com/1zS25hH.png)

### 截图演示
**管理员**
- 后台总览
![后台总览](http://i.imgur.com/dc6h7iV.png)
- 二级目录
![二级目录](http://i.imgur.com/ocvTAlt.png)
- 商品列表
![商品列表](http://i.imgur.com/hVlMnrm.png)

**用户前端**
- 首页
![首页](http://i.imgur.com/tKuVJO4.png)
- 个人中心
![个人中心](http://i.imgur.com/FYGpSfB.png)
- 商品列表
![商品列表](http://i.imgur.com/GXnGFvQ.png)
- 商品详情页
![商品详情页](http://i.imgur.com/2CAWCk4.png)

### 贡献代码
- Fork本项目到你GitHub仓库中
- Clone你GitHub上本项目到本地
- 本地修改完善语言包，Commit到本地仓库
- Push新增和改动代码到你GitHub上本项目
- Pull request, 审核通过后合并到主干

### 卸载语言包
```
cd <magento2 path>
composer remove benheart/magento2_zh_hans_cn:dev-master
```

### 注意事项
- 官方Magento2.1.3+存在[Bug](https://github.com/magento/magento2/issues/7862)会导致Js翻译出现问题
- 安装本中文包前请备份Magento2