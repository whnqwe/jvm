# JVM实操

#### young GC图例

![](image/001.png)

#### Full Gc图例

![](image/002.png)



#### java 自带JVM监控工具

> https://docs.oracle.com/javase/8/docs/technotes/tools/windows/toc.html

##### jmap

###### 网址

> https://docs.oracle.com/javase/8/docs/technotes/tools/windows/jmap.html#CEGCECJB

###### 用途

> 命令用于生成heap dump文件

###### jmap常用配置

> -heap pid
>
> 通过-heap选项，打印java堆的配置情况和使用情况，还有使用的GC算法。

##### jstat

###### 网址

> https://docs.oracle.com/javase/8/docs/technotes/tools/windows/jstat.html#BEHHGFAE

###### 用途

> 利用JVM内建的指令对Java应用程序的资源和性能进行实时的命令行的监控，包括了对Heap size和垃圾回收状况的监控。

###### jstat配置信息

> jmap -options
>
> 查看所有参数
>
> ![](image/003.png)



> -class                 显示ClassLoad的相关信息；
>
> -compiler           显示JIT编译的相关信息；
>
> -gc                     显示和gc相关的堆信息；
>
> -gccapacity 　　  显示各个代的容量以及使用情况；
>
> -gcmetacapacity 显示metaspace的大小
>
> -gcnew               显示新生代信息；
>
> -gcnewcapacity  显示新生代大小和使用情况；
>
> -gcold                 显示老年代和永久代的信息；
>
> -gcoldcapacity    显示老年代的大小；
>
> -gcutil　　           显示垃圾收集信息；
>
> -gccause             显示垃圾回收的相关信息（通-gcutil）,同时显示最后一次或当前正在发生的垃圾回收的诱因；
>
> -printcompilation 输出JIT编译的方法信息；

###### jstat常用配置

> jmap -gcutil pid time
>
> jmap -gccause pid time