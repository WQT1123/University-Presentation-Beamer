# SCU-Presentation-Beamer
四川大学的 Beamer 演示文稿模板 `scuwqt`，旨在为四川大学的师生提供一个简洁、美观且具有学校特色的演示文稿制作工具。包含三个校区的配图，以川大红为主要用色。

## 特性

- **颜色主题**：采用四川大学的官方色彩，提供统一的视觉体验。
- **中英文字体支持**：内置中英文字体配置，保证演示文稿的国际化和本地化表达。
- **自定义背景**：支持自定义首页背景和通用页脚背景，易于添加个性化元素。
- **内容布局**：提供标题页、目录页、内容页等基础布局模板，方便快速制作演示文稿。

## 使用方法

### 本地 LaTeX 环境

1. **安装 LaTeX 环境**：确保你的计算机上安装了 LaTeX 环境，推荐使用 [TeX Live](https://www.tug.org/texlive/)，并确保可以运行 XeLaTeX 编译器。

2. **下载模板**：从 [GitHub 仓库](https://github.com/WQT1123/SCU-Presentation-Beamer) 下载 `scuwqt.sty` 文件和相关资源（如背景图片、logo等）。

3. **编写文档**：在你的 `.tex` 文件的导言区使用 `\usepackage{scuwqt}` 来引入模板。配置你的演示文稿的标题、作者等信息。

4. **编译文档**：使用 XeLaTeX 编译器编译你的 `.tex` 文件，生成演示文稿。

### 在 Overleaf 上编译

1. **创建新项目**：在 Overleaf 上创建一个新项目，并上传 `scuwqt.sty` 文件及相关资源。

2. **编写文档**：在 Overleaf 的编辑器中，创建一个新的 `.tex` 文件，或者上传你已经编写的 `.tex` 文件。确保在文档的导言区引入了 `scuwqt` 模板。

3. **选择编译器**：在 Overleaf 项目的设置中，选择 XeLaTeX 作为编译器。

4. **编译项目**：点击 Overleaf 编辑器中的“编译”按钮，Overleaf 将使用 XeLaTeX 编译你的文档。
## Beamer 命令指南

本指南提供了一系列在Beamer中常用的指令，适用于特定的Beamer模板。包括页面分割、插入链接、图片、表格，以及文本格式调整等功能。

在Beamer中，可以使用`columns`环境来实现页面的水平分割，将页面分为左右两个部分。
```latex
% 使用columns环境进行水平分割
\begin{columns}
  \begin{column}{0.5\textwidth}
    % 左侧内容
  \end{column}
  \begin{column}{0.5\textwidth}
    % 右侧内容
  \end{column}
\end{columns}

% 使用minipage环境进行垂直分割
\begin{minipage}[t]{\linewidth}
  % 页面上部内容
\end{minipage}
\begin{minipage}[b]{\linewidth}
  % 页面下部内容
\end{minipage}

% 插入链接
\href{http://www.example.com}{链接文本}

% 插入图片
\includegraphics[width=\textwidth]{path/to/image}

% 创建基础表格
\begin{tabular}{|l|c|r|}
  \hline
  左 & 中 & 右 \\
  \hline
  项目1 & 项目2 & 项目3 \\
  \hline
\end{tabular}

% 创建三线表
\usepackage{booktabs} % 需要在导言区加载booktabs包
\begin{tabular}{lcr}
  \toprule
  左 & 中 & 右 \\
  \midrule
  项目1 & 项目2 & 项目3 \\
  \bottomrule
\end{tabular}

% 着重标记文本
\emph{着重文本}

% 改变文本颜色
\textcolor{Primary}{主色文本}

% 改变字体大小
{\tiny 极小文本}
{\small 小文本}
{\normalsize 正常文本}
{\large 大文本}
{\Large 更大文本}
{\LARGE 非常大文本}
{\huge 巨大文本}

% 创建项目符号列表
\begin{itemize}
  \item 第一项
  \item 第二项
\end{itemize}

% 创建描述列表
\begin{description}
  \item[术语] 定义
  \item[概念] 解释
\end{description}
```

## 致谢

首先，我要感谢四川大学提供的丰富学习资源和灵感，使得本 Beamer 模板项目得以实现。学校的学术氛围和视觉识别系统为模板的设计提供了重要的参考和依据。

特别感谢 [Texlive 社区](https://www.tug.org/texlive/) 和 [Overleaf](https://www.overleaf.com) 提供的强大 LaTeX 支持和在线编译平台，让 LaTeX 文档的编写和分享变得更加便捷。

对于 `AR PL KaitiM GB` 字体的开发者，我表示衷心的感谢。这款字体的优雅和可读性为本模板的中文展示质量增色不少。

感谢 [GPT-4](https://chat.openai.com/g/g-tDi9X7Pjd-latex-ppt) 提供的智能写作支持，让文档编写和创意发想更加高效和有趣。

此外，我还要感谢所有测试、使用和提供反馈的用户。你们的意见和建议对于模板的改进和完善至关重要。

最后，对所有支持开源项目和贡献于开源社区的个人和组织表示感谢。是你们的奉献使得这样的项目得以实现并不断进步。


## 示例代码

以下是一个使用 `scuwqt` Beamer 模板的 LaTeX 示例。此示例包括基本的演示文稿结构，如标题页、目录、几个内容板块，以及如何在演示文稿中使用表格和图片。

```latex
\documentclass{beamer}
\usepackage{scuwqt} % 使用 scuwqt 模板
\usepackage{booktabs} % 用于更好的表格线条
\setlength\parindent{2em} % 设置段落缩进
\renewcommand{\arraystretch}{1.5} % 调整表格行距

% 设置中文环境
\setCJKfamilyfont{font01}{AR PL KaitiM GB}
\newcommand{\fonta}{\CJKfamily{font01}}

% 演示文稿信息
\title{Title here}
\author{Candidate：  \ Advisor ：}
\institute{College of xxxx at Sichuan University}
\date{\today}

\begin{document}

\begin{frame}
  \titlepage % 标题页
\end{frame}

% 目录页
\begin{frame}
  \hfill
  \begin{minipage}[t]{.4\textwidth}
    \tableofcontents
  \end{minipage}
\end{frame}

% 引言部分
\section{Introduction}
\begin{frame}{Introduction}
  % 内容...
\end{frame}

% 研究意义
\section{Research Significance}
\begin{frame}{Research Significance}
  % 内容...
\end{frame}

% 技术路线
\section{Technical Route}
\subsection{Technical Route1}
\begin{frame}{Technical Route1}
  % 内容...
\end{frame}

% 结论
\section{Conclusion}
\begin{frame}{Conclusion}
  % 内容...
\end{frame}

% 参考文献
\section{References}
\begin{frame}{References}
  % 内容...
\end{frame}

% 致谢
\section{Acknowledgements}
\begin{frame}{Acknowledgements}
  % 内容...
\end{frame}

\end{document}
```
确保将示例代码中的图片路径替换为实际的图片文件路径，以及根据实际情况调整文档内容。

此外，为了提高效率，建议大家在编写 LaTeX 文档时结合使用 ChatGPT。ChatGPT 不仅能帮助解答 LaTeX 相关的问题，还能协助编写代码，从而大大提高编写和调试 LaTeX 文档的效率。


    
