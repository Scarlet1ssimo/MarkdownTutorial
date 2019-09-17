# Markdown Tutorial

## Markdown 简介

### Markdown 是什么

> Markdown 是一种轻量级标记语言，创始人为约翰·格鲁伯（John Gruber）。它允许人们“使用易读易写的纯文本格式编写文档，然后转换成有效的 XHTML（或者 HTML）文档”。这种语言吸收了很多在电子邮件中已有的纯文本标记的特性。

> 标记语言（也称置标语言、标记语言、标志语言、标识语言、markup language）是一种将文本（Text）以及文本相关的其他信息结合起来，展现出关于文档结构和数据处理细节的计算机文字编码。与文本相关的其他信息（包括例如文本的结构和表示信息等）与原来的文本结合在一起，但是使用标记（markup）进行标识。

### 为什么选择Markdown

- **让你专注于写作，双手完全不用离开键盘；**
- **拥有基本的排版能力，小输入代价展现多格式。**
- 基于纯文本，小巧，方便修改和共享；
- 可以在所有的文本编辑器中直接编写；
- 很容易转换为其他格式；
- 应用广泛，如 Github，Piazza，Wordpress，等等。

### Markdown编辑器介绍

- 在线
  - cmd Markdown
- 离线
  - Typora
  - 编辑器插件，如VSCode
  - 浏览器插件，如Markdown Here

### 注意事项

- 在原版 Markdown 语法的基础上，有很多扩展语法，但并不是所有的扩展语法都能最终被正确渲染出来。
- 不同编辑器对不同语法支持程度不同。
- 你甚至可以自己定义将每个标签解析成什么样子。

我们先介绍基础语法(CommonMark)，再介绍一点流行的扩展语法 GFM。

## Markdown 语法详解

### Basic Syntax 基础语法 (CommonMark)

#### Paragraphs 段落

> A sequence of non-blank lines that cannot be interpreted as other kinds of blocks forms a paragraph. The contents of the paragraph are the result of parsing the paragraph’s raw content as inlines. The paragraph’s raw content is formed by concatenating the lines and removing initial and final whitespace.  
> Final spaces are stripped before inline parsing, so a paragraph that ends with two or more spaces will not end with a hard line break:

不是很严谨的人话：

- 段落：最正常的字，前后是两个空行
- 段落内容：去掉多余空格后的结果
- 行尾的两个空格可以实现段内换行

_Just **copy** the code below, to see the result._ 

我想换行？  
我不想换行？
qwq

我换段成功了没？

   前面有没有空格？

中                  间有几个空格？

Markdown真神奇

```markdown
我想换行？  
我不想换行？
qwq

我换段成功了没？

   前面有没有空格？

中                  间有几个空格？

Markdown真神奇
```

[^1]:Typora的渲染不严格遵循CommonMarks（更为人性化，语法更宽松），所以上面的测试在Typora中不会正确显示。这意味着，平时在Typora上编辑的文件在Github会被不同地渲染，希望能注意到这一点。

#### Header 标题

# This is an h1 tag
## This is an h2 tag
###### This is an h6 tag

```markdown
# This is an h1 tag
## This is an h2 tag
###### This is an h6 tag
```

#### Emphasis 强调

*This text will be italic*

**This text will be bold**

```markdown
*This text will be italic*

**This text will be bold**
```

#### Lists 列表

##### Unordered 无序列表

* Item 1
* Item 2
  * Item 2a
  * Item 2b

```markdown
* Item 1
* Item 2
  * Item 2a
  * Item 2b
```

##### Ordered 有序列表

1. Item 1
2. Item 2
3. Item 3
   1. Item 3a
   2. Item 3b

```markdown
1. Item 1
2. Item 2
3. Item 3
   1. Item 3a
   2. Item 3b
```

#### Images 图片

![awsl](https://s2.ax1x.com/2019/09/17/n5Sve1.jpg)

```markdown
![awsl](https://s2.ax1x.com/2019/09/17/n5Sve1.jpg)
```

#### Links 链接

[Scarlet's blog](https://scarlet-climax.github.io/)

https://scarlet-climax.github.io/ - automatic!

```markdown
[Scarlet's blog](https://scarlet-climax.github.io/)

https://scarlet-climax.github.io/ - automatic!
```

#### Blockquotes 块引用

> 我想换行  
> 我不想换行
> 我说不换行就不换行

```markdown
> 我想换行  
> 我不想换行
> 我说不换行就不换行
```


#### Inline code 行内代码

python用`^`来表示异或运算，用`**`表示乘方运算。
所以对python来说，`3^3==0`而`3**3==81`

```markdown
python用`^`来表示异或运算，用`**`表示乘方运算。
所以对python来说，`3^3==0`而`3**3==81`
```

### GitHub Flavored Markdown GFM扩展

GitHub发布了基于CommonMark的GitHub Flavored Markdown（GFM）的正式规范。除了表格、删除线、自动链接和任务列表被GitHub规范作为扩展添加之外，它遵循CommonMark规范。GFM的大多数语法为Github交流提供了便利。

#### Syntax Highlighting 语法高亮

```cpp
#include <cstdio>
#include <iostream>
using namespace std;

int main()
{
    cout << "Hello world!" << endl;
    return 0;
}
```

~~~markdown
```cpp
#include <cstdio>
#include <iostream>
using namespace std;

int main()
{
    cout << "Hello world!" << endl;
    return 0;
}
```
~~~

#### Task Lists 任务清单

- [x] 摸鱼
- [x] l4d2
- [ ] VP260作业
- [ ] VV286作业
- [ ] VE215作业
- [ ] VE270 Lab
- [ ] VE300作业

```markdown
- [x] 摸鱼
- [x] l4d2
- [ ] VP260作业
- [ ] VV286作业
- [ ] VE215作业
- [ ] VE270 Lab
- [ ] VE300作业
```

#### Tables 表格

A | B | $\oplus$ 
- | - | - 
0 | 0 | 0 
0 | 1 | 1 
1 | 0 | 1 
1 | 1 | 0 

```markdown
A | B | $\oplus$ 
- | - | - 
0 | 0 | 0 
0 | 1 | 1 
1 | 0 | 1 
1 | 1 | 0 
```

#### Strikethrough 删除线

~~大家是不是觉得markdown还蛮简单的~~

```markdown
~~大家是不是觉得markdown还蛮简单的~~
```


