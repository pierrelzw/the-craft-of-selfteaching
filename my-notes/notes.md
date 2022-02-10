
## 1.E.4
从这个角度看，牛，对人类来说就是个函数，它吃的是草，挤出来的是奶…… 开玩笑了。

而我们所需要做的事情（所谓的 “学习使用函数”），其实只不过是 “通过阅读产品说明书了解如何使用产品” 而已，真的没多神秘……

“看说明书” 就是这样，全都看了，真不一定全部看懂，但看总是比不看强，因为总是有能看懂的部分……

很多人只看各种教材、教程，却从来不去翻阅官方文档 —— 到最后非常吃亏。只不过是多花一点点的功夫而已，看过之后，就会知道：原来 print() 这个函数是可以往文件里写数据的，只要指定 file 这个参数为一个已经打开的文件对象就可以了（真的有很多人完全不知道）……

> 我真的就不知道，原来print可以往文件里写数据


```
from IPython.core.interactiveshell import InteractiveShell
InteractiveShell.ast_node_interactivity = "all"
```
有了这两句，可以在直接输出多行的变量，无需print了


`pow(x,y,[,z])`

注意 `pow()` 函数定义部分中，圆括号内的方括号 `[, z]` —— 这是非常严谨的标注，如果没有 `z`，那么那个逗号 `,` 就是没必要的。


## 1.E.5

所以，一个字符串，有两种形式，raw 和 presentation，在后者中，\t 被转换成制表符，\n 被转换成换行。

在写程序的过程中，我们在代码中写的是 _raw_，而例如当我们调用 print() 将字符串输出到屏幕上时，是 _presentation_：

```
s = "He said, it\'s fine." # raw
print(s)                   # presentation

```

```
from IPython.core.interactiveshell import InteractiveShell
InteractiveShell.ast_node_interactivity = "all"

'Now is better than never.'.upper()

# 在 Python 命令行工具之中，单个下划线，是个特殊变量；
# 保存着最近的语句或者表达式的结果
# 上一个 Cell 执行过后，_ 中保存着 'NOW IS BETTER THAN NEVER.'

_.lower()
```

```
from IPython.core.interactiveshell import InteractiveShell
InteractiveShell.ast_node_interactivity = "all"

# casefold() 也是转换成小写，但它能处理更多欧洲语言字符

'ß'.casefold()           # 德语字符中，大写 ß 的小写形式是 ss
len('ß'.casefold())
'ß'.lower()              # lower() 对这类字符无能为力……
len('ß'.lower())
# casefold 
'\u0132'                # Ĳ 这个字符的 Unicode 编码
'\u0132'.casefold()
'\u0132'.lower()        # 对这个字符来说，lower() 和 casefold 的效果一样
len('\u0132'.casefold())

# 这是一篇有用的文章：
# Truths programmers should know about case
# https://www.b-list.org/weblog/2018/nov/26/case/
```

```
s = 'Now is better than never.'
s.capitalize() # 句首字母大写
s.title() # 每个单词首字母大写
```

```
s = 'Now is better than never.'
s.swapcase() # 逐个字符更替大小写
s.title() 
s.title().swapcase() 


# str.encode(encoding="utf-8", errors="strict")
# 关于更多可能的 encoding list, 请参阅：
# https://docs.python.org/3/library/codecs.html#standard-encodings
s = '简单优于复杂。'
s.encode()
```


> 而 = 表示该参数有个默认值。上述这段说明如果你感到熟悉的话，说明前面的内容确实阅读到位了…… 与大量 “前置引用” 相伴随的是知识点的重复出现。

