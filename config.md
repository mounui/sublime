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

## 快捷键设置

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

> 代码快速补全 Emmet语法

##### FileDiffs

> 文件对比

##### HTML-CSS-JS Prettify

> 代码格式化插件
>
> 它可以代替很多其他格式化插件，如TAG，CssComb和JSFormat

##### jQuery

> jQuery代码片段

##### SublimeLinter

> 行内语法检测插件
>
> - SublimeLinter-contrib-htmlhint -- 用于HTML的SublimeLinter插件，基于nodeJS下的htmlhint的插件
>
> - SublimeLinter-csslint -- 用于CSS的SublimeLinter插件，基于nodeJS下的csslint的插件
>
> - SublimeLinter-jshint -- 用于JS的SublimeLinter插件，基于nodeJS下的jshint的插件
>
> - SublimeLinter-php -- php语法检查

```json
// SublimeLinter Settings - User
{
    "delay": 0.3,
    // 语法检查模式 文件打开和保存时
    "lint_mode": "load_save",
    "paths": {
        "linux": [],
        "osx": [],
        "windows": [
            // 配置php路径使php语法检查起作用
            // "C:\\wamp\\bin\\php\\php5.6.40",
            // "C:\\wamp\\bin\\php\\php7.3.12",
            "C:\\wamp\\bin\\php\\php7.4.9"
        ]
    },
    "linters": {
        // htmlhint配置
        "htmlhint": {
            // 关闭语法检查
            "disable": false,
            // 自定义的配置文件
            "args": [
                // "--config",
                // "D:\\mine\\htmlhint.conf"
            ],
            // 排除
            "excludes": ["*.php"],
            // 检查范围scope，使用Tools->Develper->Show Scope Name查看当前文档的scope
            // 针对特定范围的文件检查，多个用,隔开。- 表示排除
            "selector": "text.html.basic - source.php",
        },
        // csslint配置
        "csslint": {
            "disable": false,
            "excludes": [],
            "filter_errors": [],
            // 忽略语法检查选项
            "ignore": [
                "unique-headings",
                "qualified-headings",
                "font-sizes",
                "floats",
                "box-model",
                "box-sizing",
                "compatible-vendor-prefixes",
                "outline-none",
                "ids",
                "order-alphabetical",
                "zero-units",
                "universal-selector",
                "import",
                "gradients",
                "fallback-colors",
                "duplicate-properties"
            ],
        },
        "php": {
            "disable": false,
            // "selector": "source.php,embedding.php,meta.embedded.block.php,meta.function.php,meta.block.php,meta.group.php,variable.other.php,punctuation.definition.variable.php",
        }
    }
}
```

##### TrailingSpaces

> 突出显示尾随空格，删除它们