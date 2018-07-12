# 《快速上手Linux玩转典型应用》

以Centos为例

## ssh

- 服务器安装ssh服务
	- 安装ssh yum install openssh-server
	- 启动ssh service sshd start
	- 设置开机启动 chkconfig sshd on

- 客户端安装ssh服务
	- 安装ssh yum install openssh-clients

- 常见ssh命令
	- 连接 ssh root@ip
	- 配置config，方便连接
		- cd ~/.ssh
		- touch config
		- 编辑config
		```
		host "dianxin"
		    HostName ip
		    User root
		    Port 22
		```
- 免秘钥登陆服务器
	- 生成公钥私钥 ssh-keygen 
	- 加载私钥 ssh-add ~/.ssh/私钥名称
	- 在服务器的 ~/.ssh/authorized_keys下存放生成的公钥

- 修改ssh端口 修改/etc/ssh/sshd_config中的port，然后service sshd restart重启服务

## 常见命令

- 软件操作命令
	- 软件包管理器 yum
		- 安装 yum install xx
		- 卸载 yum remove xxx
		- 搜索 yum serach xxx
		- 清缓存 yum clean packages
		- 列表 yum list
		- 软件包信息 yum info xxx

- 服务器硬件资源信息命令
	- 内存 free -m
	- 硬盘 df -h 
	- 负载 w or top
	- cpu cat /proc/cpuinfo

- 文件操作命令
	- vim
		- 移动到全文首行 gg
		- 移动到全文尾行 G
		- 删行 dd
		- 撤销 u
		- 复制一行 yy
		- 粘贴 p
	- 文件权限 rwx(4+2+1)
	- grep查找关键字 
		- grep -n "guoxingyu" test // 在test文件中查找guoxingyu，-n显示行号
	- find 
	- wc 












