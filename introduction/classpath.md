jmeter的classpath
================

注： 本文内容来自[jmeter官方手册](http://jmeter.apache.org/usermanual/get-started.html)，"2.4.1 JMeter's Classpath".

# 默认行为

JMeter自动从下面目录中的jar文件中查找class：

- JMETER_HOME/lib - 用于公用工具类 jars
- JMETER_HOME/lib/ext - 用于JMeter组件和插件

## jmeter组件和插件路径

如果开发了新的jmeter组件, 那么应该打包为jar并复制到JMeter's **"lib/ext"** 目录。jmeter会自动找到任何jar文件中的jmeter组件。不要使用lib/ext 目录来放置公用工具类或者插件用到的依赖包。lib/ext 目录仅仅用于JMeter组件和插件。

如果你不想将jmeter的插件jar放在lib/ext目录， 那么可以在jmeter.properties文件中定义search_paths 属性。

1. jmeter.properties文件在jmeter/bin目录下
2. 默认search_paths属性被注释掉了，没有打开

	> \#search_paths=/app1/lib;/app2/lib

	从例子上看，可以设置多个路径。

## 公用工具类和依赖包

公用工具类和依赖包 (类库等 etc) 可以放置在 lib 目录.

如果你不想在lib目录中放置这些jar， 那么可以在jmeter.properties文件中定义user.classpath 或者 plugin_dependency_paths属性。

后面会讲两则的差别。（TODO：哪里会讲？等待后续更新）

其他的jar（例如JDBC, JMS实现和任何其他jmeter代码需要的支持类库）应该放置在lib目录中 （而不是在lib/ext目录），或者添加到user.classpath.

注意：jmeter仅支持jar文件，不支持zip文件。

也可以在$JAVA_HOME/jre/lib/ext 目录下安装公用jar， 或者在jmeter.properties中设置user.classpath属性。

备注： 没有特别的原因，不到万不得已，不要把jar放到$JAVA_HOME/jre/lib/ext 目录下。jmeter给的这个建议简直是馊主意！

## 特别注意

**设置 CLASSPATH 环境变量不会有任何效果 **

这是因为JMeter是以"java -jar"的方式启动， 而当-jar被使用时java命令行悄悄的忽略CLASSPATH 变量和-classpath/-cp 参数。

注意所有java程序(指用"java -jar"的方式启动)都是如此， 不仅仅是JMeter.

