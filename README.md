## 梅林固件小内存V2ray

适用 RT-AX56U_V2/RT-AX56U青春版/RT-AX56U热血版/RT-AX56U刺客信条版 这种小存储空间的华硕路由器

附支持AImesh梅林固件

### 安装步骤

1、git clone 这个仓库，或者下载解压

2、打开路由器的ssh功能

![打开ssh](https://wx1.sinaimg.cn/large/001T3Wrcly1gureyy8x5bj60qq0ar0wl02.jpg)

3、清空所有数据（包括上网账号，请做好备份）

```
ssh admin@192.168.1.1 -p 10690
```

```
kill -9 $(pidof skipd)
rm -rf .[a-zA-Z_]* *
reboot
```
4、等待路由器重启

5、cmd + n 新开终端，上传shadowsocks目录，admin是你路由器用户名， -P是你设置的ssh端口号，非mac用户可以用sftp软件

```
scp -P 10690 -r /Users/yourpath/Downloads/shadowsocks admin@192.168.1.1:/tmp/
```

6、进入ss目录，更改install.sh执行权限，安装

```
cd /tmp/shadowsocks/
```

```
chmod +x install.sh 
```

```
sh install.sh
```

### done.
