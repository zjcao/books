# Markdown 简明语法

## Markdown 简明语法手册

标签： Markdown  
声明：本文摘自：[Cmd Markwon](https://www.zybuluo.com/mdeditor?url=https://www.zybuluo.com/static/editor/md-help.markdown)

### 1. 斜体和粗体

使用`*`和`**`表示斜体和粗体。

示例：`这是 *斜体*，这是 **粗体**。`

这是 _斜体_，这是 **粗体**。

### 2. 分级标题

在行首用`#`表示不同级别的标题 \(H1-H6\)，例如：\# H1, \#\# H2, \#\#\# H3，\#\#\#\# H4。

示例：

```text
# 这是一个一级标题
## 这是一个二级标题
### 这是一个三级标题
```

### 3. 超链接

使用 `[描述](链接地址)`为文字增加超链接。

示例：`这是去往 [Google](http://www.google.com) 的超链接。`

这是去往 [Google](http://www.google.com) 的超链接。

### 4. 无序列表

使用 `*，+，-` 表示无序列表。

示例：

```text
- 无序列表项 一
- 无序列表项 二
- 无序列表项 三
```

* 无序列表项 一
* 无序列表项 二
* 无序列表项 三

### 5. 有序列表

使用`数字和点`表示有序列表。

示例：

```text
1. 有序列表项 一
2. 有序列表项 二
3. 有序列表项 三
```

1. 有序列表项 一
2. 有序列表项 二
3. 有序列表项 三

### 6. 文字引用

使用`>`表示文字引用。

示例：`> 野火烧不尽，春风吹又生。`

> 野火烧不尽，春风吹又生。

### 7. 行内代码块

使用 \`代码\` 表示行内代码块。

示例：``让我们聊聊 `html`。``

让我们聊聊 `html`。

### 8.  代码块

使用`四个缩进空格`表示代码块。

示例：`这是一个代码块，此行左侧有四个不可见的空格。`

```text
这是一个代码块，此行左侧有四个不可见的空格。
```

### 9.  插入图像

使用`![描述](图片链接地址)`插入图像。

示例：`![Cmd-Markdown-Logo](https://www.zybuluo.com/static/img/logo.png)`

![Cmd-Markdown-Logo](https://www.zybuluo.com/static/img/logo.png)

## Markdown 高阶语法手册

### 1. 内容目录

在段落中填写 `[TOC]` 以插入全文内容的目录结构。

\[TOC\]

> 备注：有一些编辑器不支持\[TOC\]标记，比如简书不支持。

### 2. 标签分类

在编辑区任意行的列首位置输入以下代码给文稿标签.

示例：

```text
标签： 数学 英语 Markdown

或者

Tags： 数学 英语 Markdown
```

标签： 数学 英语 Markdown

或者

Tags： 数学 英语 Markdown

### 3. 删除线

使用 ~~ 表示删除线。

示例：`~~这是一段错误的文本。~~`

~~这是一段错误的文本。~~

### 4. 注脚

在需要添加注脚的文字后加上脚注名字，即加注， 然后在文本的任意位置\(一般在最后\)添加脚注。

> 注：注脚与注脚之间必须空一行。  
> 即使你没有把注脚写在文末，经Markdown转换后，也会自动归类到文章的最后。

示例：

```text
这是一个注脚[^1]的样例，这是第二个注脚[^2]的样例。
```

这是一个注脚的样例，这是第二个注脚的样例。

### 5. LaTeX 公式

`$`表示行内公式：

示例1：`质能守恒方程可以用一个很简洁的方程式 $E=mc^2$ 来表达。`

质能守恒方程可以用一个很简洁的方程式 $E=mc^2$ 来表达。

`$$`表示整行公式：

示例2：

```text
$$\sum_{i=1}^n a_i=0$$

$$f(x_1,x_x,\ldots,x_n) = x_1^2 + x_2^2 + \cdots + x_n^2$$

$$\sum^{j-1}_{k=0}{\widehat{\gamma}_{kj} z_k}$$$
```

$$\sum_{i=1}^n a_i=0$$

$$f(x_1,x_x,\ldots,x_n) = x_1^2 + x_2^2 + \cdots + x_n^2$$

$$\sum^{j-1}_{k=0}{\widehat{\gamma}_{kj} z_k}$$

访问 [MathJax](http://meta.math.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference) 参考更多使用方法。

### 6. 加强的代码块

支持四十一种编程语言的语法高亮的显示，行号显示。用 \`\`\``编程语言` 开头，用 \`\`\`结尾。

Python 示例：

```python
@requires_authorization
def somefunc(param1='', param2=0):
    '''A docstring'''
    if param1 > param2: # interesting
        print 'Greater'
    return (param2 - param1 + 1) or None

class SomeClass:
    pass

>>> message = '''interpreter
... prompt'''
```

### 7. 流程图

示例

   
st=&gt;start: Start:&gt;https://www.zybuluo.com  
io=&gt;inputoutput: verification  
op=&gt;operation: Your Operation  
cond=&gt;condition: Yes or No?  
sub=&gt;subroutine: Your Subroutine  
e=&gt;end  
  
st-&gt;io-&gt;op-&gt;cond  
cond\(yes\)-&gt;e  
cond\(no\)-&gt;sub-&gt;io  
 Run

```text
st=>start: Start:>https://www.zybuluo.com
io=>inputoutput: verification
op=>operation: Your Operation
cond=>condition: Yes or No?
sub=>subroutine: Your Subroutine
e=>end

st->io->op->cond
cond(yes)->e
cond(no)->sub->io
```

更多语法参考：[流程图语法参考](http://adrai.github.io/flowchart.js/)

### 8. 序列图

示例 1

```text
Alice->Bob: Hello Bob, how are you?
Note right of Bob: Bob thinks
Bob-->Alice: I am good thanks!
```

示例 2

```text
Title: Here is a title
A->B: Normal line
B-->C: Dashed line
C->>D: Open arrow
D-->>A: Dashed open arrow
```

更多语法参考：[序列图语法参考](http://bramp.github.io/js-sequence-diagrams/)

### 9. 甘特图

甘特图内在思想简单。基本是一条线条图，横轴表示时间，纵轴表示活动（项目），线条表示在整个期间上计划和实际的活动完成情况。它直观地表明任务计划在什么时候进行，及实际进展与计划要求的对比。

```text
    title 项目开发流程
    section 项目确定
        需求分析       :a1, 2016-06-22, 3d
        可行性报告     :after a1, 5d
        概念验证       : 5d
    section 项目实施
        概要设计      :2016-07-05  , 5d
        详细设计      :2016-07-08, 10d
        编码          :2016-07-15, 10d
        测试          :2016-07-22, 5d
    section 发布验收
        发布: 2d
        验收: 3d
```

更多语法参考：[甘特图语法参考](https://knsv.github.io/mermaid/#gant-diagrams)

### 10. Mermaid 流程图

```text
    A[Hard edge] -->|Link text| B(Round edge)
    B --> C{Decision}
    C -->|One| D[Result one]
    C -->|Two| E[Result two]
```

更多语法参考：[Mermaid 流程图语法参考](https://knsv.github.io/mermaid/#flowcharts-basic-syntax)

### 11. Mermaid 序列图

```text
    Alice->John: Hello John, how are you?
    loop every minute
        John-->Alice: Great!
    end
```

更多语法参考：[Mermaid 序列图语法参考](https://knsv.github.io/mermaid/#sequence-diagrams)

### 12. 表格支持

| 项目 | 价格 | 数量 |
| :--- | ---: | :---: |
| 计算机 | $1600 | 5 |
| 手机 | $12 | 12 |
| 管线 | $1 | 234 |

### 13. 定义型列表

名词 1 : 定义 1（左侧有一个可见的冒号和四个不可见的空格）

代码块 2 : 这是代码块的定义（左侧有一个可见的冒号和四个不可见的空格）

```text
    代码块（左侧有八个不可见的空格）
```

### 14. Html 标签

本站支持在 Markdown 语法中嵌套 Html 标签，譬如，你可以用 Html 写一个纵跨两行的表格：

| 值班人员 | 星期一 | 星期二 | 星期三 |
| :--- | :--- | :--- | :--- |
| 李强 | 张明 | 王平 |  |

| 值班人员 | 星期一 | 星期二 | 星期三 |
| :--- | :--- | :--- | :--- |
| 李强 | 张明 | 王平 |  |

### 15. 内嵌图标

本站的图标系统对外开放，在文档中输入

```text
<i class="icon-weibo"></i>
```

即显示微博的图标： 

替换 上述 `i 标签` 内的 `icon-weibo` 以显示不同的图标，例如：

```text
<i class="icon-renren"></i>
```

即显示人人的图标： 

更多的图标和玩法可以参看 [font-awesome](http://fortawesome.github.io/Font-Awesome/3.2.1/icons/) 官方网站。

### 16. 待办事宜 Todo 列表

使用带有 \[ \] 或 \[x\] （未完成或已完成）项的列表语法撰写一个待办事宜列表，并且支持子列表嵌套以及混用Markdown语法，例如：

* [ ] **Cmd Markdown 开发**
  * [ ] 改进 Cmd 渲染算法，使用局部渲染技术提高渲染效率
  * [ ] 支持以 PDF 格式导出文稿
  * [x] 新增Todo列表功能 [语法参考](https://github.com/blog/1375-task-lists-in-gfm-issues-pulls-comments)
  * [x] 改进 LaTex 功能
    * [x] 修复 LaTex 公式渲染问题
    * [x] 新增 LaTex 公式编号功能 [语法参考](http://docs.mathjax.org/en/latest/tex.html#tex-eq-numbers)
* [ ] **七月旅行准备**
  * [ ] 准备邮轮上需要携带的物品
  * [ ] 浏览日本免税店的物品
  * [x] 购买蓝宝石公主号七月一日的船票

对应显示如下待办事宜 Todo 列表：

* [ ] **Cmd Markdown 开发**
  * [ ] 改进 Cmd 渲染算法，使用局部渲染技术提高渲染效率
  * [ ] 支持以 PDF 格式导出文稿
  * [x] 新增Todo列表功能 [语法参考](https://github.com/blog/1375-task-lists-in-gfm-issues-pulls-comments)
  * [x] 改进 LaTex 功能
    * [x] 修复 LaTex 公式渲染问题
    * [x] 新增 LaTex 公式编号功能 [语法参考](http://docs.mathjax.org/en/latest/tex.html#tex-eq-numbers)
* [ ] **七月旅行准备**
  * [ ] 准备邮轮上需要携带的物品
  * [ ] 浏览日本免税店的物品
  * [x] 购买蓝宝石公主号七月一日的船票

