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
|\<c:import>|检索一个绝对或相对 URL，然后将其内容暴露给页面|
|\<c:forEach>|基础迭代标签，接受多种集合类型|
|\<c:forTokens>|根据指定的分隔符来分隔内容并迭代输出|
|\<c:param>|用来给包含或重定向的页面传递参数|
|\<c:redirect>|重定向至一个新的URL.|
|\<c:url>|使用可选的查询参数来创造一个URL|

## JSTL函数
JSTL包含一系列标准函数，大部分是通用的字符串处理函数。引用JSTL函数库的语法如下：

<%@ taglib prefix="fn" uri="http://java.sun.com/jsp/jstl/functions" %>

| 标签	| 描述	| 举例说明|
|:------|-------|----------|
|fn:contains(string, substring)|测试输入的字符串是否包含指定的子串|\<c:if test="${fn:contains(name, searchString)}">|
|fn:containsIgnoreCase(string, substring)|测试输入的字符串是否包含指定的子串，大小写不敏感|\<c:if test="${fn:containsIgnoreCase(name, searchString)}">|
|fn:endsWith(string, suffix)|测试输入的字符串是否以指定的后缀结尾|\<c:if test="${fn:endsWith(filename, '.txt')}">|
|fn:escapeXml(string)|把一些字符转成XML表示，例如\<字符应该转为&lt;|${fn:escapeXml(param:info)}|
|fn:indexOf(string, substring)|子字符串在母字符串中出现的位置|${fn:indexOf(name, '-')}|
|fn:join(array, separator)|将数组中的数据联合成一个新字符串，并使用指定字符格开|${fn:join(array, ';')}|
|fn:length(item)|获取字符串的长度，或者数组的大小|${fn:length(shoppingCart.products)}|
|fn:replace(string, before, after)|替换字符串中指定的字符|${fn:replace(text, '-','•')}|
|fn:split(string, separator)|把字符串按照指定字符切分|${fn:split(customerNames, ';')}|
|fn:startsWith(string, prefix)|判断字符串是否以某个子串开始|\<c:if test="${fn:startsWith(product.id, '100-')}">|
|fn:substring(string, begin, end)|获取从某个字符所在位置开始的子串|${fn:substringAfter(zip, '-')}
|fn:substringBefore(string, substring)|获取从开始到某个字符所在位置的子串|${fn:substringBefore(zip, '-')}|
|fn:toLowerCase(string)|	转为小写|${fn.toLowerCase(product.name)}|
|fn:toUpperCase(string)|	转为大写字符|${fn.UpperCase(product.name)}|
|fn:trim(string)|去除字符串前后的空格|${fn.trim(name)}





