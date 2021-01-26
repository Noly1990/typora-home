## Linux常用命令



### 基础操作

```shell
date 显示日期与时间
2021年 01月 26日 星期二 15:28:01 CST
date +%Y/%m/%d %H:%M:%S
2021/01/26
date +%Y/%m/%d' '%H:%M:%S
2021/01/26 15:34:40

cal 日历
ubuntu 没有内置，通过 apt install ncal 安装

bc 计算器
```



#### man manual操作说明

>```shell
>安装中文manpages
>sudo apt install manpages-zh
>
>man ls
>
>```

#### info page

Linux特有的用来查询命令的用法和文件的格式

```shell
info ls
```



#### nano文本编辑器

简单易用



### 开关机方法

```shell
who 
显示已登录的用户

sync 
将缓存内容同步写入持久性存储中

shutdown/halt/poweroff 
shutdown [-krhc] <time> <message>
关机

reboot
重启
```

正常的开关机重启操作都是通过systemctl调用的

