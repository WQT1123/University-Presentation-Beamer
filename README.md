# University-Presentation-Beamer
此项目包含各个大学的 Beamer 演示文稿模板 （SCU、HIT、USTC），旨在为大学师生提供一个简洁、美观且具有学校特色的演示文稿制作工具。

## 特性

- **灵活的院校选择**：通过`\setuniversity{}`命令实现对不同院校的选择
- **内容布局**：内置`\titlepages` `\contentpage` `\thankyou`等指令，对应于起始页、目录页和致谢页。（如需修改，需要在`scuwqt`中进行操作。）

## 使用方法

### 本地 LaTeX 环境

1. **安装 LaTeX 环境**：确保你的计算机上安装了 LaTeX 环境，推荐使用 [TeX Live](https://www.tug.org/texlive/)，并确保可以运行 XeLaTeX 编译器。

2. **下载模板**：从 [GitHub 仓库](https://github.com/WQT1123/SCU-Presentation-Beamer) 下载 `University` 文件夹。

3. **编写文档**：在你的 `Presentation.tex` 文件中开始你的Latex之旅（替换图片、更改颜色等操作请在`scuwqt`中进行修改）。

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

此外，我还要感谢所有测试、使用和提供反馈的用户。你们的意见和建议对于模板的改进和完善至关重要。

最后，对所有支持开源项目和贡献于开源社区的个人和组织表示感谢。是你们的奉献使得这样的项目得以实现并不断进步。


## 示例代码

以下是一个使用 `scuwqt` Beamer 模板的 LaTeX 示例。

```latex
\documentclass[aspectratio=1610]{beamer}
\usepackage{scuwqt}
\setuniversity{SCU}
%=========================================================
\title{四川大学LaTeX模版}
\author{Jack \ Ma}
\vspace{12pt}
\institute{四川大学 退学工程}
\date{\today}
\begin{document}
%=========================================================
\titlepages%切入首页
\contentspage%切入目录页
%=========================================================
%正文开始！！！
\section{Section1}
\begin{frame}
  \begin{minipage}[t][0.4\textheight][t]{\textwidth}
      \begin{columns}[t]
          % 左边区域
          \begin{column}{0.3\textwidth}
            \begin{figure}
              \includegraphics[width=\textwidth]{girl.jpg}
            \end{figure}
              
          \end{column}
          % 右边区域
          \begin{column}{0.7\textwidth}
             \begin{itemize}
              \item 教育经历：四川大学/退学工程
              \item 修读课程：\begin{itemize}
                              \item 材料力学、理论力学
                            \end{itemize}
              \item 英文水平:CET4、CET6           
             \end{itemize}
           
          \end{column}
      \end{columns}
  \end{minipage}
  \vspace{0.5cm}
\begin{minipage}[t][0.5\textheight][t]{\textwidth}
\skill{睡觉}{0,1}{任何时间任何地点，想睡就睡。}
\skill{摸鱼}{0,1,2}{擅长摸鱼不被发现}
\end{minipage}
\end{frame}
%===============================================
\section{Section2}
\subsection{Subsection1}
\begin{frame}{title}
\begin{columns}
  \begin{column}{0.5\textwidth}
    

  \end{column}
  \begin{column}{0.5\textwidth}
    
    

  \end{column}
  
\end{columns}
\end{frame}
\subsection{Subsection2}
\begin{frame}
  
\end{frame}
%===============================================
\section{致谢}
\thankyou
\end{document}

```
确保将示例代码中的图片路径替换为实际的图片文件路径，以及根据实际情况调整文档内容。

此外，为了提高效率，建议大家在编写 LaTeX 文档时结合使用 ChatGPT。ChatGPT 不仅能帮助解答 LaTeX 相关的问题，还能协助编写代码，从而大大提高编写和调试 LaTeX 文档的效率。


    
