Redirect connections from different ports at one ipv4 address to unique random ipv6 address from \64 subnetwork. Based on 3proxy

![cover](cover.svg)

## Requirements
- Centos 7
- IPv6 \64

## Installation
[Video tutorial](https://youtu.be/EKBJHSTmT4w), VPS from Vultr used as Centos setup

1. Install all packages (`yum update -y && yum install make wget curl jq git -y`)
2. Disable the limits (`ulimit -n 1009999` and `ulimit -c unlimited`)
3. For regular user/pass auth proxies, use: `bash <(curl -s "https://raw.githubusercontent.com/rafaelb128/ipv4-ipv6-proxy/master/scripts/install.sh")`
3.a For no auth proxies, use: `bash <(curl -s "https://raw.githubusercontent.com///ipv4-ipv6-proxy/master/scripts/install-ipauth.sh")`
4. If you generate a lot of proxy you can see at which state you are by running `watch "cat /home/proxy-installer/data.txt | wc -l"` and `watch "ifconfig | wc -l"`

1. After installation dowload the file `proxy.zip`
   * File structure: `IP4:PORT:LOGIN:PASS` or `IP4:PORT`
