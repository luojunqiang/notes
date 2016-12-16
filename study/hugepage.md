如果系统中共享内存比较大，使用hugepage应该会有较好的效果。
hugepage内存在linux系统中需要配置其大小，并且需要配置可以使用的用户组。
hugepage默认是lock在内存中的，所以需要相应调整limits中用户可以lock的内存大小。

下面是一些相关的资料可以参考：

- Oracle 关于HugePages的相关说明
  http://docs.oracle.com/cd/E11882_01/server.112/e10839/appi_vlm.htm#UNXAR394

- mmap有一个控制使用hugetable的参数，但有些应用不是用mmap分配共享内存
  http://stackoverflow.com/questions/40777684/create-huge-page-shared-memory-for-ipc-in-linux

- 介绍mysql使用hugetable的，可以参考
  https://www.cyberciti.biz/tips/linux-hugetlbfs-and-mysql-performance.html

- Linux下试验大页面映射（MAP_HUGETLB），相对简单的说明，可以参考
  http://blog.yufeng.info/archives/2118

- Performance Tuning: HugePages in Linux
  https://www.pythian.com/blog/performance-tuning-hugepages-in-linux/

