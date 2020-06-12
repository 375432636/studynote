# 第一章

## 3. 极限的定义

## 4. 求极限的方法

### 4.1 直接带入

1. 适用条件

x趋近于某个定值, 条件不为无穷大和无穷小的时候

2. 使用方法

把趋近于的值带入到函数之中, 得到的值为该条件下函数的极限

### 4.2 法则

1. 内容
   1. 两个函数**和差的极限**就是这两个函数**极限的和差**
   2. 两个函数**乘积的极限**就是这两个函数**极限的乘积**
   3. 两个函数**商的极限**就是这两个函数**极限的商**
4. 函数前面的系数可以移动到极限的前面
   
   $$
   \lim_{x\to0}\frac{\sin 4x}{2x}=2\lim_{x\to0}\frac{\sin4x}{4x}
   $$
   
   
   
2. 使用方法

通常来说是接替步骤, 不是解题方法

### 4.3 无穷小和无穷大的性质

#### 1. 无穷小和无穷大的定义

无穷小: 在自变量的某个变化过程中, 极限为0的函数称为无穷小量

无穷大: 在自变量的某个变化过程中, 极限为无穷大的函数成为无穷大
$$
\because \lim_{x\to+\infty}\frac{1}{x}=0,
\therefore f(\frac{1}{x})是无穷小\\
\because \lim_{x\to0}\frac{1}{x}=+\infty, 
\therefore f(\frac{1}{x})是无穷大
$$

* 注意
  * 无穷小和无穷大不是一个数, 而是一个函数在某个条件下的变化趋势
  * 无穷小和无穷大一定要指明条件
  * 只有常数0是
$$
lim_{x\to0}f(0)=0
$$
#### 2. 性质

- 无穷小与无穷大的关系: 无穷小和无穷大互为倒数
- 无穷小量的性质: 无穷小量与有界量的乘积是无穷小量, 记住四个有界函数就好`sin(x), cos(x), arctan(x), arccot(x)`

$$
利用倒数求极限\\
lim_{x\to2}\frac{1}{x-2}=+\infty\\
\because lim_{x\to2}(x-2)=0\\
\therefore lim_{x\to2}\frac{1}{x-2}=+\infty
$$
#### 例题3: 

[视频连接](https://youtu.be/5giYv5n616E?t=2668)
$$
求\lim_{x\to\infty}\frac{\sin x}{x}\\
\because \lim_{x\to\infty}\frac{\sin x}{x}=\lim_{x\to\infty}\frac{1}{x}\sin x\\
\therefore \lim_{x\to\infty}\frac{1}{x}=0 \\
而当x\to\infty, \frac{1}{x}是无穷小量 \\
\sin x是有界函数\\
\therefore \lim_{x\to\infty}\frac{\sin x}{x}=0
$$
思路: 

1. 不可以直接带入, 条件为无穷
2. 法则用不了, 拆分为`sinx` and `x`, 其中`sinx`条件下没有极限
3. 可以将其看作`sinx` and `1/x`的乘积
4. 两个条件一定要说清楚, 哪个是无穷小量, 哪个是有界函数

#### 例题4:

$$
求极限 \lim_{x\to2}(x-2)\sin\frac{1}{x-2}\\
\because \lim_{x\to2}(x-2)=0\\
\therefore x-2在x\to2是无穷小\\
\because \sin\frac{1}{x-2}是有界函数\\
\therefore \lim_{x\to2}(x-2)\sin\frac{1}{x-2}=0
$$

思路:

1. 不可以直接带入, x-2=0, 其中一项不成立都不能带入. 0x一个没有意义的数不一定是0
2. 法则也不可, 因为sin(1/x-2)是没有极限的. 
3. sin(1/x-2)是有界函数

### 4.4 三种特例

#### 1. 通过因式分解

#### 例题5:

$$
\lim_{x\to1}\frac{x-1}{x^2-1}\\
原式 = \lim_{x\to1}\frac{x-1}{x^2-1}=\lim_{x\to1}\frac{x-1}{(x-1)(x+1)}\\
=\lim_{x\to1}\frac{1}{1+x}=\frac{1}{2}
$$

思路:

1. 不能直接带入
2. 无穷小和无穷大的倒数关系也不能用
3. 也存在有界函数

#### 2. 通过分子或分母有理化

$$
计算 \lim_{x\to4}\frac{x-4}{\sqrt{x+5}-3}\\
\begin{eqnarray}
&\lim_{x\to4}\frac{x-4}{\sqrt{x+5}-3}&=\lim_{x\to4}\frac{(x-4)(\sqrt{x+5}+3)}{(\sqrt{x+5}-3)(\sqrt{x+5}+3)}&\\
&&=\lim_{x\to4}\frac{(x-4)(\sqrt{x+5}+3)}{x-4}\\
&&=\lim_{x\to4}\sqrt{x+5}+3\\
&&=6
\end{eqnarray}
$$

思路:

1. 不能带入, 带入后分母为0
2. 无穷小和无穷大的倒数不能用, 倒数带入分母为0
3. 无穷小和有界函数的性质不能用, 没有有界函数
4. 因式分解也是可以的, 麻烦一点

$$
\begin{eqnarray}
&\because &\frac{x-4}{\sqrt{x+5}-3}\\
& &=\frac{x+5-9}{\sqrt{x+5}-3}\\
& &=\frac{(\sqrt{x+5})^2-3^2}{\sqrt{x+5}-3}\\
& &=\frac{(\sqrt{x+5}-3)(\sqrt{x+5}+3)}{\sqrt{x+5}-3}\\
& &=\sqrt{x+5}+3\\
&\therefore &\lim_{x\to4}\frac{x-4}{\sqrt{x+5}-3}=\lim_{x\to4}\sqrt{x+5}+3=6
\end{eqnarray}
$$

#### 3. 分子, 分母同时除以指数最高项

使用条件: 

1. x --> ∞
2. 有理分式

情况1, 分子分母指数最高项指数是一样的.则结果是最高项系数之比
情况2, 分子指数最高项次数比分母指数最高项次数小, 结果为0
情况3, 分子指数最高项次数比分母指数最高项次数达, 结果为∞
$$
\begin{eqnarray}
&&情况1&\lim_{x\to\infty}\frac{2x^3+3x^2+5}{7x^3+4x^2-1}&=\frac{2}{7}\\
&&情况2&\lim_{x\to\infty}\frac{3x^2+5}{7x^3+4x^2-1}&=0\\
&&情况3&\lim_{x\to\infty}\frac{2x^3+3x^2+5}{4x^2-1}&=\infty\\
\end{eqnarray}
$$


### 4.5 两个重要极限

#### 1. 第一个重要极限

$$
\lim_{u(x)\to0}\frac{\sin u(x)}{u(x)} =1
$$



第一个重要极限可以解决的, 用洛必达法则也可以解决, 只是难易程度上会有区别

注意: 

1. 三统一原则
2. u(x) 要趋近于0

#### 例题8:

$$
求\lim_{x\to0}\frac{\sin 4x}{2x}\\
$$



第一重要极限解法
$$
\begin{eqnarray}

&&\lim_{x\to0}\frac{\sin4x}{2x}=2\lim_{x\to0}\frac{\sin4x}{4x}=2\\
&&当x\to0是, 存在4x\to0\\

\end{eqnarray}
$$
洛必达法则解法
$$
\begin{eqnarray}

&&\lim_{x\to0}\frac{\sin4x}{2x}=2\lim_{x\to0}\frac{4\cos4x}{2}=2\\

\end{eqnarray}
$$


思路:

1. 不能直接带入, 分母为0
2. 不能用法则
3. 无穷小量和有界函数, 没法做, 1/2x 是无穷大
4. 三种特例, 不需要因式分解, 不含根号不能有理化, 不是趋近于无穷大不能使用有理分式
5. 利用法则进行分解, **乘积的极限等于极限的乘积**, 函数体\*2 = 极限\*2

#### 例题9:

[视频连接](https://youtu.be/5giYv5n616E?t=4919)
$$
求\lim_{x\to0}\frac{\tan2x}{x}
$$

$$
\begin{eqnarray}
&\lim_{x\to0}\frac{\tan2x}{x}&=\lim_{x\to0}\frac{sin2x}{x}\cdot\frac{1}{\cos2x}\\
&&=2\lim_{x\to0}\frac{\sin2x}{2x}\cdot\frac{1}{\cos2x}\\
&&=2
\end{eqnarray}
$$

#### 例题10:

[视频连接]([https://youtu.be/5giYv5n616E?t=5189)
$$
求\lim_{x\to0}\frac{\sin^2x}{x}
$$

$$
\begin{eqnarray}
&\lim_{x\to0}\frac{\sin^2x}{x}&=\lim_{x\to0}\frac{\sin x}{x}\cdot\lim_{x\to0}\sin x\\
&&=1\cdot0\\
&&=0
\end{eqnarray}
$$

思路:

1. 利用法则, **乘积的极限等于极限的乘积**, 
2. 利用第一个重要极限求第一个极限, 利用带入法求第二个极限

#### 2. 第二种重要极限

$$
\lim_{}(1+\frac{1}{A})^B=e
$$

条件:

1. 函数一定是1+
2. (1/A)*B = 1, 即A与B互为倒数

#### 例题11:

[视频连接](https://youtu.be/5giYv5n616E?t=5583)
$$
求\lim_{x\to\infty}(1-\frac{2}{x})^x
$$

$$
\begin{eqnarray}
&&\lim_{x\to\infty}(1-\frac{2}{x})^x\\
&=&\lim_{x\to\infty}(1+\frac{-2}{x})^2\\
&=&[\lim_{x\to\infty}(1+\frac{-2}{x})^{-\frac{x}{2}}]^{-2}\\
&=&e^{-2}
\end{eqnarray}
$$



### 4.6 等价无穷小的替换

### 4.7 洛必达法则

























∞





























