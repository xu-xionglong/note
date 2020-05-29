# Least Square

### 问题一

给定一组个数为$$n$$的常数数据样本

$$
c_i
$$

假设数据的准确值为$$y$$，则误差平方为

$$
S(y)=\sum_{i=1}^n{(y-c_i)}^2\\
$$

令其导数为$$0$$

$$
S'(y)=2ny-2\sum_{i=1}^nc_i=0
$$

求得$$y$$

$$
y=\frac{\sum_{i=1}^nc_i}n
$$

### 问题二

给定一组个数为$$n$$的二维向量数据样本，求$$x$$和$$y$$的映射关系

$$
(x_i,y_i)
$$

假设$$x$$和$$y$$为线性关系，$$y=ax+b$$，则误差平方为

$$
S(a,b)=\sum_{i=1}^n\left[(ax_i+b)-y_i\right]^2\\
$$

令其偏导数为$$0$$

$$
\left\{\begin{array}{l}S_a^{'}(a,b)=2\sum_{i=1}^n(ax_i^2+bx_i-x_iy_i)=0\\S_b^{'}(a,b)=2\sum_{i=1}^n(ax_i+b-y_i)=0\end{array}\right.
$$

解方程组求得$$a$$，$$b$$

$$
a=\\
b=
$$

用矩阵形式表达误差平方

$$
S(a,b)=\begin{Vmatrix}\begin{bmatrix}1&x_1\\...&...\\1&x_n\end{bmatrix}\begin{bmatrix}b\\a\end{bmatrix}-\begin{bmatrix}y_1\\...\\y_n\end{bmatrix}\end{Vmatrix}^2
$$

如果$$x$$和$$y$$的关系为$$k$$次多项式，$$y=\sum_{i=0}^ka_ix^i$$，则矩阵形式的误差平方表示为

$$
S(a_0...a_k)=\left\|\begin{bmatrix}x_1^0&...&x_1^k\\...&...&...\\x_n^0&...&x_n^k\end{bmatrix}\begin{bmatrix}a_0\\...\\a_k\end{bmatrix}-\begin{bmatrix}y_1\\...\\y_n\end{bmatrix}\right\|^2\\
S(\boldsymbol a)=\left\|\boldsymbol X\boldsymbol a-\boldsymbol Y\right\|^2
$$

解得（步骤todo）

$$
\boldsymbol a={(\boldsymbol X^T\boldsymbol X)}^{-1}\boldsymbol X^T\boldsymbol Y
$$

### 问题三

给定一组个数为$$n$$的$$m$$维向量对数据样本，求$$\overset\rightharpoonup p$$和$$\overset\rightharpoonup q$$的映射关系

$$
\overset\rightharpoonup{q_i}\rightarrow\overset\rightharpoonup{p_i}
$$

假设

$$
p=\boldsymbol Aq+\boldsymbol t\\
\boldsymbol A={(a_{j,k})}_{j,k=1,...,m}\\
\boldsymbol t={(t_1,...,t_m)}^T
$$

则误差平方为

$$
S(\boldsymbol A,\boldsymbol t)=\sum_{i=1}^n\left\|\boldsymbol Aq_i+\boldsymbol t-p_i\right\|^2
$$

先对向量$$\boldsymbol t$$求偏导并令其为零向量（拆开单独对每个$$t_m$$求偏导结果是一样的）

$$
S^{'}_\boldsymbol t(\boldsymbol A,\boldsymbol t)=2\sum_{i=1}^n(\boldsymbol t+(\boldsymbol Aq_i-p_i))=\boldsymbol0\\
\boldsymbol t=\frac{{\displaystyle\sum_{i=1}^n}(p_{\mathbf i}-\boldsymbol Aq_{\mathbf i})}n=\frac{\displaystyle\sum_{i=1}^np_{\mathbf i}}n-\boldsymbol A\frac{\displaystyle\sum_{i=1}^nq_{\mathbf i}}n
$$

令

$$
p_\ast=\frac{\displaystyle\sum_{i=1}^np_i}n\\
q_\ast=\frac{\displaystyle\sum_{i=1}^nq_i}n\\
{\widehat p}_i=p_i-p_\ast\\
{\widehat q}_i=q_i-q_\ast
$$

重新代入误差平方得

$$
t=p_\ast-\boldsymbol Aq_\ast\\
S(\boldsymbol A,t)=\sum_{i=1}^n\left\|\boldsymbol A{\widehat q}_i-{\widehat p}_i\right\|^2
$$

若$$\boldsymbol A$$是仿射变换（公式中的向量默认为列向量）

$$
\boldsymbol A=\frac{\left(\sum_{i=1}^n{\widehat p}_i\widehat q_i^T\right)\left(\sum_{i=1}^n{\widehat p}_i\widehat p_i^T\right)^{-1}}n
$$

若$$\boldsymbol A$$是相似变换

若$$\boldsymbol A$$是刚体变换

