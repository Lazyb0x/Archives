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

在 GitHub 里面解析 `[名字](链接)`时并不会解析所有协议，例如 `[gparted](apt://gparted)` 和 `[zh_groups](tg://resolve?domain=zh_groups_bot)` 这样的写法并不会被解析成超链接。

解决办法：利用 GitPages 可以展示 HTML 页面，先把链接地址改成 GitPages 中的页面，再由该页面通过 Js 的 `window.location` 跳转。

```html
<script language="javascript" type="text/javascript">
function GetQueryString(name) {
	var reg = new RegExp('(^|&)' + name + '=([^&]*)(&|$)', 'i');
	var r = window.location.search.substr(1).match(reg);
	if (r != null)
		return unescape(r[2]);
	return null;
}

var myurl=GetQueryString("url");
if(myurl !=null && myurl.toString().length>1){
	window.location.href=GetQueryString("url");
}
else{
	document.write("无 url 参数。")
}
</script>
```

原生：

```markdown
[CSGO，启动！](steam://rungame/730/76561202255233023/)
```

[CSGO，启动！](steam://rungame/730/76561202255233023/)

跳转：

```markdown
[CSGO，启动！](https://Lazyb0x.github.io/jump?url=steam://rungame/730/76561202255233023/)
```

[CSGO，启动！](https://Lazyb0x.github.io/jump?url=steam://rungame/730/76561202255233023/)