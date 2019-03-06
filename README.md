# newDays
总结归纳：https://github.com/alienzhou/frontend-tech-list#11-javascript
    一、JS
  1、js工作原理：引擎，运行与调用栈
  https://blog.sessionstack.com/how-does-javascript-actually-work-part-1-b0bacc073cf
  2、V8引擎    https://zhuanlan.zhihu.com/p/27628685
    解析和执行js脚本
  3、js运行机制
    https://blog.sessionstack.com/how-javascript-works-memory-management-how-to-handle-4-common-memory-leaks-3f28b94cfbec
    http://www.ruanyifeng.com/blog/2014/10/event-loop.html
    https://juejin.im/entry/5847c101128fe10058bcef6e
    （1）js是单线程的，同一时间只能做一件事情。原因：js是一种浏览器脚本语言，主要用途是用户交互和操作DOM。
   虽然H5提出了用web work来创建线程，但是子线程完全受主线程的控制，且不能操作DOM.
     (2)任务队列（同步 异步）: 一个接一个完成任务，就意味着有些任务需要排队， （任务计算量过大，CPU处于忙碌状态，任务所需的东西为准备好所以无法继续执行，
     导致CPU闲置，等待输入输出设备（I/O设备）。> 比如有的任务你需要Ajax获取到数据才能往下执行）JS的设计者意识到了这个问题，等待的过程完全可以先运行后面已经
     就绪的任务来提高效
4、浏览器的工作原理 https://www.html5rocks.com/zh/tutorials/internals/howbrowserswork/
  （1）浏览器的主要功能是向服务器发送请求
    (2)浏览器的主要组件：用户界面（输入栏、书签、前进后退）、浏览器引擎（在用户界面和呈现引擎之间传送指令）、呈现引擎（ 负责显示请求的内容。如果请求的内容是 HTML，它就负责解析 HTML 和 CSS 内容，并将解析后的内容显示在屏幕上）、网络、用户界面后端、JS解析器（用于解析执行js代码）、数据存储（cookie）
    (3)浏览器中有不同的解析器，解析css、js,浏览器的容错处理、
5、内存管理、内存泄漏

关于CSS https://lhammer.cn/You-need-to-know-css/#/stripes-background

https://codepen.io/rachelandrew/pen/LmawOy 存css设置当导航栏滚动到顶部的时候导航栏固定不动


6、关于跨域：同源策略 https://github.com/alienzhou/cross-domain-demo
  （1）跨域其实就是协议、域名、端口不同的情况下会跨域
  解决跨域的办法：【1】 代理：同源政策是浏览器层面的限制，我们可以将跨域交给后端服务，这样就规避了同源策略
               【2】配置CORS，服务器设置响应头信息 Access-Control-Allow-Origin为*则代表可以接受所有域的请求，Access-Control-Allow-Credentials的响应头，如果设置为true则表明服务器允许该请求内包含cookie信息
               【3】jsonp 通过script标签，回调函数


经常忽视的问题：
你不知道的img标签： https://www.jianshu.com/p/9f47ae6b3b5b
    （重点：最好为图片设置宽、高，避免浏览器在渲染的时候不断的计算和调整页面布局，会延迟文档的显示，并且会造成重绘）

安全
xss攻击：  https://tech.meituan.com/fe_security.html
注意点：
xss攻击，对于用户提交恶意代码，做好防护措施，需要转义，
上传图片  校验图片的MIME格式  防止用户恶意修改后缀而导入非法文件

csrf攻击： https://juejin.im/post/5bc009996fb9a05d0a055192
1、同源检测，阻止不明的外域访问
2、提交时要求附加本域才能获取的信息CSRF Token，双重Cookie验证，





