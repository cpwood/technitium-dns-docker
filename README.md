# Unofficial Docker container for [Technitium DNS Server](https://github.com/TechnitiumSoftware/DnsServer)

Simple and sweet, even includes a healthcheck. Works great on a Raspberry Pi, too!

[](media/dashboard.png)

## Usage

~~~
docker run \  
-d \
--name technitium-dns \
--restart always \
-p 5380:5380/tcp \
-p 53/53/tcp \
-p 53/53/udp \
-v [path]:/app/config
~~~

## Running on Ubuntu on vultr. 

### Firewall rules
[](media/firewall-rules.png)

### Install docker
```
apt install docker.io
```

### Machine firewall disable
```
ufw status
Status: inactive
```

## Technitium Setup

Enable recursive resolver, or the DNS server will not be usable from other machines. Beware that vultr will send you email warnings that you have a recursive DNS resolver running. 

[](media/enable-recursive-resolver.png)


Configure the dns forwarder to which ever technology and provider you like

[](media/set-dns-forwarder.png)