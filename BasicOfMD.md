#Markdown基础
本文件将展示使用由JOHN GRUBER制定的Markdown的基本语法，参考内容是[JOHN GRUBER对于Markdown基本语法的介绍](https://daringfireball.net/projects/markdown/basics)。

练习Markdown语法也可以使用[Dingus](https://daringfireball.net/projects/markdown/dingus)。Dingus是一个可以将Markdown语法转换成XHTML的Web应用。

段落、标题和块级引用
-----------------
段落是单纯连续的一些文本行的集合，由一个或多个空行分隔。空行是看起来像空行的行，连续的空格或tab缩进组成的行也是空行。普通的段落不应该被多个空格或tab分裂开来。

Markdown提供了两种风格的标题——Setext和atx。对应到`<h1>`和`<h2>`标签的Setext风格的标题是通过在标题文本下面一行添加连续的等号(=)和连字符(-)实现的。若是要创建一个atx风格的标题，在标题文本前添加一到六个井号(#)即可，井号的数量与HTML标题级别对应。

块级引用则是通过email风格的尖角括号(>)实现的。

Markdown示例代码:

	A First Level Header
	====================
	
	A Second Level Header
	---------------------
	
	Now is the time for all good men to come to
	the aid of their country. This is just a
	regular paragraph.
	
	The quick brown fox jumped over the lazy
	dog's back.
	
	### Header 3
	
	> This is a blockquote.
	> 
	> This is the second paragraph in the blockquote.
	>
	> ## This is an H2 in a blockquote
	

##斜体与加粗

Markdown使用星号与下划线来定义一段重点，使用一对星号或下划线包围文字来定义。

Markdown示例代码：

	Some of these words *are emphasized*.
	Some of these words _are emphasized also_.
	
	Use two asterisks for **strong emphasis**.
	Or, if you prefer, __use two underscores instead__.
	
Markdown示例：  
可以通过一对星号来划斜体重点，*比如说这样子*！  
也可以通过一对下划线来划斜体重点，_比如说这样子_！

可以通过一对双星号来进行加粗重点，**比如说这样子**！
也可以通过一对双下划线进行加粗重点，__比如这样子__!

##列表

无排序的列表使用星号、加号、减号作为列表标记，这三个符号是可互换的。

Markdown示例代码：

	* Computer
	* Calculator
	* Telephone
	
	+ Apple
	+ Pineapple
	+ WaterMelon
	
	- Chair
	- Desk
	- Elevator

Markdown示例：  

* Computer
* Calculator
* Telephone

排序列表使用规则的数字后跟点号作为列表标记。

Markdown示例代码：

	1. Operaotr
	2. Nearest
	3. Mind

Markdown示例：

1. Operaotr
2. Nearest
3. Mind

如果你在两个列表元素之间加入空行，你就相当于为列表元素添加了p标签。你可以通过在段之前添加四个空格或一个制表符来创建多段列表元素。

Markdown示例代码：

	*   A list item.
	
	    With multiple paragraphs.
	
	*   Another item in the list.

Markdown示例：

*	西瓜香蕉牛奶面包

	萝卜青菜各有所爱
	
*	琵琶罗汉还可以

##链接

Markdown提供两种创建链接的方式：内联和引用。这两种方式可以让你用方括号把想要转换链接的文本框起来。

内联样式的链接使用在文本后立刻用圆括号将链接括起来的方式。

Markdown示例代码：

	This is an [example link](http://example.com/).
	
Markdown示例：
	
I am looking for [Google](http://google.com), you know why?

作为可选项，你可以在圆括号内添加标题属性。

Markdown示例代码：

	This is an [example link](http://example.com/ "With a Title").
	
Markdown示例：

What do you think [google](http://google.com "This is title of google")?
	
引用风格的链接让你可以通过名称来引用链接，引用链接可以在文档其他位置定义。

Markdown示例代码：

	I get 10 times more traffic from [Google][1] than from
	[Yahoo][2] or [MSN][3].
	
	[1]: http://google.com/        "Google"
	[2]: http://search.yahoo.com/  "Yahoo Search"
	[3]: http://search.msn.com/    "MSN Search"
	
Markdown示例：

属于中国公司的搜索引擎有[百度][测试百度]、[搜狗][测试搜狗]、[搜搜][测试搜搜]。

[测试百度]: https://www.baidu.com "百度链接"
[测试搜狗]: https://www.sogou.com "搜狗链接"
[测试搜搜]: https://www.soso.com "搜搜链接"

在引用风格链接中，链接名可以包含字母数字和空格，但是字母不区分大小写。

Markdown示例代码：

	I start my morning with a cup of coffee and
	[The New York Times][NY Times].
	
	[ny times]: http://www.nytimes.com/
	
Markdown示例：

How often do you go [google][Google]？

[gOOGLE]: http://google.com/   "Google Page"

##图片

图片的语法很像链接的语法，也有内联和引用两种方式。

Markdown示例代码：

	![alt text](/path/to/img.jpg "Title")
	
	![alt text][id]
	[id]: /path/to/img.jpg "Title"
	
Markdown示例：
	![无害啦啦啦](https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fimage.biaobaiju.com%2Fuploads%2F20180802%2F00%2F1533141603-CMQsJnpLSb.jpeg&refer=http%3A%2F%2Fimage.biaobaiju.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=jpeg?sec=1613201853&t=a1308c2255ac79dc7b5f4c4c4240346c "这是无害的")
	
##代码

在一个普通的段落中，你可以通过将文本用反引号括起来创建代码段。任何&符号和尖括号将自动转化为HTML标记。这使得Markdown可以支持HTML示例代码段。

Markdown示例代码：

	I strongly recommend against using any `<blink>` tags.
	I wish SmartyPants used named entities like `&mdash;`
	instead of decimal-encoded entites like `&#8212;`.
	
Markdown示例：

I strongly recommend against using any `<blink>` tags.
I wish SmartyPants used named entities like `&mdash;`
instead of decimal-encoded entites like `&#8212;`.

若要将已编辑好的代码段添加到Markdown文件中，将每一行之前都添加四个空格或一个制表符即可，正如前文演示的一样。





