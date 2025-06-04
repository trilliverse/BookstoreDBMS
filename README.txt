项目名称：
“网上书店综合管理”数据库应用系统
简介:

这是一个基于 Java、JavaFX 和 MySQL 开发的网上书店管理系统，支持书籍、订单、顾客、供应商等模块的增删改查操作。

环境配置指南

1. 系统要求
操作系统：Windows / macOS / Linux
Java：JDK 11 或更高版本
数据库：MySQL 8.x
依赖库：
MySQL Connector/J (JDBC 驱动)
JavaFX SDK

2. MySQL 配置

下载 MySQL：
访问 MySQL Community Downloads 下载 MySQL Community Server。
安装后设置 root 用户的密码（例如 123456）。

创建数据库：
使用 MySQL创建项目使用的数据库在 “数据库初始化需要的sql语句.txt” 文件中，直接复制到MySQL中即可完成初始化

配置项目文件：
修改DatabaseUtil.java文件中的下面几行代码
private static final String DB_URL = "jdbc:mysql://localhost:3306/BookStoreDB"; // 数据库地址
private static final String DB_USER = "root"; // 数据库用户名
private static final String DB_PASSWORD = "123456"; // 数据库密码

如果您的端口号不是3306，将localhost:后面更改为你的端口号
将数据库密码(原文的123456)DB_PASSWORD更改为您设置的密码


3. 添加 JDBC 驱动

下载 JDBC 包：
访问 MySQL Connector/J 下载最新的驱动包。
下载后解压，找到 mysql-connector-java-x.x.x.jar 文件。
将其放到您项目的lib文件夹中或加入到项目的libraries中

4. JavaFX 配置

下载 JavaFX：
访问 Gluon JavaFX 下载对应的 JavaFX SDK。

配置 JavaFX：
将JavaFX 的所有 JAR 文件放到您项目的lib文件夹中或加入到项目的libraries中。
配置项目的launch.json和setting.json文件。

5. 环境变量配置

JDK 配置：
设置 JAVA_HOME 为 JDK 的安装路径，例如：
JAVA_HOME=C:\Program Files\Java\jdk-17
将 %JAVA_HOME%\bin 添加到 Path 环境变量。

MySQL 配置：
将 MySQL 的安装路径添加到 Path，例如：
C:\Program Files\MySQL\MySQL Server 8.0\bin

6.注意事项
兼容性检查：确保 MySQL、JDBC 驱动和 JDK 的版本匹配。
项目依赖更新：保持 JDBC 和 JavaFX 的版本更新，避免兼容性问题。
