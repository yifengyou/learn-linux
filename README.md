# Linux 学习笔记 - linux调优

![20200920_111538_07](image/20200206_115630_90.png)

```
Something I hope you know before go into the coding~
First, please watch or star this repo, I'll be more happy if you follow me.
Bug report, questions and discussion are welcome, you can post an issue or pull a request.
```

## 目录

* [经验之谈](docs/经验之谈.md)
* [CPU性能](docs/CPU性能.md)
    * [如何理解平均负载](docs/CPU性能/如何理解平均负载.md)
    * [基础篇1-经常说的CPU上下文切换是什么意思](docs/CPU性能/基础篇1-经常说的CPU上下文切换是什么意思.md)
    * [基础篇2-经常说的CPU上下文切换是什么意思](docs/CPU性能/基础篇2-经常说的CPU上下文切换是什么意思.md)
    * [基础篇-某个应用的CPU使用率居然达到100%该怎么办](docs/CPU性能/基础篇-某个应用的CPU使用率居然达到100%该怎么办.md)
    * [案例篇-系统的CPU使用率很高但为啥却找不到高CPU的应用](docs/CPU性能/案例篇-系统的CPU使用率很高但为啥却找不到高CPU的应用.md)
    * [案例篇-系统中出现大量不可中断进程和僵尸进程怎么办1](docs/CPU性能/案例篇-系统中出现大量不可中断进程和僵尸进程怎么办1.md)
    * [案例篇-系统中出现大量不可中断进程和僵尸进程怎么办2](docs/CPU性能/案例篇-系统中出现大量不可中断进程和僵尸进程怎么办2.md)
    * [基础篇-怎么理解Linux软中断](docs/CPU性能/基础篇-怎么理解Linux软中断.md)
    * [案例篇-系统的软中断CPU使用率升高该怎么办](docs/CPU性能/案例篇-系统的软中断CPU使用率升高该怎么办.md)
    * [套路篇-如何迅速分析出系统CPU的瓶颈在哪里](docs/CPU性能/套路篇-如何迅速分析出系统CPU的瓶颈在哪里.md)
    * [套路篇-CPU性能优化的几个思路](docs/CPU性能/套路篇-CPU性能优化的几个思路.md)
    * [答疑篇-无法模拟出RES中断问题](docs/CPU性能/答疑篇-无法模拟出RES中断问题.md)
    * [答疑篇-使用perf工具分析Java问题](docs/CPU性能/答疑篇-使用perf工具分析Java问题.md)
* [内存性能](docs/内存性能.md)
* [IO性能](docs/IO性能.md)
* [网络性能](docs/网络性能.md)
* [诊断工具](docs/诊断工具.md)
    * [vmstat](docs/诊断工具/vmstat.md)
    * [pidstat](docs/诊断工具/pidstat.md)
    * [iostat](docs/诊断工具/iostat.md)
    * [ifstat](docs/诊断工具/ifstat.md)
    * [sysstat](docs/诊断工具/sysstat.md)
    * [dstat](docs/诊断工具/dstat.md)
    * [execsnoop](docs/诊断工具/execsnoop.md)
