# EasyDoc

`The new version v2.0.1 has been released, users are welcome to update and download timely use.`

`新版本 v2.0.1 已发布，欢迎用户及时更新和下载使用。`

### Documentation

- [中文文档](https://wuyumin.github.io/easydoc/dist/zh-CN.html)
- [English Document](https://wuyumin.github.io/easydoc/dist/en.html)

### What is EasyDoc?

EasyDoc, `Easy` to generate `Documents`.

EasyDoc pronunciation [ˈiziˈdɑk] [sound file](https://wuyumin.github.io/easydoc/dist/static/EasyDoc.mp3)

### Communication

- GitHub: <https://github.com/wuyumin/easydoc> Welcome star it

### Software Updates and Downloads

[link to download software](https://github.com/wuyumin/easydoc/releases) (Compressed package need to extract the software file.)

Only one software file, do not install, not to rely on others, support to Microsoft system computer, Apple system computer, Linux system computer.

How to update the software: Please download the new software file overwrite the old software file.

EasyDoc is developed by Go language, open source software, you can use the source code to compile. In fact, you do not have to do that, we have compiled and optimized software for download.

### Command Line to Use

> Ensure that easydoc software file can executable!

software file in the current directory:  
Windows system `$ easydoc -version`  
Unix-like system (such as Mac, Linux. Note that in front of ./ ) `$ ./easydoc -version`  
You can put easydoc software file in the global environment directory(recommended use this), Using anywhere `$ easydoc -version`.

##### EasyDoc Currently Supported Command:

> Do not forget to a small horizontal line in front of!

`-init` Init the document structure  
`-build` Build the document  
`-server` Start web server(used[or not] with the port `-port` and the path` -path`, the default port is 80 `-port 80`, the default path is dist directory`-path ./dist`)  
`-emptydist` Empty dist directory  
`-help` Help about EasyDoc  
`-version` Print the version number of EasyDoc  

Static documents which Generated by EasyDoc are placed in the `dist` directory, use or copy this directory directly as a site directory.

### Basic Directory Structure

Use `-init` command automatically generate

```html
├── dist  //release directory
├── config
│   └── config.toml  //Configuration file, using toml syntax
├── src  //Writing directory: store .md source files(required, support to store in this directory and its subdirectories)
│   ├── index.md  //Home(not required, but recommended)
│   ├── NO-asset-folder.txt  //To avoid conflicts, prompt src directory with caution asset and static subdirectory
│   └── NO-static-folder.txt
├── static  //Static file directory, this directory will be completely copied to the release directory(Flexibility to use it for file layout)
└── theme  //Template directory (support multiple sets of templates)
    └── default  //This default template
        ├── css
        │   └── style.css //Css file in template(No,use the software's default)
        ├── js
        │   └── app.js //Js file in the template(No,use the software's default)
        ├── doc.tpl  //Document template(No,use the software's default)
        └── menu.tpl //Menu template(The menu is generated in order, Explanations below.)
├── easydoc.exe  //software file(Recommended put it on the global environment directory
```

- `Source files written using Markdown syntax. `Writing is in the src directory, multi-level subdirectory support (hint: src directory caution asset and static subdirectories).
- Generate web links wrong path, you can use config.toml the fixLink fix (absolute path is better).
- Menu generation by order: menu.tpl template content is not empty > The scanFile array for config.toml is not empty(The setting title as the link title) > Automatic scanning .md files in src directory to generation(The filename[no suffix] as the link title).
- Document generation by order: The scanFile array for config.toml is not empty(The setting title as the document title) > Automatic scanning .md files in src directory to generation(The filename[no suffix] as the document title).
- config.toml scanFile array fill format：

```html
scanFile = [
	["Link title", "base on src directory, src beginning of character, .md file path(support external link)"],
	["Home", "src/index.md"],
	["XXX page", "src/sub/XXX.md"],
]
```

### Contribution

GitHub: <https://github.com/wuyumin/easydoc> Welcome star it  
Suggest or help us to improve: [submit an issue to us](https://github.com/wuyumin/easydoc/issues) or [pull request to us](https://github.com/wuyumin/easydoc/pulls).

### Who Use EasyDoc

Welcome to provide "Who Use EasyDoc".

- [EasyDoc Document Website](https://wuyumin.github.io/easydoc)
