# xmrig for ARMhf 

Monero XMR mining via termux ;ubuntu

1. install ubuntu in termux
command;
(ubuntu is optional)
```shell
pkg install update && upgrade
apt install git
apt install wget
apt install proot
termux-setup-storage
git clone https://github.com/hootan09/xmrigARMhf
cd xmrigARMhf
chmod +x ubuntu.sh
sh ubuntu.sh
./start-ubuntu.sh

```

2. install xmrig cpu miner to ubuntu termux
```shell
apt update
apt upgrade
apt install git
apt install wget
apt install proot
apt-get install git build-essential cmake libuv1-dev libmicrohttpd-dev libssl-dev

### orginal Link https://github.com/xmrig/xmrig
tar xvf xmrig-v5.5.3_source.tar.gz
cd xmrig-5.5.3
mkdir build
cd bulid
cmake -DWITH_HWLOC=OFF -DARM_TARGET=8 ..
make
```
then you can creat a config.json file in /build dir
xmrig.exe -a cryptonight -o stratum+tcp://xmr.pool.minergate.com:45700 -u hootan09@gmail.com -p x -3

