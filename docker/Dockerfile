FROM n8nio/n8n:latest
USER root
RUN apk add --update python3 py3-pip py3-snmp busybox-extras net-snmp-tools expect nano gcc libc-dev python3 python3-dev net-snmp net-snmp-dev
RUN npm install fs dhcpd-leases express
RUN python3 -m venv /opt/venv
ENV PATH="/opt/venv/bin:$PATH"
RUN python3 -m pip install easysnmp netconf_client python-dotenv flask
COPY router /usr/local/lib/node_modules/n8n/node_modules/express/lib/router
COPY express.js /usr/local/lib/node_modules/n8n/node_modules/express/lib/express.js
USER node
