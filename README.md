# OpenWrt-arm64


## Usage
固件适用arm64，包括N1、章鱼星球等

基本包括了常用的所有插件

r20.01.19:Lienol/lean-lede最新源码编译

r20.01.17:重大更新！共存ssrplus+和Lienol大佬的科学！【passwall（正确上网姿势 √）支持】：socks5、ss、ssr、v2Rray、trojan

r20.01.13:Lean最新源码编译，常规更新

r20.01.01:Lean最新源码，更新Trojan等

包含ShadowSocksR Plus+，Adbyby Plus+，ddns，Turbo ACC网络加速，文件传输等常用插件

创建docker的虚拟网络（可用docker network ls查看已创建了哪些）

docker network create -d macvlan --subnet=192.168.88.0/24 --gateway=192.168.88.1 -o parent=eth0 macnet

【名称为macnet，macvlan模式，将88.x修改为你自己主路由的网段】

开启openwrt容器：

docker run --restart always -d --network macnet --privileged buddyfly/openwrt-aarch64:latest

默认密码:password


