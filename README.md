# maven 学习笔记
***
## maven archetype 

maven archetype 用来生成符合maven要求目录结构的工程，例如使用`mvn archetype:generate -DarchetypeCatalog=internal` 可以使用maven内置的一些模版工成。

同时，我们一也可以定义自己的archetype. 创建一个工程后，在工程中使用`mvn archetype:create-from-project`，maven会将当前工程作为一个骨架工程，在`target/generated-sources/archetype` 生成相应的骨架目录，前往生成的archetype目录，执行`mvn isntall` 命令，将生成的archetype装载在本地。

最后，移动到其他目录下面，运行`mvn archetype:generate -DarchetypeCatalog=local`来使用自己的archetype。

maven-archetype 的 base-project 下包含了练习的例子



***
## 学习资源
1. [maven-archetype-plugin](http://maven.apache.org/archetype/maven-archetype-plugin/advanced-usage.html)