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

##### Package Control

> 包管理器 配置

```json
{
	// 插件更新目录 下载慢时可以修改为国内地址
	"channels": [
		"http://packagecontrol.cn/channel_v3.json"
	]
}
```

##### Alignment

> 代码对齐插件

##### AutoFileName

> 路径/文件自动提示插件

##### ChineseLocalizations

> 汉化包插件

##### ConvertToUTF8

> 转换编码插件
>
> 通过本插件可以编辑并保存目前编码不被 Sublime Text 支持的文件

##### DeleteBlankLines

> 删除空行插件

##### DocBlockr

> 文档注释插件

```json
{
    "jsdocs_extra_tags": [
        "@Author 木凡",
        "@DateTime {{datetime}}",
        "@Email maojunhui5214@163.com",
        "@Domian http://mounui.com"
    ],
    "jsdocs_extra_tags": [
        "@Author mao",
        "@DateTime {{datetime}}",
    ],
}
```

##### Emmet

> Emmet语法

##### FileDiffs

> 文件对比

##### HTML-CSS-JS Prettify

```json
{
    // Simply using `node` without specifying a path sometimes doesn't work :(
    // https://github.com/victorporof/Sublime-HTMLPrettify#oh-noez-command-not-found
    // http://nodejs.org/#download
    "node_path":
    {
        "windows": "C:/Program Files/nodejs/node.exe",
        "linux": "/usr/bin/nodejs",
        "osx": "/usr/local/bin/node"
    },

    // Automatically format when a file is saved.
    "format_on_save": false,

    // Automatically format when a file is opened. (Sublime Text 3 only)
    "format_on_open": false,

    // Automatically format when a file is focused. (Sublime Text 3 only)
    "format_on_focus": false,

    // Automatically format when a file loses focus. (Sublime Text 3 only)
    "format_on_focus_lost": false,

    // Automatically format while a file is being edited. (Experimental / Sublime Text 3 only)
    "format_while_editing": false,

    // Only format the selection if there's one available.
    "format_selection_only": true,

    // Save to a temporary file before prettifying.
    "save_to_temp_file_before_prettifying": true,

    // Settings determining which files are allowed to be prettified.
    // !!! All the keys below need to be included in your user settings for them to work. !!!
    "global_file_rules":
    {
        // Be sure to include all of the `html`, `css`, `js` and `json` keys in your user settings
        // if you want to be able to prettify the default files as well.
        "html":
        {
            "allowed_file_extensions": ["htm", "html", "xhtml", "shtml", "xml", "svg", "vue"],
            "allowed_file_syntaxes": ["html", "xml", "vue"],
            "disallowed_file_patterns": []
        },
        // Be sure to include all of the `html`, `css`, `js` and `json` keys in your user settings
        // if you want to be able to prettify the default files as well.
        "css":
        {
            "allowed_file_extensions": ["css", "scss", "sass", "less"],
            "allowed_file_syntaxes": ["css", "sass", "less"],
            "disallowed_file_patterns": []
        },
        // Be sure to include all of the `html`, `css`, `js` and `json` keys in your user settings
        // if you want to be able to prettify the default files as well.
        "js":
        {
            "allowed_file_extensions": ["js", "jsx"],
            "allowed_file_syntaxes": ["javascript", "ecma", "react", "babel"],
            "disallowed_file_patterns": []
        },
        // Be sure to include all of the `html`, `css`, `js` and `json` keys in your user settings
        // if you want to be able to prettify the default files as well.
        "json":
        {
            "allowed_file_extensions": [
                "json",
                "babelrc",
                "eslintrc",
                "jshintrc",
                "jsbeautifyrc",
                "sublime-settings",
                "sublime-keymap",
                "sublime-commands",
                "sublime-menu"
            ],
            "allowed_file_syntaxes": ["json"],
            "disallowed_file_patterns": []
        }
    },

    // Respect `.editorconfig` rules, overriding settings from `.jsbeautifyrc`.
    // Note that `use_editor_syntax` and `use_editor_indentation` have precedence
    // and will always override any other settings from any configuration file
    // like `.jsbeautifyrc` and `.editorconfig`.
    "respect_editorconfig_files": true,

    // Use current syntax to determine file type, instead of the extension.
    "use_editor_syntax": true,

    // Use current identation settings to override the ones from `.jsbeautifyrc`.
    "use_editor_indentation": false,

    // Log the settings passed to the prettifier from `.jsbeautifyrc`.
    "print_diagnostics": true
}
```



#### SublimeLinter

#### SublimeLinter-contrib-htmlhint

#### SublimeLinter-csslint

#### SublimeLinter-jshint

#### SublimeLinter-php

#### TrailingSpaces

#### jQuery

keymap

```json
[
	// 系统快捷键 //
	// 保存全部
	{ "keys": ["ctrl+alt+s"], "command": "save_all" },
	// Trailing​Spaces插件快捷键 //
	// 删除行尾空格
	{ "keys": ["ctrl+alt+t"], "command": "delete_trailing_spaces" },
	// 切换空格高亮显示
	{ "keys": ["ctrl+alt+d"], "command": "toggle_trailing_spaces" }
]

```

