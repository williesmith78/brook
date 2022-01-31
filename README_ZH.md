# Brook

[🇬🇧 English](README.md)

[![Build Status](https://travis-ci.org/txthinking/brook.svg?branch=master)](https://travis-ci.org/txthinking/brook)
[![开源协议: GPL v3](https://img.shields.io/badge/%E5%BC%80%E6%BA%90%E5%8D%8F%E8%AE%AE-GPL%20v3-blue.svg)](http://www.gnu.org/licenses/gpl-3.0)

[📜 Document](https://txthinking.github.io/brook/)
[🤝 Telegram](https://t.me/brookgroup)
[🗣 Talks](https://t.me/txthinking_talks)
[💬 Join](https://join.txthinking.com)
[🩸 Youtube](https://www.youtube.com/txthinking) 
[❤️ Sponsor](https://github.com/sponsors/txthinking)

---

## 什么是 Brook

Brook 是一个跨平台的强加密无特征的代理软件. 偏爱 KISS 哲学.

❤️ A project by [txthinking.com](https://www.txthinking.com)

### 通过 curl 安装 CLI (命令行版本), 并运行 `brook wserver`

```
curl -L https://github.com/txthinking/brook/releases/latest/download/brook_linux_amd64 -o /usr/bin/brook
chmod +x /usr/bin/brook
brook server --listen :9999 --password hello
```

> 然后, 你的 `brook server` 是 `YOUR_SERVER_IP:9999`, 密码是 `password`

### 通过 curl 安装 CLI (命令行版本) 和 [joker](https://github.com/txthinking/joker), 并用 [joker](https://github.com/txthinking/joker) 运行 `brook wserver`

```
curl -L https://github.com/txthinking/joker/releases/latest/download/joker_linux_amd64 -o /usr/bin/joker
chmod +x /usr/bin/joker
curl -L https://github.com/txthinking/brook/releases/latest/download/brook_linux_amd64 -o /usr/bin/brook
chmod +x /usr/bin/brook
joker brook server --listen :9999 --password hello
```

> 然后, 你的 `brook server` 是 `YOUR_SERVER_IP:9999`, 密码是 `password`

### 通过 [nami](https://github.com/txthinking/nami) 安装 CLI, 并通过 [joker](https://github.com/txthinking/joker) 运行 `brook wserver`

```
bash <(curl https://bash.ooo/nami.sh)
nami install joker brook
joker brook server --listen :9999 --password hello
```

> 然后, 你的 `brook server` 是 `YOUR_SERVER_IP:9999`, 密码是 `password`

### 通过一键脚本

```
bash <(curl https://bash.ooo/brook.sh)
```

[查看文档](https://txthinking.github.io/brook/#/zh-cn/install-cli)

### 安装 GUI (图形客户端)

[查看文档](https://txthinking.github.io/brook/#/zh-cn/install-gui-client)

## 使用

```
NAME:
   Brook - A cross-platform strong encryption and not detectable proxy

USAGE:
   brook [global options] command [command options] [arguments...]

VERSION:
   20210701

AUTHOR:
   Cloud <cloud@txthinking.com>

COMMANDS:
   server          Run as brook server, both TCP and UDP
   client          Run as brook client, both TCP and UDP, to start a socks5 proxy, [src <-> socks5 <-> brook client <-> brook server <-> dst]
   wsserver        Run as brook wsserver, both TCP and UDP, it will start a standard http server and websocket server
   wsclient        Run as brook wsclient, both TCP and UDP, to start a socks5 proxy, [src <-> socks5 <-> brook wsclient <-> brook wsserver <-> dst]
   wssserver       Run as brook wssserver, both TCP and UDP, it will start a standard https server and websocket server
   wssclient       Run as brook wssclient, both TCP and UDP, to start a socks5 proxy, [src <-> socks5 <-> brook wssclient <-> brook wssserver <-> dst]
   relayoverbrook  Run as relay over brook, both TCP and UDP, this means access [from address] is equal to [to address], [src <-> from address <-> brook server/wsserver/wssserver <-> to address]
   dns             Run as dns server over brook, both TCP and UDP, [src <-> brook dns <-> brook server/wsserver/wssserver <-> dns] or [src <-> brook dns <-> dnsForBypass]
   tproxy          Run as transparent proxy, both TCP and UDP, only works on Linux, [src <-> brook tproxy <-> brook server/wsserver/wssserver <-> dst]
   link            Print brook link
   qr              Print brook server QR code
   connect         Connect via standard sharing link (brook server & brook wsserver & brook wssserver)
   relay           Run as standalone relay, both TCP and UDP, this means access [from address] is equal to access [to address], [src <-> from address <-> to address]
   socks5          Run as standalone standard socks5 server, both TCP and UDP
   socks5tohttp    Convert socks5 to http proxy, [src <-> listen address(http proxy) <-> socks5 address <-> dst]
   hijackhttps     Hijack domains and assume is TCP/TLS/443. Requesting these domains from anywhere in the system will be hijacked . [src <-> brook hijackhttps <-> socks5 server] or [src <-> direct]
   pac             Run as PAC server or save PAC to file
   servers         Run as multiple brook servers
   relays          Run as multiple standalone relays
   map             Run as mapping, both TCP and UDP, this means access [from address] is equal to [to address], [src <-> from address <-> brook <-> to address]
   howto           Print some useful tutorial resources
   help, h         Shows a list of commands or help for one command

GLOBAL OPTIONS:
   --debug, -d               Enable debug (default: false)
   --listen value, -l value  Listen address for debug (default: ":6060")
   --help, -h                show help (default: false)
   --version, -v             print the version (default: false)

COPYRIGHT:
   https://github.com/txthinking/brook
```

[文档](https://txthinking.github.io/brook/#/zh-cn/)

## 贡献

请先阅读 [CONTRIBUTING.md](https://github.com/txthinking/brook/blob/master/.github/CONTRIBUTING.md)

## 开源协议

基于 GPLv3 协议开源
