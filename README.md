学习阶段

初步实现登录功能
返回一个可视化的网页怎么做，只依赖web和test启动目录；Thymeleaf（复制粘贴dependency）下载依赖。创建一个注解@Controller （name = ？）model

<模板thymeleaf> spring解析

spring用容器去管理bean； springboot：所有带有注解的文件只要在这个文件的同一级或下一级目录，都会自动的加载进来。@Controller 允许这个类接受前端的一个请求。

@GetMapping（） return “hello” 自动去找这个模板，去模板目录找（templates）

怎么改端口号：在application.properties中  server.port = 8887；
用Bootstrap 快速set up 前端的站点 然后去学习服务端的知识、组件图标的格式是字体不是图片，可以减少带宽。导航条、分页、徽章（展示消息和评论数）、缩略图、媒体对象（用作列表页 头像、名称）、列表组

如何做到响应式布局：栅格系统，@media标签（定义css样式）（根据xs、md等尺寸改变屏幕占比），可以根据屏幕的尺寸和浏览器的尺寸改变不同的样式。

将bootstrap导航条代码拷贝过去修改生成导航栏。

登录功能（调用GitHubAPI）：（申请GitHub APP 去做GitHub的登陆）OAuth App 根据步骤创建APP （Homepage URL、Authorization callback）

1、调用GitHub获取授权、传递参数（redirect_uri)；GitHub跳转回来的地址会携带一个参数code；我们提前写好API接收这个code，用服务端模拟post请求调用GitHub的access_token接口并传递code给GitHub；GitHub返回access_token（一个签名），得到后我们可以再次调用GitHub的一个API（get user）拿到用户信息

//登录功能（调用GitHubAPI）：用户访问社区，点击登录，页面调用一个GitHub的授权地址authorize，验证登录成功后GitHub回调redirect-uri code 页面解析code（调用access_token code)  GitHub 返回 code 页面 user 携带 access_token 访问 返回 user 信息
