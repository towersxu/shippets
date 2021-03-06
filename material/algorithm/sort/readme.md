# 排序相关的知识

- *有序度*：有序度是数组中具有有序关系的元素对的个数。对于一个倒序排列的数组,比如 6,5,4,3,2,1,有序度是 0;对于一个完全有序的 数组,比如 1,2,3,4,5,6,有序度就是n*(n-1)/2,也就是 15。

- *冒泡排序*和*插入排序*的时间复杂度都是 O(n2),都 是原地排序算法,为什么插入排序要比冒泡排序更受欢迎呢?
  
  冒泡排序不管怎么优化,元素交换的次数是一个固定值,是原始数据的逆序度。插入排序是同样的,不管怎么优化,元素移动的次数也等于原始数据的逆序度。但是,从代码实现上来看,冒泡排序的数据交换要比插入排序的数据移动要复杂,冒泡排序需要 3 个赋值操作,而插入排序只需要 1 个。
  冒泡排序和插入排序的最好情况时间复杂度 O(n)、最坏情况和平均情况时间复杂度都为 O(n^2)。

- 选择排序算法的实现思路有点类似插入排序,也分已排序区间和未排序区间。但是选择排序每次会从未排序区间中找到最小的元素,将其放到已排序区间的末尾。选择排序的最好情况时间复杂度、最坏情况和平均情况时间复杂度都为 O(n^2)。选择排序是一种不稳定的排序算法。

- *归并排序*：时间复杂度O(nlogn), 最好最坏都是O(nlogn);空间复杂度O(n);。归并排序虽然是稳定的、时间复杂度 为 O(nlogn) 的排序算法,但是它是非原地排序算法。

- *快速排序*：快排是一种原地、不稳定的排序算法。

  如何优化快速排序?

  导致快排时间复杂度降为O(n)的原因是分区点选择不合理,最理想的分区点是:被分区点分 开的两个分区中,数据的数量差不多。如何优化分区点的选择?有2种常用方法,如下:

  1.三数取中法

  从区间的首、中、尾分别取一个数,然后比较大小,取中间值作为分区点。

  如果要排序的数组比较大,那“三数取中”可能就不够用了,可能要“5数取中”或者“10 数取中”。

  2.随机法:每次从要排序的区间中,随机选择一个元素作为分区点。

  >警惕快排的递归发生堆栈溢出,限制递归深度,一旦递归超过了设置的阈值就停止递归。在堆上模拟实现一个函数调用栈,手动模拟递归压栈、出栈过程,这样就没有系统栈大小的限制。

- *桶排序*，*计数排序*，*基数排序*

## 参考资料

[算法复杂度速查表](https://mp.weixin.qq.com/s/oKHqA0dYXp2IYkezZ8iMHA)
