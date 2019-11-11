# 字符串
字符串是字符的序列。字符串基本上就是一组单词。

* 使用单引号（'）
你可以用单引号指示字符串，就如同'Quote me on this'这样。所有的空白，即空格和制表符都照原样保留。

* 使用双引号（"）
在双引号中的字符串与单引号中的字符串的使用完全相同，例如"What's your name?"。

* 使用三引号（'''或"""）
利用三引号，你可以指示一个多行的字符串。你可以在三引号中自由的使用单引号和双引号。例如：

```
'''This is a multi-line string. This is the first line.
This is the second line.
"What's your name?," I asked.
He said "Bond, James Bond."
'''
```

* 转义符
假设你想要在一个字符串中包含一个单引号（'），那么你该怎么指示这个字符串？例如，这个字符串是What's your name?。你肯定不会用'What's your name?'来指示它，因为Python会弄不明白这个字符串从何处开始，何处结束。所以，你需要指明单引号而不是字符串的结尾。可以通过 转义符 来完成这个任务。你用\'来指示单引号——注意这个反斜杠。现在你可以把字符串表示为'What\'s your name?'。

另一个表示这个特别的字符串的方法是"What's your name?"，即用双引号。类似地，要在双引号字符串中使用双引号本身的时候，也可以借助于转义符。另外，你可以用转义符\\来指示反斜杠本身。

值得注意的一件事是，在一个字符串中，行末的单独一个反斜杠表示字符串在下一行继续，而不是开始一个新的行。例如：

```
"This is the first sentence.\
This is the second sentence."
```
等价于"This is the first sentence. This is the second sentence."

* 自然字符串  
如果你想要指示某些不需要如转义符那样的特别处理的字符串，那么你需要指定一个自然字符串。自然字符串通过给字符串加上前缀r或R来指定。例如r"Newlines are indicated by \n"。

* Unicode字符串
Unicode是书写国际文本的标准方法。如果你想要用你的母语如北印度语或阿拉伯语写文本，那么你需要有一个支持Unicode的编辑器。类似地，Python允许你处理Unicode文本——你只需要在字符串前加上前缀u或U。例如，u"This is a Unicode string."。

记住，在你处理文本文件的时候使用Unicode字符串，特别是当你知道这个文件含有用非英语的语言写的文本。

* 字符串是不可变的
这意味着一旦你创造了一个字符串，你就不能再改变它了。虽然这看起来像是一件坏事，但实际上它不是。我们将会在后面的程序中看到为什么我们说它不是一个缺点。

* 按字面意义级连字符串
如果你把两个字符串按字面意义相邻放着，他们会被Python自动级连。例如，'What\'s' 'your name?'会被自动转为"What's your name?"。