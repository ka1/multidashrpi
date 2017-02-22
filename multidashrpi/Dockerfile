FROM hypriot/rpi-node:7-slim

RUN apt-get update \
    && apt-get install -yq libpcap-dev vim git python make g++ \
    && npm install -g node-dash-button request \
    && npm install -g mqtt --save \
    && apt-get clean \
    && apt-get autoclean \
    && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

VOLUME /app
WORKDIR /app

#ADD app.js /app/app.js

ENV NODE_PATH=/usr/local/lib/node_modules

CMD ["node", "app.js"]
