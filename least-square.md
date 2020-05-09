# Least Square

### 问题一

给定一组个数为$$n$$的常数

$$
y_i=c_i
$$

使用最小二乘法估算$$y$$

$$
S(y)=\sum_{i=1}^n{(y-c_i)}^2\\
S'(y)=2ny-2\sum_{i=1}^nc_i=0\\
y=\frac{\sum_{i=1}^nc_i}n
$$

### 问题二

给定一组个数为$$n$$的二维向量

$$
(x_i,y_i)
$$

使用最小二乘法估算函数$$f$$

假设$$f$$为线性函数$$y=ax+b$$

$$
S(x,y)=\sum_{i=1}^n\left[ax_i+b)-y_i\right]^2\\
\left\{\begin{array}{l}S_a^{'}(a,b)=2\sum_{i=1}^n(ax_i^2+bx_i-x_iy_i)=0\\S_b^{'}(a,b)=2\sum_{i=1}^n(ax_i+b-y_i)=0\end{array}\right.
$$



