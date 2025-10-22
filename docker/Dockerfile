FROM oven/bun:latest

RUN apt-get update \
    && DEBIAN_FRONTEND=noninteractive apt-get install --no-install-recommends -y \
        apt-transport-https ca-certificates curl ttfautohint bash \
    && rm -rf /var/lib/apt/lists/*

COPY build.sh /
RUN chmod +x /build.sh
WORKDIR /work
ENTRYPOINT ["bash", "/build.sh"]
