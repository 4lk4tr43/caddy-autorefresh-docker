FROM alpine

RUN apk update
RUN apk add bash curl inotify-tools
RUN curl https://getcaddy.com | bash -s http.cache,http.cgi,http.cors,http.expires,http.filemanager,http.filter,http.forwardproxy,http.git,http.ipfilter,http.jwt,http.locale,http.login,http.mailout,http.minify,http.nobots,http.proxyprotocol,http.ratelimit,http.realip,http.reauth,http.upload

ADD ./src /src
ADD ./seed /mnt

VOLUME /mnt
VOLUME /root/.caddy

ENTRYPOINT /bin/bash /src/watch-caddyfile.sh