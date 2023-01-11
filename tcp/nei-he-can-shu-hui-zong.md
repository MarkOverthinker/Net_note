# 内核参数汇总

第一次握手syn重传次数：tcp\_syn\_retries，默认5次

第二次握手的syn+ack重传次数：tcp\_synack\_retries,默认5次

第三次握手ack丢包会导致对方重传syn+ack，己方已建立连接，再发送报文如果对方未断开，报文内含ack，能建立连接。（第三次握手能携带数据，所以发送的数据报文发挥了握手报文的作用）若对方已断开则不会收到回应，则己方会触发超时重传，重传次数：tcp\_retries2，默认15次。

保活机制：双方在一段时间内无任何连接相关的活动触发

```
保活时间，这段时间内无活动则触发保活，开始发送探测报文。time
net.ipv4.tcp_keepalive_time=7200
```

<pre><code><strong>每隔这段时间发送一次。intvl
</strong><strong>net.ipv4.tcp_keepalive_intvl=75  
</strong></code></pre>

<pre><code><strong>最大探测的次数.probes
</strong><strong>net.ipv4.tcp_keepalive_probes=9
</strong></code></pre>

**快速建立连接功能（fast open）**:tcp\_fastopn

**sack**:tcp\_sack

**tcp\_tw\_reuse:**如果开启该选项的话，客户端（连接发起方） 在调用 connect() 函数时，**如果内核选择到的端口，已经被相同四元组的连接占用的时候，就会判断该连接是否处于 TIME\_WAIT 状态，如果该连接处于 TIME\_WAIT 状态并且 TIME\_WAIT 状态持续的时间超过了 1 秒，那么就会重用这个连接，然后就可以正常使用该端口了**。所以该选项只适用于连接发起方
