---
title: Latex使用指南
date: 2026-03-13 21:05:53
tags: 
  - Latex
categories: 
  - 随笔
mathjax: true
---

这份Latex使用指南旨在帮你快速掌握最常用的 LaTeX 语法，建议收藏备用。

---

## 1. 基础结构与模式

在 LaTeX 中，最核心的概念是**命令**和**环境**。

* **命令：** 通常以反斜杠开头，例如 `\command{argument}`。
* **数学模式：**
* **行内公式 (Inline):** 使用 `$公式内容$`，例如：$E=mc^2$。
* **行间公式 (Display):** 使用 `$$公式内容$$`，公式会独立成行并居中。



---

## 2. 常用数学符号

这里是公式编辑中最常用的“零件”：

### 上标与下标

* **下标：** 使用 `_`，如 `x_n` $\rightarrow x_n$
* **上标：** 使用 `^`，如 `x^2` $\rightarrow x^2$
* **组合使用：** 如果内容超过一个字符，必须用花括号 `{}` 包起来，如 `x_{i+1}^{n-1}` $\rightarrow x_{i+1}^{n-1}$

### 希腊字母

| 输入 | 结果 | 输入 | 结果 |
| --- | --- | --- | --- |
| `\alpha` | $\alpha$ | `\beta` | $\beta$ |
| `\gamma` | $\gamma$ | `\delta` | $\delta$ |
| `\pi` | $\pi$ | `\Omega` | $\Omega$ |
| `\theta` | $\theta$ | `\lambda` | $\lambda$ |

### 运算符与分式

* **分式：** `\frac{分子}{分母}` $\rightarrow \frac{a}{b}$
* **根号：** `\sqrt{x}` $\rightarrow \sqrt{x}$，`\sqrt[n]{x}` $\rightarrow \sqrt[n]{x}$
* **乘除：** `\times` ($\times$), `\div` ($\div$)
* **不等式：** `\le` ($\le$), `\ge` ($\ge$), `\neq` ($\neq$)

---

## 3. 复杂结构

### 求和、积分与极限

这些符号通常需要配合上下限使用：

* **求和：** `\sum_{i=1}^n` $\rightarrow \sum_{i=1}^n$
* **积分：** `\int_a^b f(x)dx` $\rightarrow \int_a^b f(x)dx$
* **极限：** `\lim_{x \to \infty}` $\rightarrow \lim_{x \to \infty}$

### 矩阵 (Matrix)

矩阵需要用到环境 `\begin{...} ... \end{...}`。常见的类型有：

* `matrix`: 无括号
* `pmatrix`: 圆括号 $()$
* `bmatrix`: 方括号 $[]$

**示例代码：**

```latex
\begin{bmatrix}
1 & 0 \\
0 & 1
\end{bmatrix}

```

渲染效果：


$$\begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}$$

> **小贴士：** 在矩阵内部，`&` 用于分隔列，`\\` 用于分隔行。

---

## 4. 括号自适应大小

如果你写一个很高的分式，普通的括号会显得很小：$(\frac{a}{b})$。
使用 `\left` 和 `\right` 可以让括号自动包住内容：

* 输入：`\left( \frac{a}{b} \right)`
* 结果：$\left( \frac{a}{b} \right)$

---

## 5. 常用环境备忘表

| 环境名称 | 用途 |
| --- | --- |
| `equation` | 自动编号的行间公式 |
| `align` | 多行公式对齐（通常用 `&` 对齐等号） |
| `itemize` | 无序列表 |
| `enumerate` | 有序列表 |

---

## 快速速查示例

如果你需要写一个复杂的公式，可以参考这个：

**输入：**

```latex
f(x) = \int_{-\infty}^{\infty} \hat{f}(\xi) e^{2\pi i x \xi} d\xi

```

**结果：**


$$f(x) = \int_{-\infty}^{\infty} \hat{f}(\xi) e^{2\pi i x \xi} d\xi$$

---

希望这份指南能帮你快速上手！LaTeX 的学习曲线虽然初期陡峭，但只要多练几次常用的命令，后期效率极高。

**需要我帮你把某个具体的数学公式转换成 LaTeX 代码，或者为你生成一个学术论文的 LaTeX 基础模版吗？**