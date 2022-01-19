# 微积分

## Concepts

Two Important Limitations

$$
\begin{aligned}
    \sin x &< x < \tan x \\
    1 &< \frac{x}{\sin x} < \frac{1}{\cos x} \\
    \cos x &< \frac{\sin x}{x} < 1 \\
    &\lim_{x \rightarrow 0} \frac{\sin x}{x} = 1
\end{aligned}
$$

$$
\begin{aligned}
    A_n &= (1 + \frac{1}{n})^n \\
    &= \sum_{k=0}^{n} \binom{n}{k} \frac{1}{n^k} \\
    A_{n+1} &= \sum_{k=0}^{n+1} \binom{n+1}{k} \frac{1}{(n+1)^k} \\
    &\binom{n+1}{k} \frac{1}{(n+1)^k} - \binom{n}{k} \frac{1}{n^k} \\
    &= \frac{1}{k!} [(1 - \frac{1}{n+1})(1 - \frac{2}{n+1}) \cdots (1 - \frac{k-1}{n+1}) \\
    &- (1 - \frac{1}{n})(1 - \frac{2}{n}) \cdots (1 - \frac{k-1}{n})] \\
    &>0 \\
    A_{n+1} &> A_n \\
    A_n &= 1 + 1 + \frac{n(n-1)}{2} \frac{1}{n^2} + \frac{n(n-1)(n-2)}{3 \times 2} \frac{1}{n^3} + \cdots \\
    &+ \frac{n(n-1) \cdots n(n-1) \cdots [n-(n-1)]}{n!} \frac{1}{n^n} \\
    &< 2 + \frac{1}{2!} + \frac{1}{3!} + \cdots + \frac{1}{n!} \\
    &< 2 + \frac{1}{2^1} + \frac{1}{2^2} + \cdots + \frac{1}{2^{n-1}} \\
    &< 3
\end{aligned}
$$

单调有界数列必有极限。

定义
$$
e = \lim_{n \rightarrow \infty} (1 + \frac{1}{n})^n
$$

---

在求数列极限的时候，假设 $a$ 为数列极限之前必须证明数列是收敛的。不然必然无法得到有意义的结果。

---

证明数列发散：

- 存在不收敛的子列
- 存在两个收敛的子列，但他们的极限不相等

证明函数发散：

可以将函数的自变量作为一个数列的极限，对于数列 $\{ f(x_n) \}$，应用上面的方法。基于以下定理：
$$
\lim_{x \rightarrow x_0} f(x) = A (\infty) \\
\iff \forall \{x_n\} \in \{\{x_n\}: \lim_{n \rightarrow \infty} x_n = x_0\}, \lim_{n \rightarrow \infty} f(x_n) = A (\infty)
$$

---

初等函数在**定义区间**内连续，而不是在**定义域**内连续。

因为对于仅仅在孤立点上有定义的初等函数（例如 $f(x) = \sqrt{\sin x -1}$），不存在极限的概念，也就不能说连续。

这一点和复变函数中解析函数的定义有相似之处。?

---

无穷大和无界的区别：

- 无穷大：数列的极限是无穷大
- 无界：包括了数列的极限是无穷大和数列不存在极限且上极限（或者下极限）是无穷大两种情况，对于后者，存在两个子列的极限不相等。

因此无穷大必定无界，无界不一定无穷大。

---

在求解参数方程的导数以及高阶导数的时候要注意到参数方程的导函数也是参数方程的形式。

$$
\begin{cases}
x = x(t) \\
\frac{\mathrm{d}y}{\mathrm{d}x} = \frac{y'(t)}{x'(t)}
\end{cases}
$$

因此对于更高阶的导数：

$$
\begin{cases}
x = x(t) \\
\frac{\mathrm{d}^2 y}{\mathrm{d}t^2} = \frac{(\frac{y'(t)}{x'(t)})'}{x'(t)}
\end{cases}
$$

## Exercises

第一类换元法

$$
\begin{aligned}
\int \frac{x+1}{x(1 + x e^x)} \mathrm{d}x &= \int \frac{(x+1)e^x}{x e^x (1+xe^x)} \mathrm{d}x \\
&= \int \frac{\mathrm{d}(x e^x)}{x e^x} - \int \frac{\mathrm{d}(x e^x)}{1 + x e^x} \\
&= \ln \left| \frac{x e^x}{1 + x e^x}\right|
\end{aligned}
$$

***Attention***:
$$
(x e^x)' = (x+1)e^x
$$

---

$$
\begin{aligned}
\int_{\frac{\pi}{2}}^{2 \arctan 2} \frac{\mathrm{d}x}{(1- \cos x)\sin^2 x} &= \int_{\frac{\pi}{2}}^{2 \arctan 2} \frac{(1 + \cos x)\mathrm{d} x}{\sin^4 x} \\
&= \int_{\frac{\pi}{2}}^{2 \arctan 2} \frac{{\mathrm{d}x}}{\sin^4 x} + \int_{\frac{\pi}{2}}^{2 \arctan 2} \frac{\mathrm{d}(\sin x)}{\sin^4 x} \\
&= - \int_{\frac{\pi}{2}}^{2 \arctan 2} (1 + \cot^2 x) \mathrm{d}(\cot x) - \left.\frac{1}{3 \sin^3 x}\right|_{\frac{\pi}{2}}^{2 \arctan 2} \\
&= \left.\left(- \cot x - \frac{\cot^3 x}{3} - \frac{1}{3 \sin^3 x}\right)\right|_{\frac{\pi}{2}}^{2 \arctan 2} \\
&= \frac{55}{96}
\end{aligned}
$$

OR
$$
\begin{aligned}
\int_{\frac{\pi}{2}}^{2 \arctan 2} \frac{\mathrm{d}x}{(1-\cos x)\sin^2 x} &= - \int_{\frac{\pi}{2}}^{2 \arctan 2} \frac{\mathrm{d}(\cot x)}{1 - \frac{\cot x}{\sqrt{1 + \cot^2 x}}} \\
&= - \int_{\frac{\pi}{2}}^{2 \arctan 2} \frac{\sqrt{1 + \cot^2 x}\mathrm{d} x}{\sqrt{1 + \cot^2 x}-\cot x} \\
&= - \int_{0}^{-\frac{3}{4}} (1 + u^2 + \sqrt{1 + u^2} u) \mathrm{d}u \\
&= - \left.\left(u + \frac{u^3}{3} + \frac{1}{3} (1+u^2)^{\frac{3}{2}}\right)\right|_{0}^{-\frac{3}{4}}
\end{aligned}
$$

***Attention***:
也可以用万能公式换元。

---

$$
\begin{aligned}
\int_0^{\frac{\pi}{2}} \frac{\mathrm{d}x}{1 + \tan^{\sqrt{2}}x} & \overset{u = \frac{\pi}{2} - x}{=} \int_{\pi/2}^0 \frac{- \mathrm{d}u}{1 + \tan^{\sqrt{2}}(\frac{\pi}{2} - u)} \\
&= \int_0^{\pi /2} \frac{\mathrm{d}u}{1 + \frac{1}{\tan^{\sqrt{2}}u}} \\
&= \int_0^{\pi /2} \frac{\tan^{\sqrt{2}}u \mathrm{d}u}{1 + {\tan^{\sqrt{2}}u}} \\
&\overset{x=u}{=} \int_0^{\pi /2} \frac{\tan^{\sqrt{2}}x \mathrm{d}x}{1 + {\tan^{\sqrt{2}}x}} \\
\int_0^{\frac{\pi}{2}} \frac{\mathrm{d}x}{1 + \tan^{\sqrt{2}}x} & = \int_0^{\pi /2} \frac{\tan^{\sqrt{2}}x \mathrm{d}x}{1 + {\tan^{\sqrt{2}}x}} = \frac{1}{2} \int_0^{\frac{\pi}{2}} \mathrm{d} x = \frac{\pi}{4}
\end{aligned}
$$

***Attention***:

遇到不能写出原函数的定积分，需要转化成和原来积分有关系的形式。

---

?There are some questions in following process.
$$
\begin{aligned}
\lim_{x \rightarrow 0} \frac{\int_0^{x^2}t^2 \sin \sqrt{x^2 - t^2} \mathrm{d} t}{x^7} &= \lim_{x \rightarrow 0} \frac{x^4 \sin \sqrt{x^2 - x^4} \cdot 2x}{7 x^6} \\
&= \frac{2}{7} \lim_{x \rightarrow 0} \frac{\sin x \sqrt{1 - x^2}}{x} \\
&= \frac{2}{7}
\end{aligned}
$$

因为上面的被积函数中显含有 $x$，不可以直接讲上下限作为自变量进行链式求导。

---

$$
\begin{aligned}
\lim _{x \rightarrow+\infty}(\sin \sqrt{x+1}-\sin \sqrt{x}) & = \lim _{x \rightarrow+\infty} 2 \cos \frac{\sqrt{x+1}+\sqrt{x}}{2} \sin \frac{\sqrt{x+1}-\sqrt{x}}{2} \\ & = \lim _{x \rightarrow+\infty} 2 \cos \frac{\sqrt{x+1}+\sqrt{x}}{2} \sin \frac{1}{2(\sqrt{x+1}+\sqrt{x})}
\end{aligned}
$$

***Attention***:

一般来说，和差的极限都不能直接算，需要先转化称因式乘积的形式。

---

$$
\begin{aligned}
\int_0^{\pi/2} \frac{\mathrm{d}x}{1 + \cos \theta \cos x} &= \int_0^{\pi/2} \frac{\mathrm{d}x}{1 + \cos \theta \frac{1 - \tan^2 \frac{x}{2}}{1 + \tan^2 \frac{x}{2}}} \\
&= \int_0^{\pi/2} \frac{(1+\tan^2 \frac{x}{2})\mathrm{d}x}{1+\tan^2 \frac{x}{2}+ \cos \theta (1 - \tan^2 \frac{x}{2})} \\
&= 2 \int_0^{\pi/2} \frac{\mathrm{d}(\tan \frac{x}{2})}{1 + \cos \theta + (1 - \cos \theta) \tan^2 \frac{x}{2}} \\
&= 2 \int_0^1 \frac{\mathrm{d}x}{1+\cos \theta + (1 - \cos \theta)x^2} \\
&= \frac{2}{1 + \cos \theta} \int_0^1 \frac{\mathrm{d}x}{1 + \left(\sqrt{\frac{1 - \cos \theta}{1 + \cos \theta}}x\right)^2} \\
&= 2 \sqrt{\frac{1}{(1 - \cos \theta)(1 + \cos \theta)}} \int_0^{\sqrt{\frac{1 - \cos \theta}{1 + \cos \theta}}} \frac{\mathrm{d}x}{1 + x^2} \\
&= \frac{2}{|\sin \theta|} \arctan \sqrt{\frac{1 - \cos \theta}{1 + \cos \theta}} \\
&= \frac{2}{|\sin \theta|} \arctan \left| \tan \frac{\theta}{2} \right| \\
&= \frac{\theta}{\sin \theta} & (\theta \in (0, \pi))
\end{aligned}
$$

---

$$
\begin{aligned}
\lim_{x \rightarrow + \infty} \left(\frac{x-1}{x}\right)^{\sqrt{x}} &= \lim_{x \rightarrow + \infty} \left(\frac{\sqrt{x}-1)(\sqrt{x}+1)}{\sqrt{x} \cdot \sqrt{x}}\right)^{\sqrt{x}} \\
&= \lim_{x \rightarrow + \infty} \left(\frac{\sqrt{x}-1}{\sqrt{x}}\right)^{\sqrt{x}} \left(\frac{\sqrt{x}+1}{\sqrt{x}}\right)^{\sqrt{x}} \\
&= e^{-1} e \\
&= 1
\end{aligned}
$$

---

$$
\begin{aligned}
\int \frac{\sec x \tan^2 x + \sec^3 x}{\sqrt{\sec^4 x + \tan^4 x}} \mathrm{d}x &= \int \frac{\tan x \mathrm{d} \sec x + \sec x \mathrm{d} \tan x}{\sqrt{(\sec^2 x - \tan^2 x)^2 + 2 \sec^2 x \tan^2 x}} \\
&= \int \frac{\mathrm{d} \sec x \tan x}{\sqrt{1 + 2 (\sec x \tan x)^2}} \\
&= \frac{\sqrt{2}}{2} \sinh^{-1} (\sqrt{2} \sec x \tan x) + C
\end{aligned}
$$

This is an end for this document. I write this in order to prevent the preview interface to be gone.

Here I want to say something to my self:

This is a notebook that seems to be foolish. As a matter of fact, before this foolish notebook, you were always doing something foolish and this is far from the first time. All this foolish things makes you a people different-or more narcissisticly, distinguishing.

This world need more people with a foolish mind instead of smart or sharp ones. The former can't be gained until you devote matched vigor and time absorbed.
