---
title: LaTeX 中文支持
date: 2020-07-04 22:30:41
categories: LaTeX 教程
---

LaTeX 最初是不支持中文的，后来才添加了unicode 字符的支持。经过热爱 LaTeX 的开源英雄们的努力，现在可以愉快的在 LaTeX 中编写中文了。

LaTeX 的中文支持方案主要有两类：ctex 和 xeCJK。其实在使用 xelatex 编译时，ctex 也是通过调用 xeCJK 来实现的。

### 1. ctex 的用法

ctex 中文支持的用法主要有两种，一是直接使用 ctex，二是使用 ctex 相关的文档类。

**使用 ctex 的文档类例子：**
```
\documentclass{ctexart}

\usepackage{xeCJK}
\setCJKmainfont{Microsoft YaHei}

\begin{document}

\par 你好，世界!

\end{document}
```

ctex 提供的文档类有：`ctexart、ctexrep、ctexbook、ctexbeamer`，这几个文档类其实就是 LaTeX 中默认的这几个文档类 `article、report、book、beamer` 的汉化版本。

**使用 ctex 宏包的例子:**
```
\documentclass{article}  
\usepackage[UTF8]{ctex}

\begin{document}

\par 你好，世界!

\end{document}
```
在使用时，需要指定 UTF8 编码, 就是中括号里的 UTF8 `\usepackage[UTF8]{ctex}` 

**怎么选择使用哪一种方式呢？**

* 如果编写的文档绝大部分是中文的，建议直接使用 ctex 的文档类
* 如果编写的文档中英文都不少，建议使用 ctex 宏包

### 2. xeCJK 的用法

xeCJK 是比较底层的，如果很熟悉 xeCJK 的大佬，直接使用 xeCJK 会更顺手，一般用户还是使用 ctex 更方便些。

xeCJK 例子：

```
\documentclass{article}

\usepackage{xeCJK}
\setCJKmainfont{Microsoft YaHei}

\begin{document}

\par 你好，世界!

\end{document}
```

`\usepackage{xeCJK}` 是用来引入 xeCJK 包。

`\setCJKmainfont{Microsoft YaHei}` 是用来设置正文的中文字体, 大括号里填写的就是字体名称，这里填写的字体名称您的 LaTeX 编译环境中必须要有对应的字体。

无论用哪种方式，TeXPage 都是支持的，可以在 TeXPage 中新建个文档体验下效果。[前往 TeXPage >>](https://www.texpage.com)

在 TeXPage 中的效果:

![cn-demo](https://latex-static-1251145186.cos.ap-shanghai.myqcloud.com/latex-zh-cn-demo.png)

TeXPage 支持的中文字体列表：

```
% 微软雅黑
Microsoft YaHei

% 宋体 
SimSun

% 黑体
SimHei

% 楷体
KaiTi

% 幼园
YouYuan

% 隶书
LiSu

% 仿宋
FangSong
```
<small>您在使用相关中文字体时，请留意相关字体的版权。</small>
