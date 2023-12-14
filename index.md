## Welcome to GitHub Pages

>1.假设 $A$ 是 $s\times n$ 实矩阵，在通常的内积下，$A$的每个行向量的长度为$a$，任意两个不同的列向量的内积为$b$，其中$a,b$是两个固定的实数.
>
>(1) 求矩阵$AA^T$的行列式.
>
>(2) 若$a^2>b\geq 0$，证明:$AA^T$的特征值均大于零.

$\textbf{解}$ (1) 
$$\begin{aligned}
        |AA^T|&=\begin{vmatrix}
            a^2&b&\cdots&b\\
            b&a^2&\cdots&b\\
            \vdots&\vdots&\ddots&\vdots\\
            b&b&\cdots&a^2
        \end{vmatrix}=[a^2+(s-1)b]\begin{vmatrix}
            1&b&\cdots&b\\
            1&a^2&\cdots&b\\
            \vdots&\vdots&\dots&\vdots\\
            1&b&\cdots&a^2
        \end{vmatrix}\\
        &=[a^2+(s-1)b]\begin{vmatrix}
            1&b&\cdots&b\\
            0&a^2-b&\cdots&0\\
            \vdots&\vdots&\ddots&\vdots\\
            0&0&\cdots&a^2-b
        \end{vmatrix}=[a^2+(s-1)b](a^2-b)^{s-1}
    \end{aligned}$$
(2) 由于
$$\begin{aligned}
        |\lambda E-AA^T|&=\begin{vmatrix}
            \lambda-a^2&-b&\cdots&-b\\
            -b&\lambda-a^2&\cdots&-b\\
            \vdots&\vdots&\ddots&\vdots\\
            -b&-b&\cdots&\lambda-a^2
        \end{vmatrix}=[\lambda-a^2+(s-1)(-b)]\begin{vmatrix}
            1&-b&\cdots&-b\\
            1&\lambda-a^2&\cdots&-b\\
            \vdots&\vdots&\ddots&\vdots\\
            1&-b&\cdots&\lambda-a^2
        \end{vmatrix}\\
        &=[\lambda-a^2+(s-1)(-b)]\begin{vmatrix}
            1&-b&\cdots&-b\\
            0&\lambda-a^2+b&\cdots&0\\
            \vdots&\vdots&\ddots&\vdots\\
            0&0&\cdots&\lambda-a^2+b
        \end{vmatrix}=[\lambda-a^2+(s-1)(-b)](\lambda-a^2+b)^{s-1}
    \end{aligned}$$
故$AA^T$的特征值为$a^2+b(s-1),a^2-b$($s-1$重)，当$a^2>b>0$时，$AA^T$的特征值均大于0.

>2.设 $A, B$ 均是正定矩阵, 证明:
>
>(1) 方程 $|\lambda A-B|=0$ 的根均大于 0 .
>
>(2) 方程 $|\lambda A-B|=0$ 的所有根等于 1 当且仅当 $A=B$.

$\textbf{证明}$ (1) $A$是正定阵，故$|A|>0\ne 0$，自然$A$可逆.由$|\lambda A-B|=|A||\lambda E-A^{-1}B|=0$可得，$|\lambda E-A^{-1}B|=0$，方程的解就是$A^{-1}B$的特征值.而$A^{-1}B$为正定矩阵，那么$A^{-1}B$的特征值均大于0，故方程$|\lambda A-B|=0$的根均大于0.

(2) ($\Longrightarrow$) 由$|\lambda A-B|=|A||\lambda E-A^{-1}B|$和方程$|\lambda A-B|$的根全是1可知，$A^{-1}B$的特征值全为1，故存在正交矩阵$P$，使$P^TA^{-1}BP=E$，即$A^{-1}B=E$，那么$A=B$.

($\Longleftarrow$) 若$A=B$，则$|\lambda A-B|=|\lambda A-A|=|A||\lambda E-E|=0$.由$|A|\ne 0$，得$|\lambda E-E|=0$，故$\lambda=1$.

> 3.证明:实反对称矩阵的特征值为0或纯虚数.

$\textbf{证明}$ 设$A$为实反对称矩阵，$\lambda$是$A$的特征值，则有$X\ne 0,AX=\lambda X$.取共轭，有$\overline{AX}=\overline{\lambda X}$.考虑$\overline{X}^TAX$，一方面$\overline{X}^TAX=\lambda\overline{X}^TX$，另一方面，$\overline{X}^TAX=-\overline{X}^T\overline{A}^TX=-(\overline{AX})^TX=-\overline{\lambda X}^TX$，于是$(\lambda+\overline{\lambda})\overline{X}^TX=0$.又因为$X\ne 0$，所以$\overline{X}^TX>0$，故$\lambda+\overline{\lambda}=0$，即$\lambda=0$或纯虚数.

>4. 设$A$为$n$阶正定阵，$B$为$n$阶实反对称矩阵，求证:$A-B^2$为正定阵.

$\textbf{证明}$ 由$B$为实反对称矩阵可知，$B^T=-B$.那么$|A-B^2|=|A+(-B)B|=|A+B^TB|>0$，即$A-B^2$为正定阵.

> 5.假设 $n \times n$ 阶实对称矩阵 $A, B$ 以及 $A-B$ 均是正定矩阵, 证明: $B^{-1}-A^{-1}$ 也是正定矩阵.

$\textbf{证明}$ 易知$B^{-1}-A^{-1}$是实对称矩阵.由于存在可逆矩阵$P$，使
$$A=P^{-1}EP,B=P^{-1}\mathrm{diag}\left\{\lambda_1,\cdots,\lambda_n\right\}P,\lambda_i>0$$
于是由$A-B$正定知$1-\lambda_i>0$，从而
$$B^{-1}-A^{-1}=P^{-1}\mathrm{diag}\left\{\frac{1}{\lambda_1}-1,\cdots,\frac{1}{\lambda_n}-1\right\}P$$
且$\displaystyle\frac{1}{\lambda_i}-1>0$，故$B^{-1}-A^{-1}$正定.

> 6.设$A$为$n$阶实对称矩阵，$\lambda_0$是$A$的最大特征值.证明:$\lambda_1=\displaystyle\max_{x\in \mathbb{R}}\frac{x^TAx}{x^Tx}$，其中$x$为非零向量.

$\textbf{证明}$ 设$y$是$A$的属于特征值$\lambda_1$且长度为1的特征向量，即有
$$Ay=\lambda_1 y,\text{且}||y||=1$$
所以$\lambda_1=\frac{y^TAy}{y^Ty}$.

又因为$A$为$n$阶实对称矩阵，故存在正交阵$P$，使
$$P^TAP=\begin{pmatrix}
        \lambda_1&&&\\
        &\lambda_2&&\\
        &&\ddots&\\
        &&&\lambda_{n}
    \end{pmatrix}$$
其中$\lambda_1\geq \lambda_2\geq \cdots\geq \lambda_{n}$为$A$的$n$个特征向量.作变换$x=Pz$，那么$\forall x\in \mathrm{R}^n$，且$||x||=1$，有
$$\frac{x^TAx}{x^Tx}=\frac{z^TP^TAPz}{z^TP^TPz}=\frac{\lambda_1 z_1^2+\lambda_2 z_2^2+\cdots+\lambda_{n}z_n^2}{z_1^2+z_2^2+\cdots+z_n^2}\leq \lambda_1
$$
即
$$\lambda_0=\max_{x\in \mathbb{R}}\frac{x^TAx}{x^Tx}$$
