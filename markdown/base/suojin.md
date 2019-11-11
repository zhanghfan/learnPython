# 逻辑行与物理行
* 物理行是你在编写程序时所看见的。逻辑行是Python看见的单个语句。Python假定每个物理行对应一个逻辑行 。

* 逻辑行的例子如print 'Hello World'这样的语句——如果它本身就是一行（就像你在编辑器中看到的那样），那么它也是一个物理行。

* 默认地，Python希望每行都只使用一个语句，这样使得代码更加易读。

* 如果你想要在一个物理行中使用多于一个逻辑行，那么你需要使用分号（;）来特别地标明这种用法。分号表示一个逻辑行/语句的结束。例如：
```
i = 5
print i
```
与下面这个相同：
```
i = 5;
print i;
```
同样也可以写成：
```
i = 5; print i;
```
甚至可以写成：
```
i = 5; print i
```
然而，我强烈建议你坚持在每个物理行只写一句逻辑行。仅仅当逻辑行太长的时候，在多于一个物理行写一个逻辑行。这些都是为了尽可能避免使用分号，从而让代码更加易读。事实上，我 从来没有 在Python程序中使用过或看到过分号。

下面是一个在多个物理行中写一个逻辑行的例子。它被称为明确的行连接。
```
s = 'This is a string. \
This continues the string.'
print s
```
它的输出：
```
This is a string. This continues the string.
```
类似地，
```
print \
i
```
与如下写法效果相同：
```
print i
```
有时候，有一种暗示的假设，可以使你不需要使用反斜杠。这种情况出现在逻辑行中使用了圆括号、方括号或波形括号的时候。这被称为暗示的行连接。你会在后面介绍如何使用列表的章节中看到这种用法。

* 缩进
空白在Python中是重要的。事实上行首的空白是重要的。它称为缩进。在逻辑行首的空白（空格和制表符）用来决定逻辑行的缩进层次，从而用来决定语句的分组。

* 这意味着同一层次的语句必须有相同的缩进。每一组这样的语句称为一个块。我们将在后面的章节中看到有关块的用处的例子。

* 你需要记住的一样东西是错误的缩进会引发错误。例如：
```
i = 5
 print 'Value is', i # Error! Notice a single space at the start of the line
print 'I repeat, the value is', i
```
* 当你运行这个程序的时候，你会得到下面的错误：
```
  File "whitespace.py", line 4
    print 'Value is', i # Error! Notice a single space at the start of the line
    ^
SyntaxError: invalid syntax
```
* 注意，在第二行的行首有一个空格。Python指示的这个错误告诉我们程序的语法是无效的，即程序没有正确地编写。它告诉你， 你不能随意地开始新的语句块 （当然除了你一直在使用的主块）。何时你能够使用新块，将会在后面的章节，如控制流中详细介绍。

* 如何缩进  
不要混合使用制表符和空格来缩进，因为这在跨越不同的平台的时候，无法正常工作。我 强烈建议 你在每个缩进层次使用 单个制表符 或 两个或四个空格 。
选择这三种缩进风格之一。更加重要的是，选择一种风格，然后一贯地使用它，即 只 使用这一种风格。