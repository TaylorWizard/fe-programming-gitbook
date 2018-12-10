## Commander Module

> 提供了用户命令行输入各参数解析的强大功能, 可以帮助我们简化命令行开发
>
> [教你从零开始搭建一款前端脚手架工具](https://segmentfault.com/a/1190000006190814)](https://segmentfault.com/a/1190000006190814)

#### API

| API         | Remark                                                       |
| ----------- | ------------------------------------------------------------ |
| command     | 定义命令行指令，后面可跟上一个name， 用空格隔开              |
| alias       | 定义一个更短的命令行指令 ，如执行命令**$ app m** 与之是等价的 |
| description | 描述，它会在help里面展示                                     |
| option      | 接受4个参数<br>第一个参数中，它可输入短名字 -a和长名字–app ,使用 \| 或者, 分隔, 在命令行里使用时, 这两个是等价的,区别是后者可以在程序里通过回调获取到<br />第二个参数, 会在help信息中展示<br />第三个参数为回调函数, 他接受的是一个string， 就是接受到第一个参数中长名字<br />第四个参数为默认值 |
| Action      | 注册一个callback函数, 这里需要注意目前回调不支持let声明      |
| parse       | 解析命令行                                                   |

#### 全局方式运行

> 我们可以通过 模块名  + command 的方式运行, 实现这种方式分三步走
>
> - 配置package.json的bin字段, 用来存放一个可执行文件, 如下配置所示
>
> ```json
> "bin": {
>     "app": "app"
> }
> ```
>
> - 执行npm link。它将会把**app**这个字段复制到npm的全局模块安装文件夹node_modules内，并创建符号链接（symbolic link，软链接），也就是**将 app 的路径加入环境变量 PATH**
> - [5分钟让你明白“软链接”和“硬链接”的区别](https://www.jianshu.com/p/dde6a01c4094)
> - [理解 Linux 的硬链接与软链接](https://www.ibm.com/developerworks/cn/linux/l-cn-hardandsymb-links/index.html)

## Download-git-repo

> 下载并提取git仓库, 用于下载项目模板



## Inquirer.js

> 通用的命令行用户界面集合, 用于和用户进行交互



## handlerbar.js

> 模板引擎, 将用户提交的信息动态填充到文件中



## ora

> 下载过程久的话, 可以用于显示下载中的动画效果



## chalk

> 可以给终端的字体加上颜色



## log-symbols

> 可以在终端上显示出√ 或 × 等的图标。