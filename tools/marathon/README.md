Marathon和Chonos基于Mesos做任务调度时，一定是动态调度，也就是每个任务在执行之前是不知道它将来在哪一台服务器上执行和绑定哪一个端口。如图5所示，9台服务器组成的Mesos集群上混合运行各种Marathon调度的任务，
中间一台服务器坏掉以后，这台服务器上的两个任务就受影响，然后Marathon把这两个任务迁移到其他服务器上，这就是动态任务调度带来的好处，非常容易实现容错。