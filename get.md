### 我的需求：

> editor: ace

> 导入，修改，保存：ajax

> web ssh: 一般都是前端发请求（比如socket），后端实现相关操作。本例node实现。[GateOne](https://github.com/liftoff/GateOne),python实现。其他有浏览器插件实现，以及调用本地shell工具：[详情](http://kbnix.com/2013/03/22/web%E6%B5%8F%E8%A7%88%E5%99%A8%E8%B0%83%E7%94%A8%E5%A4%96%E9%83%A8%E7%A8%8B%E5%BA%8F%E5%AE%9E%E7%8E%B0%E7%BD%91%E9%A1%B5%E7%89%88ssh%E5%8E%9F%E5%88%9B%E5%BC%80%E6%BA%90/)。

> debug: 有引入v8引擎，只能做js的debug(?) https://docs.c9.io/running_and_debugging_code.html,https://c9.io/site/blog/2014/09/terminalmonitor/

> 同步操作： webDEV



### 本例使用的技术：

> async.js：操作文件以及异步处理，基本都是服务端的事情

> jsDEV: 用户之间协同编辑管理存储在服务器的文档[webDEV](http://webdav.org/)

> connect: 建立一个网络应用

> smith.io&engine.io: socket的封装

> ace: 编辑器（{emmet](http://docs.emmet.io/)自动完成HTML等）

> [apf](https://github.com/ajaxorg/apf)，前端UI，处理了输入事件以及ace编辑器的一些配置

> [如何编写 Cloud9 JavaScript IDE 的功能扩展](http://www.oschina.net/translate/writing-an-extension-for-cloud9-javascript-ide)

> terminal ???? 木有开源

### plugins-server

> cloud9.ide.shell>shell.js: 引入process-manager，处理基本的cmd命令。