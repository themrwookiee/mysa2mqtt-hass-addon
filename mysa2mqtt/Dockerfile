ARG BUILD_FROM=ghcr.io/home-assistant/amd64-base:latest
FROM ${BUILD_FROM}

ARG mysa2mqttRevision=1.2.2

RUN \
    apk add --no-cache \
        nodejs \
        npm

RUN npm install -g "mysa2mqtt@${mysa2mqttRevision}"

COPY run.sh /
RUN chmod a+x /run.sh

CMD ["/run.sh"]
