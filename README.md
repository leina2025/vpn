# 4500 Port 已被严格监控无法用于建立VPN IPSec隧道

500端口未见异常，4500端口被封的效率非常高，1小时以内就会被墙识别并马上封锁。
IKE NAT端口（默认是4500）不能使用4500，必须更改为其他端口。
如果服务器不支持更改端口，那就无法建立连接。

测试更改IKE NAT端口到其他端口的情况下，连接稳定，不会被封。
已持续测试1年多，没有问题。

服务器使用的是strongSwan。

（2025/1/14）

