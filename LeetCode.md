## 一、算法思想
#### 1.滑动窗口
维护左、右两个指针，先移动右指针，知道找到一个符合题意的可行解。这个可行解不一定是题目想要的最优解，多亿保持右指针不动，移动左指针，找到更优的可行解。如此反复移动左右指针，右指针扩展窗口，找到可行解。左指针缩小窗口，找到更优解。

[转载自：https://www.cnblogs.com/lydiammzuo/p/12432783.html](https://www.cnblogs.com/lydiammzuo/p/12432783.html)
