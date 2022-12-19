FROM        node:18-bullseye-slim

LABEL       author="ShielD" maintainer="parker@pterodactyl.io"

RUN         apt update \
            && apt -y install ffmpeg imagemagick iproute2 git sqlite3 libsqlite3-dev python3 python3-dev ca-certificates dnsutils tzdata zip tar curl build-essential libtool \
	    && curl -s https://install.speedtest.net/app/cli/install.deb.sh | bash && apt -y install speedtest \
	    && speedtest --accept-license \
            && npm install -g npm@latest \
            && useradd -m -d /home/container container


USER        container
ENV         USER=container HOME=/home/container
WORKDIR     /home/container

COPY        ./../entrypoint.sh /entrypoint.sh

CMD         [ "/bin/bash", "/entrypoint.sh" ]
