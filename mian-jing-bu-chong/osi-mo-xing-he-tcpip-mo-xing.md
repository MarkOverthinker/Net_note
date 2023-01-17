# osi模型和TCP/IP模型

#### TCP/IP模型：

（1）物理层 物理层利用物理媒介为比特流提供物理连接，一般将网络接口层和物理层统称 TCP/IP协议的物理网。 常用协议：IEEE 802.3以太网；ARPANET网络；ATM网络；令牌环网；IEEE 802.11（无线局域网协议）。

（2）数据链路层 数据链路层负责与物理传输的连接媒介打交道，主要功能是接收数据报，并把接收到的数据报发送到指定的网络中去。 常用协议：PPP、SDLC、HDLC、PPP、STP（Spanning Tree Protocol）、帧中继。

（3）网络层 网络层采用的协议称为互联网协议，它提供跨多个网络的选址路由功能。 常用协议：IP、IPX、ICMP、RIP、OSPF(Open Shortest Path First开放式最短路径优先)

（4）传输层 它的主要功能是对应用层传递过来的用户信息分成若干数据报，加上报头，便于端到端的通信。提供分割与重组数据，按端口号寻址，连接管理差错控制和流量控制,纠错的功能。 常用协议：TCP（面向连接，可靠稳定）、UDP（面向无连接，尽最大努力交付）、SPX 、滑动窗口协议。

（5）应用层 提供应用程序间的通信。 常用协议：TELNET（远程登陆协议）、FTP（文件传输协议）、TFTP（简单文件传输协议）、SMTP(邮件传输协议)、SNMP（简单网络管理协议）、HTTP(超文本链接)、BOOTP、DHCP（动态主机配置协议）、DNS（DNS使用的传输协议既可为TCP又可为UDP，域名解析服务）。

最下面两层也可以合起来称为网络接口层/数据链路层

#### OSI模型

就是比上面多了会话层和表示层

（1）会话层 建立、维护和管理会话。 常用协议：Socket、NFS、SQL、RPC 、X-WINDOWS、ASP（APPTALK会话协议）、SCP等。&#x20;

（2）表示层 处理数据格式、数据加密等。 常用协议： 文本：ASCII，EBCDIC 图形：TIFF，JPEG，GIF，PICT 音视频：MIDI，MPEG，QUICKTIME&#x20;

\
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200324130846990.png?x-oss-process=image/watermark,type\_ZmFuZ3poZW5naGVpdGk,shadow\_10,text\_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2FhOTg4NjU2NDY=,size\_16,color\_FFFFFF,t\_70)
