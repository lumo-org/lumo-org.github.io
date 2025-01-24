---
title: "浅谈不等式问题"
date: 2025-01-24
author: GGapa
tag: "Math"
category: "Study"
---

$$\frac{2}{\frac{1}{a}+\frac{1}{b}} \le \sqrt{ab} \le \frac{a+b}{2} \le \sqrt{\frac{a^2+b^2}{2}}$$

# ${ \mathrm{Example\enspace 1}} $

##### 问题描述

已知 $x >0, y > 0$ 且 $2x + 8y - xy = 0$ 求 $x + y$ 的最小值

##### 分析与解答

通过`1的代换`来解决问题

考虑将 $2x + 8y - xy = 0$ 化简可得：

$2x + 8y = xy$ 两边同乘 $\frac{1}{xy}$ 可得：

$ \frac{2}{y} + \frac{2}{x} =1 $

$ \because x+y=(x+y)\cdot 1 $

$\therefore (x+y)=(x+y)(\frac{8}{x}+\frac{2}{y} )=\frac{2x}{y} +\frac{8y}{x} +10$

$\because x>0,y>0 $

$\therefore \frac{2x}{y} +\frac{8y}{x} \ge2\sqrt[]{16} $

当且仅当 $x = 6, y = 12$ 时 $(\frac{2x}{y} +\frac{8y}{x})\_{min}=8$

此时 $(x+y)\_{min}=18$

# ${ \mathrm{Example\enspace 2}} $

##### 问题描述

已知 $x，y> 0,x+2y+xy-6=0$，解决下列问题： 1. 求 $xy$ 的最大值 2. $x+2y$的最小值 3. $x+y$ 的最小值 4. $(x+2)^2+(y+1)^2$的最小值

##### 分析与解答

$ \mathrm{{\Large 第一问} } $

第一问可以使用基本不等式可将 $x+2y\Rightarrow \sqrt{2xy}$ 然后进行因式分解：

$\because x+2y \ge \sqrt{2xy},x+2y+xy-6=0$

$\therefore 2\sqrt{2xy}+xy-6 \le 0$

$\because x,y>0$

$\therefore (\sqrt[]{xy} )^2+2\sqrt[]{2xy} -6\le 0$

$=(\sqrt[]{xy} )^2+2\sqrt[]{2} \sqrt[]{xy} -6\le 0$

若将上面的不等式中的 $\sqrt{xy}$ 看成一个整体，可得一个一元二次不等式，可解得：

$0 < \sqrt[]{xy} \le\sqrt[]{2} $

$0 \le {xy} \le 2$

$\therefore xy\_{max}=2$

- - - - - -

$ \mathrm{{\Large 第二问} } $

由第一问可得 $xy\_{max}=2$

$\because x+2y=6-xy$

$ \therefore (x+2y)\_{max}=6-xy\_{min} = 6-2=4$

- - - - - -

$ \mathrm{{\Large 第三问} } $

$\because x+2y+xy-6=0$

$\therefore 2y+xy=6-x \Rightarrow y(2+x)=(6-x) \Rightarrow y=\frac{6-x}{2+x} $

$\therefore x+y=x+\frac{6-x}{2+x}=x-\frac{2+x-8}{2+x} =x-1+\frac{8}{x+2} =x+2+\frac{8}{x+2} -3$

$\because x > 0$

$\therefore x+2+\frac{8}{x+2} \ge 2\sqrt[]{8}$ 当且仅当 $x+2=\frac{8}{x+2}=\sqrt{8}$ 时，等号成立，此时 $x=\sqrt{8}-2$

$\therefore (x+y)\_{min}= (x+2+\frac{8}{x+2})\_{min}-3=4\sqrt[]{2} -3$

- - - - - -

$ \mathrm{{\Large 第四问} } $

**步骤可能可以简化*

由第三问可知 $y=\frac{6-x}{2+x}, x+2+\frac{8}{x+2} \ge 2\sqrt[]{8}$

$\therefore (x+2)^2+(y+1)=(x+2)^2+(\frac{6-x}{2+x}+1)=(x+2)^2+(\frac{8}{2+x})^2=(x+2)^2+\frac{8^2}{(2+x)^2}$

$\because \frac{8^2}{(2+x)^2},(x+2)^2\ge 0$

$\therefore (x+2)^2+\frac{8^2}{(2+x)^2}\ge 2\sqrt[]{8^2} =16$ 当且仅当 $ (x+2)^2=\frac{8^2}{(2+x)^2}=8$ 时成立 此时 $x=\sqrt{8}-2$

$\therefore [(x+2)^2+(y+1)^2]\_{min}=16$

##### 总结

此题乍看可以使`1的代换`但深究发现因为有常数的存在而不能使用。此题利用了**整体思想/换元法**和**消元法**。
- 若发现分母较为复杂可使用**整体思想/换元法**
- 通过**因式分解**将多个未知数化简为一个未知数或许能方便运算 
- 分子上有未知数时一定要设法删除 
- 注意符号的改变