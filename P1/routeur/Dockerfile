FROM frrouting/frr:latest

RUN sed -i 's/^bgpd=no/bgpd=yes/; s/^ospfd=no/ospfd=yes/; s/^isisd=no/isisd=yes/' /etc/frr/daemons

RUN apk add --no-cache busybox-extras iproute2 bridge-utils tcpdump

COPY start.sh /start.sh
RUN chmod +x /start.sh
