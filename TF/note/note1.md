## Tensorflow基本概念

    * 使用图（Graphs）来表示计算任务  
    
    * 在被称之为会话（Session）的上下文（Context）中执行图
    
    * 使用tensor表示数据
    
    * 通过变量（Variable）维护状态
    
    * 使用feed和fetch可以为任意的操作赋值或者从其中获取数据
    
TensorFlow是一个编程系统，使用图来表示计算任务，图中的节点称之为op(operation)，一个op获得0或多个Tensor，执行计算，产生0或多个Tensor。Tensor看做是一个n维的数组或列表。图必须在会话中被启动。

![](../image/note1/structure_of_graph.jpg )

tensor和Variable有什么区别？

Variable和Tensor之间的区别：
1. Variable是可更改的，而Tensor是不可更改的。
2. Variable用于存储网络中的权重矩阵等变量，而Tensor更多的是中间结果等。
3. Variable是会显示分配内存空间的，需要初始化操作（assign一个tensor），由Session管理，可以进行存储、读取、更改等操作。相反地，诸如Const, Zeros等操作创造的Tensor，是记录在Graph中，所以没有单独的内存空间；而其他未知的由其他Tensor操作得来的Tensor则是只会在程序运行中间出现。
4. Tensor可以使用的地方，几乎都可以使用Variable。
————————————————
版权声明：本文为CSDN博主「Peanut_范」的原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/u013841196/article/details/82960765

