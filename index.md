## Welcome to GitHub Pages

\begin{exercise}
    证明$\lim_{x\to +\infty}f(x)=A$的充分必要条件是对任何$\lim_{n\to \infty}x_n=+\infty$的数列$\left\{x_n\right\}$，有$\lim_{n\to \infty}f(x_n)=A$.
\end{exercise}
\begin{solution}
    必要性.根据$\lim_{x\to +\infty}f(x)=A$可知，$\forall\varepsilon>0,\exists X>0$，当$x>X$时，有$|f(x)-A|<\varepsilon$.因为$\lim_{n\to \infty}x_n=+\infty$，所以对上述$X>0,\exists N\in \mathbb{N}^*$，当$n>N$时，$x_n>X$.故当$n>N$时，$|f(x)-A|<\varepsilon$，即$\lim_{n\to \infty}f(x_n)=A$.

    充分性.对任何$\lim_{n\to \infty}x_n=+\infty$的数列$\left\{x_n\right\}$，都有$\lim_{n\to \infty}f(x_n)=A$.下面用反证法证明$\lim_{x\to +\infty}f(x)=A$.假设$\lim_{x\to +\infty}f(x)\ne A$，则$\forall \varepsilon_0>0,\forall X>0,\exists x>X$，但$|f(x)-A|\geq \varepsilon_0$.

    对$X_1=1,\exists x_1>X_1$，但$|f(x_1)-A|\geq \varepsilon_0$；

    对$X_2=2,\exists x_2>X_2$，但$|f(x_2)-A|\geq \varepsilon_0$；

    $\cdots$

    对$x_n=n,\exists x_n>X_n$，但$|f(x_n)-A|\geq \varepsilon_0$.

    得到了$\lim_{n\to \infty}x_n=+\infty$，可是相应的函数值数列$\left\{f(x_n)\right\}$并不收敛到$A$，所以假设错误，$\lim_{x\to \infty}f(x)=A$.
\end{solution}
\begin{exercise}
    求函数$f(x)=\frac{(x^2+x-6)\mathrm{e}^{\frac{1}{x}}}{(x^2-4)\arctan x}$的所有渐近线.
\end{exercise}
\begin{solution}
    因为$f(x)$在$x=0,x=\pm 2$无定义，且$\lim_{x\to 0}f(x)=\lim_{x\to 0}\frac{x^2+x-6}{x^2-4}\lim_{x\to 0}\frac{\mathrm{e}^{\frac{1}{x}}}{\arctan x}$不存在.
    
    $\lim_{x\to 2}f(x)=\lim_{x\to 2}\frac{(x+3)}{x+2}\lim_{x\to 2}\frac{\mathrm{e}^{\frac{1}{x}}}{\arctan x}=\frac{5\mathrm{e}^{\frac{1}{x}}}{4\arctan 2}$.$\lim_{x\to -2}f(x)=\lim_{x\to -2}\frac{(x^2+x-6)\mathrm{e}^{\frac{1}{x}}}{(x^2-4)\arctan x}=\lim_{x\to -2}\frac{(x+3)\mathrm{e}^{\frac{1}{x}}}{(x+2)\arctan x}=+\infty$.所以$f(x)$的垂直渐近线只有$x=-2$.

    而$\lim_{x\to +\infty}f(x)=\lim_{x\to +\infty}\frac{(x^2+x-6)\mathrm{e}^{\frac{1}{x}}}{(x^2-4)\arctan x}=\frac{2}{\pi}$，所以$y=\frac{2}{\pi}$是$f(x)$的水平渐近线.

    又$\lim_{x\to \infty}\frac{f(x)}{x}=0$，所以$f(x)$无斜渐近线.

    综上，$f(x)$有渐近线:$x=-2,y=\frac{2}{\pi}$.
\end{solution}
\begin{exercise}
    证明级数$\sum_{n=1}^{\infty}(-1)^{n-1}(\sqrt[n]{n}-1)$条件收敛.
\end{exercise}
\begin{solution}
    因为$\sqrt{n}-1>0$，所以该级数为交错级数.

    令$y=x^{\frac{1}{x}}$，则$y'=\frac{x^{\frac{1}{x}}}{x^2}(1-\ln x)$，故当$x>e$时，$y$单调减少.即当$n>3$时，数列$\left\{\sqrt[n]{n}-1\right\}$单调减少，且$\lim_{n\to \infty}(\sqrt[n]{n}-1)=0$.由Leibniz判别法可知$\sum_{n=1}^{\infty}(-1)^{n-1}(\sqrt[n]{n}-1)$收敛.但是
    $$\lim_{n\to \infty}\frac{\sqrt[n]{n}-1}{\displaystyle\frac{1}{n}}=\lim_{n\to \infty}\frac{\displaystyle\frac{1}{n^2}\cdot \sqrt[n]{n}(1-\ln n)}{\displaystyle -\frac{1}{n^2}}=+\infty$$
    而$\sum_{n=1}^{\infty}\frac{1}{n}$发散，故$\sum_{n=1}^{\infty}(\sqrt[n]{n}-1)$发散，所以级数$\sum_{n=1}^{\infty}(-1)^{n-1}(\sqrt[n]{n}-1)$条件收敛.
\end{solution}
\begin{exercise}
    若数列
    $$\left\{|a_2-a_1|+|a_3-a_2|+\cdots+|a_n-a_{n-1}|\right\}$$
    有界，则称$\left\{a_n\right\}$为有界变差数列，证明有界变差数列一定是收敛的数列.
\end{exercise}
\begin{solution}
    设$x_n=|a_2-a_1|+|a_3-a_2|+\cdots+|a_n-a_{n-1}|$，易见$\left\{x_n\right\}$单调增加，且有上界，故$\left\{x_n\right\}$收敛.进一步，有
    $$|a_{n+p}-a_n|\leq |a_{n+p}-a_{n+p-1}|+|a_{n+p-1}-a_{n+p-2}|+\cdots+|a_{n+2}-a_{n+1}|+|a_{n+1}-a_n=x_{n+p}-x_n$$
    由于$\left\{x_n\right\}$收敛且$\left\{x_n\right\}$单调增加，故$x_{n+p}-x_n<\varepsilon$，从而
    $$|a_{n+p}-a_n|<\varepsilon$$
    这说明$\left\{a_n\right\}$是一个Cauchy数列，因而$\left\{a_n\right\}$收敛.
    
\end{solution}
\begin{exercise}
    设$V(t)$是曲线$y=\frac{\sqrt{x}}{1+x^2}$在$x\in [0,t]$上的弧段绕$x$轴所得到的体积，试求常数$c$，使$\lim_{t\to \infty}V(t)=2V(c)$.
\end{exercise}
\begin{solution}
    由于$V(t)$是曲线$y=\frac{\sqrt{x}}{1+x^2}$在$x\in [0,t]$上的弧段绕$x$轴所得到的体积，故
    $$V(t)=\pi\int_0^t \frac{x}{(1+x^2)^2}\mathrm{d}x=\frac{\pi}{2}\left(1-\frac{1}{1+t^2}\right)$$
    所以
    $$\lim_{t\to \infty}V(t)=\frac{\pi}{2}=2\times \frac{\pi}{2}\left(1-\frac{1}{1+c^2}\right)$$
    故$c=\pm 1$.又因为$t\geq 0$，所以$c=1$.
\end{solution}
\begin{exercise}
    证明正项级数$\sum_{n=1}^{\infty}\left[\frac{1}{\sqrt{n}}-\sqrt{\ln\left(1+\frac{1}{n}\right)}\right]$收敛.
\end{exercise}
\begin{solution}
    因为$\frac{1}{n+1}<\ln\left(1+\frac{1}{n}\right)<\frac{1}{n}$，所以原级数为正项级数，且
    $$\frac{1}{\sqrt{n}}-\sqrt{\ln\left(1+\frac{1}{n}\right)}<\frac{1}{\sqrt{n}}-\frac{1}{\sqrt{n+1}}=\frac{\sqrt{n+1}-\sqrt{n}}{\sqrt{n(n+1)}}=\frac{1}{\sqrt{n(n+1)}(\sqrt{n+1}+\sqrt{n})}$$
    又因为
    $$\lim_{n\to \infty}\frac{n^{\frac{3}{2}}}{\sqrt{n(n+1)}(\sqrt{n+1}+\sqrt{n})}=\lim_{n\to \infty}\frac{1}{\displaystyle\sqrt{1+\frac{1}{n}}\left(\sqrt{1+\frac{1}{n}}+1\right)}=\frac{1}{2}$$
    而$\sum_{n=1}^{\infty}\frac{1}{n^{\frac{3}{2}}}$收敛，故正项级数$\sum_{n=1}^{\infty}\left[\frac{1}{\sqrt{n}}-\sqrt{\ln\left(1+\frac{1}{n}\right)}\right]$收敛.
\end{solution}
\begin{exercise}
    证明级数$\sum_{n=1}^{\infty}(-1)^n\left[e-\left(1+\frac{1}{n}\right)^n\right]$条件收敛.
\end{exercise}
\begin{solution}
    因为
    $$\lim_{x\to 0}\frac{e-(1+x)^{\frac{1}{x}}}{x}=e\lim_{x\to 0}\frac{\displaystyle 1-\mathrm{e}^{\displaystyle\frac{\ln(1+x)}{x}-1}}{x}=e\lim_{x\to 0}\frac{\displaystyle 1-\mathrm{e}^{\displaystyle\frac{x+\frac{1}{2}x^2+o(x^2)}{x}-1}}{x}=e\lim_{x\to 0}\frac{\displaystyle\frac{1}{2}x}{x}=\frac{e}{2}$$
    从而
    $$\lim_{n\to \infty}\frac{\displaystyle e-\left(1+\frac{1}{n}\right)^n}{\displaystyle\frac{1}{n}}=\frac{e}{2}$$
    故$\sum_{n=1}^{\infty}\left[e-\left(1+\frac{1}{n}\right)^n\right]$与$\sum_{n=1}^{\infty}\frac{1}{n}$敛散性相同.那么
    $$\sum_{n=1}^{\infty}\left|(-1)^{n}\left[e-\left(1+\frac{1}{n}\right)^n\right]\right|$$
    发散.进一步，由
    $$e-\left(1+\frac{1}{n+1}\right)^{n+1}<e-\left(1+\frac{1}{n}\right)^n,n=1,2,\cdots$$
    $$\lim_{n\to \infty}\left[e-\left(1+\frac{1}{n}\right)^n\right]=0$$
    可知$\sum_{n=1}^{\infty}(-1)^n\left[e-\left(1+\frac{1}{n}\right)^n\right]$为Leibniz型级数，故收敛.

    综上，级数$\sum_{n=1}^{\infty}(-1)^n\left[e-\left(1+\frac{1}{n}\right)^n\right]$条件收敛.
\end{solution}
\begin{exercise}
    设$f(x)$在$[0,1]$上连续可导，证明对$\forall x\in [0,1]$，有
    $$f(x)\leq \int_0^1 (|f(t)|+|f'(t)|)\mathrm{d}t$$
\end{exercise}
\begin{solution}
    由积分第一中值定理，存在$\xi\in [0,1]$，使$\int_0^1 |f(t)|\mathrm{d}t=|f(\xi)|$.又$f(x)=f(\xi)+\int_{\xi}^x f'(t)\mathrm{d}t$，故
    $$f(x)\leq |f(\xi)|+\int_{\xi}^x|f'(t)|\mathrm{d}t=\int_0^1 |f(t)|\mathrm{d}t+\int_{\xi}^x|f'(t)|\mathrm{d}t\leq \int_0^1 (|f(t)|+|f'(t)|)\mathrm{d}t$$
\end{solution}
\begin{exercise}
    设函数$f(x)$在$[0,1]$上二次可导，且$f''(x)<0$.证明:
    $$\int_0^1 f(x^n)\mathrm{d}x\leq f\left(\frac{1}{n+1}\right)(n\in \mathbb{N})$$
\end{exercise}
\begin{solution}
    将$f(t)$在$t=t_0$处作Taylor展开，有
    $$f(t)=f(t_0)+f'(t_0)(t-t_0)+\frac{f''(\xi)}{2}(t-t_0)^2,\xi\in [0,1]$$
    由$f''(x)<0,x\in [0,1]$可知
    $$f(t)\leq f(t_0)+f'(t_0)(t-t_0)$$
    代入$t=x^n,t_0=\frac{1}{n+1}$，并积分得
    $$\int_0^1 f(x^n)\mathrm{d}t\leq f\left(\frac{1}{n+1}\right)$$
\end{solution}
\begin{exercise}
    令$f:[0,1]\to \mathbb{R}$为连续的，满足$f(0)=f(1)=0$.假设$f''$在$(0,1)$内存在，且具有$f''+2f'+f\geq 0$.证明对所有$0\leq x\leq 1$，有$f(x)\leq 0$成立.
\end{exercise}
\begin{solution}
    令$g(x)=\mathrm{e}^xf(x),x\in [0,1]$，则$g'(x)=\mathrm{e}^x[f(x)+f'(x)],g''(x)=\mathrm{e}^x[f(x)+2f'(x)+f''(x)]\geq 0$，故$g(x)$在$[0,1]$上为下凸函数.又因为$g(0)=g(1)=0$，故对所有$0\leq x\leq 1$，有$g(x)\leq 0$成立.再根据$\mathrm{e}^x$在$[0,1]$上大于零，故对所有$0\leq x\leq 1$，有$f(x)\leq 0$成立.
\end{solution}
\begin{exercise}
    设$f(x)$在$[0,1]$上可积，求证$\lim_{n\to \infty}\int_0^1 \sqrt[n]{n}f(x)\mathrm{d}x=\int_0^1 f(x)\mathrm{d}x$.
\end{exercise}
\begin{solution}
    首先证明$\lim_{n\to \infty}\sqrt[n]{n}=1$.当$n\geq 2$时，利用均值不等式，得
    $$1\leq \sqrt[n]{n}=\sqrt[n]{\sqrt{n}\cdot\sqrt{n}\cdot \underbrace{1\cdots 1}_{n-2\text{个}}}\leq \frac{2\sqrt{n}+n-2}{n}<1+\frac{2}{\sqrt{n}}$$
    于是
    $$0\leq |\sqrt[n]{n}-1|\leq \frac{2}{\sqrt{n}}$$
    因此，对任意的$\varepsilon>0$，取$N=\max\left\{4,\frac{4}{\varepsilon^2}\right\}$，当$n>N$时，有
    $$|\sqrt[n]{n}-1|<\frac{2}{\sqrt{n}}<\varepsilon$$
    即$\lim_{n\to \infty}\sqrt[n]{n}=1$.

    因为$f(x)$在$[0,1]$上可积，故$f(x)$在$[0,1]$上有界，即存在$M>0$，使得$|f(x)|\leq M,x\in [0,1]$.那么
    $$\left|\int_0^1\sqrt[n]{n}f(x)\mathrm{d}x-\int_0^1 f(x)\mathrm{d}x\right|\leq |\sqrt[n]{n}-1|\left|\int_0^1 f(x)\mathrm{d}x\right|\leq |\sqrt[n]{n}-1|\int_0^1 |f(x)|\mathrm{d}x<M\varepsilon$$
    这就证明了$\lim_{n\to \infty}\int_0^1 \sqrt[n]{n}f(x)\mathrm{d}x=\int_0^1 f(x)\mathrm{d}x$.
\end{solution}
\begin{exercise}
    假设$f(x)$在$(0,1)$上单调，反常积分$\int_0^1 f(x)\mathrm{d}x$收敛，则有
    $$\lim_{n\to \infty}\frac{1}{n}\left[f\left(\frac{1}{n}\right)+f\left(\frac{2}{n}\right)+\cdots+f\left(\frac{n-1}{n}\right)\right]=\int_0^1 f(x)\mathrm{d}x$$
\end{exercise}
\begin{solution}
    不妨设$f(x)$非负单调增加，且以1为瑕点.则有不等式
    $$\int_0^{1-\frac{1}{n}}f(x)\mathrm{d}x\leq \frac{1}{n}\left[f\left(\frac{1}{n}\right)+f\left(\frac{2}{n}\right)+\cdots+f\left(\frac{n-1}{n}\right)\right]\leq \int_0^{1-\xi_n}f(x)\mathrm{d}x+\xi_n f\left(\frac{n-1}{n}\right)$$
    这里取$0<\xi_n<\frac{1}{n}$，且使得当$n\to \infty$时，$\xi_n f\left(\frac{n-1}{n}\right)\to 0$.于是结论成立.
\end{solution}
\begin{exercise}
   设$f\in C^1[0,1],f(0)=0,f(1)=1$，证明:
   $$\lim_{n\to \infty}n\left[\int_0^1 f(x)\mathrm{d}x-\frac{1}{n}\sum_{k=1}^n f\left(\frac{k}{n}\right)\right]=-\frac{1}{2}$$
\end{exercise}
\begin{solution}
    将区间$[0,1]$等分$n$份，分点$x_k=\frac{k}{n}$，区间长度为$\frac{1}{n}$，则
    $$\begin{aligned}
       \lim_{n\to \infty}n\left[\int_0^1 f(x)\mathrm{d}x-\frac{1}{n}\sum_{k=1}^n f\left(\frac{k}{n}\right)\right]&=\lim_{n\to \infty}n\left[\sum_{k=1}^n\int_{x_{k-1}}^{x_k} f(x)\mathrm{d}x-\sum_{k=1}^n f(x_k)\Delta x_k\right]\\
       &=\lim_{n\to \infty}n\left[\sum_{k=1}^n \int_{x_{k-1}}^{x_k}[f(x)-f(x_k)]\mathrm{d}x\right]\\
       &=\lim_{n\to \infty}n\left[\sum_{k=1}^n\frac{f(\xi_k)-f(x_k)}{\xi_k-x_k}\int_{x_{k-1}}^{x_k}(x-x_k)\mathrm{d}x\right]\\
       &=\lim_{n\to \infty}n\left[\sum_{k=1}^n f'(\eta_k)\int_{x_{k-1}}^{x_k}(x-x_k)\mathrm{d}x\right]\\
       &=\lim_{n\to \infty}n\left\{\sum_{k=1}^n f'(\eta_k)\left[-\frac{1}{2}(x_k-x_{k-1})^2\right]\right\}\\
       &=-\frac{1}{2}\lim_{n\to \infty}\left[\sum_{k=1}^n f'(\eta_k)(x_k-x_{k-1})\right]=-\frac{1}{2}\int_0^1 f'(x)\mathrm{d}x=-\frac{1}{2}
    \end{aligned}$$
\end{solution}
\begin{exercise}
    设积分$\int_{-\infty}^{+\infty}f(x)\mathrm{d}x$绝对收敛，证明函数$g(\alpha)=\int_{-\infty}^{+\infty}f(x)\cos\alpha x\mathrm{d}x$在$(-\infty,+\infty)$上一致连续.
\end{exercise}
\begin{solution}
    要证$g(\alpha)$在$(-\infty,+\infty)$上一致连续，即证:对$\forall\varepsilon>0,\exists\delta>0$，使得当$|\alpha'-\alpha''|<\delta$时，有
    $$|g(\alpha')-g(\alpha'')|<\varepsilon$$
    事实上，有
    $$|g(\alpha')-g(\alpha'')|\leq \int_{-\infty}^{\infty}|f(x)||\cos\alpha' x-\cos\alpha'' x|\mathrm{d}x$$
    因为$\int_{-\infty}^{+\infty}|f(x)|\mathrm{d}x$存在，对$\forall\varepsilon>0,\exists A_0>0$，当$A\geq A_0$时，有
    $$\int_{-\infty}^{-A}|f(x)|\mathrm{d}x<\frac{\varepsilon}{8},\int_A^{+\infty}|f(x)|\mathrm{d}x<\frac{\varepsilon}{8}$$
    对此$A$，取$\delta=\frac{\varepsilon}{\displaystyle 2A\int_{-\infty}^{+\infty}|f(x)|\mathrm{d}x}$，则当$|\alpha'-\alpha''|<\delta$时，有
    $$\begin{aligned}
        \int_{-\infty}^{\infty}|f(x)||\cos\alpha' x-\cos\alpha'' x|\mathrm{d}x&\leq 2\int_{-\infty}^{-A}|f(x)|\mathrm{d}x+2\int_{A}^{+\infty}|f(x)|\mathrm{d}x+2\int_{-A}^A|f(x)|\left|\sin \frac{\alpha'-\alpha''}{2}\right|\sin\left|\frac{\alpha'+\alpha''}{2}\right|\\
        &\leq 2\int_{-\infty}^{-A}|f(x)|\mathrm{d}x+2\int_{A}^{+\infty}|f(x)|\mathrm{d}x+A|\alpha'-\alpha''|\int_{-\infty}^{+\infty}|f(x)|\mathrm{d}x\\
        &<2\cdot \frac{\varepsilon}{8}+2\cdot \frac{\varepsilon}{8}+\frac{\varepsilon}{2}=\varepsilon
    \end{aligned}$$
    那么就有
    $$|g(\alpha')-g(\alpha'')|<\varepsilon$$
    这就证明了函数$g(\alpha)=\int_{-\infty}^{+\infty}f(x)\cos\alpha x\mathrm{d}x$在$(-\infty,+\infty)$上一致连续.
\end{solution}
\begin{exercise}
    讨论级数$\sum_{n=1}^{\infty}\int_0^{\frac{\pi}{n}}\frac{\sin x}{1+x}\mathrm{d}x$的敛散性.
\end{exercise}
\begin{solution}
    因为$\frac{\sin x}{1+x}$在$\left[0,\frac{\pi}{n}\right]$上单调增加，且最大值$\frac{\displaystyle\sin \frac{\pi}{n}}{\displaystyle 1+\frac{\pi}{n}}<\frac{\displaystyle\frac{\pi}{n}}{\displaystyle 1+\frac{\pi}{n}}=\frac{\pi}{n+\pi}$，则有$0<\int_0^{\frac{\pi}{n}}\frac{\sin x}{1+x}\mathrm{d}x\leq \frac{\pi}{n+\pi}\int_0^{\frac{\pi}{n}}\mathrm{d}x=\frac{\pi^2}{n(n+\pi)}$.而$\sum_{n=1}^{\infty}\frac{\pi^2}{n(n+\pi)}$收敛，故级数$\sum_{n=1}^{\infty}\int_0^{\frac{\pi}{n}}\frac{\sin x}{1+x}\mathrm{d}x$也收敛.
\end{solution}
\begin{exercise}
    讨论级数
    $$v_1^s+v_2^s+\cdots+v_n^s+\cdots$$
    的敛散性，其中$v_1=\sin x>0,v_{n+1}=\sin v_n(n=1,2,\cdots)$.
\end{exercise}
\begin{solution}
    根据$v_1=\sin x>0,v_{n+1}=\sin v_n(n=1,2,\cdots)$，不难得到$v_n$单调减少，且有下界0，故根据单调有界原理，$\left\{v_n\right\}$收敛.易知$\left\{v_n\right\}$收敛到0.根据Stolz定理，有
    $$\lim_{n\to \infty}\frac{n}{\displaystyle\frac{1}{v^2_n}}=\lim_{n\to \infty}\frac{1}{\displaystyle \frac{v_n^2-v^2_{n+1}}{v^2_{n+1}v^2_n}}=\lim_{n\to \infty}\frac{v^2_{n+1}v^2_n}{v_n^2-v^2_{n+1}}=\lim_{n\to \infty}\frac{v_n^4}{\displaystyle v_n^2-\left(v_n-\frac{v_n^3}{6}+o(v_n^3)\right)^2}=3$$
    故
    $$v_n\sim \sqrt{\frac{3}{n}}~~(n\to\infty)$$
    于是
    $$v_1^s+v_2^s+\cdots+v_n^s+\cdots\sim \sum_{n=1}^{\infty} \left(\frac{3}{n}\right)^{\displaystyle\frac{s}{2}}$$
    那么当$\frac{s}{2}>1$即$s>2$时，原级数收敛；其余情况均发散.
\end{solution}
\begin{exercise}
    如果正项级数$\sum_{n=1}^{\infty}a_n$发散，$S_n$表示前$n$项的和.证明

    (1) $\sum_{n=1}^{\infty}\frac{a_n}{S_n}$发散.

    (2) $\sum_{n=1}^{\infty}\frac{a_n}{S_n^{1+\alpha}}(\alpha>0)$收敛.
\end{exercise}
\begin{solution}
    (1) 因$a_n>0,S_n$单调增加，所以
        $$\sum_{k=n+1}^{n+p}\frac{a_k}{S_k}\geq \frac{\displaystyle\sum_{k=n+1}^{n+p}a_k}{S_{n+p}}=\frac{S_{n+p}-S_n}{S_{n+p}}=1-\frac{S_n}{S_{n+p}}$$
        因为$S_n\to +\infty$，故$\forall n$，当$p\in \mathbb{N}$充分大时，$\frac{S_n}{S_{n+p}}<\frac{1}{2}$，从而$\sum_{k=n+1}^{n+p}\frac{a_k}{S_k}\geq 1-\frac{1}{2}=\frac{1}{2}$.所以$\sum_{n=1}^{\infty}\frac{a_n}{S_n}$发散.
    
    (2)首先，$\frac{a_n}{S_n^{1+\alpha}}=\frac{S_n-S_{n-1}}{S_n^{1+\alpha}}$.当$\alpha >0$时，对函数$x^{-\alpha}$在区间$[a,b]$上用Lagrange中值定理，可知存在$\xi\in (a,b)$，使成立
    $$\frac{1}{a^{\alpha}}-\frac{1}{b^{\alpha}}=\frac{\alpha}{\xi^{1+\alpha}}\cdot (b-a)>\alpha\cdot \frac{b-a}{b^{1+\alpha}}$$
    用$a=S_{n-1},b=S_n$代入，得到不等式
    $$\frac{a_n}{S_n^{1+\alpha}}=\frac{S_n-S_{n-1}}{S_n^{1+\alpha}}<\frac{1}{\alpha}\left(\frac{1}{S_{n-1}^{\alpha}}-\frac{1}{S_n^{\alpha}}\right)$$
    由此可以作出级数$\sum_{n=1}^{\infty}\frac{a_n}{S_n^{1+\alpha}}$的部分和数列的上界估计:
    $$\begin{aligned}
        \sum_{n=1}^{\infty}\frac{a_n}{S_n^{1+\alpha}}&=\frac{1}{a_1^{\alpha}}+\sum_{k=2}^{\infty}\frac{a_k}{S_k^{1+\alpha}}<\frac{1}{a_1^{\alpha}}+\frac{1}{\alpha}\sum_{k=2}^{\infty}\left(\frac{1}{S_{n-1}^{\alpha}}-\frac{1}{S_n^{\alpha}}\right)\\
        &<\frac{1}{a_1^{\alpha}}+\frac{1}{\alpha}\cdot\frac{1}{a_1^{\alpha}}=\frac{\alpha+1}{\alpha}\cdot \frac{1}{a_1^{\alpha}}
        \end{aligned}$$
        由此可得级数$\sum_{n=1}^{\infty}\frac{a_n}{S_n^{1+\alpha}}$收敛.

        
\end{solution}
\begin{exercise}
    判断级数$\sum_{n=0}^{\infty}\frac{(-1)^n}{n}\frac{\sin^n x}{1+\sin^n x}$在$[0,\pi]$是否一致收敛，并证明你的结论.
\end{exercise}
\begin{solution}
    级数$\sum_{n=0}^{\infty}\frac{(-1)^n}{n}\frac{\sin^n x}{1+\sin^n x}$在$[0,\pi]$一致收敛.理由如下:由于$\frac{\sin^n x}{1+\sin^n x}$关于$n$单调减少，且一致有界$\left|\frac{\sin^n x}{1+\sin^n x}\right|<\frac{1}{2}$.又$\sum_{n=0}^{\infty}\frac{(-1)^n}{n}$收敛.由Abel判别法知，级数$\sum_{n=0}^{\infty}\frac{(-1)^n}{n}\frac{\sin^n x}{1+\sin^n x}$在$[0,\pi]$一致收敛.
\end{solution}
\begin{exercise}
    证明$(3x^2y+8xy^2)\mathrm{d}x+(x^3+8x^2y+12y\mathrm{e}^y)\mathrm{d}y$为某个函数的全微分，并求它的原函数.
\end{exercise}
\begin{solution}
    设$P(x,y)=3x^2y+8xy^2,Q(x,y)=x^3+8x^2y+12y\mathrm{e}^y$，则
    $$\frac{\partial Q}{\partial x}=3x^2+16xy=\frac{\partial P}{\partial y}$$
    所以存在函数$u(x,y)$，使得$\mathrm{d}u=P\mathrm{d}x+Q\mathrm{d}y$.并且积分与路径无关，可选取从$(0,0)$到$(x,0)$，再到$(x,y)$.故
    $$u(x,y)=\int_0^x P(x,0)\mathrm{d}x+\int_0^yQ(x,y)\mathrm{d}y=\int_0^y (x^3+8x^2y+12y\mathrm{e}^y)\mathrm{d}y=x^3y+4x^2y^2+12(y-1)\mathrm{e}^y$$
\end{solution}
\begin{exercise}
    设$p>0$，判别积分$F(p)=\int_1^{\infty}\frac{\cos x\arctan x}{x^p}\mathrm{d}x$的敛散性，包括绝对收敛，条件收敛和发散，并证明$F(p)$在$p>0$上连续.
\end{exercise}
\begin{solution}
    当$p>1$时，$\frac{|\cos x\arctan x|}{x^p}\leq \frac{\pi}{2x^p}$，而$\int_1^{\infty}\frac{1}{x^p}\mathrm{d}x$收敛，故$F(p)$绝对收敛.

    当$0<p\leq 1$时，积分$\int_1^{\infty}\frac{\cos x}{x}\mathrm{d}x$收敛，$\arctan x$在$[1,+\infty)$上单调有界，故根据Abel判别法，$F(p)$收敛.但是$0<p\leq 1$时，
    $$\frac{\arctan x|\cos x|}{x^p}\geq \frac{\arctan x\cos^2 x}{x^p}=\frac{\arctan x}{2x^p}+\frac{\cos 2x\arctan x}{2x^p}$$
    根据Abel判别法同样能得到$\int_1^{\infty}\frac{\cos 2x\arctan x}{2x^p}$收敛.而由$\frac{\arctan x}{2x^p}\sim \frac{\pi}{4x^p}$可知，$\int_1^{\infty}\frac{\arctan x}{2x^p}\mathrm{d}x$发散，从而$F(p)$条件收敛.

    综上，当$0<p\leq 1$时，$F(p)$条件收敛；当$p>1$时，$F(p)$绝对收敛.

    另外，对于任意的闭区间$[a,b]\subset (0,+\infty)$，有
    $$\frac{\cos x\arctan x}{x^b}\leq \frac{\cos x\arctan x}{x^p}\leq \frac{\cos x\arctan x}{x^a},1\leq x <+\infty,0<a\leq p\leq b<+\infty$$
    而$\int_1^{\infty}\frac{\cos x\arctan x}{x^a}\mathrm{d}x$与$\int_1^{\infty}\frac{\cos x\arctan x}{x^b}\mathrm{d}x$都收敛，故根据Weierstrass判别法，$F(p)$在$(0,+\infty)$上内闭一致收敛，故$F(p)$在$p>0$上连续.
\end{solution}
\begin{exercise}
    设$f(x,y)$在$x^2+y^2\leq 1$上二阶连续可微，且满足
    $$\frac{\partial^2f}{\partial x^2}+\frac{\partial^2f}{\partial y^2}=\mathrm{e}^{-(x^2+y^2)}$$
    证明$\iint\limits_{x^2+y^2\leq 1}\left(x\frac{\partial f}{\partial x}+y\frac{\partial f}{\partial y}\right)\mathrm{d}x\mathrm{d}y=\frac{\pi}{2\mathrm{e}}$.
\end{exercise}
\begin{solution}
    令$x=r\cos\theta,y=r\sin\theta$，则$\frac{\partial f}{\partial r}=\frac{\partial f}{\partial x}\cos\theta+\frac{\partial f}{\partial y}\sin\theta$.因$r\frac{\partial f}{\partial r}=x\frac{\partial f}{\partial x}+y\frac{\partial f}{\partial y}$，所以
    $$\iint\limits_{x^2+y^2\leq 1}\left(x\frac{\partial f}{\partial x}+y\frac{\partial f}{\partial y}\right)\mathrm{d}x\mathrm{d}y=\int_0^1 r\mathrm{d}r\int_0^{2\pi}r\frac{\partial f}{\partial r}\cdot r\mathrm{d}\theta~~~(*)$$
    再根据Green公式，有
    $$\begin{aligned}
        \int_0^{2\pi}\frac{\partial f}{\partial r}r\mathrm{d}\theta&=\iint\limits_{x^2+y^2=r^2}\frac{\partial f}{\partial \overrightarrow{n}}\mathrm{d}S=\iint\limits_{x^2+y^2\leq r^2}\left(\frac{\partial^2 f}{\partial x^2}+\frac{\partial^2 f}{\partial y^2}\right)\mathrm{d}x\mathrm{d}y\\
        &=\iint\limits_{x^2+y^2\leq r^2}\mathrm{e}^{-(x^2+y^2)}\mathrm{d}x\mathrm{d}y=\int_0^{2\pi}\mathrm{d}\theta\int_0^r t\mathrm{e}^{-t^2}\mathrm{d}t=\pi (1-\mathrm{e}^{-t^2})~(0<r<1)
    \end{aligned}$$
    把所得结果代入$(*)$式，得到
    $$\iint\limits_{x^2+y^2\leq 1}\left(x\frac{\partial f}{\partial x}+y\frac{\partial f}{\partial y}\right)\mathrm{d}x\mathrm{d}y=\int_0^1 \pi (1-\mathrm{e}^{-r^2})\mathrm{d}r=\frac{\pi}{2}+\frac{\pi}{2}(\mathrm{e}^{-1}-1)=\frac{\pi}{2\mathrm{e}}$$
\end{solution}
\begin{exercise}
    设$D\subset \mathbb{R}^2$是有界区域，$u=u(x,y)$在$D$内二阶连续可微，且满足
    $$u_{x^2}+u_{y^2}+cu=0$$
    其中$c<0$为常数.证明:

    (1) $u$在$D$上正的最大值(负的最小值)不能在$D$的内部取到.

    (2) 若$u$在$D$上连续，在$D$的边界上为0，则在$D$上$u\equiv 0$.
\end{exercise}
\begin{solution}
    (1) 反证法.设$u$在$D$上正的最大值在$D$内部取到，则$\exists (x_0,y_0)\in \overline{D}$，使$u(x_0,y_0)=\max_{(x,y)\in D}u(x,y)\geq 0$.于是$(x_0,y_0)$必是$u(x,y)$的极大值点，且$u_{x^2}\leq 0,u_y^2\leq 0$(否则$(x_0,y_0)$非极大值点)，从而$(u_{x^2}+u_{y^2})\bigg|_{(x_0,y_0)}\leq 0$.则由等式$u_{x^2}+u_{y^2}+cu=0(c<0)$知$u(x_0,y_0)\leq 0$，与假设矛盾.故$u$在$D$上正的最大值不能在$D$内部取到.同理可证，$u$在$D$上负的最小值不能在$D$内部取到.

    (2) 反证法.设$u\not\equiv 0$，则$\exists (x_0,y_0)\in D$，使$u(x_0,y_0)\ne 0$.不妨设$u(x_0,y_0)>0$，由于在$D$的边界上$u=0$，所以$(x_0,y_0)\in \overline{D}$.又$u$在有界闭区域上连续，必有最大值，且由于$u(x_0,y_0)>0$，则$u$在$D$上的最大值为正，且在$\overline{D}$取得.这与(1)矛盾.故$u\equiv 0,\forall (x,y)\in D$.
\end{solution}
