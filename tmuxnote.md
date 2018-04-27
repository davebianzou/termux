# TMUX NOTE
#### 导语:
>tmux是指通过一个终端登录远程主机并运行后，在其中可以开启多个控制台的终端复用软件。
## 一、安装与卸载
```
apt install tmux
apt remove tmux
```
## 二、使用TMUX
tmux是一个优秀的终端复用软件，类似GNU Screen，但来自于OpenBSD，采用BSD授权。使用它最直观的好处就是，通过一个终端登录远程主机并运行tmux后，在其中可以开启多个控制台而无需再“浪费”多余的终端来连接这台远程主机；当然其功能远不止于此。
### 模块
Tmux使用C/S模型构建，主要包括以下单元模块：
* server：服务器。输入tmux命令时就开启了一个服务器。
* session：会话。一个服务器可以包含多个会话。
* window：窗口。一个会话可以包含多个窗口。
* panel：面板。一个窗口可以包含多个面板。
### 操作
***
* Ctrl+b *激活控制台；此时以下按键生效*
* Ctrl+b :kill-server *删除所有session*
* tmux new -s name *创建并指定session名字*
* Ctrl+b :kill-session *删除session*
* tmux attach -t name *进入已存在的session*
* Ctrl+b+d *临时退出session*
* Ctrl+b+s *列出session*
* Ctrl+b+( *切换session*
***
* Ctrl+b+c *创建window*
* Ctrl+b+& *删除window*
* Ctrl+b+n *下一个window*
* Ctrl+b+p *上一个window*
* Ctrl+b+num *window*
***
* Ctrl+b+" *横切*
* Ctrl+b+% *竖切*
* Ctrl+b+x *删除pane*
* Ctrl+b+<space> *更换pane排版*
* Ctrl+b+o *按顺序在pane之间移动*
***
* Ctrl+b+[ *copy mode*
* Ctrl+b+] *paste*
***
* Ctrl+b+?
* Ctrl+b:list-commands
***
