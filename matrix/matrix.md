### 矩阵和空间的关系（1）

已知矩阵 A 和 向量 b：

![alt text](https://raw.githubusercontent.com/satoxi/satoxi.github.io/master/matrix/matrix_1.png "Fig.1")

如何计算 Ab 的乘积？比较普遍的计算方式，是使用 A 的每个行向量与 b 做点积运算，得出：

![alt text](https://raw.githubusercontent.com/satoxi/satoxi.github.io/master/matrix/matrix_2.png "Fig.2")

不过今天要说的，是另一种计算方式：**从矩阵 A 的列向量出发求解**。

如果把矩阵 A 的列向量看做从世界原点出发的一个方向，那么，向量 b 中的每一个元素就表示，沿着某一个方向我们会走多远[1]。

上面的例子中，矩阵 A 定义了从世界原点出发的两个方向，(1, 0) 和 (0, 1)，向量 b 则表示，沿着 (1, 0) 方向走了 b1 的距离，同时沿着 (0, 1) 方向 走了 b2 的距离，也就是：

![alt text](https://raw.githubusercontent.com/satoxi/satoxi.github.io/master/matrix/matrix_3.png "Fig.3")

现在，我们来看一下平面直角坐标系：

![alt text](https://raw.githubusercontent.com/satoxi/satoxi.github.io/master/matrix/matrix_4.png "Fig.4")

可以发现，**矩阵 A 的列向量定义的两个方向刚好分别与坐标系的 x 轴和 y 轴方向重合**，也就是说，矩阵 A 定义了这个平面直角坐标系，或者说定义了一个**二维空间**。

在坐标系中找到一个点 (b1, b2)，b1 和 b2 分别是这个点在 x 轴和 y 轴上的取值。形象的说，**就是在坐标系中，沿着 x 轴走了 b1 的距离，同时沿着 y 轴走了 b2 的距离，最终到达了这个点，这正对应了 Ab 乘积的另一种计算方式**。

基于此，我们插播一条纯粹的数学问题，目的是希望大家明白，将矩阵与空间关联起来是多么的美好：

![alt text](https://raw.githubusercontent.com/satoxi/satoxi.github.io/master/matrix/matrix_5.png "Fig.5")

学过线性代数的应该知道，如果想要上述等式有解，矩阵 B 需要满足一些条件，由于我当时学的时候是硬背下来的，所以并不能理解个中奥秘。但如果用空间的思想，就会容易很多。

可是看到，矩阵 B 定义了两个方向，分别是（1, 0）和 (2, 0)，但是很明显，这两个方向其实是重合的（线性代数中定义为线性相关）。也就是说，矩阵 B 定义的空间是一维空间，而（3，5）却是二维空间中的一个点，因此，上述方程一定没有解。

下一篇，将会基于这种思想，介绍制作游戏时常用到的几个空间变换矩阵。

参考：
[1]  伊恩·古德费洛, 约书亚·本吉奥, 亚伦·库维尔, 深度学习[M]. 译者: 赵申剑, 黎彧君, 符天凡, 李凯. 北京: 人民邮电出版社.  2017, 22-24.
