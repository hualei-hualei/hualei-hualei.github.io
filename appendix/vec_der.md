# 函数求导

## 1. $f(x) \in \mathbb{R}$为标量
- $x \in \mathbb{R}$为标量（标量-标量）
$$
\begin{equation}
\begin{aligned}
f'(x) &= \lim_{\triangle x \to 0} \frac{f(x + \triangle x) - f(x)} 
{\triangle x} \\
&= \frac{dy}{dx}
\end{aligned}
\end{equation}
$$

- $\mathbf{x} \in \mathbb{R}^{m}$为向量（标量-向量）
记$f(\mathbf{x}) = f(x_1, x_2, \cdots, x_m)$
$$
\begin{equation}
\begin{aligned}
\frac{df}{d \mathbf{x}} &= \left[
                                    \begin{array}{c}
                                        \frac{\partial f}{\partial x_1}\\
                                        \frac{\partial f}{\partial x_2}\\
                                        \vdots \\
                                        \frac{\partial f}{\partial x_m}
                                    \end{array}
                            \right] \\
                            &= \triangledown f
\end{aligned}
\end{equation}
$$
$\triangledown f$称为$f(\mathbf{x})$的**梯度**。

- [$\mathbf{x} \in \mathbb{R}^{p \times q}$为矩阵](https://en.wikipedia.org/wiki/Matrix_calculus#Scalar-by-matrix)（标量-矩阵）
$$
\begin{equation}
\frac{df(\mathbf{x})}{d \mathbf{x}} = \left[
                                      \begin{array}{c}
                                        \frac{df(\mathbf{x})}{d\mathbf{x}_{11}} & 
                                        \frac{df(\mathbf{x})}{d\mathbf{x}_{12}} & 
                                        \cdots &
                                        \frac{df(\mathbf{x})}{d\mathbf{x}_{1q}} \\
                                        \frac{df(\mathbf{x})}{d\mathbf{x}_{21}} & 
                                        \frac{df(\mathbf{x})}{d\mathbf{x}_{22}} & 
                                        \cdots &
                                        \frac{df(\mathbf{x})}{d\mathbf{x}_{2q}} \\
                                        \vdots & \vdots & \vdots & \vdots \\
                                        \frac{df(\mathbf{x})}{d\mathbf{x}_{p1}} & 
                                        \frac{df(\mathbf{x})}{d\mathbf{x}_{p2}} & 
                                        \cdots &
                                        \frac{df(\mathbf{x})}{d\mathbf{x}_{pq}}
                                      \end{array}
                                      \right]
\end{equation}
$$
等价于
$$
\begin{equation}
\left[ \frac{df(\mathbf{x})}{d\mathbf{x}} \right]_{ij} = \frac{df(\mathbf{x})}{d\mathbf{x}_{ij}}
\end{equation}
$$

## 2. $f(x) \in \mathbb{R}^{n}$为向量

- $x \in \mathbb{R}$为标量（向量-标量）
记$f(x) = [f_1(x), f_2(x), \cdots, f_n(x)]$，其中$f_i, f_j$相互独立。则
$$
\begin{equation}
\left[\frac{d f(x)}{d x} \right]_i = \frac{d f_i(x)}{d x}
\end{equation}
$$
为向量。即
$$
\begin{equation}
\frac{d f(x)}{d x} = \left[
                        \begin{array} {c}
                            \frac{d f_1(x)}{d x} \\
                            \frac{d f_2(x)}{d x} \\
                            \vdots\\
                            \frac{d f_n(x)}{d x}
                        \end{array}
                     \right]
\end{equation}
$$

- $\mathbf{x} \in \mathbb{R}^m$为向量（向量-向量）
记$f(\mathbf{x}) = [f_1(\mathbf{x}), f_2(\mathbf{x}), \cdots, f_n(\mathbf{x})]^T$；其中$f_i(\mathbf{x}) \in \mathbb{R}$，$f_i(\mathbf{x}), f_j(\mathbf{x})$相互独立。则
$$
\begin{equation}
\left[ \frac{d f}{d \mathbf{x}} \right]_{ij} = \frac{ \partial f_i(\mathbf{x})}{\partial \mathbf{x}_j}
\end{equation}
$$
为矩阵。
即
$$
\begin{equation}
\frac{df}{d\mathbf{X}} = \left[ 
                                \begin{array}{c}
                                    \frac{\partial f_1}{\partial x_1} & \frac{\partial f_1}{\partial x_2} & \cdots & \frac{\partial f_1}{\partial x_n} \\
                                    \frac{\partial f_2}{\partial x_1} & \frac{\partial f_2}{\partial x_2} & \cdots & \frac{\partial f_2}{\partial x_n} \\
                                    \vdots & \vdots & \cdots & \vdots\\
                                    \frac{\partial f_n}{\partial x_1} & \frac{\partial f_n}{\partial x_2} & \cdots & \frac{\partial f_n}{\partial x_n}
                                \end{array}
                         \right]
\end{equation}
$$
该矩阵称为[**Jacobian matrix**](https://en.wikipedia.org/wiki/Jacobian_matrix_and_determinant)。

## 3. $f(x)$为矩阵
记$f(x) = [f_{ij}(x)], (1 \leq i \leq m, 1 \leq j \leq n)$.
- $x \in \mathbb{R}$为标量(矩阵-标量)
其结果为矩阵：
$$
\begin{equation}
\left[ \frac{df}{dx} \right]_{ij} = \frac{d f_{ij}(x)}{dx}
\end{equation}
$$
等价于
$$
\begin{equation}
\frac{df(x)}{dx} = \left[
                    \begin{array}{c}
                        \frac{df_{11}(x)}{dx} & \frac{df_{12}(x)}{dx} & \cdots & \frac{df_{1n}(x)}{dx}\\
                        \frac{df_{21}(x)}{dx} & \frac{df_{22}(x)}{dx} & \cdots & \frac{df_{2n}(x)}{dx}\\
                        \vdots & \vdots & \vdots & \vdots \\
                        \frac{df_{m1}(x)}{dx} & \frac{df_{m2}(x)}{dx} & \cdots & \frac{df_{mn}(x)}{dx}
                    \end{array}
                    \right]
\end{equation}
$$

## 4. 导数的性质
- $f(x)$为一次函数

$$
\begin{equation}
\begin{aligned}
\frac{\partial a^TX}{\partial X} &= \frac{\partial \sum_{i=1}^{n} a_i X_i}{\partial X} \\
                                 &= \left[
                                                                \begin{array}{c}
                                                                \frac{\partial \sum_{i=1}^{n} a_i X_i}{\partial X_1}\\
                                                                \frac{\partial \sum_{i=1}^{n} a_i X_i}{\partial X_2} \\
                                                                \vdots \\
                                                                \frac{\partial \sum_{i=1}^{n} a_i X_i}{\partial X_n}
                                                                \end{array}
                                                               \right] \\
                                &= \left[
                                    \begin{array}{c}
                                        a_1 \\
                                        a_2 \\
                                        \vdots \\
                                        a_n
                                    \end{array}
                                    \right] \\
                                &= a
\end{aligned}
\end{equation}
$$

- $f(x)$为二次函数

$$
\begin{equation}
\begin{aligned}
\frac{\partial a^TXb}{\partial X}
    &= \frac{\partial \left( \begin{array}{c}
                                     a_1 X_{11} b_1 &+ & a_1 X_{12} b_2 &+ \cdots & +a_1 X_{1q} b_q +\\
                                     a_2 X_{21} b_1 &+ &a_2 X_{22} b_2 &+ \cdots &+ a_2 X_{2q} b_q +\\
                                     \vdots & &\vdots & &\vdots\\
                                     a_p X_{p1} b_1 &+ &a_p X_{p2} b_2 &+\cdots &+ a_p X_{pq} b_{q}
                             \end{array}
                      \right)
            }
            {\partial
                \left(
                    \begin{array}{c}
                        \left[
                            \begin{array}{c}
                                X_{11} & X_{12} &\cdots & X_{1q} \\
                                X_{21} & X_{22} & \cdots & X_{21} \\
                                \vdots & \vdots & \vdots & \vdots \\
                                X_{p1} & X_{p2} & \cdots & X_{pq}
                            \end{array}
                        \right]
                    \end{array}
                \right)
            } \\
    &= \left[
       \begin{array}{c}
       \frac{\partial ()}{\partial X_{11}} & \frac{\partial ()}{\partial X_{12}} & \cdots & \frac{\partial ()}{\partial X_{1q}} \\
       \frac{\partial ()}{\partial X_{21}} & \frac{\partial ()}{\partial X_{22}} & \cdots & \frac{\partial ()}{\partial X_{2q}} \\
       \vdots & \vdots & \vdots & \vdots \\
       \frac{\partial ()}{\partial X_{p1}} & \frac{\partial ()}{\partial X_{p2}} & \cdots & \frac{\partial ()}{\partial X_{pq}}
       \end{array} 
       \right] \\
    &= \left[
       \begin{array}{c}
        a_1 b_1 & a_1 b_2 &\cdots & a_1 b_q \\
        a_2 b_1 & a_2 b_2 &\cdots & a_2 b_q \\
        \vdots & \vdots & \vdots & \vdots \\
        a_p b_1 & a_p b_2 &\cdots & a_p b_q
       \end{array} 
       \right] \\
    &= ab^T
\end{aligned}
\end{equation}
$$

$$
\begin{equation}
\begin{aligned}
\frac{\partial a^T X^T b}{\partial X}
    &= \frac{\partial \left( \begin{array}{c}
                                        a_1 X_{11} b_1 &+ & a_1 X_{12} b_2 &+ \cdots & +a_1 X_{1q} b_q +\\
                                        a_2 X_{21} b_1 &+ &a_2 X_{22} b_2 &+ \cdots &+ a_2 X_{2q} b_q +\\
                                        \vdots & &\vdots & &\vdots\\
                                        a_p X_{p1} b_1 &+ &a_p X_{p2} b_2 &+\cdots &+ a_p X_{pq} b_{q}
                                \end{array}
                        \right)
                }
                {\partial
                    \left(
                        \begin{array}{c}
                            \left[
                                \begin{array}{c}
                                    X_{11} & X_{21} &\cdots & X_{p1} \\
                                    X_{12} & X_{22} & \cdots & X_{p2} \\
                                    \vdots & \vdots & \vdots & \vdots \\
                                    X_{1q} & X_{2q} & \cdots & X_{pq}
                                \end{array}
                            \right]
                        \end{array}
                    \right)
                } \\
    &= \left[
            \begin{array}{c}
                a_1 b_1 & a_2 b_1 & \cdots & a_p b_1 \\
                a_1 b_2 & a_2 b_2 & \cdots & a_p b_2 \\
                \vdots & \vdots & \vdots & \vdots \\
                a_1 b_q & a_2 b_q & \cdots & a_p b_q
            \end{array}
       \right] \\
    &= b a^T
\end{aligned}
\end{equation}
$$

## 参考资料
[1] https://en.wikipedia.org/wiki/Matrix_calculus
[2] https://www.math.uwaterloo.ca/~hwolkowi/matrixcookbook.pdf