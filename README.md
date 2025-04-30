# 基于OpenWRT在Azure上搭建VPN站点实现科学上网全记录

本文将围绕OpenWRT，通过在Azure上的VM，与家里的路由器建立VPN隧道，从而实现自动路由，国内国外访问分离。  
VPN隧道使用被最广泛使用的IPSEC隧道，为何使用IPSEC我后面再详细说明。  
DNS分流采用mosdns，曾经使用过overture，也研究过smartdns,mosdns优势明显，非常好用。后面会具体说明。  

***
## 目录

- 整体网络设计和架构
- 为何选择IPSEC协议？
- 创建Azure VM
  - VHD虚拟磁盘制作
  - Azure VM新建
- OpenWRT基本设置，应用安装
- Strongswan设置
- mosdns设置
