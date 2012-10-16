InnoSQL - A branch version of MySQL
===================================

InnoSQL是MySQL数据库的一个分支版本，其完全兼容于Oracle MySQL，添加的补丁、插件、存储引擎都是动态的。InnoSQL的目标是提供更好的MySQL数据库性能，以及将一些富有创意的想法用于数据库的生产环境。

 * Homepage: <https://github.com/NetEase/InnoSQL>
 * Wiki: <https://github.com/NetEase/InnoSQL/wiki/>
 * Issues: <https://github.com/NetEase/InnoSQL/issues/>
 * Tags: C, C++, MySQL, InnoDB

目前主要包括的特性有:
---------------------

1. InnoDB Flash Cache
2. MySQL Profiler
3. Virtual Sync Replication with group commit
4. Share Memory for InnoDB

Getting Started
----------------

首先克隆这个仓库

    git clone git://github.com/NetEase/InnoSQL.git

进入InnoSQL/src，在当前目录下即得到InnoSQL的各种Patch包。