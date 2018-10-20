IntelliJ IDEA 安装Golang插件
nickso · 2017-08-16 10:03:19 · 6914 次点击 · 预计阅读时间 1 分钟 · 7分钟之前 开始浏览    
这是一个创建于 2017-08-16 10:03:19 的文章，其中的信息可能已经有所发展或是发生改变。
网上的例子比较多，这里不重复，只解决我遇到的  --新版本的Intellij无法安装插件的问题。

1、输入仓库网址，搜索不到新的golang插件

2、从https://plugins.jetbrains.com/plugin/5047-go-language-golang-org-support-plugin下载插件，选择 “install plugin from disk”，提示plugin ×××　is incompatible with this installation。

３、满足 1、2后恭喜你，无可适配的插件版本。 解压插件zip包，找到lib中 intellij-go-***.jar ，打开jar中的META-INF\plugin.xml，修改 <idea-version since-build="AAA.BBBB" until-build="AAA.*"/> （你的idea版本是 AAA.BBBB.CCC,自己找readme），替换好后，从新打zip包。 

然后，就可以安装了