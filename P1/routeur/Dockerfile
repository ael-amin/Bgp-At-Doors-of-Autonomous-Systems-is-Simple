# Image "routeur": FRR (zebra + bgpd + ospfd + isisd) 3la Alpine
FROM frrouting/frr:latest

# Nfa3lou les daemons li talbin f subject
RUN sed -i 's/^bgpd=no/bgpd=yes/; s/^ospfd=no/ospfd=yes/; s/^isisd=no/isisd=yes/' /etc/frr/daemons

# Outils li ghadi n7tajou f P2 w P3 (bridge, vxlan, tcpdump)
RUN apk add --no-cache busybox-extras iproute2 bridge-utils tcpdump

# Ma kayn 7ta IP configuré par défaut
# Script li kaylanci daemons w kaykhalli shell
COPY start.sh /start.sh
RUN chmod +x /start.sh
