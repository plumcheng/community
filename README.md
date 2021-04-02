学习阶段

初步实现登录功能
返回一个可视化的网页怎么做，只依赖web和test启动目录；Thymeleaf（复制粘贴dependency）下载依赖。创建一个注解@Controller （name = ？）model

<模板thymeleaf> spring解析

spring用容器去管理bean； springboot：所有带有注解的文件只要在这个文件的同一级或下一级目录，都会自动的加载进来。@Controller 允许这个类接受前端的一个请求。

@GetMapping（） return “hello” 自动去找这个模板，去模板目录找（templates）

怎么改端口号：在application.properties中  server.port = 8887；
