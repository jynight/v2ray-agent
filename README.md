# Xray-core/sing-box 一键脚本快速安装

# 一、项目介绍

## 核心

- Xray-core
- sing-box

## 协议

> 以下均使用TLS，支持多种协议组合

- VLESS(Reality、Vision(TCP)、WS、gRPC、XHTTP)
- VMess(TCP、WS、HTTPUpgrade)
- Trojan(TCP、gRPC)
- Hysteria2(sing-box)
- Tuic(sing-box)
- NaiveProxy(sing-box)

## 功能

- 支持不同核心之间的配置读取
- 支持个性化安装单个协议
- 支持无域名版本的VLESS Reality搭建
- 支持多种分流用于解锁（wireguard、IPv6、Socks5、DNS、VMess(ws)、SNI反向代理）
- 支持批量添加CDN节点并配合ClashMeta自动优选
- 支持普通证书和通配符证书自动申请及更新
- 支持订阅以及多VPS组合订阅
- 支持批量新增端口
- 支持核心的升级以及回退
- 支持自主更换伪装站点
- 支持BT下载管理以及域名黑名单管理

# 二、使用指南

- 搭建最新的VLESS Vision和VLESS Reality防止VPS端口封禁
- 协议组合：VLESS-Vision-TLS / VLESS-Vision-uTLS-REALITY / VLESS-gRPC-uTLS-REALITY
- 建议选择 2任意组合安装->选择0,7 ，这样的安装会同时安装 Vision_TLS、Reality+TCP+uTLS+Vision、Reality+gRPC+uTLS
- 路径：vasma->2->1->0,7，第一步，输入域名；第二步，端口默认443即可，也可以自定义端口安装；第三步，当配置VLESS+Reality 需要注意一下，这里的端口可以自定义，如果上方使用了自定义端口这里则可以输入 443 。

# 三、安装使用

## 1.下载脚本

- 支持快捷方式启动，安装完毕后，shell输入【**vasma**】即可打开脚本，脚本执行路径[**/etc/v2ray-agent/install.sh**]

- Github

```
wget -P /root -N --no-check-certificate "https://raw.githubusercontent.com/jynight/v2ray-agent/main/install.sh" && chmod 700 /root/install.sh && /root/install.sh
```

