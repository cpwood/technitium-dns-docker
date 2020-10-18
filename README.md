# Unofficial Docker container for [Technitium DNS Server](https://github.com/TechnitiumSoftware/DnsServer)

Simple and sweet, even includes a healthcheck. Works great on a Raspberry Pi, too!

![](https://raw.githubusercontent.com/sjkp/technitium-dns-docker/master/media/dashboard.png)

## Usage

~~~
docker run \  
-d \
--name technitium-dns \
--restart always \
-p 5380:5380/tcp \
-p 53:53/tcp \
-p 53:53/udp \
-p 67:67/udp \
-p 68:68/udp \
-v [path]:/app/config
cpwood/technitium-dns-docker
~~~
