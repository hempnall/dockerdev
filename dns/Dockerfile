FROM ubuntu:16.04
RUN apt-get -y update && apt-get -y install  bind9 dnsutils nano
RUN mkdir -p /etc/bind/zones/master
COPY 	etc/bind/zones/master/db.dev.local \
	etc/bind/zones/master/db.stg.local \
	etc/bind/zones/master/db.prd.local \
	/etc/bind/zones/master/ 
COPY 	etc/bind/named.conf.local /etc/bind/
EXPOSE 53/udp 53/tcp 
CMD ["named","-c","/etc/bind/named.conf.local","-g"]



