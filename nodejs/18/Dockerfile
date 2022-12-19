FROM        node:18-bullseye-slim

LABEL       author="ShielD" maintainer="quay.io/kanvret12/shield"

RUN            apt update 
RUN            apt install ffmpeg imagemagick iproute2 git sqlite3 libsqlite3-dev python3 python3-dev ca-certificates dnsutils tzdata zip tar curl build-essential libtool -y
RUN            apt install gconf-service libasound2 libatk1.0-0 libc6 libcairo2 libcups2 libdbus-1-3 -y
RUN            apt install libexpat1 libfontconfig1 libgcc1 libgconf-2-4 libgdk-pixbuf2.0-0 libglib2.0-0 libgtk-3-0 libnspr4 libgbm-dev libexpat1 libfontconfig1 libgcc1 libgconf-2-4 libgdk-pixbuf2.0-0 libglib2.0-0 libgtk-3-0 libnspr4 libpango-1.0-0 libpangocairo-1.0-0 libstdc++6 libx11-6 libx11-xcb1 libxcb1 libxcomposite1 libxcursor1 libxdamage1 libxext6 libxfixes3 libxi6 libxrandr2 libxrender1 libxss1 libxtst6 ca-certificates fonts-liberation libappindicator1 libnss3 lsb-release xdg-utils wget -y
RUN            apt install libpango-1.0-0 libpangocairo-1.0-0 libstdc++6 libx11-6 libx11-xcb1 libxcb1 libxcomposite1 -y
RUN            apt install libxcursor1 libxdamage1 libxext6 libxfixes3 libxi6 libxrandr2 libxrender1 libxss1 libxtst6 ca-certificates fonts-liberation libnss3 lsb-release xdg-utils wget neofetch -y
RUN            npm -g install npm@latest
RUN            npm i -g pm2
RUN            npm install -g puppeteer --unsafe-perm=true -allow-root
RUN            curl -s https://install.speedtest.net/app/cli/install.deb.sh | bash 
RUN            apt install speedtest-cli php -y
RUN            useradd -m -d /home/container container
RUN            touch BY SHIELD
RUN            speedtest --accept-license
RUN            curl https://raw.githubusercontent.com/Kanvret12/BOT-PLUGINS/master/run.js
USER        container
ENV         USER=container HOME=/home/container
WORKDIR     /home/container
RUN            touch BY SHIELD.ID
CMD         [ "bash"]
