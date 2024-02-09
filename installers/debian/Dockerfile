

FROM        --platform=$TARGETOS/$TARGETARCH debian:bullseye-slim

LABEL       author="NexoHost Corporation" maintainer="support@nexohost.es"

LABEL       org.opencontainers.image.source="https://github.com/NexoHost/yolks"
LABEL       org.opencontainers.image.licenses=MIT

ENV         DEBIAN_FRONTEND=noninteractive

RUN         dpkg --add-architecture i386 \
				&& apt update \
				&& apt upgrade -y \
				&& apt -y --no-install-recommends install ca-certificates curl lib32gcc-s1 libsdl2-2.0-0:i386 git wget
