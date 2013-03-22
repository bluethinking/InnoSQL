InnoSQL - A branch version of MySQL
===================================

InnoSQL是杭研开发维护的MySQL分支，目前基于MySQL 5.5。InnoSQL的主要目标是提供更好的性能以及高可用性，同时便于DBA的运维以及监控管理。其完全兼容于原版MySQL数据库，所有添加的功能都是动态的。若不开启这些功能，与原版MySQL数据库的工作方式完全相同。

 * Homepage: <https://github.com/NetEase/InnoSQL>
 * Wiki: <https://github.com/NetEase/InnoSQL/wiki/>
 * Issues: <https://github.com/NetEase/InnoSQL/issues/>
 * Tags: C, C++, MySQL, InnoDB

目前主要包括的特性有:
---------------------
高可用特性：

1. virtual sync replication with group commit，高性能同步复制
2. crash safe replication slave，宕机主从数据依然一致
3. slave batch commit 极大减少slave与master的延时，基本达到实时同步
4. InnoDB share memory，缓冲池快速预热技术

高性能特性：

1. InnoDB flash cache 将SSD作为L2cache，见percona CTO对此测试的结果
2. InnoDB IO enhance 对于InnoDB的IO进行优化，尤其是SSD
3. InnoDB死锁检测优化

运维特性：

1. 观察InnoDB undo log信息
2. 观察不同刷新方式的的次数
3. 观察master thread和purge thread的线程ID
4. slow log记录SQL语句的物理与逻辑IO次数
5. binlog记录SQL语句执行者的user和ip信息
6. Profiler功能，对用户资源进行限制
7. Role Table 将用户添加到角色表中，便于对用户的管理

Getting Started
----------------

首先克隆这个仓库

    git clone git://github.com/NetEase/InnoSQL.git

进入InnoSQL/src，在当前目录下即得到InnoSQL的各种Patch包。