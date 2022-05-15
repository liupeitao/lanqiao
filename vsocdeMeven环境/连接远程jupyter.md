# 连接远程jupyter


#### 通过ssh建立连接

使用screen session维持服务器端口转发

通过ssh建立连接

确保你的服务器有jupyter notebook，如果没有bash输入pip install jupyter安装

---
先ssh连接到服务器，然后创建jupyter notebook密码， bash输入

`jupyter notebook password`

在服务器的某端口打开jupyter notebook，bash输入

`jupyter notebook --no-browser --port=12345`

建立ssh连接：我们将服务器打开jupyter notebook的端口远程转发到本地即可，在新的命令行窗口输入（非服务器bash）

`ssh -N -L 8080:localhost:12345 <user_name>@<host_ip>`

可以设置ssh免密登录这样就不用输入user\_name@hostname了.如下`myubuntu` 设置详情参照....

```bash
ssh -f  -N -L  8080:localhost:12345 myubuntu
# -f 后天执行 -N说明不执行任何远程命令；-L指明执行端口转发
# 12345是服务器为jupyter设置的.
```
我们已经将服务器12345端口转发到了本地的8080端口，此时浏览器打开本地8080端口即可，***浏览器地址栏输入http://localhost:8080/即可在本地浏览器打开远程服务器的jupyter notebook***

开始使用jupyter notebook吧！如果存在端口占用问题，自行修改端口



> 原文链接：https://blog.csdn.net/qq\_34769162/article/details/107947034



> 正能量传播人 2022/5/5 上午12:05:35

首先要安装jupyter