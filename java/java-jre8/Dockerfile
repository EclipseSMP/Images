# ----------------------------------
# EclipseSMP JRE 8
# Image: ghcr.io/eclipsesmp/images:java-jre8
# ----------------------------------

FROM        openjdk:8-slim-bullseye

LABEL       author="EclipseSMP" maintainer="abuse@eclipsesmp.au"

RUN apt-get update -y \
 && apt-get install fontconfig iproute2 curl -y \
 && useradd -d /home/container -m container

USER container
ENV  USER=container HOME=/home/container

WORKDIR     /home/container

COPY        ./entrypoint.sh /entrypoint.sh

CMD         ["/bin/bash", "/entrypoint.sh"]

