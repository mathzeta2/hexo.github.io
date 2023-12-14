## Welcome to GitHub Pages

填空题.第一题做烂了都，到现在还能记得答案$\displaystyle\frac{\sin x}{x}$，那么$x\to 0$时，答案就是$1$.这道题不断使用二倍角公式即可.

第二题求$n$阶导数，写出前几阶导数，找规律即可；或者将$\ln(1+x)$写成$\mathrm{Taylor}$级数形式.

第三题.只需利用$\displaystyle\cos x=2\cos^2 \frac{x}{2}-1$化简被积函数，注意有绝对值.

第四题直接用Cauchy判别法，抓大头，$\displaystyle\frac{1}{R}=3$.分子$2^n$影响很小，可以当作没有.当$\displaystyle x=-\frac{1}{3}$时，级数是Leibniz型级数，收敛；当$\displaystyle x=\frac{1}{3}$时，级数是调和级数，发散.

第五题.利用隐函数公式
$$z_{x}=-\frac{F_x}{F_z}$$
再进一步计算二阶偏导数.

第六题.根据对称性，有
$$\iint\limits_{S}x^2\mathrm{d}S=\iint\limits_{S}y^2\mathrm{d}S=\iint\limits_{S}z^2\mathrm{d}S=\frac{1}{3}\iint\limits_{S}(x^2+y^2+z^2)\mathrm{d}S$$
问题迎刃而解.

在看判断题.第一题，对的.

第二题.对的.

第三题.对的.

第四题.错的.可微偏导数一定存在，但不一定连续.

第五题.错的.考虑反例:级数$\displaystyle \sum_{n=0}^{\infty}\frac{(-1)^n}{n}$.

第六题.错的.考虑反例:$a_n=n^{\displaystyle \frac{1}{3n^2}-2}$.

接下来是计算题.第一题分子提出$\sqrt[3]{\cos x}$，接下来直接可以用等价无穷小.

第二题.将$\tan^4x$变成$\tan^2 x(\sec^2 x-1)$，分成两个积分进一步求解.

第三题.利用积分级数换序求解.

第四题.画出积分区域，交换积分次序求解.注意积分区域与被积函数无关.

第五题.利用以下公式:
$$S=\iint\limits_{4x^2+y^2=4}\sqrt{1+(z_x)^2+(z_y)^2}\mathrm{d}x\mathrm{d}y$$

最后看证明题.

第一题.第一小问默写，第二小问根据定义证明.第三小问利用Cauchy准则，取点列$x_n'=\displaystyle \frac{1}{n\pi},x_n'=\displaystyle \frac{1}{\displaystyle n\pi+\frac{\pi}{2}}$，那么当$n\to \infty$时，有
$$|x_n'-x_n''|\to 0$$
但是
$$|f(x_n')-f(x_n'')|\to 1\not\to 0$$
推出非一致连续.

第二题.连续性通过不等式放缩得到.不可微通过定义计算，发现极限不存在.

第三题.$(\Longrightarrow)$ 由一致收敛得,$\forall \varepsilon>0$及$x\in I$，存在$N\in \mathbb{N}_+$，当$x>N$时，
$$|f_n(x)-f(x)|<\varepsilon$$
那么由上确界的定义可知
$$\sup |f_n(x)-f(x)|\leq \varepsilon$$

$(\Longleftarrow)$ $\forall \varepsilon>0$及$x\in I$，存在$N\in \mathbb{N}_+$，当$x>N$时，
$$\sup |f_n(x)-f(x)|< \varepsilon$$
那么
$$|f_n(x)-f(x)|\leq \sup |f_n(x)-f(x)|< \varepsilon$$
于是$\left\{f_n(x)\right\}$在区间$I$上一致收敛于$f(x)$.


