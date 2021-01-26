## 文件目录与磁盘格式

#### 文件权限与目录配置

>用户（User），用户组（Group），非本用户组外的其他人（Others）

```shell
ls -al
drwxr-xr-x   7    root    root      4096    12月 29 12:26 .config

文件类型权限 链接数  拥有者  所属用户组   文件大小  最后修复日期时间   文件名
```

```
drwxr-xr-x
1. 首位代表文件类型，(d)目录   (-)文件   (l)链接  (b)可供存储的周边设备  (c) 串行端口设备 (s) sockets接口文件 (p)pipe数据传输文件
2. 234位是拥有者的权限
3. 567位为用户组的权限
4. 890位为其他用户的权限

权限 r 可读  w 可写  r 可执行  -无

```

目录类型的文件， 如果权限中没有x，也无法进入该目录（r--）

```shell
chgrp 修改文件所属用户组
chown 修改文件拥有者
chmod 修改文件权限
-R 递归，目录下所有其他执行相同操作

chmod -R <filename>
r 4
w 2
x 1
rwx = 4+2+1 = 7
7 7 7 则为所有人全部权限

chmod u=rwx,go=rx <filename>
u  user
g  group
o  others
a  all
+ 增加
- 删除
= 设置
```

文件的rwx

r 读取

w 修改

x 执行

目录的rwx

r 读取目录结构

w 修改目录下内容（新建，删除，更名，移动）

x 能否进入目录



目录文件名最长255字节



#### Linux目录配置

> FHS Filesystem Hierarchy Standard 标准

/usr  软件存放处

/etc 配置文件

/opt 第三方辅助软件

/boot 启动与内核文件

/var 可变文件（程序运行相关）



/bin 单人维护模式下的常用命令的程序所存放的位置

/dev 接口设备相关的文件

/lib 函数库，标准库，链接库     /lib/modules  驱动程序相关

/media 软盘光盘DVD等可删除的媒体文件

/mnt 特指用来挂载一些媒体的目录与/media类似

/run 运行的程序所产生依赖的各种信息文件

/sbin 启动过程中启动、修复、还原系统所需要的关键的命令 

/srv 存放一些服务所依赖的文件数据

/tmp

