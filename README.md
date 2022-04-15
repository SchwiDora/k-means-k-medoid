# k-means-k-medoid


（小白新手向）使用k-means算法和k-medoid算法对二维数据集进行聚类
===

代码修改自：https://blog.csdn.net/weixin_39220714/article/details/84867035
我的博客：https://blog.csdn.net/m0_66480474/article/details/124203923
Git bash还没弄明白，下载代码请去博客。

新手向代码参数修改教程：
---

k-medoid可能支持三维数据聚类，但k-means不支持。各参数的意义如下：


1.k-medoid
---

首先是随机生成测试点集的参数。

第27行的n_features=2表示生成二维数据集

centers=4表示生成的点集簇数为4，即生成的点可分为4类。这里要和97行的k_num_center=4相等，和接下来要说的cluster_std也要对应好。

center_box=(-30.0,30.0)表示生成的点集要在这个范围内。

cluster_std=[2.0,2.0,2.0,2.0]表示的是每一类的方差，数值越大点越分散。注意，这里对应的是centers=4且k_num_center=4的情况。
如果要改成生成3类点集（即centers=3，k_num_center=3），那么要把cluster_std修改为只有三项，即cluster_std=[2.0,2.0,2.0]。

32行的pyplot.savefig("114514.jpg")意思是把生成好的点集图存为114514.jpg，这里建议改个名。90行的也是同一个道理，表示把聚类结果存为1919810.jpg。

94行的n_points=1000表示生成1000个点。



2.k-means
---

和k-medoid基本一样，但是修改为三维数据集的时候还要修改70行的代码。

