Jmeter介绍
=================

# 介绍

[apache jmeter官网](http://jmeter.apache.org/)是这样介绍自己的：

Apache JMeter™ 程序是一个开源软件， 一个100%纯java的应用， 设计用来测试功能和评估性能。最初设计用于测试web 应用，并扩展为为其他测试功能。

> The Apache JMeter™ application is open source software, a 100% pure Java application designed to load test functional behavior and measure performance. It was originally designed for testing Web Applications but has since expanded to other test functions.

## 可以用jmeter来做什么？

Apache JMeter可以用于测试静态和动态资源的性能(Webservices (SOAP/REST), Web 动态语言 - PHP, Java, ASP.NET, Files, etc. -, Java 对象, 数据库查询, FTP 服务器和其他)。

可以用来模拟高负载来测试单台服务器，服务器组， 网络或者其他对象，测试它的健壮性或者分析在不同负载类型下的整体性能。

可以使用他做一个性能的图形分析， 或者测试高并发负载下你的服务器/脚本/对象行为。

> Apache JMeter may be used to test performance both on static and dynamic resources (Webservices (SOAP/REST), Web dynamic languages - PHP, Java, ASP.NET, Files, etc. -, Java Objects, Data Bases and Queries, FTP Servers and more). It can be used to simulate a heavy load on a server, group of servers, network or object to test its strength or to analyze overall performance under different load types. You can use it to make a graphical analysis of performance or to test your server/script/object behavior under heavy concurrent load.

另外，jmeter可以帮助你回归测试你的应用，通过让你创建测试带断言的脚本来验证你的应用是否返回期待的结果。为了最大的弹性，jmeter让你使用正则表达式来创建这些断言。

> Additionally, JMeter can help you regression test your application by letting you create test scripts with assertions to validate that your application is returning the results you expect. For maximum flexibility, JMeter lets you create these assertions using regular expressions.

## jmeter的功能

- 可以为不同服务器/协议做负载和性能测试：

    - Web - HTTP, HTTPS
    - SOAP / REST
    - FTP
    - Database via JDBC
    - LDAP
    - Message-oriented middleware (MOM) via JMS
    - Mail - SMTP(S), POP3(S) and IMAP(S)
    - MongoDB (NoSQL)
    - Native commands or shell scripts
    -  TCP

- 完全便携（指平台适用性）， 100%纯java
- 完整的多线程框架，容许多线程并发采样和多个独立的线程组同时对不同功能采样
- 细致的GUI设计，让测试计划更快的构建和调试
- 缓存和离线分析/重放测试结果
- 高可扩展的核心:

    - 可拔插的采样器，提供无限的测试能力
    - 多个负载分析器可供选择，并带有可拔插的定时器
    - 数据分析和可视化插件，容许大幅扩展来实现定制化
    - 函数可以用于给测试提供动态输入或者提供数据操作
    - 脚本化采样器(BeanShell, BSF-兼容 语言和JSR223-兼容 语言)

### JMeter不是浏览器

**JMeter不是浏览器**, 它工作在协议层.

> please note that JMeter is not a browser, it works at protocol level.

虽然在web-services和远程服务看起来，jmeter看上去像一个浏览器（或者，多个浏览器）。但是jmeter是不执行任何浏览器支持的操作的。实际上， jmeter不执行在HTML页面上的javascript，也不像浏览器做的那样渲染HTML页面。

# jmeter资料

## 官方资料

- [apache jmeter官网](http://jmeter.apache.org/)
- [github上的jmeter代码]()
- [User's Manual](http://jmeter.apache.org/usermanual/index.html)












