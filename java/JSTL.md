#JSTL

JSP 标准标签库（JSTL）

JSP标准标签库（JSTL）是一个JSP标签集合，它封装了JSP应用的通用核心功能。

JSTL支持通用的、结构化的任务，比如迭代，条件判断，XML文档操作，国际化标签，SQL标签。 除了这些，它还提供了一个框架来使用集成JSTL的自定义标签。

根据JSTL标签所提供的功能，可以将其分为5个类别。

* 核心标签
* 格式化标签
* SQL 标签
* XML 标签
* JSTL 函数


## JSTL 库安装
不同的JAVAEE 对应的jstl版本不同**[maven依赖](http://www.mvnrepository.com/artifact/javax.servlet/jstl)**
``` xml
<dependency>
    <groupId>javax.servlet</groupId>
    <artifactId>jstl</artifactId>
    <version>1.2</version>
</dependency>

```
## 核心标签

核心标签是最常用的JSTL标签。引用核心标签库的语法如下：

<%@ taglib prefix="c" uri="http://java.sun.com/jsp/jstl/core" %>

| 标签	| 描述	|
|:------|-------|
|\<c:out>|用于在JSP中显示数据，就像<%= ... >	|
|\<c:set>|用于保存数据						|
|\<c:remove>|用于删除数据	|
|\<c:catch>|用来处理产生错误的异常状况，并且将错误信息储存起来|
|\<c:if>|与我们在一般程序中用的if一样|
|\<c:choose>|本身只当做\<c:when>和\<c:otherwise>的父标签|
|\<c:when>|\<c:choose>的子标签，用来判断条件是否成立|
|\<c:otherwise>|\<c:choose>的子标签，接在\<c:when>标签后，当\<c:when>标签判断为false时被执行|







