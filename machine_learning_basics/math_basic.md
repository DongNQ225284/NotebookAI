# Giải tích ma trận

## **1. Ký hiệu toán học**

### a) Số vô hướng

\- Ký hiệu bằng chữ cái viết thường in nghiêng – ví dụ: $x$

### b) Vector

\- Ký hiệu bằng chữ cái viết thường in đậm – ví dụ: $\mathbf{x}$

### c) Array (Vector theo hàng)

\- Ký hiệu bằng chữ cái viết thường – ví dụ: x

### d) Ma trận

\- Ký hiệu bằng chữ cái viết hoa in đậm – ví dụ: $\mathbf{X}$

## **2. Đạo hàm của hàm trả về một số vô hướng**

### **2.1** Cho hàm số $f(\mathbf{x}): \mathbb{R}^n \to \mathbb{R}$

Đạo hàm cấp 1 theo $\mathbf{x}$ được định nghĩa:

$$
\nabla f
=
\begin{bmatrix}
\frac{\partial f(\mathbf{x})}{\partial x_1} \\
... \\
\frac{\partial f(\mathbf{x})}{\partial x_n}
\end{bmatrix}
$$

Hessian được định nghĩa như sau:

$$
\nabla^2 f
=
\begin{bmatrix}
\frac{\partial^2 f(\mathbf{x})}{\partial x_1^2} & ... & \frac{\partial^2 f(\mathbf{x})}{\partial x_1x_n} \\
... & ... & ...\\
\frac{\partial^2 f(\mathbf{x})}{\partial x_nx_1} & ... & \frac{\partial^2 f(\mathbf{x})}{\partial x_n^2}
\end{bmatrix}
$$

### **2.2** Cho hàm số $f(\mathbf{X}):\mathbb{R}^{n \times d}\to\mathbb{R}$

Đạo hàm cấp 1 theo $\mathbf{X}$ được định nghĩa:

$$
\nabla f
=
\begin{bmatrix}
\frac{\partial f(\mathbf{X})}{\partial x_{11}} &
... &
\frac{\partial f(\mathbf{X})}{\partial x_{1d}} \\
... & ... & ...\\
\frac{\partial f(\mathbf{X})}{\partial x_{n1}} &
... &
\frac{\partial f(\mathbf{X})}{\partial x_{nd}}
\end{bmatrix}
$$

## **3 Đạo hàm của hàm trả về là một vector**

### **3.1** Cho hàm số $f(x):\mathbb{R}\to\mathbb{R}^n$

$$
f(x)
=
\begin{bmatrix}
f_1(x) \\
... \\
f_n(x)
\end{bmatrix}
$$

Đạo hàm cấp 1 theo $x$ được định nghĩa:

$$
\nabla f
=
\begin{bmatrix}
\frac{\partial f_1(x)}{\partial x} &
... &
\frac{\partial f_n(x)}{\partial x}
\end{bmatrix}
$$

### **3.2** Cho hàm số $f(\mathbf{x}): \mathbb{R}^k \to \mathbb{R}^n$

Đạo hàm cấp 1 theo $\mathbf{x}$ được định nghĩa:

$$
\nabla f(\mathbf{x}) =
\begin{bmatrix}
\frac{\partial f_1(\mathbf{x})}{\partial x_1} & \dots & \frac{\partial f_n(\mathbf{x})}{\partial x_1} \\
\vdots & \ddots & \vdots \\
\frac{\partial f_1(\mathbf{x})}{\partial x_k} & \dots & \frac{\partial f_n(\mathbf{x})}{\partial x_k}
\end{bmatrix}
=
\left[ \nabla f_1(\mathbf{x})^T \quad \dots \quad \nabla f_n(\mathbf{x})^T \right]
$$

## **4 Tính chất quan trọng của đạo hàm**

### **4.1 Quy tắc tích (Product rule)**

$$
\nabla (f(X)^T g(X)) = (\nabla f(X)) g(X) + (\nabla g(X)) f(X)
$$

### **4.2 Quy tắc chuỗi (Chain rule)**

Giả sử $h(\mathbf{x}) = f(g(\mathbf{x}))$, với $g: \mathbb{R}^k \to \mathbb{R}^m$ và $f: \mathbb{R}^m \to \mathbb{R}^n$. Khi đó:

$$
\nabla h(\mathbf{x}) = \nabla g(\mathbf{x}) \nabla f(g(\mathbf{x}))
$$

## **5. Phụ lục chứng minh**

### **5.1 $ f: \mathbb{R}^n \to \mathbb{R},\quad f(\mathbf{x}) = a^T \mathbf{x} $**

Khi đó, đạo hàm cấp 1:

$$
f(\mathbf{x}) = a_1 x_1 + \dots + a_n x_n
$$

$$
\nabla f(\mathbf{x}) =
\begin{bmatrix}
\frac{\partial f(\mathbf{x})}{\partial x_1} \\
\vdots \\
\frac{\partial f(\mathbf{x})}{\partial x_n}
\end{bmatrix}
=
\begin{bmatrix}
a_1 \\
\vdots \\
a_n
\end{bmatrix}
= a
$$

**Hessian:**

$$
\nabla^2 f(\mathbf{x}) =
\begin{bmatrix}
\frac{\partial^2 f(\mathbf{x})}{\partial x_1^2} & \dots & \frac{\partial^2 f(\mathbf{x})}{\partial x_1 \partial x_n} \\
\vdots & \ddots & \vdots \\
\frac{\partial^2 f(\mathbf{x})}{\partial x_n \partial x_1} & \dots & \frac{\partial^2 f(\mathbf{x})}{\partial x_n^2}
\end{bmatrix}
=
\begin{bmatrix}
0 & \dots & 0 \\
\vdots & \ddots & \vdots \\
0 & \dots & 0
\end{bmatrix}
= 0 \in S^n
$$

### **5.2 $ f: \mathbb{R}^n \to \mathbb{R}^m, \quad f(\mathbf{x}) = \mathbf{A}\mathbf{x} $**

$$
f(\mathbf{x}) =
\begin{bmatrix}
a_{11} & \dots & a_{1n} \\
\vdots & \ddots & \vdots \\
a_{m1} & \dots & a_{mn}
\end{bmatrix}
\begin{bmatrix}
x_1 \\
\vdots \\
x_n
\end{bmatrix}
=
\begin{bmatrix}
a_{11}x_1 + \dots + a_{1n}x_n \\
\vdots \\
a_{m1}x_1 + \dots + a_{mn}x_n
\end{bmatrix}
=
\begin{bmatrix}
\mathbf{a_1^T} \mathbf{x} \\
\vdots \\
\mathbf{a_m^T} \mathbf{x}
\end{bmatrix}
$$

Khi đó, đạo hàm cấp 1:

$$
\nabla f(\mathbf{x}) = [\nabla f_1(\mathbf{x}) \quad \dots \quad \nabla f_m(\mathbf{x})] = [\mathbf{a_1} \quad \dots \quad \mathbf{a_m}] = \mathbf{A}^T
$$

### **5.3 $ f: \mathbb{R}^n \to \mathbb{R},\quad f(\mathbf{x}) = \mathbf{x^T} \mathbf{A} \mathbf{x} $**

$$
\nabla f(\mathbf{x}) = \nabla (\mathbf{x^T} \mathbf{A} \mathbf{x})
= (\nabla \mathbf{x}) \mathbf{A} \mathbf{x} + \nabla (\mathbf{A} \mathbf{x}) \mathbf{x}
= \mathbf{A} \mathbf{x} + \mathbf{A^T} \mathbf{x}
= (\mathbf{A} + \mathbf{A^T})\mathbf{x}
$$

### **5.4 $ f: \mathbb{R}^n \to \mathbb{R},\quad f(\mathbf{x}) = \|\mathbf{A}\mathbf{x} - \mathbf{b}\|_2^2 = (\mathbf{A}\mathbf{x} - \mathbf{b})^T (\mathbf{A}\mathbf{x} - \mathbf{b}) $**

$$
\nabla f(\mathbf{x}) = 2 (\nabla (\mathbf{A}\mathbf{x} - \mathbf{b}))(\mathbf{A}\mathbf{x} - \mathbf{b}) = 2\mathbf{A^T} (\mathbf{A}\mathbf{x} - \mathbf{b})
$$

### **5.5 $ f: \mathbb{R}^n \to \mathbb{R},\quad f(\mathbf{x}) = \mathbf{a^T} \mathbf{x} \mathbf{x^T} \mathbf{b} $**

$$
\nabla f(\mathbf{x}) = \nabla (\mathbf{a^T} \mathbf{x} \mathbf{x^T} \mathbf{b})
$$

$$
= \nabla (\mathbf{x^T} \mathbf{a})(\mathbf{x^T} \mathbf{b}) + \nabla (\mathbf{x^T} \mathbf{b})(\mathbf{x^T} \mathbf{a})
$$

$$
= \nabla (\mathbf{a^T} \mathbf{x})(\mathbf{b^T} \mathbf{x}) + \nabla (\mathbf{b^T} \mathbf{x})(\mathbf{a^T} \mathbf{x})
$$

$$
= \mathbf{a} \mathbf{b^T} \mathbf{x} + \mathbf{b} \mathbf{a^T} \mathbf{x} = (\mathbf{a} \mathbf{b^T} + \mathbf{b} \mathbf{a^T}) \mathbf{x}
$$

### **5.6 $ f: \mathbb{R}^{n \times d} \to \mathbb{R}, \quad f(\mathbf{X}) = \text{trace}(\mathbf{A} \mathbf{X}) $**

$$
b_{ij} = \sum_{k=1}^n a_{ik} x_{kj}
$$

$$
f(\mathbf{X}) = \text{trace}(\mathbf{A}\mathbf{X}) = \text{trace}(\mathbf{B}) = \sum_{i=1}^d b_{ii} = \sum_{i=1}^d \sum_{j=1}^n a_{ij} x_{ji}
$$

$$
= b_{11} + \dots + b_{dd} = (a_{11}x_{11} + \dots + a_{1n}x_{n1}) + \dots + (a_{d1}x_{1d} + \dots + a_{dn}x_{nd})
$$

$$
\nabla f(\mathbf{X}) =
\begin{bmatrix}
\frac{\partial f(\mathbf{X})}{\partial x_{11}} & \dots & \frac{\partial f(\mathbf{X})}{\partial x_{1d}} \\
\vdots & \ddots & \vdots \\
\frac{\partial f(\mathbf{X})}{\partial x_{n1}} & \dots & \frac{\partial f(\mathbf{X})}{\partial x_{nd}}
\end{bmatrix}
=
\begin{bmatrix}
a_{11} & \dots & a_{d1} \\
\vdots & \ddots & \vdots \\
a_{1n} & \dots & a_{dn}
\end{bmatrix}
= \mathbf{A^T}
$$

### Tổng hợp

| STT | Hàm                                                                      | Gradient / Jacobian                                                                   | Hessian                                                                    |
| --- | ------------------------------------------------------------------------ | ------------------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| 5.1 | $f(\mathbf{x}) = \mathbf{a}^T \mathbf{x}$                                | $\nabla f(\mathbf{x}) = \mathbf{a}$                                                   | $\nabla^2 f(\mathbf{x}) = 0 \in S^n$                                       |
| 5.2 | $f(\mathbf{x}) = \mathbf{A}\mathbf{x},\ f:\mathbb{R}^n \to \mathbb{R}^m$ | $\nabla f(\mathbf{x}) = \mathbf{A}^T$ (Jacobian)                                      | –                                                                          |
| 5.3 | $f(\mathbf{x}) = \mathbf{x}^T \mathbf{A} \mathbf{x}$                     | $\nabla f(\mathbf{x}) = (\mathbf{A} + \mathbf{A}^T) \mathbf{x}$                       | $\nabla^2 f(\mathbf{x}) = \mathbf{A} + \mathbf{A}^T$                       |
| 5.4 | $f(\mathbf{x}) = \|\mathbf{A}\mathbf{x} - \mathbf{b}\|_2^2$              | $\nabla f(\mathbf{x}) = 2 \mathbf{A}^T (\mathbf{A}\mathbf{x} - \mathbf{b})$           | $\nabla^2 f(\mathbf{x}) = 2 \mathbf{A}^T \mathbf{A}$                       |
| 5.5 | $f(\mathbf{x}) = \mathbf{a}^T \mathbf{x} \mathbf{x}^T \mathbf{b}$        | $\nabla f(\mathbf{x}) = (\mathbf{a}\mathbf{b}^T + \mathbf{b}\mathbf{a}^T) \mathbf{x}$ | $\nabla^2 f(\mathbf{x}) = \mathbf{a}\mathbf{b}^T + \mathbf{b}\mathbf{a}^T$ |
| 5.6 | $f(\mathbf{X}) = \mathrm{trace}(\mathbf{A}\mathbf{X})$                   | $\nabla f(\mathbf{X}) = \mathbf{A}^T$                                                 | –                                                                          |
