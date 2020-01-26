# Actions-OpenWrt

[![LICENSE](https://img.shields.io/github/license/mashape/apistatus.svg?style=flat-square&label=LICENSE)](https://github.com/P3TERX/Actions-OpenWrt/blob/master/LICENSE)
[![GitHub Stars](https://img.shields.io/github/stars/P3TERX/Actions-OpenWrt.svg?style=flat-square&label=Stars)](https://github.com/P3TERX/Actions-OpenWrt/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/P3TERX/Actions-OpenWrt.svg?style=flat-square&label=Forks)](https://github.com/P3TERX/Actions-OpenWrt/fork)

Build OpenWrt using GitHub Actions

[Read the details in my blog (in Chinese) | 中文教程](https://p3terx.com/archives/build-openwrt-with-github-actions.html)

[GitHub Actions Group](https://t.me/GitHub_Actions) | [GitHub Actions Channel](https://t.me/GitHub_Actions_Channel)

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
- Sign up for [GitHub Actions](https://github.com/features/actions/signup)
- Fork [this GitHub repository](https://github.com/P3TERX/Actions-OpenWrt)
- Generate `.config` files using [Lean's OpenWrt](https://github.com/coolsnowwolf/lede) source code.
- Push `.config` file to the GitHub repository, and the build starts automatically.Progress can be viewed on the Actions page.
- When the build is complete, click the `Artifacts` button in the upper right corner of the Actions page to download the binaries.

