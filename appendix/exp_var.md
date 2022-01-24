<head>
    <script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
    <script type="text/x-mathjax-config">
        MathJax.Hub.Config({
            tex2jax: {
            skipTags: ['script', 'noscript', 'style', 'textarea', 'pre'],
            inlineMath: [['$','$']]
            }
        });
    </script>
</head>

### 1 随机变量$X$的数学期望、方差
#### （1）$X$为标量
对随机变量$X \in \mathbb{R}$，分两种情况讨论：

（1.1）$X$为离散型随机变量

令$X$的取值为$\{x_1, x_2, \cdots , x_n\}$，这些取值点上对应的概率为$\{p_1, p_2, \cdots, p_n\}$。

$X$的数学期望为：
$$
\begin{equation}
\begin{aligned}
E(X) &= x_1 p_1 + x_2 p_2 + \cdots + x_n p_n\\
&= \sum_{i=1}^{n} x_i p_i\\
\end{aligned}
\end{equation}
$$

$X$的方差为：
$$
\begin{equation}
\begin{aligned}
Var(X) &= E\{(X - E(X))^2\}\\
&= (x_1 - E(X))^2 p_1 + (x_2 - E(X))^2 p_2 + \cdots + (x_n - E(X))^2 p_n \\
&= E(X^2) - E^2(X)
\end{aligned}
\end{equation}
$$

（1.2）$X$为连续型随机变量

令$X$的概率密度函数为$f(x)$，$X$的定义域为$[a, b]$。则$X$的数学期望为：
$$
\begin{equation}
\begin{aligned}
E(X) = \int_a^b f(x) d(x)
\end{aligned}
\end{equation}
$$

$X$的方差为：

$$
\begin{equation}
\begin{aligned}
Var(X) &= \int_a^b (x - E(X))^2 dx \\
&= E(X^2) - E^2(X)
\end{aligned}
\end{equation}
$$

#### （2）$X$为向量
记$X \in \mathbb{R}^{n}$，$X = [X_1, X_2, \cdots, X_n]^T$，其中$X_i, (i=1,2, \cdots, n),$均为随机变量。

$X$的数学期望为各个分量的数学期望：

$$
\begin{equation}
\begin{aligned}
E(X) &= E \left( \left[ \begin{array}{c} X_1\\ X_2\\ \vdots\\ X_n \end{array}\right] \right)\\
&=\left[ \begin{array}{c} E(X_1) \\ E(X_2) \\ \vdots \\ E(X_n) \end{array}\right] \\
\end{aligned}
\end{equation}
$$

$X$的方差为各个分量的方差：

$$
\begin{equation}
\begin{aligned}
Var(X) &= Var\left( \left[ \begin{array}{c} X_1\\ X_2\\ \vdots\\ X_n \end{array} \right] \right) \\
&= \left[ \begin{array}{c} Var(X_1) \\ Var(X_2) \\ \vdots \\ Var(X_n) \end{array} \right]
\end{aligned}
\end{equation}
$$
#### （3）$X$为矩阵
记随机变量$X \in \mathbb{R}^{m \times n}$为：

$$
\begin{equation}
X = \left[ \begin{array}{cccc} X_{1,1} & X_{1, 2} & \cdots & X_{1, n} \\ X_{2, 1} & X_{2, 2} & \cdots & X_{2, n} \\ \vdots & \vdots & \vdots & \vdots \\ X_{m, 1} & X_{m, 2} & \cdots & X_{m, n}\end{array} \right]
\end{equation}
$$

$X$的数学期望定义为：
$$
\begin{equation}
\begin{aligned}
E(X) &= E\left( \left[ \begin{array}{cccc} X_{1,1} & X_{1, 2} & \cdots & X_{1, n} \\ X_{2, 1} & X_{2, 2} & \cdots & X_{2, n} \\ \vdots & \vdots & \vdots & \vdots \\ X_{m, 1} & X_{m, 2} & \cdots & X_{m, n}\end{array} \right] \right) \\
&= \left[ \begin{array}{cccc} E(X_{1,1}) & E(X_{1, 2}) & \cdots & E(X_{1, n}) \\ E(X_{2, 1}) & E(X_{2, 2}) & \cdots & E(X_{2, n}) \\ \vdots & \vdots & \vdots & \vdots \\ E(X_{m, 1}) & E(X_{m, 2}) & \cdots & E(X_{m, n})\end{array} \right]
\end{aligned}
\end{equation}
$$

$X$的方差定义为：
$$
\begin{equation}
\begin{aligned}
Var(X) &= Var\left( \left[ \begin{array}{cccc} X_{1,1} & X_{1, 2} & \cdots & X_{1, n} \\ X_{2, 1} & X_{2, 2} & \cdots & X_{2, n} \\ \vdots & \vdots & \vdots & \vdots \\ X_{m, 1} & X_{m, 2} & \cdots & X_{m, n}\end{array} \right] \right) \\
&= \left[ \begin{array}{cccc} Var(X_{1,1}) & Var(X_{1, 2}) & \cdots & Var(X_{1, n}) \\ Var(X_{2, 1}) & Var(X_{2, 2}) & \cdots & Var(X_{2, n}) \\ \vdots & \vdots & \vdots & \vdots \\ Var(X_{m, 1}) & Var(X_{m, 2}) & \cdots & Var(X_{m, n})\end{array} \right]
\end{aligned}
\end{equation}
$$