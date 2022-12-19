# 部分课后习题与课本习题答案，欢迎补充纠错
## 第一章


<u>课本习题</u>


### 例 1.26
> 求 1000! 中从右到左位数连续为 0 的数的个数。(末尾有几个 0)

0 只能由 2 和 5 相乘得到，对各个数字进行因数分解后 2
的个数明显大于 5 的个数，故只要统计因数是 5 的倍数的个数。

5 的 1 次幂 5 的倍数增加 1 个 0 (5,10,15,20,25,30,\.....)

5 的 2 次幂 25 的倍数增加 2 个 0(必然是 5 的倍数)(25,50,75,100,125\.....)

5 的 3 次幂 125 的倍数增加 3 个 0(必然是 25 的倍数)(125,250,375,500\.....)

5 的 4 次幂 625 的倍数增加 4 个 0(必然是 125 的倍数)(625,1250,1875,2500\.....)

所以先求出 5 的倍数

加上 25 的倍数 (2 个 0, 其中 1 个已记入 5 的倍数)

加上 125 的倍数 (3 个 0, 其中 1 个已记入 5 的倍数 1 个已记入 25 的倍数)

加上 625 的倍数 (4 个 0, 其中 \...\...\...\...\...\...\...\...\...\...\...\...) 的个数。

1000/5=200
(1000 里面含有 200 个 5 的倍数，但同时也包含了 25 倍数，125 的倍数，625 的倍数各一次)

1000/25=40(1000 里面含有 40 个 25 的倍数，同时也含有 125 的倍数，625 的倍数各一次)

1000/125=8(1000 里面含有 8 个 125 的倍数，同时也含有 625 的倍数)

1000/625=1（1000 里含有 1 个 625 的倍数）

所以 1000！里面含 有 0 的个数为 200+40+8+1=249 个


<u>课后作业</u>


### 1.2

> 5 个女生，7 个男生进行排列，

1. $$
   5!\times 8!
   $$

2. $$
   7!\times C_8^5 \times 5!
   $$

3. $$
   C_5^3 \times 3 ! \times 2 \times 7!
   $$

   

### 1.3

1. $$
   n! \times C_{n+1}^m\times m!
   $$

2. $$
   n! \times (m+1)!
   $$

3. $$
   2 \times (m+n-1)!
   $$

   

### 1.4
> 26 个英文字母进行排列, 求 x 和 y 之间有 5 个字母的排列数.

$$
{(26-7)}!\times C_{(26-2)}^5 \times 5! \times 2
$$



### 1.5
> 求 3000 到 8000 之间的奇整数的数目, 而且没有相同的数字.

1. 首位是奇数，$1\times8\times7\times4$(去除首位奇数)

2. 首位是偶数，$1\times8\times7\times5$

   相加得：$1\times8\times7\times(4\times3+5\times2)=1232$

### 1.8
> 求 10 的 40 次方和 20 的 30 次方的公因数.

首先求二者的最大公因数：$10^{40}=(2\times5)^{40}=2^{40}\times5^{40},20^{30}=(2\times2\times5)^{30}=2^{60}\times5^{30}$
则最大公因数为：$2^{40}\times5^{30}$.
因为所有公因数都是最大公因数的因数，那么由最大公因数可以求得所有公因数的数目.$2^{40}$
有 $41$ 种取法 $(2^0, 2^1, 2^2,\cdots,2^{40})$，相应的，$5^{30}$ 有 $31$
种取法，那么公因数的总数目为 $41\times31=1271$ 种.

### 1.15
> 试求从 1 到 1000000 的整数中, 0 出现的次数.

先分别考虑每个位数情况，然后统计每类 0 以 1，2，3\.... 位数出现的次数

1 位 $\cdots 0 .$

2 位 $\cdots  9  .$

3 位 $\cdots  2 \times 9 + 9 \times 9 \times 2 = 180 .$

4 位 $\cdots 3 \times 9 + 9 \times 9 \times 3 \times 2 + 9 \times 9 \times 9 \times 3 = 2700.$

5 位 $\cdots 4 \times 9 + 9 \times 9 \times 4 \times 3 + 9 \times 9 \times 9 \times 6 \times 2 + 9 \times 9 \times 9 \times 9 \times 4 = 36000 .$

6 位 $\cdots$ $9 \times9^4\times5\times1+9\times9^3\times10\times2+9\times9^2\times10\times3+9\times9\times5\times4+9\times5=450000.$

7 位 $\cdots 6.$

共计 $\cdots 488895$

### 1.18
> 8 个盒子排成一列, 5 个有标志的球放到盒子中，每盒最多放一个球，要求空盒不相邻, 问有多少种排列方案?

参考 $P21$ 定理 1-3：从 $n$ 个数中选取 $r$ 个不相邻的数的组合数是：$C_{n-r+1}^r$.

本题中 $n= 8,r=3$​，则结果是：
$$
C_6^3\times5!=2400
$$
或者使用整体减掉相邻的情况
$$
(C_8^3 - 2\times5 - 5\times4 - 6)\times5!=2400
$$


### 1.19
> n+m 位由 m 个 0，n 个 1 组成的符号串，其中 n <= m + 1, 试问不存在两个 1 相邻的符号串的数目.

参考 $P21$ 定理 1-3. 答案是：
$$C_{m+1}^n$$

### 1.20

$$
C_4^2 \times C_{10}^2 \times C_{15}^3+ C_4^1 \times C_{10}^3 \times C_{15}^2 \times C_{10}^1+C_4^0  \times C_{10}^4 \times C_{15}^1 \times C_{10}^2
$$

### 1.22

1. $$
   C_5^3\times C_8^3
   $$

   

2. $$
   C_5^3\times C_7^3
   $$

   

3. $$
   C_5^3\times C_4^1 \times C_8^3
   $$

   

4. $$
   C_{13}^5 - C_5^3 \times C_8^3
   $$

   

### 1.27

1. $$
   5! \times C_6^5 \times 5!
   $$

2. $$
   5! \times 6 \times 5!
   $$

3. $$
   A_6^2 \times 8!
   $$

### 1.32

> 在 a,b,c,d,e,f,x,x,x,y,y 的排列中, 要求 y 必须夹在两个 x 之间, 问这样的排列数等于多少?

$xyxyx$ 视作整体参加排列。答案是：$7!$

### 1.34
> 在 r,s,t,u,v,w,x,y,z 的排列中求 y 居于 x 和 z 中间的排列数.

$xyz$ 相邻，且 $x$ 和 $z$ 可以调换位置。答案是：$2\times 7!$

### 1.43

$$
\frac{C_n^k}{C_n^{k-1}}=\frac{n-k+1}{k}\geq1,\frac{C_n^k}{C_n^{k+1}}=\frac{k+1}{n-k}\geq 1
$$

 

$$
k\leq \frac{n+1}{2}, k\geq \frac{n-1}{2}
$$


### 1.50

#### 1.50.1

> 注意到：我们可以把字符串中连续的 0 用 1 个 0 替换而不改变 N01 和 N10 的个数（N01 和 N10 分别表示字符串中 01 的个数和 10 的个数），同理也可以把字符串中连续的 1 用 1 个 1 替换，为叙述方便，称得到的为原字符串的 “模式”

比如，10100011 的模式是 10101

下面考虑有几种可能的模式呢？

思路：我们考虑 1 的可能位置，如果 1 在左端，则对 N10 的贡献为 1；若在右端，则对 N01 的贡献为 1；若在中间（非端点），则对 N10 和 N01 的贡献各为 1，总贡献为 2

01 或 10 出现次数为 4，那么 0 在模式中出现的情况有以下几种可能：

1. 中间没有 0——这不可能，因为即使两端都出现 0，01 或 10 出现总次数也只有 2
2. 中间有 1 个 0——这 1 个 0 对 N 的贡献为 2，那么两端必然都必须为 0，这样才会有 N=4。模式为 $01010$
3. 中间有 2 个 0——这 2 个 0 对 N 的贡献为 4，两端必然都必须为 1，模式为 10101
4. 中间有超过 2 个 0——这不可能

总结起来只有两种可能的模式：01010 和 10101

先考虑 01010：

1. 选择 5 个 0 产生的四个空位放入 2 个 1: $C_4^2$
2. 将剩余的 1 放到已经安置好的 1 的附近（因为剩余的 1 不能再对 N 有贡献），那么已经安置好了 2 个 1，剩余 2 个 1，按照 $p_{20}$ 定理 $1-2$ ，所有可能的组合是 $C_{2+2-1}^2=C_3^2=3$
3. 结合 1,2. 可得结果：
   $$
   C_4^2 \times C_3^2
   $$


接着讨论 10101：

1. 首位各有 1 个 1，对总数 $N$ 贡献为 2，再在 5 个 0 产生的 4 个空位放入 1 个 1 即可：$C_4^1$
2. 安置剩下的 1 个 1，可以任意放到已经安置好的 3 个 1 的” 附近 “，共：$C_3^1$
3. 最后结果
   $$
   C_4^2 \times C_3^2
   $$

结合以上两种情况，可得总数：
$$
C_4^2 \times C_3^2 + C_4^1 \times C_3^1 = 30
$$

#### 1.50.2

k 为偶数时，可能的模式有两个：

一个是 $010…010$

1. 选择 $\dfrac{k}{2}$ 个 1 放入 m 个 0 产生的 m-1 个空位中：$C_{m-1}^{k/2}$
2. 安置剩余的 1，已经安置好的： $\dfrac{k}{2}$，剩余的总数为   $n-\dfrac{k}{2}$，则按照 定理 $1-2$ 总组合数：$C_{n-1}^{k/2}$
3. 总数：
$$
C_{m-1}^{k/2} \times C_{n-1}^{k/2-1}
$$

另一个是 $1010…01$，

1. 首尾各有 1 个 1，只要选择 $\dfrac{k-2}{2}=\dfrac{k}{2}-1$ 个 1 放入 0 产生的空位中：$C_{m-1}^{k/2-1}$
2. 安置剩余的 1，已经安置好的总数：$\dfrac{k}{2}-1 + 2=\dfrac{k}{2}+1$，剩余未安置 $n-(\dfrac{k}{2}+1)$：那么可能的组合数是：$C_{n-1}^{k/2}$
3. 总数
$$
C_{m-1}^{k/2-1}\times C_{n-1}^{k/2}
$$

总的符合要求的字符串数为
$$
C_{m-1}^{k/2-1}\times C_{n-1}^{k/2}+ C_{m-1}^{k/2-1}\times C_{n-1}^{k/2}
$$
k 为奇数时，可能的模式也有两个：

一个是 $010…01$
$$
C_{m-1}^{(k-1)/2}\times C_{n-1}^{(k-1)/2}
$$
另一个是 $10…010$，符合要求的也相同。

总的符合要求的字符串数为
$$
2 \times C_{m-1}^{(k-1)/2}\times C_{n-1}^{(k-1)/2}
$$

## 第三章

### 汉诺塔通项

$$
H(k)=2H(k-1)+1,H(k)+1=2(H(k-1)+1)
$$



${H(k)+1}$ 是首项为 $H(1)=1$，公比为 2 的等比数列，求得 $H(k)+1 = 2^k$，所以
$$
H(k) = 2^k-1
$$

### 3.41
> 从 26 个英文字母中抽 35 次, 求出现 MERRYCHRISTMAS 的几率.

MERRYCHRISTMAS 长度为 14.
$$
\frac{C_{22}^1\times 26^{21} - C_9^2 \times 26^7}{26^{35}}
$$
I will assume that the draws are done with a uniform distribution, where every letter is equally likely to be selected.

Therefore, we need to count the number of ways of getting the substring MERRYCHRISTMAS and divide by the total number of possible strings.

The string MERRYCHRISTMAS has $14$ characters in it.

To simplify the problem, think about this: to have MERRYCHRISTMAS somewhere in the string, that means you have MERRYCHRISTMAS as characters 1–14, or as characters 2–15, or as characters 3–16, etc… as characters 22–35.

That means the numerator will be the number of ways of getting the union of those 22 sets.

If we had MERRYCHRISTMAS as characters 1–14, that means there is only 1 option for the first 14 characters, but every character after the 14th will have all 26 options. Therefore, the number of ways of having it in characters 1–14 is $1\times26^{21}$. Using the same reasoning, we can determine the number of ways of doing it in the other 22 cases is the same.

Now we need to take the union of all of those counts. However, you may see there is a problem here. It is possible to get 2 of those sets at the same time. For example, it is possible to get MERRYCHRISTMAS as characters 1–14 AND characters 15–28. Those are double counted, because we will count it once in our counts of 1–14, and we will count it again in our counts of 15–28. Therefore, we must subtract how many ways there are to get MERRYCHRISTMAS twice.

First, I will consider the possible positions for those 2 substrings. Each substring is a length of 14, which is essentially 1 unit because they are all together. Therefore, we have 2 units composed of the 2 blocks of MERRYCHRISTMAS, then we are left with 7 other characters. Therefore, there are 9 units to place in order, the 2 big blocks, and the 7 remaining characters. Out of those 9 units, the number of ways of choosing which 2 are the MERRYCHRISTMAS blocks is $C_9^2$. Again there is only 1 way to choose the letters MERRYCHRISTMAS, but for the remaining 7 characters there are 26 ways to choose each of them. Therefore, the number of ways of getting MERRYCHRISTMAS twice would be:

$C_9^226^7$

That means the union ends up being:

$22⋅26^{21}−C_9^226^7$

We have to divide that by the total number of ways of choosing the 35 characters:

$\dfrac{22⋅26^{21}−C_9^226^7}{26^{35}}$

### 3.46

> 任给5个整数，试证其中必然存在3个数的和被3除尽。

整数除以3的余数有0，1，2三种可能，那么所有的整数可以划分为3 个同余类。

若存在三个数属于同一类的，符合条件。

若不存在，则必然有2个数属于其中一类，2个数属于另一类，1个数属于另一类。

三个之间都去一个$0+1+2=3mod3=0$，符合条件。

### 3.47&#x20;

> A 是 n+1个数的集合，试证其中必存在两个数，它们的差被 n除尽

构造序列$S_1=a_2-a_1,S_2=a_3-a_2,\cdots,S_n=a_{n+1}-a_n$

1.  若$\{S_n\}$中有符合条件的，那么已符合题意。
2.  若不存在，因为$\{S_n\}$中所有的数都不是n的倍数，那么必然有两个数对n取余结果相同。不妨设为$S_i,S_j$，设

$$
S_i=a_{i+1}-a_1=cn+r\\
 S_j=a_{j+1}-a_1=dn+r\\
 
$$

则$S_i-S_j=a_{i+1}-a_{j+1}=(c-d)n$，符合题意。

### 3.50

> A 是$\{1,2,\cdots,2n\}$中任意$n+1$个数，试证明至少存在一对 $a,b$ 属于 $A$，其中$a$与$b$互素。

构造$\{1,2\},\{3,4\},\cdots,\{2n-1,2n\}$共$n$个抽屉，则取$n+1$个数至少有两个数取至同一个抽屉，而相邻两个自然数一定互素，证毕。

### 3.55&#x20;

> 令$A$为等差数列$1,4,7,10,\cdots,100$中选$20$个不同的数，试证其中至少存在两个数，它们的和为$104$

$$
104=100+4=97+7=\cdots=55+49
$$

总共有16对符合条件的数，从 A 中任取 20 个数，除去 1 和 52，从余下的 16 对数中取 18 个，根据鸽巢原理，其中至少存在一对数的和为 104.

### 3.67

> 任意给出7个正整数，必有两个数，它们之和或差是10的倍数。

证明：将$0, 1, 2\cdots,9$分成$[0], [5], [1, 9], [2, 8], [3, 7], [4, 6]$六个抽屉，对于给定的$7$个正整数，按其末位放进上面六个抽屉，则必有两个整数属于同一抽屉，它们的和或差必是$10$的倍数。





