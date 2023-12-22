# FscanSnipaste

## 初衷

1、攻防时内网fs大保健后，一大堆打印机、FTP等，重复截图效率太低

2、蓝队应急快、动不动拔网线，人工截图速度慢

## 使用

> FscanSnipaste_1.8.2 -h

![](img/bcae8eab848317a5d4404f0639d7276.png)

本地靶场环境使用截图：

> FscanSnipaste_1.8.2.exe -f 172.168.txt -m all -t 3

![](img/2f6ca7180970c07770105f69cc91d55.png)

**默认：**

example:

> FscanSnipaste -f result.txt

所有模块都会连接，超时时间为3s

单选项截图，例如：

```下述测试均为本地虚拟机环境```

**ftp**

> FscanSnipaste -f result.txt -m ftp -t 5

![](img/9bf95ec9a57fb5dcd67e7f5847e6b57.png)

**mysql**

> FscanSnipaste -f result.txt -m mysql -t 5

![](img/9503dc95684deae3367d33ff0a469cd.png)

**redis**

> FscanSnipaste -f result.txt -m redis

![](img/46cbb10a044754834666eb69793b468.png)

**postgres**

> FscanSnipaste -f result.txt -m postgres

![](IMG/612ecd15c3ff38c2203d2c41d009a6f.png)

**web**

> FscanSnipaste -f result.txt -m web

只会批量打开url，不会打poc

![](img/95925b4cd3d6b88b9ea8d86a3c88914.png)

## 下载



## 问题

1、Oracle连接不上，存在客户端和服务端版本不一致的问题

2、web模块不能适配POC，只能批量打开infoscan的url，没有"/druid/index.html"这些POC拼接进去

3、只适配fs1.8.2，1.8.3输出的格式不一样了

