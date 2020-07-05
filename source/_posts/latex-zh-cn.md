---
title: LaTeX 中文支持
date: 2020-07-04 22:30:41
categories: LaTeX 教程
---

LaTeX 最初是不支持中文的，后来才添加了unicode 字符的支持。经过热爱 LaTeX 的开源英雄们的努力，现在可以愉快的在 LaTeX 中编写中文了。

LaTeX 的中文支持方案有 CTeX，ctexart 以及 xeCJK 三个方案，我们推荐使用 xeCJK 方案。在使用 xeCJK 时，需要使用 xelatex 编译 LaTeX 文档。

一个简短的示例 LaTeX 文档：

```
\documentclass{article}

\usepackage{xeCJK}
\setCJKmainfont{Microsoft YaHei}

\begin{document}

\par 你好，世界!

\end{document}
```

在 TeXPage 中的效果:

![cn-demo](https://latex-static-1251145186.cos.ap-shanghai.myqcloud.com/latex-zh-cn-demo.png)

`\usepackage{xeCJK}` 是用来引入 xeCJK 包。

`\setCJKmainfont{Microsoft YaHei}` 是用来设置正文的中文字体, 大括号里填写的就是字体名称，这里填写的字体名称您的 LaTeX 编译环境中必须要有对应的字体。

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
