FROM		frrouting/frr:v8.4.0

COPY		script/	/root/script

RUN			chmod +x /root/script/conf_router.sh
RUN			chmod +x /root/script/conf_leaf.sh
RUN			chmod +x /root/script/conf_spine.sh

RUN 		sed -i 's/bgpd=no/bgpd=yes/g' /etc/frr/daemons && \
    		sed -i 's/ospfd=no/ospfd=yes/g' /etc/frr/daemons && \
    		sed -i 's/isisd=no/isisd=yes/g' /etc/frr/daemons

ENTRYPOINT	["/root/script/conf_router.sh"]
