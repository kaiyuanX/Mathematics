## 奇异分解 (the singular value decomposition)
==$A=U\Sigma V^{-1}$==

$A_{m\times n}$

$\begin{aligned}
A\begin{bmatrix}v_1&v_2&\cdots&v_r&\cdots&v_n\end{bmatrix}&=\begin{bmatrix}u_1&u_2&\cdots&u_r&\cdots&u_m\end{bmatrix}\begin{bmatrix}\sigma_1&\ &\ &\ \ \\\ &\sigma_2\\\ &\ &\ddots\\\ &\ &\ &\ \sigma_r\\\ &\ &\ &\ \ &\ddots\\\ &\ &\ &\ \ &\ &0\end{bmatrix}\\AV&=U\Sigma\\
\end{aligned}$


其中 $r$ 为 $rank$ 

$v\ u$ 单位正交

$v$ 为行空间的基

$u$ 为列空间的基

填充 $\begin{cases}v_{r+1}\cdots v_n &N(A)\\u_{r+1}\cdots u_m&N(A^T)\end{cases}$

## $A^TA$
$A=U\Sigma V^{-1}$

$A^TA={(U\Sigma V^{-1})}^TU\Sigma V^{-1}$

① $A^TA=V\Sigma^2 V^T$

② $A^TA=U\Sigma^2 U^T$