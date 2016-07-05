# hadoop-common-2.2.0-bin
hadoop-common-2.2.0/bin

#  WIN7下运行hadoop程序报：Failed to locate the winutils binary in the hadoop binary path
#  通过断点调试、查看源码发现程序需要根据HADOOP_HOME找到winutils.exe,由于win机器并没有配置该环境变量，所以程序报 null\bin\winutils.exe。
#  找到原因后就去网上问了度娘，找到了解决方案，很简单，如下：

#　　1.下载winutils的windows版本

#　　GitHub上，有人提供了winutils的windows的版本，项目地址是：https://github.com/srccodes/hadoop-common-2.2.0-bin,直接下载此项目的zip包，下载后是文件名是hadoop-common-2.2.0-bin-master.zip,随便解压到一个目录

#　　2.配置环境变量

#　　增加用户变量HADOOP_HOME，值是下载的zip包解压的目录，然后在系统变量path里增加$HADOOP_HOME\bin 即可。　　

#　　再次运行程序，正常执行。
