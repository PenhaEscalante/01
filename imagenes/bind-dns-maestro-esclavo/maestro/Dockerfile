FROM debian:latest
RUN apt-get update && apt-get install -y bind9 dnsutils
ADD bind9-config.tar.gz /etc/bind/
RUN mv /etc/bind/db.pachangamix.com /var/lib/bind/db.pachangamix.com
RUN named-checkconf && named-checkzone pachangamix.com /var/lib/bind/db.pachangamix.com
EXPOSE 53
CMD named -f
