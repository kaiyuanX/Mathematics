## 基的变换
不同基下的同一个点( 坐标系不变 )

$\big[\ B\ \big]\ ,\ \big[\ C\ \big] \in R^n$ ( $R^n$ 的基 )

设 $P_{C\gets B}[x]_B=[x]_C$

$\,$
① 

$\big[\ B\ \big]{[x]}_B=\big[\ C\ \big][x]_C\implies \color{red}{P_{C\gets B}={\big[\ C\ \big]}^{-1}\big[\ B\ \big]}$
$\,$

② $\begin{cases}
[x]_B=\begin{bmatrix}r_1\\r_2\\\vdots\\r_n\end{bmatrix}\\\\
\begin{aligned}
[x]_C&=[r_1b_1+r_2b_2+\cdots+r_nb_n]_C\\&=r_1[b_1]_C+r_2[b_2]_C+\cdots+r_n[b_n]_C
\end{aligned}
\end{cases}\implies \color{red}{P_{C\gets B}=\begin{bmatrix}[b_1]_C&[b_2]_C&\cdots&[b_n]_C\end{bmatrix}}$
$\,$

$\Big[C\quad B\Big]\thicksim\Big[I\quad P_{C\gets B}\Big]$
$\,$

$\Big(P_{C\gets B}\Big)^{-1}= P_{B\gets C}$

## 线性变换
设 $\Big[T(x)\Big]_C=M[x]_B$
$\,$

①

$\big[\ B\ \big]\in R^n\ ,\ \big[\ C\ \big] \in R^m$
$\,$

$[x]_B=\begin{bmatrix}r_1\\r_2\\\vdots\\r_n\end{bmatrix}$
$\,$

$T(x)=T(r_1b_1+r_2b_2+\cdots+r_nb_n)$
$\,$

$\Big[T(x)\Big]_C=r_1\Big[T(b_1)\Big]_C+r_2\Big[T(b_2)\Big]_C+\cdots+r_n\Big[T(b_n)\Big]_C$
$\,$

$\color{red}{M=\Bigg[\Big[T(b_1)\Big]_C \quad \Big[T(b_2)\Big]_C \quad \cdots \quad \Big[T(b_n)\Big]_C\Bigg]}$

② 

$Ax=T(x)$

$A\big[\ B\ \big][x]_B=\big[\ C\ \big]\Big[T(x)\Big]_C$

${\big[\ C\ \big]}^{-1}A\big[\ B\ \big][x]_B=\Big[T(x)\Big]_C$

$\color{red}{M={\big[\ C\ \big]}^{-1}A\big[\ B\ \big]}$
$\,$
$\,$

**特别的 , 当 $\big[\ C\ \big]=\big[\ B\ \big]$**

$M={\big[\ B\ \big]}^{-1}A\big[\ B\ \big]=\overbrace{{\big[\ B\ \big]}^{-1}I}^{P_{B\gets I}}A\overbrace{I^{-1}\big[\ B\ \big]}^{P_{I\gets B}}$

$M[x]_B$ 把基 $B$ 下的向量 $x$

1. 先标准化
2. 进行 $A$ 变换
3. 换原为基 $B$ 的视角