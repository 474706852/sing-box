# 介绍

最好用的 sing-box 一键安装脚本 & 管理脚本

# 特点

- 快速安装
- 无敌好用
- 零学习成本
- 自动化 TLS
- 简化所有流程
- 兼容 sing-box 命令
- 强大的快捷参数
- 支持所有常用协议
- 一键添加 VLESS-REALITY (默认)
- 一键添加 TUIC
- 一键添加 Trojan
- 一键添加 Hysteria2
- 一键添加 Shadowsocks 2022
- 一键添加 VMess-(TCP/HTTP/QUIC)
- 一键添加 VMess-(WS/H2/HTTPUpgrade)-TLS
- 一键添加 VLESS-(WS/H2/HTTPUpgrade)-TLS
- 一键添加 Trojan-(WS/H2/HTTPUpgrade)-TLS
- 一键启用 BBR
- 一键更改伪装网站
- 一键更改 (端口/UUID/密码/域名/路径/加密方式/SNI/等...)
- 还有更多...

- Github 地址：https://github.com/233boy/sing-box添加SOCKS5
我来帮您了解这个GitHub项目以及如何添加SOCKS5配置。首先让我获取这个项目的详细信息。

读取
https://github.com/233boy/sing-box
查看
现在让我获取这个项目的更多详细信息，包括如何配置SOCKS5：

搜索
233boy sing-box SOCKS5 配置教程
查看
让我获取233boy官方文档的详细信息：

读取
https://233boy.com/sing-box/sing-box-script/
查看
现在让我搜索更多关于配置SOCKS5的详细信息：

搜索
sing-box SOCKS5 配置 添加 教程
查看
让我获取一些具体的配置教程：

读取
https://icloudnative.io/posts/sing-box-tutorial/
查看
基于获取的信息，我来为您详细介绍如何在 233boy 的 sing-box 脚本中添加 SOCKS5 配置。

233boy sing-box 脚本添加 SOCKS5 教程
项目简介
233boy/sing-box 是一个功能强大的 sing-box 一键安装与管理脚本，支持多种协议包括 SOCKS5。该脚本具有以下特点：

🚀 快速安装，零学习成本
🔧 自动化 TLS 配置
📦 支持所有常用协议（包括 SOCKS5）
🎯 简化所有配置流程
💪 强大的快捷参数系统
安装脚本
首先需要安装 233boy 的 sing-box 脚本：

Copybash <(wget -qO- -o- https://github.com/233boy/sing-box/raw/main/install.sh)
系统要求：

支持：Ubuntu、Debian、CentOS
推荐：Ubuntu 22
⚠️ 注意：CentOS 可能无法正常运行
添加 SOCKS5 配置
安装完成后，添加 SOCKS5 配置非常简单：

基本添加命令
Copy# 最简单的方式 - 自动配置所有参数
sb add socks

# 或使用完整命令
sing-box add socks
自定义参数添加
Copy# 指定端口、用户名和密码
sb add socks 端口 用户名 密码

# 示例：端口233，用户名233boy，密码233boy.com
sb add socks 233 233boy 233boy.com
参数说明
SOCKS5 配置的可选参数包括：

端口 (port): 监听端口，使用 auto 自动分配
用户名 (username): 认证用户名，使用 auto 自动生成
密码 (password): 认证密码，使用 auto 自动生成
管理 SOCKS5 配置
查看配置
Copy# 查看所有配置
sb info

# 查看 SOCKS 相关配置
sb info socks
修改配置
Copy# 修改端口
sb change socks port 新端口号
sb change socks port auto  # 自动分配新端口

# 修改密码
sb change socks passwd 新密码
sb change socks passwd auto  # 自动生成新密码

# 修改用户名（如果支持）
sb change socks username 新用户名
获取连接信息
Copy# 生成连接 URL
sb url socks

# 生成二维码
sb qr socks
删除配置
Copy# 删除 SOCKS 配置
sb del socks
⚠️ 警告：删除操作不可逆，请谨慎使用

快速管理命令
脚本提供了多个快捷命令：

Copy# 查看帮助
sb help

# 查看状态
sb status

# 重启服务
sb restart

# 查看日志
sb log

# 更新脚本/核心
sb update      # 更新核心
sb update sh   # 更新脚本
使用 SOCKS5 代理
配置完成后，你可以在各种客户端中使用：

代理服务器信息
类型: SOCKS5
服务器: 你的服务器 IP
端口: 配置时设置的端口
用户名: 配置时设置的用户名
密码: 配置时设置的密码
客户端配置示例
在浏览器、应用程序或系统代理设置中：

SOCKS5 代理地址：你的服务器IP:端口
如果需要认证，填入用户名和密码
防火墙配置
如果连接失败，可能需要开放端口：

Copy# 关闭防火墙（谨慎使用）
systemctl stop firewalld
systemctl disable firewalld
ufw disable
测试连接
可以使用在线工具测试端口连通性：

访问 https://tcp.ping.pe/
输入格式：你的IP:端口（如：1.1.1.1:1080）
点击 Go 测试
高级功能
脚本目录结构
脚本：/etc/sing-box/sh
核心：/etc/sing-box/bin
配置：/etc/sing-box/conf
Web 管理界面
脚本还支持 Clash API 管理界面，可通过 Web 界面管理配置。

注意事项
端口选择: 建议使用高位端口（1024-65535）
安全性: 设置强密码，定期更换
备份: 重要配置建议备份
更新: 定期更新脚本和内核到最新版本
相关链接
GitHub 项目: https://github.com/233boy/sing-box
官方文档: https://233boy.com/sing-box/sing-box-script/
详细教程: https://233boy.com/sing-box/sing-box-server/
通过以上步骤，您就可以成功在 233boy 的 sing-box 脚本中配置和使用 SOCKS5 代理了。整个过程非常简单，脚本已经将复杂的配置过程自动化，您只需要几个简单的命令就能完成配置。

复制
保存到Notion
反馈

# 设计理念

设计理念为：**高效率，超快速，极易用**

脚本基于作者的自身使用需求，以 **多配置同时运行** 为核心设计

并且专门优化了，添加、更改、查看、删除、这四项常用功能

你只需要一条命令即可完成 添加、更改、查看、删除、等操作

例如，添加一个配置仅需不到 1 秒！瞬间完成添加！其他操作亦是如此！

脚本的参数非常高效率并且超级易用，请掌握参数的使用

# 文档

安装及使用：https://233boy.com/sing-box/sing-box-script/

# 帮助

使用：`sing-box help`

```
sing-box script v1.0 by 233boy
Usage: sing-box [options]... [args]...

基本:
   v, version                                      显示当前版本
   ip                                              返回当前主机的 IP
   pbk                                             同等于 sing-box generate reality-keypair
   get-port                                        返回一个可用的端口
   ss2022                                          返回一个可用于 Shadowsocks 2022 的密码

一般:
   a, add [protocol] [args... | auto]              添加配置
   c, change [name] [option] [args... | auto]      更改配置
   d, del [name]                                   删除配置**
   i, info [name]                                  查看配置
   qr [name]                                       二维码信息
   url [name]                                      URL 信息
   log                                             查看日志
更改:
   full [name] [...]                               更改多个参数
   id [name] [uuid | auto]                         更改 UUID
   host [name] [domain]                            更改域名
   port [name] [port | auto]                       更改端口
   path [name] [path | auto]                       更改路径
   passwd [name] [password | auto]                 更改密码
   key [name] [Private key | atuo] [Public key]    更改密钥
   method [name] [method | auto]                   更改加密方式
   sni [name] [ ip | domain]                       更改 serverName
   new [name] [...]                                更改协议
   web [name] [domain]                             更改伪装网站

进阶:
   dns [...]                                       设置 DNS
   dd, ddel [name...]                              删除多个配置**
   fix [name]                                      修复一个配置
   fix-all                                         修复全部配置
   fix-caddyfile                                   修复 Caddyfile
   fix-config.json                                 修复 config.json
   import                                          导入 sing-box/v2ray 脚本配置

管理:
   un, uninstall                                   卸载
   u, update [core | sh | caddy] [ver]             更新
   U, update.sh                                    更新脚本
   s, status                                       运行状态
   start, stop, restart [caddy]                    启动, 停止, 重启
   t, test                                         测试运行
   reinstall                                       重装脚本

测试:
   debug [name]                                    显示一些 debug 信息, 仅供参考
   gen [...]                                       同等于 add, 但只显示 JSON 内容, 不创建文件, 测试使用
   no-auto-tls [...]                               同等于 add, 但禁止自动配置 TLS, 可用于 *TLS 相关协议
其他:
   bbr                                             启用 BBR, 如果支持
   bin [...]                                       运行 sing-box 命令, 例如: sing-box bin help
   [...] [...]                                     兼容绝大多数的 sing-box 命令, 例如: sing-box generate uuid
   h, help                                         显示此帮助界面

谨慎使用 del, ddel, 此选项会直接删除配置; 无需确认
反馈问题) https://github.com/233boy/sing-box/issues
文档(doc) https://233boy.com/sing-box/sing-box-script/
```
