## 用户设置

打开sublime > 首选项 > 设置 复制以下内容粘贴进去

```json
{
	"font_face": "YaHei Consolas Hybrid",
	"font_size": 14,
	"ignored_packages":
	[
		"Vintage"
	],
	"update_check": false,
	"word_wrap": false
}
```

## 常用插件

### 插件控制台Package Control安装

通过`ctrl*+*` 或 View *>* Show Console打开控制台，将Python代码粘贴到控制台，回车

```python
import urllib.request,os,hashlib; h = '6f4c264a24d933ce70df5dedcf1dcaee' + 'ebe013ee18cced0ef93d5f746d80ef60'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.cn/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)
```

### 常用插件

###### Package Control

##### ChineseLocalizations

##### **ChineseLo**

#### SublimeLinter

#### SublimeLinter-contrib-htmlhint

#### SublimeLinter-csslint

#### SublimeLinter-jshint

#### SublimeLinter-php

#### HTML-CSS-JS Prettify

#### Emmet2

#### FileDiffs

#### DocBlockr

#### TrailingSpaces

#### Alignment

#### jQuery