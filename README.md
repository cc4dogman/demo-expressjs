# 云函数Expressjs示例

此插件为express的demo使用样例，修改自官方的基础demo而来，主要增加了express框架的适配，支持服务器单路由，支持callFunction和url云化的同时调用

# 1. 安装指引

    1 .点击右上角 使用HBuilderX导入插件，将云函数模板导入到您的项目中（导入后检查expresjs目录下如果没有node_modules的自行安装一次）
    2 .将云函数 上传部署 到您的云服务空间（初始化云函数和云数据库）
    3 .直接启动到内置浏览器即可


# 2. 代码说明

由于目前云函数在上传的时候不支持指定目录上传，所以把具体的后端业务代码放在了目录首层(expressjs),目录名称可以随意修改，可以认为是一个独立的后端项目，demo没有增加views视图组件，云函数目前已提供api服务为准，尽量减少不必要的依赖包提高响应速度


使用rollup作为优化打包工具，将expressjs目录下的文件合并打包到云函数目录下，具体可参看里面的rollup.config.js
执行优化并打包到云函数目录下
```bash
npm run build
```


目前只在阿里云测试过，腾讯云暂未测试，理论上应该也行，不过要自己去修改了，源码可以随意修改的