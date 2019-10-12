# 阿里云



## 使用指南
### 使用本地客户端远程连接
1. 在 阿里云 ECS 控制台，重置实例密码 
2. 采用 ssh root@IP 方式，输入密码后登录

### 开通访问端口
1. 在 阿里云 ECS 控制台，打开 “网络与安全组” -》 “安全组配置” -》“配置规则” -》 “快速创建规则”
![](_pic/AliYun-Port-Open-Rule.png)
2. 配置防火墙
```bash
# firewall-cmd --state
running
```
如果防火墙开启的情况下，需要配置打开端口：
```bash
firewall-cmd --add-port=8080/tcp --permanent
firewall-cmd --reload 
firewall-cmd --list-all
```
