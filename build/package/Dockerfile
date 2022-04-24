# MC Java Docker container
FROM debian:stable-slim

ARG TARGETOS
ARG TARGETARCH
ARG TARGETVARIANT

RUN apt-get update
RUN apt-get install -y curl openjdk-17-jre-headless

RUN groupadd -g 1000 minecraft &&\
    useradd -r -s /bin/false -u 1000 -g 1000 -m minecraft

RUN mkdir -m 755 /data
    #chown minecraft:minecraft /data

RUN curl -sfL -o /server.jar https://launcher.mojang.com/v1/objects/c8f83c5655308435b3dcf03c06d9fe8740a77469/server.jar

COPY scripts/start.sh /start.sh

RUN chmod +x /start.sh
RUN echo "eula=true" > eula.txt

ENV MEMORY="1G"

#USER minecraft
EXPOSE 25565/tcp
CMD ["/start.sh"]


# To build
# docker buildx build \
 #      -t mc-server \
 #      -f ./build/package/Dockerfile . \
 #      --load