homebrew 安装

> homebrew install kafka

但是会出现以下问题

> /usr/local/Cellar/kafka/3.1.0/libexec/bin/kafka-run-class.sh: line 342: /Users/bao-mac/@@HOMEBREW_JAVA@@/bin/java: No such file or directory
> /usr/local/Cellar/kafka/3.1.0/libexec/bin/kafka-run-class.sh: line 342: exec: /Users/bao-mac/@@HOMEBREW_JAVA@@/bin/java: cannot execute: No such file or directory

原因如下：
>HOMEBREW_BOTTLE_DOMAIN: https://mirrors.ustc.edu.cn/homebrew-bottles/bottles/

解决方案

> HOMEBREW_BOTTLE_DOMAIN= brew reinstall kafka

启动zookeeper

> /opt/homebrew/opt/zookeeper/bin/zkServer.sh

启动kafka

> cd /opt/homebrew/opt/kafka/bin
>
> ./kafka-server-start /opt/homebrew/etc/kafka/server.properties