# 01_gioi_thieu_latex.md

````markdown
# Giới thiệu LaTeX

## LaTeX là gì?

LaTeX là hệ thống typesetting dùng để soạn thảo:

- Báo cáo kỹ thuật
- Luận văn
- Tài liệu khoa học
- Công thức toán học
- Slide trình chiếu

LaTeX mạnh hơn Word ở:

- Quản lý tài liệu lớn
- Công thức toán đẹp
- Tự động đánh số
- Quản lý mục lục
- Cross-reference
- Bibliography

**Trong LaTeX, thứ tự level section là:**

\part

\chapter

\section

\subsection

\subsubsection

\paragraph

\subparagraph

---

## Compile cơ bản

```bash
xelatex main.tex
````

---

## Cấu trúc file cơ bản

```latex
\documentclass{article}

\begin{document}

Hello LaTeX

\end{document}
```

````

---

# 02_cau_truc_tai_lieu.md

```markdown
# Cấu trúc tài liệu

## Document class

```latex
\documentclass[12pt,a4paper]{article}
````

Các class phổ biến:

| Class   | Ý nghĩa      |
| ------- | ------------ |
| article | Báo cáo ngắn |
| report  | Báo cáo lớn  |
| book    | Sách         |
| beamer  | Slide        |

---

## Package

```latex
\usepackage{graphicx}
```

---

## Begin/End document

```latex
\begin{document}
...
\end{document}
```

---

## Title

```latex
\title{HELLO}
\author{THK}
\date{\today}

\maketitle
```

````

---

# 03_format_van_ban.md

```markdown
# Format văn bản

## In đậm

```latex
\textbf{Hello}
````

## In nghiêng

```latex
\textit{Hello}
```

## Gạch chân

```latex
\underline{Hello}
```

---

## Xuống dòng

```latex
Line 1 \\
Line 2
```

---

## Căn giữa

```latex
\begin{center}
Hello
\end{center}
```

---

## Căn trái/phải

```latex
\begin{flushleft}
Text
\end{flushleft}
```

```latex
\begin{flushright}
Text
\end{flushright}
```

````

---

# 04_section_va_muc_luc.md

```markdown
# Section và mục lục

## Section

```latex
\section{Introduction}
````

## Subsection

```latex
\subsection{USB}
```

## Subsubsection

```latex
\subsubsection{Descriptor}
```

---

## Table of contents

```latex
\tableofcontents
```

---

## Đánh dấu label

```latex
\section{TCP/IP}
\label{sec:tcp}
```

---

## Reference

```latex
Xem mục \ref{sec:tcp}
```

````

---

# 05_toan_hoc_latex.md

```markdown
# Toán học LaTeX

## Inline math

```latex
$a+b=c$
````

---

## Display math

```latex
\[
a^2+b^2=c^2
\]
```

---

## Fraction

```latex
\frac{a}{b}
```

---

## Căn bậc hai

```latex
\sqrt{x}
```

---

## Mũ

```latex
x^2
```

---

## Chỉ số dưới

```latex
x_1
```

---

## Sigma

```latex
\sum_{i=0}^{n}
```

---

## Tích phân

```latex
\int_a^b f(x)dx
```

---

## Matrix

```latex
\begin{bmatrix}
1 & 2 \\
3 & 4
\end{bmatrix}
```

````

---

# 06_hinh_anh_va_bang.md

```markdown
# Hình ảnh và bảng

## Chèn package

```latex
\usepackage{graphicx}
````

---

## Chèn ảnh

```latex
\begin{figure}[h]
    \centering
    \includegraphics[width=0.5\textwidth]{image.png}
    \caption{Demo}
    \label{fig:test}
\end{figure}
```

---

## Table cơ bản

```latex
\begin{tabular}{|c|c|}
\hline
A & B \\
\hline
1 & 2 \\
\hline
\end{tabular}
```

---

## Booktabs đẹp hơn

```latex
\usepackage{booktabs}
```

````

---

# 07_code_va_listing.md

```markdown
# Code và listing

## Package listings

```latex
\usepackage{listings}
````

---

## Hiển thị code C

```latex
\begin{lstlisting}[language=C]
int main()
{
    return 0;
}
\end{lstlisting}
```

---

## Hiển thị số dòng

```latex
\begin{lstlisting}[language=C,numbers=left]
...
\end{lstlisting}
```

---

## Đổi font code

```latex
\ttfamily
```

````

---

# 08_header_footer_va_layout.md

```markdown
# Header Footer và Layout

## Geometry

```latex
\usepackage[
left=3cm,
right=2cm,
top=2.5cm,
bottom=2.5cm
]{geometry}
````

---

## Fancyhdr

```latex
\usepackage{fancyhdr}
```

---

## Header/Footer

```latex
\pagestyle{fancy}

\fancyhead[L]{Embedded}
\fancyhead[R]{BKU}

\fancyfoot[C]{\thepage}
```

---

## New page

```latex
\newpage
```

````

---

# 09_hyperlink_va_mau_sac.md

```markdown
# Hyperlink và màu sắc

## Hyperref

```latex
\usepackage{hyperref}
````

---

## Tạo link

```latex
\href{https://google.com}{Google}
```

---

## Xcolor

```latex
\usepackage{xcolor}
```

---

## Text color

```latex
\textcolor{red}{Hello}
```

---

## Background color

```latex
\colorbox{yellow}{Text}
```

````

---

# 10_xelatex_va_tieng_viet.md

```markdown
# XeLaTeX và tiếng Việt

## Fontspec

```latex
\usepackage{fontspec}
````

---

## Set font

```latex
\setmainfont{Times New Roman}
```

---

## Compile bằng XeLaTeX

```bash
xelatex main.tex
```

---

## Babel tiếng Việt

```latex
\usepackage[vietnamese]{babel}
```

---

## Template tiếng Việt hoàn chỉnh

```latex
\documentclass[12pt,a4paper]{report}

\usepackage{fontspec}
\setmainfont{Times New Roman}

\usepackage[vietnamese]{babel}
\usepackage{graphicx}
\usepackage{amsmath}
\usepackage{geometry}

\begin{document}

Hello Việt Nam

\end{document}
```

````

---

# 11_template_bao_cao_hoan_chinh.md

```markdown
# Template báo cáo hoàn chỉnh

```latex
\documentclass[12pt,a4paper]{report}

\usepackage{fontspec}
\setmainfont{Times New Roman}

\usepackage[vietnamese]{babel}

\usepackage{graphicx}
\usepackage{amsmath}
\usepackage{amssymb}
\usepackage{xcolor}
\usepackage{hyperref}
\usepackage{geometry}
\usepackage{fancyhdr}
\usepackage{listings}

\geometry{
left=3cm,
right=2cm,
top=2.5cm,
bottom=2.5cm
}

\pagestyle{fancy}
\fancyhead[L]{Embedded Linux}
\fancyhead[R]{BKU}
\fancyfoot[C]{\thepage}

\begin{document}

\title{USB RNDIS Report}
\author{Tran Hoang Kien}
\date{\today}

\maketitle

\tableofcontents

\chapter{Introduction}

Hello LaTeX

\chapter{Math}

\[
F = ma
\]

\chapter{Image}

\begin{figure}[h]
    \centering
    \includegraphics[width=0.5\textwidth]{image.png}
    \caption{Demo}
\end{figure}

\end{document}
````

```
```
