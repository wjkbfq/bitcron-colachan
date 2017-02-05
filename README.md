## 写给从Farbox过来的朋友

肯定有许多朋友是从Farbox过来的，Bitcron与Farbox是同一个作者，这套博客系统可以说是Farbox的升级重制版。虽然外表看起来没有多大的变化，但是系统底层可以说是翻天覆地，能够创造的可能性比Farbox要大得多。

如果你之前有自己的Farbox模板，迁移过来也并不难。粗略估计，Farbox模板想用在Bitcron里，需要改动的代码量不会超过5%。只是你需要仔细看看Bitcron的API，细微差异还是有的。

## 可乐橙的Bitcron博客模版源码

可乐橙要提醒一下，这是[Bitcron](https://bitcron.com/)模板，它不能用在wordpress或其他博客系统中。

老实说这不是个多么灵活的模板，没有自定义背景图，没有自定义主题颜色，而且多数内容都是静态的，基本是按照可乐橙自己的需求定制的。

但是我相信，既然你有兴趣采用Bitcron这套博客系统，一定是个热爱钻研之人，水平一定在我之上，将它改造成你的专属模版一定不在话下。

注：还可以[在此下载相关设计资源](https://www.dropbox.com/sh/35zp8ef7t2w4d43/AADSv0YaAHX-74GAG5xUNWIpa?dl=0)，请随意取用，希望你喜欢。

实际效果请参考[colachan.com](http://colachan.com/)

## FAQ

### 首页首屏中央的文字要怎么改？

这里由于用了特殊字体，所以我做成图片了。在开发人员工具里可以看到有张背景图slogen.png。所以，要改掉这里文字，有两个办法：

1. 自己做一张新的slogen.png，把url替换掉。
2. 去掉背景图，改用浏览器支持的字体实现。

### 主导航的菜单项如何修改？ 

在include文件夹下的header.jade里，都是静态的，需要手工修改。

### 日志分类如何实现？

在Dropbox对应的网站目录下新建文件夹，用分类名来命名（生活、相册、设计等等），把相应文章放进去就可以了。

### 为什么多说评论出不来？

为了保证多说评论组件的可靠性，也为了方便我自己管理多说文章唯一key，可乐橙把多处评论相关代码都写死了。post.jade里的部分，控制所有文章的评论。几个特殊页面的评论分别写在对应的.jade文件里。由于我在多说里给自己的域名加了白名单，所以在你自己的域名下调用会报错，改成你的多说账号信息就可以了。