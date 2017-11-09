"# hyperledger fabric for python" 

## in this website supported  conventions in editing python :
         https://www.python.org/dev/peps/pep-0008/#introduction
## 1.we need learning some code style conventions for writen python contribution.
### 1.1 code layout  代码布局
>#### 1.1.1 indentation : use 4 spaces per indentation level #每个缩进级别需要使用4个空格.
>##### example:
	1. Aligned with opening delimiter. 
	#使用分开的界定符对齐
	foo = long_function_name(var_one, var_two,
	                         var_three, var_four)
	2.  More indentation included to distinguish this from the rest.
	#包含更多的缩进来区分一行和剩下的行
	def long_function_name(
	        var_one, var_two, var_three,
	        var_four):
	    print(var_one)
	3. Hanging indents should add a level.
	#悬挂式缩进应该增加一个级别(另起一个4个空格行)
	foo = long_function_name(
	    var_one, var_two,
	    var_three, var_four)
	    
>#### 反例：
	1. Arguments on first line forbidden when not using vertical alignment.
	#如果不使用垂直对齐方式，参数不要在第一行出现
	foo = long_function_name(var_one, var_two,
	    var_three, var_four)
	2. Further indentation required as indentation is not distinguishable.
	#由于无法区分缩进应该进一步缩进
	def long_function_name(
	    var_one, var_two, var_three,
	    var_four):
	    print(var_one)
>####	可选项：
	The 4-space rule is optional for continuation lines.
	# 空4个空格的规则在后续行是可选的。
	Optional:
	Hanging indents *may* be indented to other than 4 spaces.
	foo = long_function_name(
	  var_one, var_two,
	  var_three, var_four)
>#### When the conditional part of an if-statement is long enough to require that it be written 
>#### 当if条件语句的条件部分很长跨了多个行的时候，值得注意的是由2个字符关键词加上一个空格，再加上
>####	across multiple lines, it's worth noting that the combination of a two character keyword (i.e.
>####	一个打开的方括号构成的一个正常的4个空格缩进给子行的多行条件。
>####	 if), plus a single space, plus an opening parenthesis creates a natural 4-space indent for the subsequent lines of    the multiline conditional. 
>#### This can produce a visual conflict with the indented suite of code nested inside the if-statement, which would also naturally be indented to 4 spaces. 
>####        这可以产生与嵌套在if语句内的缩进的代码的视觉冲突，这也自然会被缩进4个空格
>#### This PEP takes no explicit position on how (or whether) to further visually distinguish such conditional lines from the nested suite inside the if-statement. Acceptable options in this situation include, but are not limited to:
>#### 此PEP在如何(或是否)在if语句中从嵌套的套件中进一步直观地区分这类条件行没有明确的位置。在这种情况下可接受的选项包括，但不限于：
>####    # No extra indentation.  不需要额外的缩进
	if (this_is_one_thing and
	    that_is_another_thing):
	    do_something()

>####	# Add a comment, which will provide some distinction in editors
	# supporting syntax highlighting.
	增加一行注释这将在一些支持语法高亮的编辑器中提供一些区分。
	if (this_is_one_thing and
	    that_is_another_thing):
	    # Since both conditions are true, we can frobnicate.
	    do_something()