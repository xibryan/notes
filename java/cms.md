CMS参数：

-XX:+UseParNewGC	
-XX:+UseConcMarkSweepGC	
-XX:ParallelGCThreads	Sets the number of threads used during parallel phases of the garbage collectors. The default value varies with the platform on which the JVM is running.
-XX:ParallelCMSThreads	
-XX:MaxTenuringThreshold	对象从新生代晋升到老年代的年龄阈值（每次 Young GC 留下来的对象年龄加一），默认值15，表示对象要经过15次 GC 才能从新生代晋升到老年代。设置太小会严重影响 CMS GC 性能，建议默认值即可。
-XX:+UseCMSCompactAtFullCollection	这个参数表示开启 Full GC 时的压缩功能，减少内存碎片。默认开启
-XX:CMSFullGCsBeforeCompaction	多少次Full GC 后压缩old generation一次。默认0
-XX:+UseCMSInitiatingOccupancyOnly	只是用设定的回收阈值(上面指定的70%),如果不指定,JVM仅在第一次使用设定值,后续则自动调整.
-XX:CMSInitiatingOccupancyFraction	是指设定CMS在对内存占用率达到70%的时候开始GC
-XX:+CMSClassUnloadingEnabled	
-XX:+CMSScavengeBeforeRemark	在CMS GC前启动一次ygc，目的在于减少old gen对ygc gen的引用，降低remark时的开销
-XX:+CMSParallelRemarkEnabled	启用并行标记，降低标记停顿
-XX:ConcGCThreads	The flag -XX:ConcGCThreads=<value> (in earlier JVM versions also known as -XX:ParallelCMSThreads) defines the number of threads with which the concurrent CMS phases are run.
-XX:SurvivorRatio=8	Eden区与Survivor区的大小比值
-XX:MaxTenuringThreshold	新生代需要经历多少次GC晋升到老年代中的最大阈值

