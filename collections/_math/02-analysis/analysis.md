---
title: Notes on Mathematical Analysis by Chen
categories: 02-Analysis
tags: Notes Ongoing
---


## 数学分析的特征

1. 在研究**无规律变速运动**时，已有的数学方法已无法满足。此时已产生了微积分的思想萌芽。牛顿和莱布尼兹系统地提出了微分和积分的概念，并找到了二者的深刻联系。
2. 牛顿力学、麦克斯韦的电磁学，都是建立在微积分的基础之上。数学分析的基本要求是**平滑性、连续性**，**是在实数集合上讨论问题**。
   > 普朗克提出“普朗克黑体”公式之后，与黑体辐射问题的各个波段都吻合，但在处理熵和概率的关系时，如果要使新方程成立，必须假设能量在吸收和发射时，必须不是连续不断（无限分割）的，而是分成一小一小的， 被命名为量子。

## 学习重点：

1. 微积分的核心思想、原理、方法是最核心的内容。
2. 提高逻辑思维、论证推理能力。
3. 通过严格的训练，掌握熟练的计算能力和技巧，多练习和思考，长期积累。
4. 知晓应用的价值，数学模型的思想。

## 证明技巧

1. 基本功：用定义证明
3. 式中变量在指数上时，可两边取对数，如 lg
4. 放大的技巧：在解不等式时，如果只要求证明存在性，可以将不等式适当放大，以得到一个容易得出的值。
5. 需证 x 是有理数，则 x 可写为 n/m，n、m 为正整数且互质；或与此两条相悖以反证
6. 数学归纳法套娃证明时，也可以先证 n=1，2，2^m 成立，再证任意 2^(m-1)到 2^m 项成立，并推广到以其他方法划间隔。例：1.2节 平均值不等式
7. 需证明 x 存在，尝试规定某些结构，构造一个 x 的形式。例：2.1 确界存在定理
8. 需证比任意值都小，对于无限的项，可以尝试用无限性构造一个数，比任意小值还小。例：2.1 确界存在定理
9. 项数不一导致无法使用平均值不等式时，可以为其添加若干平凡项，每项都是已经知道的某种平均值。如例2.4.6。

### 常用定理

1. 三角不等式：
   $$ ||a| - |b|| <= |a + b| <= |a| + |b| $$
2. 平均值不等式 算术平均值 >= 几何平均值 >= 调和平均值
3. 夹逼性定理常用于难于直接解出极限的数列

## 第一章 集合与映射

### 1.1 集合

元素：（特定）性质 对象

集合 set：（特定）性质 对象 汇集 （没有顺序）

属于、不属于：集合 元素 关系 是

空集（Ø）：无 元素 集合

子集 subset：所有 元素 属于 集合

真子集 proper subset：子集 存在 不属于

集合相同：集合 所有 元素 元素相同；集合 子集 且

区间 interval 开区间 open interval 闭区间 closed interval：实数 子集

> 常用集合：正整数集 N+，自然数集 N，整数集 Z，有理数集 Q，实数集 ℝ

> 集合的表示：枚举法 enumeration method 描述法 descriptive method

并 union：所有 元素 汇集

交

#### 集合的运算

1. 定义 并（∪），交（∩）
   1. 交换律 Commutative
   2. 结合律 Associative
   3. 分配率 Distributive
2. 定义 差（\或-） relative complement，S-T 是属于 S 但是不属于 T 的集合
3. 定义 补 Complement，S^c_X = X\S
   1. 对偶律（de Morgan 对偶原理）：
      $$
      (A∪B)^c = A^c ∩ B^c
      (A∩B)^c = A^c ∪ B^c
      $$

#### 有限集、无限集

1. 定义 有限集
2. 定义 无限集
3. 定义 可列集（首先是无限集）：按照规则 排成一列，无一遗漏，无一重复
   > 任一无限集，一定包含可列子集
   > 无限集不一定是可列集
   > ℝ 是无限集，但不是可列集
   > Z 是可列集
   > 任意有限个可列集的并都是可列集 Any finite union of countable sets is countable.
4. 定理 1.1.1 可列个可列集之并，也是可列集 The union of countably many countable sets is countable.(Assuming *the axiom of countable choice*)
   > 对角法排列（`康托三角形`），用于表示可列个可列集之并。
5. 定理 1.1.2 有理数集合 Q 是可列集
6. 定义 有序对 ordered pair
7. Descartes 乘积集合 Cartesian product [kɑrˈtiʒən]
   > ℝ _ ℝ Descartes 平面直角坐标系 Rectangular coordinate system.
   > ℝ _ ℝ \* ℝ Descartes 空间直角坐标系

### 1.2 映射与函数

#### 映射

> 映射是集合之间的一种对应关系

1. 定义 映射：
   > 映射的基本要素：<br>
   > X = D_f 定义域<br>
   > Y 限制了值域的范围<br>
   > f 像是唯一的<br>
   > 逆像不一定是唯一的
2. 定义 单射 injection， $$ x_1 ≠ x_2 ⇒ y_1 ≠ y_2 $$
3. 定义 满射 surjection，
4. 定义 双射 bijection，又称一一对应
5. 定义 逆映射 inverse mapping $ g: R_f -> X , g -> x(f(x) = y)，则 g 是 f 的逆映射，记为 f^-1 $
6. 定义 复合映射 composite mapping，⚬
   > 映射 f: X -> Y，有逆映射 f^-1: R_f -> X，
   > 则 f^-1 ⚬ f(x) = x, x ∈ X
   > f ⚬ f^-1(y) = y, y ∈ R_f
   > arcsin(sin(x)) = x, x ∈ [- pi/2, pi/2]
   > sin(arcsin(y)) = y, y ∈ [-1, 1]
   > 此处应注意对 x、y 的定义域进行规定

#### 函数

> 函数是映射的一种特殊情况。X ⊂ R，Y = R，则为一元实函数，简称函数。X Y 在复数集合上，则为复变函数。

1. 定义 函数（一元实函数）、自变量、因变量
2. 基本初等函数
   - 常数函数：y = c
   - 幂函数： y = x^a （a ∈ ℝ）
   - 指数函数：y = a^x (a > 0, a != 1)
   - 对数函数：y = log_a（x） (a > 0, a != 1)
   - 三角函数：y = sin（x），y = cos（x），y = tan（x），y = cot（x），……
   - 反三角函数：y = arcsin（x），y = arccos（x），y = arctan（x），……
3. 初等函数：由基本初等函数经过有限次四则运算、复合运算所产生的函数。
4. 自然定义域：自变量的最大取值范围。（若函数自变量取自然定义域，则省略）
5. 函数的表示
   1. 显式表示 y = f（x）
   2. 分段表示（可分为无限段）
      > 例：符号函数
      > 整数部分函数
      > 注意：(0, -1)的整数部分是-1，(-1, -2)的整数部分是-2，……
      > 非负小数部分函数
   3. 隐式表示 F(x, y) = 0
      > 例：上半圆的方程 x^2 + y^2 = R^2
      > 并非所有的隐式表示的方程，都能解出关系，得到显式表示，如 Kepler 方程
      > y = x + εsin(y), ε 是椭圆的离心率，0 < ε < 1x 与时间有关，y 与位置有关
   4. 参数表示
      > 例：上半圆的方程，设 t 是函数图像中一点与原点的连线与 x 轴的角度。那么：
      > x = Rcos(t), y = Rsin(t), t ∈ [0, pi/2]
      > 有的函数很难给出显式表示，但容易给出参数表示
      > 例：旋轮线
6. 函数的简单特性
   1. 有界性，上界，下界
   2. 单调性，单调增加（记为 f↑），严格单调增加（f 严格 ↑）， 单调减少，严格单调减少
   3. 奇偶性，奇函数，偶函数
   4. 周期性，周期，最小周期
      > 周期函数不一定都有最小周期
      > 例：Dirichlet 函数，常用作反例，无法画出图形，偶函数，处处不连续，处处不可导，处处无极限，是一个有界函数
      > 对 Dirichlet 函数，任意有理数都是它的周期，但无最小周期
7. 定理 1.2.1 三角不等式 ||a| - |b|| <= |a + b| <= |a| + |b|
   > 需证明：- |a||b| <= ab <= |a||b| 显然成立，每项加 a^2 + b^2
8. 定理 平均值不等式 算术平均值 >= 几何平均值 >= 调和平均值
   > 需证明：视频 P6 47：00

## 第二章 数列极限

关键概念：
* 实数连续统
* 最大数、最小数、上界、上确界、下界、下确界
* 确界存在定理、Dedekind切割定理
* 数列、通项、极限、收敛、发散、无穷小量、邻域、有界数列
* 数列极限的性质：唯一性、有界性、保序性、夹逼性定理
* 数列极限的四则运算
* 无穷大量、正无穷大量、负无穷大量、不定无穷大量
* 定理 2.3.1、定理2.3.2及其推论
* 待定型、单调增加数列、严格单调增加数列、单调减少数列、严格单调减少数列
* Stolz定理

> 引入量词符号：
> ∃ 存在量词：存在，可以找到
> ∀ 全称量词：对于任意的，对于每一个

### 2.1 实数系的连续性

> 数系的扩充（人类对数系认识的历史）：<br>
> 1. 自然数集 N：对加法、乘法封闭<br>
> 2. 整数集 Z：对加法、乘法、减法封闭<br>
> 3. 有理数集 Q：对加减乘除封闭<br>
> 4. 数学的第一次危机：毕达哥拉斯学派发现单位正方形的对角线不可*公度*，即发现 $$\sqrt{2}$$ 为无理数<br>
> 5. 现代实数理论的建立
> 6. 实数集 R = {x | x是有理数或无理数}，实数布满了整个数轴，具有连续性

1. 实数连续统
2. 最大数 max
3. 最小数 min
4. 上界 每个元素都小于等于
5. 上确界（sup）
6. 下界
7. 下确界（inf）
8. 定理 **确界存在定理**，又称为实数系连续定理（需证明 P8）
   > 非空有上界的数集必有上确界；非空有下界的数集必有下确界
   > 需证明例 2.1.3 的：无理数不具有连续性？
9. 定理 **Dedekind切割定理**

### 2.2 数列极限

> 按正整数编号的一串数

定义 数列、通项
* 数列的项可重复、次序确定。
* 虽然与集合同样用"{}"表示，但二者不同。

定义 极限（lim） 收敛 发散
   > 数列极限：ε-N 语言
   > 函数极限：ε-δ 语言 这两种语言是数学系的基本功

定义 无穷小量：以0为极限的变量（数列）为无穷小量。

定义 邻域
   > 数列收敛与否，与前有限项无关
   > 以 0 为极限的变量称为无穷小量
   > 例 2.1.6

* 需证明例2.2.1，以掌握：ε-N语言，放大技巧 
* 证明数列极限时使用放大技巧（只要得到N，则无所谓其大小）

* 需证明例2.2.6 只能定义证明

数列极限的性质

定理 2.2.1 **唯一性**：极限若存在，则唯一

定义： 有界数列

定理 2.2.2 **有界性**：收敛数列必定有界

> 数列若既有上界，又有下界，则称有界

定理 2.2.3 保序性：
      1. 逆命题 a<=b
      2. 推论 1：鞋履
      3. 推论 2：

定理 2.2.4 夹逼性定理：

> 夹逼性定理用于求某一不能直接求极限的数列。构造两个易求极限的数列，然后此两数列极限相等。

需证例 2.2.8

数列极限的四则运算

**证明技巧**
1. 证明极限：放大
2. 求极限：四则运算一下？构造俩极限夹逼一下？构造一个保序性推论，然后带入以放大？
3. 四则运算只能推广到**有限个**数列，**不能**随意推到**无限个**或**不定个数个**数列上去。

### 2.3 无穷大量

> 随着n的增加，数列的绝对值不断增加，称为无穷大量。

定义 2.3.1 若对于人以给定的 G > 0，可以找到正整数N，使得的那个n > N时，成立：
$$ \left | x_n\right | > G $$
，则 $$ {x_n} $$ 是无穷大量，记为： $$ \displaystyle \lim_{n \to \infty} x_n = \infty  $$  。

> 正无穷大量，负无穷大量

定理 2.3.1 设 $$ x_n \neq 0 $$ ，则 $$ \{x_n\} $$ 是无穷大量的充要条件是 $$ \{\frac{1}{x_n}\} $$ 是无穷小量.

> 无穷大量与无穷小量是倒数关系。

定理 2.3.2  设 $$ \{x_n\} $$ 是无穷大量，  $$ \{y_n\} $$ 满足： $$ \exist N_0, \forall n > N $$ ，有
$$ \| y_n \geq \delta > 0
$$
，则 $$ \{ x_n y_n \} $$ 也是无穷大量。

推论：(需要证明)

定义 2.3.2 **待定型**

定义 2.3.3 **单调增加数列** **严格单调增加数列** **单调减少数列** **严格单调减少数列**

定理 2.3.3 **Stolz 定理** 设  $$ \{y_n\} $$  是严格单调增加数列，且 $$ 是正无穷大量 $$ 。若  $$  $$ ，a是有限数，或正无穷大，负无穷大（不包括不定号无穷大），则  $$ x_n \over y_n 的极限是 a $$ 。

需证明

> Stolz 定理可以用来求极限，求那些直接四则运算不能算的极限。但注意“y_n 得是严格单调增加数列”这个条件。

证明技巧：有通项公式，求极限：造出上下两个数列，下数列是严格单调递增的无穷大量。构造stolz定理，代入上下数列的通项，然后四则运算

### 2.4 收敛准则

> 收敛数列有界，有界数列不一定收敛。那么：<br>
> 有界数列加上什么条件可以保证收敛？（加上单调性）<br>
> 有界数列不加其他条件，可以得到什么弱一些的结论？

定理 2.4.1 单调有界数列必定收敛。

需证明
> 定理 2.4.1 的意义：使我们可以从数列本身的性质，去研究其敛散性。（用定义证明收敛，则必须事先知道极限具体为何，这往往并不现实）

定义 递推公式

需证 例2.4.2（

证明技巧：有递推公式，不知极限，求证有极限，并求极限：
* 应用定理2.4.1，先证有界，再证单调。
* 证明有界，用数学归纳法，带入通项公式；
* 证明单调，用任意前后项相减，带入递推公式 $$ x_{n+1} - x_n  $$ ，求得其必定为正或为负。 
* 再假设a为其极限，在递推公式两边同时求极限，带入a，四则运算，求得a。

例 2.4.4 **Fibonacci数列**与兔群的自然增长率

**π 和 e**

> 曲线长度的定义：对其进行分段得到的折线长度的极限值（而不是拉直）。

为圆内接正n边形，单位圆正多边形的周长为： $$ 2n \sin{\frac{180°}{n}}  $$ 。

证明单位圆面积为pi，需证例2.4.5

欧拉常数，需证例2.4.8

定理 闭区间套定理

## 第三章 函数极限与连续函数

### 3.1 函数极限

### 3.2 连续函数

### 3.3 无穷小量与无穷大量的阶

### 3.4 闭区间上的连续函数

## 第四章 微分

### 4.1 微分和导数

### 4.2 导数的意义和性质

### 4.3 倒数的四则运算和反函数求导法则

### 4.4 复合函数求导法则及其应用

### 4.5 高阶导数和高阶微分

## 第五章 微分中值定理及其应用

### 5.1 微分中值定理

### 5.2 L'Hospital 法则

### 5.3 Taylor公式和插值多项式

### 5.4 函数的Taylor公式及其应用

### 5.5 应用举例

### 5.6 方程的近似求解

## 第六章 不定积分

### 6.1 不定积分的概念和运算法则

### 6.2 换元积分法和分部积分法

### 6.3 有理函数的不定积分及其应用

## 第七章 定积分

### 7.1 定积分的概念和可积条件

### 7.2 定积分的基本性质

### 7.3 微积分的基本定理

### 7.4 定积分在几何计算中的应用

### 7.5 微积分实际应用距离

### 7.6 定积分的数值计算

## 第八章 反常积分

### 8.1 反常积分的概念和计算

### 8.2 反常积分的收敛判别法

## 第九章 数项级数

### 9.1 数项级数的收敛性

### 9.2 上极限与下极限

### 9.3 正项级数

### 9.4 任意项级数

### 9.5 无穷乘积

## 第十章 函数项级数

### 10.1 函数项级数的一致收敛性

### 10.2 一致收敛级数的判别与性质

### 10.3 幂级数

### 10.4 函数的幂级数展开

### 10.5 用多项式逼近连续函数

## 第十一章 Euclid空间上的极限和连续

### 11.1 Euclid空间上的基本定理

### 11.2 多元连续函数

### 11.3 连续函数的性质

## 第十二章 多元函数的微分学

### 12.1 偏导数与全微分

### 12.2 多元复合函数的求导法则

### 12.3 中值定理和Taylor公式

### 12.4 隐函数

### 12.5 偏导数在几何中的应用

### 12.6 无条件极值

### 12.7 条件极值与Lagrange乘数法

## 第十三章 重积分

### 13.1 有界闭区域上的重积分

### 13.2 重积分的性质与计算

### 13.3 重积分的变量代换

### 13.4 反常重积分

### 13.5 微分形式

## 第十四章 曲线积分、曲面积分与场论

### 14.1 第一类曲线积分与第一类曲面积分

### 14.2 第二类曲线积分与第二类曲面积分

### 14.3 Green公式、Gauss公式和Stokes公式

### 14.4 微分形式的外微分

### 14.5 场论初步

## 第十五章 含参变量积分

### 15.1 含参变量的常义积分

### 15.2 含参变量的反常积分

### 15.3 Euler积分

## 第十六章 Fourier级数

### 16.1 函数的Fourier级数展开

### 16.2 Fourier级数的收敛判别法

### 16.3 Fourier级数的性质

### 16.4 Fourier变换和Fourier积分

### 16.5 快速Fourier变换



## 参考资料

课程视频：陈纪修：https://www.bilibili.com/video/BV12s411h7v4

讲义：《数学分析讲义》陈天权；《数学分析》陈纪修
