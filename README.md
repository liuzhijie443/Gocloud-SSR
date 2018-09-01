

## 简介：

方法来自恩山论坛大神 [tsl0922](http://www.right.com.cn/forum/space-uid-96481.html)，Github [tsl0922](https://github.com/tsl0922/)，原项目和文件已经被删除，我顶多算备份。


## 部署方法：
1.进入高恪后台，选择导入配置，导入backup-ssh.config文件，等待路由重启后导入成功。
2.启动Putty，登陆192.168.1.1，端口22222，用户名密码admin。登陆后输入opkg update
3.输入命令 
`
【cd /etc & wget -O opkg.conf https://raw.githubusercontent.com/liuzhijie443/Gocloud-SSR/master/opkg.conf
【cd /tmp & wget -O ShadowsocksR-Gocloud.ipk https://raw.githubusercontent.com/liuzhijie443/Gocloud-SSR/master/ShadowsocksR-Gocloud.ipk】
【opkg update】
【opkg install ShadowsocksR-Gocloud.ipk】
`
4.路由器联网。
5.启动Putty，登陆192.168.1.1，端口同样为22222，用户名密码同上。登陆后输入opkg update
6.刷新完成后输入cd /tmp,回车，opkg install S-S R.ipk
7.完成，登陆您的路由器您就可以看到在网络设置里多了个S-S R选项。
8.警告：完成以上内容后替换/etc/dropbear/authorized_keys中的公钥为您的公钥，并删除/etc/rc.local中的echo至/etc/dropbear/authorized_keys ，以免有心人从远程登陆您的路由
9.        WinSCP跟Putty自行下载
