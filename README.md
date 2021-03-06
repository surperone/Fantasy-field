# 幻想领域

[哇塞，终于有一款属于自己的图床了.](http://www.52ecy.cn/post-68.html "幻想领域")

幻想领域是使用 PHP 语言开发的一款轻量级的新浪图床系统.

它的诞生，并不是最终的解决方案，开发它的目的是为了方便自己使用.

# 系统介绍

在 幻想领域 中, 图床图片全部托管在新浪云, 每张图片都有多张不同级别的缩略图.这便是幻想领域的最大特色之一.

拥有较为完善的用户系统与管理员系统。管理员在后台拥有完全权限，对网站的一切基本配置

我的图库，将会罗列出用户自己所上传的所有图片，管理员则显示系统托管的所有图片.你可以在这里对图片进行删除、预览或者复制它，但删除仅仅只是不再出现在本系统中，图片仍然是存在于新浪之上，这点你是要知道的.

探索，它是前台对用户图片预览的功能，在这里你可以发现和找到你需要的东西.如果你不需要它，可以在后台进行关闭设置.

上传新浪图床并非无要求，它需要你进行登录验证，但我们拥有一套独立的新浪登录程序，不依赖任何扩展，并且无验证码，cookie过期将自动为你进行登录，为你解决一切后顾之忧，所以你必须在后台设置你的新浪账号密码才能正常使用.


# 安装

你需要将幻想领域的源代码解压缩并上传至网站根目录，访问网站域名会自动跳转到安装程序，根据向导提示安装即可。如果未跳转，请手动访问http://您的域名/install.php 进行安装

首次安装成功后需要登录管理员后台对图床进行一些基本配置，才能使用

后台地址：http://您的域名/admin  但是讽刺的是，您需要在前台进行登录


## 环境支持

> 请注意，幻想领域自1.0版本起只支持PHP版本≥5.6，请注意更新您的PHP版本。     

## Miya's Edit

于是在原作者宣布停止维护半年后,个人Fork了一下这个项目,fork了也没干什么别的,大概就做了三件事:

1. 修改掉内置的库的链接,这样布局就不会乱了

2. 修改了一些 CSS ,保证在现代浏览器下显示没有不违和的地方

3. 在 `.htaccess` 中内置了两套方案以解决验证码不显示问题

如果还说有一点什么成绩那就是还补充了[这个文档](#修改部分详情(2018.10.14)).很惭愧,就只做了三件微小的工作,谢谢大家



## 修改部分详情(2018.10.14)

1. 将公共库从 BootCDN 迁移至七牛公共云存储

- 一部分已经无法使用 CDN 且代码量较少的库将采用内联样式( IE10 兼容库 )

2. 修改掉左上角标题的定位位置防止错位

- 删除掉为了保证 IE10兼容而给标题添加的`margin-top:10px`这条 CSS

3. 在`.htaccess`中添加一套配置(默认为注释状态)用于适配二级目录及修复验证码不显示问题

- 若你的图床链接地址为`https://yoursite.site` 的形式,则使用默认第一种

- 若你的图床建立在二级目录(链接地址为`https://yoursite.site/img` 或 `https://img.yoursite.site` )的情况下,请注释掉或删掉第一种配置,并删除掉第二种配置每行前面的`#`号

- 宝塔面板用户请直接使用面板中的 ThinkPHP 伪静态设置(来自原作者)

# 效果展示

![](https://ws1.sinaimg.cn/large/0072Vf1pgy1fp4ju6yg11j30xe0mp102.jpg)

