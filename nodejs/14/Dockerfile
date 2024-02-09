

FROM        --platform=$TARGETOS/$TARGETARCH node:14-alpine

LABEL       author="NexoHost Corporation" maintainer="support@nexohost.es"

LABEL       org.opencontainers.image.source="https://github.com/NexoHost/yolks"
LABEL       org.opencontainers.image.licenses=MIT

RUN         apk add --update --no-cache ca-certificates curl ffmpeg git openssl sqlite tar tzdata \
				&& adduser -D -h /home/container container

USER        container
ENV         USER=container HOME=/home/container
WORKDIR     /home/container

COPY        ./../entrypoint.sh /entrypoint.sh
CMD         [ "/bin/ash", "/entrypoint.sh" ]
