# 存档及备忘
这里存放一些实用的批处理，配置文件等，以及编译完成的程序。

## Github单个文件夹下载

要下载单个文件或文件夹可能比较不方便，下面是找到的几种方法：

* ##### Raw按钮

  在Raw按钮上右键点击文件另存为，可以保存文件。

* ##### DownGit

  [这里](https://minhaskamal.github.io/DownGit/#/home)，可以直接下载打包成zip的文件夹，但总是抽风。

* ##### SVN

  **Windows** : TortoiseSVN [官网下载](https://tortoisesvn.net/downloads.html) [百度下载](http://rj.baidu.com/search/index/?kw=TortoiseSVN)

  **Ubuntu** : Subversion <a href="https://Lazyb0x.github.io/jump?url=apt://subversion" target="_blank">点我安装</a>

  或者使用命令:
  ```shell
  sudo apt install subversion
  ```
  将仓库名和下一个文件夹名之间的分支信息`tree/master`改为`trunk`。

  如`https://github.com/probonopd/linuxdeployqt/tree/master/tools/linuxdeployqt`

  改为`https://github.com/probonopd/linuxdeployqt/trunk/tools/linuxdeployqt`

  下载该链接

  Windows在文件浏览器下右键 -> SVN Checkout，填入链接下载。

  Subversion使用命令`svn co [链接]`。

## .md 文件超链接

[测试apt](apt://gparted)

[测试tg](tg://resolve?domain=zh_groups)