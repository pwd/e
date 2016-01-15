# e
Simple shell scripts for remote interactives using expect.

SSH登录到主机`a1`

```
➜  ~  e s a1
```

在远程主机`a1`上执行`uptime`命令

```
➜  ~  e e a1 uptime
```

将`abc.txt`文件通过`scp`命令拷贝到主机`a1`

```
➜  ~  e put a1 abc.txt /home/tom/abc.txt
```

将主机`a1`上的`/home/tom/abc.txt`文件通过`scp`命令拷贝到本地`a1`

```
➜  ~  e get a1 /home/tom/abc.txt abc.txt
```

根据`list1.conf`文件在一组主机上远程执行命令，每行为一个预定义的主机名

```
➜  ~  e all ./list1.conf uptime
```

列出通过`e`命令管理的主机列表

```
➜  ~  e
s.a1: root@192.168.0.1 Pandora 10023 pass
s.a2: root@example.com Pandora 22 nopass
```