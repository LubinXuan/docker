FROM openresty/openresty:1.19.3.1-1-alpine

COPY qrencode /qrencode

RUN apk add --no-cache --virtual .build-deps \
        build-base \
        coreutils \
        curl \
        gd-dev \
        geoip-dev \
        libxslt-dev \
        linux-headers \
		libpng-dev \
		libqrencode-dev \
        make \
        readline-dev \
        zlib-dev \
    && apk add --no-cache \
		libpng \
		libqrencode \
	&& cd /qrencode \
	&& make && make install \

CMD ["/usr/local/openresty/bin/openresty", "-g", "daemon off;"]
STOPSIGNAL SIGQUIT