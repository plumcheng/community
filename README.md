
## 功能列表  
开源论坛、问答系统，现有功能提问、回复、通知、最新、最热、消除零回复功能。功能持续更新中…… 


## 本地运行手册
1. 安装必备工具  
JDK，Maven
2. 克隆代码到本地
```sh
git clone https://github.com/codedrinker/community.git
````
3. 运行打包命令
```sh
mvn package
```
4. 运行项目  
```sh
java -jar target/community-0.0.1-SNAPSHOT.jar
```
5. 访问项目
```
http://localhost:8887
```


## 资源文件
未使用 Flyway 之前的数据库脚本
```sql
CREATE TABLE USER
(
    ID int AUTO_INCREMENT PRIMARY KEY NOT NULL,
    ACCOUNT_ID VARCHAR(100),
    NAME VARCHAR(50),
    TOKEN VARCHAR(36),
    GMT_CREATE BIGINT,
    GMT_MODIFIED BIGINT
);
```
运行 migrate 和 generator 的命令
```bash
mvn flyway:migrate
mvn -Dmybatis.generator.overwrite=true mybatis-generator:generate
```


## 更新日志
 修复 session 过期时间很短问题   
 修复因为*和+号产生的搜索异常问题  
 添加首页按照最新、最热、零回复排序  
 修复搜索输入 ? 号出现异常问题
 修复图片大小限制和提问内容为空问题
 添加动态导航栏
