### Linux command : basename

2022年05月05日12:28:21

basename [pathname] [suffix]

basename [string] [suffix]

**去除路径与suffix。**

----

 为basename指定一个路径，

 basename命令会删掉所有的前缀包括最后一个slash（‘/’）字符，

if command has suffix, basename will pop it. 

然后将字符串显示出来。

eg. 

```shell

╰─○ basename Anaconda3-2021.11-Linux-x86_64.sh .sh

Anaconda3-2021.11-Linux-x86_64

(base) ╭─ubuntu at VM-16-11-centos in ~ 22-05-05 - 12:12:48

╰─○ basename Anaconda3-2021.11-Linux-x86_64.sh   

Anaconda3-2021.11-Linux-x86_64.sh
```

