## 第六章 多元函数微分学
***
### 第一节 多元函数
#### 1.1 二元函数的概念

**平面点集**
集合 $\bold{R}^2 = \{(x, y)|x \in \bold{R}, y \in \bold{R}\}$对应着整个二维空间，其子集为平面点集。

**邻域**
$\bold{R}^2$中任意两点$M_1(x_1, y_1)$与$M_2(x_2, y_2)$之间的距离为
$$\rho(M_1, M_2) = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2}$$
设$M_0(x_0, y_0)$为一定点，凡与$M_0$距离小于$\varepsilon(\varepsilon > 0)$的点构成的平面点集，叫做$M_0$的$\varepsilon$（圆形）邻域。记作
$$U(M_0, \varepsilon) = \{(x, y)|\sqrt{(x - x_0)^2 + (y - y_0)^2} < \varepsilon\}$$
而以$M_0$为心，以$2r$为边长的正方形内的所有点组成的平面点集叫做$M_0$的$r$(方形)邻域。记作
$$V(M_0, r) = \{(x, y)| |x - x_0| < r, |y - y_0| < r\}$$

接下来，设$E$为以平面点集。
**内点**
设$M_1 \in E$，如果存在$M_1$的一个$\delta$邻域$U(M_1, \delta)$使得$U(M_1, \delta) \subset E$，则称$M_1$是$E$的内点。
**内点**
设$M_1 \notin E$，如果存在$M_1$的一个$\eta$邻域$U(M_1, \eta)$使得$U(M_1, \eta)$中无点在$E$内，则称$M_1$是$E$的外点。
**聚点**
设$M_1$是平面上的任意一点，如果$M_1$的任何$\varepsilon$邻域$U(M_1, \epsilon)$内，至少含有$E$中的一个（异于$M_0$的点），则称$M_1$是$E$的聚点，也称极限点。
**边界点**
设$M_1$是平面上的任意一点，如果$M_1$的任何$\varepsilon$邻域$U(M_1, \epsilon)$内，既含有$E$内的点，又含有不在$E$内的点，则称$M_1$是$E$的边界点。$E$的边界点之合集为$E$的边界。
**开集、闭集**
如果$E$的任意点都是$E$的内点，则$E$为开集。
如果$E$的所有聚点都在$E$内，则$E$为闭集。
**区域**
如果$E$为开集，且$E$内的任何两点都可用属于$E$的折线连接起来，则$E$被称为开区域，开区域加上其边界，则为闭区域。
**有界集、无界集**
如果存在原点$O$的某个邻域$U(0, \varepsilon)$，使得$E \subset U(0, \varepsilon)$，则$E$是有界集，反之则为无界集。

设$D$为平面点集，$\bold{R}$为实数集，$f$是一个$D \to \bold{R}$的映射，则称$f$为$D$上的二元函数。

#### 1.2 二元函数的极限和连续
**二重极限**
设函数$z = f(x, y)$在点$P_0(x_0, y_0)$的邻域有定义，如果动点$P(x, y)$沿**任意路径**趋于定点$P_0(x_0, y_0)$时，$f(x, y)$总是趋于一个常数$A$，便称$A$为函数$f(x, y)$在点$P_0(x_0, y_0)$的极限。一般记作
$$\lim_{(x, y) \to (x_0, y_0)}f(x, y) = A$$
类似一元函数的极限，二元函数也能提出$\varepsilon$形式的极限，也不用需要在$P_0$点上有定义。

**二次极限**
如果把$y$看作一个常数，当$x \to x_0$时，$f(x, y)$的极限存在，设
$$\lim_{x \to x_0}f(x, y) = \phi(y)$$
而当$y \to y_0$时，$\phi(y)$极限存在为$A$，即
$$\lim_{y \to y_0}\phi(y) = A$$
则$A$为$f(x, y)$先对$x$，后对$y$的二次极限
$$\lim_{y \to y_0}\lim_{x \to x_0}f(x, y) = A$$
类似的有$f(x, y)$先对$y$，后对$x$的二次极限。

多元函数极限的计算性质类似一元函数。

**二次极限和二重极限的关联**
二次极限和二重极限是独立的两个概念。
当函数$f(x, y)$在点$P_0(x_0, y_0)$的二重极限和二次极限都存在时，有
$$\lim_{(x, y) \to (x_0, y_0)}f(x, y) = \lim_{x \to x_0}\lim_{y \to y_0}f(x, y)$$

**二元函数的连续性**
设函数$z = f(x, y)$在点$P_0(x_0, y_0)$与其邻域内定义，若有
$$\lim_{(x, y) \to (x_0, y_0)}f(x, y) = f(x_0, y_0)$$
则称函数$f(x, y)$在点$P_0(x_0, y_0)$连续。
若函数$f(x, y)$在闭区域$D$的内点连续，且在区域的边界点也连续，则称函数$f(x, y)$在闭区域$D$连续。

**复合函数的连续性**
设$u = u(x, y), v = v(x, y)$都在$(x_0, y_0)$连续，且$u(x_0, y_0) = u_0, v(x0, y0) = v_0$；又有$f(x, y)$在$(u_0, v_0)$连续，则复合函数$f[u(x, y), v(x, y)]$在$(x_0, y_0)$连续。

**有界性**
若函数$f(x, y)$在有界闭区域$D$上连续，则它在$D$上有界，即存在$M > 0$，对$D$上任意一点$(x, y)$，有
$$|f(x, y)| \le M$$
**最大最小值性**
若函数$f(x, y)$在有界闭区域$D$上连续，则它在$D$上必有最大值和最小值，即有
$$f(x_1, y_1) \le f(x, y) \le f(x_2, y_2)$$
**介值性**
若函数$f(x, y)$在有界闭区域$D$上连续，$M$和$m$分别是$f(x, y)$在$D$上的最大值和最小值，则对$[m, M]$内的数$c$，在$D$内必然存在一点$P(x_0, y_0)$，有
$$f(x_0, y_0) = c$$

**一致连续性**
设$f(x, y)$定义在区域$D$上，对任意给定的正数$\varepsilon$，存在相应的正数$\delta$，对$D$上任意两点$P_1(x_1, y_1)$和$P_2(x_2, y_2)$，当$|x_1 - x_2| < \delta, |y_1 - y_2| < \delta$时，有
$$|f(x_1, y_1) - f(x_2, y_2)| < \varepsilon$$
则称函数$f(x, y)$在$D$上一致连续。
如果函数$f(x, y)$在有界闭区域$D$上连续，则它在$D$上一致连续。

#### 1.3 偏导数

**偏导数**
设函数$z = f(x, y)$在点$(x_0, y_0)$的邻域内有定义，如果极限
$$\lim_{\Delta x \to 0} \frac{f(x_0 + \Delta x, y_0) - f(x_0, y_0)}{\Delta x}$$
存在，称此极限为函数$f(x, y)$在点$(x_0, y_0)$关于$x$的偏导数，记作
$$f'_x(x_0, y_0), z'_x|_{x=x_0,y=y_0}, \frac{\partial f}{\partial x}|_{x=x_0,y=y_0}, \frac{\partial z}{\partial x}|_{x=x_0,y=y_0}$$
关于$y$的偏导数类似。

**偏导函数**
如果函数$z = f(x, y)$在区域$D$内的每一点$(x, y)$处对$x$的偏导数都存在，那么这个偏导数就是函数$z = f(x, y)$对自变量$x$的偏导函数，记作
$$\frac{\partial z}{\partial x}, \frac{\partial f}{\partial x}, z_x, f_x(x, y)$$
关于$y$的偏导函数类似。

**高阶偏导数**
如果$z'_x$和$z'_y$关于自变量$x,y$的偏导数还存在，则有二间偏导数，记作
$$\frac{\partial}{\partial x}(\frac{\partial z}{\partial x}) = \frac{\partial ^2z}{\partial x^2} = z''_{xx} = z''_{x^2},\qquad
\frac{\partial}{\partial y}(\frac{\partial z}{\partial x}) = \frac{\partial ^2z}{\partial x \partial y} = z''_{xy}$$
$$\frac{\partial}{\partial y}(\frac{\partial z}{\partial y}) = \frac{\partial ^2z}{\partial y^2} = z''_{yy} = z''_{y^2},\qquad
\frac{\partial}{\partial x}(\frac{\partial z}{\partial y}) = \frac{\partial ^2z}{\partial y \partial x} = z''_{yx}$$
类似的，可以定义更高阶的偏导数。

需要注意的是，$f''_{xy}$和$f''_{yx}$可以同时存在但不相等。
当$f(x, y)$在点$P(x_0, y_0)$之邻域$G$内有连续的二级偏导数$f''_{xy}(x, y),f''_{yx}(x, y)$时，有$f''_{xy}(x, y) = f''_{yx}(x, y)$。

#### 1.4 全微分

**全微分**
当$z = f(x, y)$的自变量$x, y$相对于$(x_0, y_0)$分别有改变量$\Delta x,\Delta y$时，有
$$\text{d}z = A\Delta x + B\Delta y$$
$$\Delta z = dz + o(\rho), \rho = \sqrt{(\Delta x)^2 + (\Delta y)^2}\to 0$$
则记$\text{d}z$为函数$z = f(x, y)$在点$(x_0, y_0)$的全微分。

如果函数$z = f(x, y)$在点$(x_0, y_0)$处有全微分，则有函数$z = f(x, y)$在点$(x_0, y_0)$连续，且偏导数皆存在。

**函数可微的充分条件**
设函数$(x_0, y_0)$在点$(x_0, y_0)$的某一邻域内，其两个偏导数都存在，并在点$(x_0, y_0)$上连续，则函数$(x_0, y_0)$在点$(x_0, y_0)$可微。

#### 1.5 复合函数的微分法
若函数$z = f(x, y)$可微
设$x = \phi(t), y = \psi(t)$，则复合函数$z = f[\phi(t), \psi(t)]$对$t$的导数存在，且有
$$\frac{\text{d}z}{\text{d}t} = \frac{\partial z}{\partial x} \frac{\text{d}x}{\text{d}t} + \frac{\partial z}{\partial y} \frac{\text{d}y}{\text{d}t}$$
设$x = \phi(s, t), y = \psi(s, t)$的四个一阶偏导数在点$(s, t)$都存在，则复合函数$z = [\phi(s, t), \psi(s, t)]$对于$s, t$的偏导数都存在，且有
$$\frac{\partial z}{\partial s} = \frac{\partial z}{\partial x} \frac{\partial x}{\partial s} + \frac{\partial z}{\partial y} \frac{\partial y}{\partial s}$$
$$\frac{\partial z}{\partial t} = \frac{\partial z}{\partial x} \frac{\partial x}{\partial t} + \frac{\partial z}{\partial y} \frac{\partial y}{\partial t}$$
如果要求复合函数的高阶偏导数的话，只要重复上面的方法即可。

#### 1.6 隐函数的微分法