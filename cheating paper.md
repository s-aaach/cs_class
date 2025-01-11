
一.dfs和bfs模板

![img](file:///C:\Users\29910\AppData\Local\Temp\ksohtml15928\wps1.jpg) 

可以用来debug所有和枚举有关的dfs

![img](file:///C:\Users\29910\AppData\Local\Temp\ksohtml15928\wps2.jpg) 

迪杰斯特拉专属heapq

注意在一般bfs的时候不要用

![img](file:///C:\Users\29910\AppData\Local\Temp\ksohtml15928\wps3.jpg) 

Dfs的模板，建议在写各种走迷宫的时候一定要加上visited这样一个数据集而不是单纯的保护圈，这样就可以避免像这道题目中的同时占据很多个格子以及前面拿到题目中的方向问题

![img](file:///C:\Users\29910\AppData\Local\Temp\ksohtml15928\wps4.jpg) 

其实变换的迷宫就是一个需要考虑事件影响的bfs，所以在写bfs的时候可以不像寻宝那样step+=1这个样子，而是直接把时间这个变量带入deque之中

![img](file:///C:\Users\29910\AppData\Local\Temp\ksohtml15928\wps5.jpg) 

![img](file:///C:\Users\29910\AppData\Local\Temp\ksohtml15928\wps6.jpg) 

二.dp和贪心

这里主要总结一些特殊的dp题型

（1）二分查找问题

河中跳房子和aggressive cow

![img](file:///C:\Users\29910\AppData\Local\Temp\ksohtml15928\wps7.jpg) 

二分查找的方法解决贪心其实更像是穷举，而二分查找就是找到哪一个合适。

（2）dp问题中的背包问题

0—1背包：

![img](file:///C:\Users\29910\AppData\Local\Temp\ksohtml15928\wps8.jpg) 

多重背包：

![img](file:///C:\Users\29910\AppData\Local\Temp\ksohtml15928\wps9.png)![img](file:///C:\Users\29910\AppData\Local\Temp\ksohtml15928\wps10.png)![img](file:///C:\Users\29910\AppData\Local\Temp\ksohtml15928\wps11.jpg) 

但是这段代码对于python3来说是超时的，所以我们可以采用二进制优化。

 

 

![img](file:///C:\Users\29910\AppData\Local\Temp\ksohtml15928\wps12.jpg) 

二进制优化的原理：

我们知道任何一个数都可以用2，4，8，等一系列数表示

所以在每一次的多重背包之中对于每一个元素都按照这个方法讨论其取法

完全背包

![img](file:///C:\Users\29910\AppData\Local\Temp\ksohtml15928\wps13.jpg) 

（注：

这里我们不排除考试的时候会在我们到底要输出哪个上面做文章，如果是恰好k块钱，那么就输出dp[k]就可以，如果是至少或者至多。我们要知道，如果k+-我们背包中最大的量，那么结果就是等差数列因此无意义。所以我们把范围控制在这个区间就可以了）

3. 买卖股票问题——状态机

![img](file:///C:\Users\29910\AppData\Local\Temp\ksohtml15928\wps14.jpg) 

![img](file:///C:\Users\29910\AppData\Local\Temp\ksohtml15928\wps15.jpg) 

后者是恰好交易k次

或许状态机dp也是一种双dp

4. 正难则反：剪绳子

![img](file:///C:\Users\29910\AppData\Local\Temp\ksohtml15928\wps16.jpg) 

把问题反过来看，剪绳子变成拼绳子

![img](file:///C:\Users\29910\AppData\Local\Temp\ksohtml15928\wps17.jpg) 

![img](file:///C:\Users\29910\AppData\Local\Temp\ksohtml15928\wps18.jpg) 

这道题目就是再i，j之间不断戳。最后就是返回再0和n+1之间随便戳。

![img](file:///C:\Users\29910\AppData\Local\Temp\ksohtml15928\wps19.jpg) 

一个路径问题的实例：

![img](file:///C:\Users\29910\AppData\Local\Temp\ksohtml15928\wps20.jpg) 

5. 双dp

双dp感觉就可以看成一种状态机dp，比如说土豪购物，其中的状态就是仍不扔掉那一个东西。

用状态机和双dp写的土豪购物：

 

![img](file:///C:\Users\29910\AppData\Local\Temp\ksohtml15928\wps21.jpg) 

![img](file:///C:\Users\29910\AppData\Local\Temp\ksohtml15928\wps22.jpg) 

值得注意的是这里的状态机其实和前面讲的不太一样，少了一个维度。

原因是如果你丢掉了一个你就不能再丢掉了。

然后另一点就是我们说的“至多”。

6. dp加上搜索

![img](file:///C:\Users\29910\AppData\Local\Temp\ksohtml15928\wps23.jpg) 

注意如何剪枝

三．语法问题等

![img](file:///C:\Users\29910\AppData\Local\Temp\ksohtml15928\wps24.jpg) 

滑动窗口问题

![img](file:///C:\Users\29910\AppData\Local\Temp\ksohtml15928\wps25.jpg) 

螺旋矩阵（洋葱类似问题）

![img](file:///C:\Users\29910\AppData\Local\Temp\ksohtml15928\wps26.jpg) 

单调栈问题

![img](file:///C:\Users\29910\AppData\Local\Temp\ksohtml15928\wps27.jpg) 

![img](file:///C:\Users\29910\AppData\Local\Temp\ksohtml15928\wps28.jpg) 

一定要善用字典和集合！！！！

![img](file:///C:\Users\29910\AppData\Local\Temp\ksohtml15928\wps29.jpg) 

![img](file:///C:\Users\29910\AppData\Local\Temp\ksohtml15928\wps30.jpg) 
