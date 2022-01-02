## 介绍
==基本概念==

$Ax=\lambda x$ 任意不为零向量的 $x$ 使得等式成立

$\lambda$ 特征值
$x$ 特征向量

( 大部分 $A_{n\times n}$ 有 $n$ 个线性无关的特征向量 )

==求解==

$(A-\lambda I)x=0$ 

$\bigg|A-\lambda I\bigg|=0$ 特征方程

$\implies 特征多项式$

$\implies \lambda=$

==性质==

① $Ax=\lambda x$

$\quad A \implies \lambda$

$\quad A^2-3A+2I \implies \lambda^2-3\lambda+2$

② $det\ A=\lambda_1\lambda_2\lambda_3\dots\lambda_n$

③ $\displaystyle\sum_{i=1}^{n}\lambda_i = \displaystyle\sum_{i=1}^{n}a_{ii}$

④ $det\ (A-\lambda I)=det\ (A^T-\lambda I)\,$ 即 $A$ 与 $A^T$ 有相同的特征值

==对角化==

$S^{-1}AS=\Lambda$

$\begin{aligned}
AS=A\begin{bmatrix}x_1&x_2&x_3\end{bmatrix}&=\begin{bmatrix}\lambda_1x_1&\lambda_2x_2&\lambda_3x_3\end{bmatrix}\\\\
&=\begin{bmatrix}x_1&x_2&x_3\end{bmatrix}\begin{bmatrix}\lambda_1&0&0\\\ &\lambda_2&0\\\ &\ &\lambda_3\end{bmatrix}\\\\
&=S\Lambda
\end{aligned}$

$x_i$ 为特征向量 , $\lambda_i$ 为特征值

当 $S$ 可逆 , 可对角化

==相似==

$B=M^{-1}AM$

特征值一样

**证明**

$\qquad Ax=\lambda x$

$\qquad (M^{-1}AM)M^{-1}x=\lambda M^{-1}x$

$\qquad B(M^{-1}x)=\lambda (M^{-1}x)$

$\begin{bmatrix}4&0\\0&4\end{bmatrix} 和 \underbrace{\begin{bmatrix}4&1\\0&4\end{bmatrix}}_{Jordan\ form}$ 特征值一样 , 但不相似 ( 它们之间不能构建等式 )

## Fibonacci
$\begin{bmatrix}F_1\\F_2\end{bmatrix}=A\begin{bmatrix}F_1\\F_0\end{bmatrix}$
$\,$

$\begin{cases}
\mu_{k+1}=A\mu_{k}\\\\
\mu_0=c_1x_1+c_2x_2+c_3x_3+\cdots+c_nx_n=SC
\end{cases}$
$\,$

$\begin{aligned}
\mu_{100}&=A^{100}\mu_0\\\\
&=c_1A^{100}x_1+c_2A^{100}x_2+c_3A^{100}x_3+\cdots+c_nA^{100}x_n\\\\
&=c_1\lambda_1^{100}x_1+c_2\lambda_2^{100}x_2+c_3\lambda_3^{100}x_3+\cdots+c_n\lambda_n^{100}x_n\\\\
&=S\Lambda^{100}C
\end{aligned}$

( $S$ 即是特征向量的集合)

<!--
## 一阶常系数线性微分方程
方程组：$\displaystyle\begin{bmatrix}u_1'\\u_2'\end{bmatrix}=A\begin{bmatrix}u_1\\u_2\end{bmatrix}$

解的形式：$u(t)=c_1e^{\lambda_1 t}x_1+c_2e^{\lambda_2 t}x_2$

$\begin{bmatrix}\lambda_1c_1e^{\lambda_1 t}x_{11}+\lambda_2c_2e^{\lambda_2 t}x_{21}\\\\
\lambda_1c_1e^{\lambda_1 t}x_{12}+\lambda_2c_2e^{\lambda_2 t}x_{22}\end{bmatrix}=A\begin{bmatrix}c_1e^{\lambda_1 t}x_{11}+c_2e^{\lambda_2 t}x_{21}\\\\c_1e^{\lambda_1 t}x_{12}+c_2e^{\lambda_2 t}x_{22}\end{bmatrix}$

$\lambda_1\begin{bmatrix}c_1e^{\lambda_1 t}x_{11}\\\\c_1e^{\lambda_1 t}x_{12}\end{bmatrix}+\lambda_2\begin{bmatrix}c_2e^{\lambda_2 t}x_{21}\\\\c_2e^{\lambda_2 t}x_{22}\end{bmatrix}=A\left(\begin{bmatrix}c_1e^{\lambda_1 t}x_{11}\\\\c_1e^{\lambda_1 t}x_{12}\end{bmatrix}+\begin{bmatrix}c_2e^{\lambda_2 t}x_{21}\\\\c_2e^{\lambda_2 t}x_{22}\end{bmatrix}\right)$
-->

## 对称矩阵
==① 对称矩阵的特征值为实数==

证明

$\qquad$前提：若 $A$有 特征向量 $\bar{x}$ 为虚 , 那一定对应有 $x$ 也为其的特征向量 , 原因我暂时不知 , 可能与 `特征多项式` 的形式有关 :confused:

$\qquad\begin{cases}
Ax=\lambda x \Longrightarrow \,\,\, \bar{x}^TAx=\lambda\bar{x}^Tx\\\\
A\bar{x}=\lambda \bar{x} \xRightarrow{转置} \bar{x}^TA=\bar{\lambda} \bar{x}^T\implies  \bar{x}^TAx=\lambda\bar{x}^Tx
\end{cases}$

$\qquad \implies \bar{\lambda}=\lambda\quad$ 假设不成立

==② signs of pivots same as signs of $\lambda$s==

==③ 有 $n$ 个特征值 , 可以被对角化==

## 正定矩阵
==性质==
1. $subdetermination\ is\ positive$
2. $\lambda s>0$
3. $Pivots>0$
4. $\forall x \quad x^TAx>0$
$\,$
5. $\begin{cases}
x^TAx>0\\
x^TBx>0
\end{cases}\implies x^T(A+B)x>0$

==$A^TA$==

$x^T\big(A^TA\big)x={(Ax)}^TAx$

即是 $Ax$ 长度的平方

$A_{m\times n}$ , 当 $m>n \text{ , } rank\ A=n$ 时 

$Ax\not = 0$

$x^T\big(A^TA\big)x\geq 0$

$Ax$ 正定

