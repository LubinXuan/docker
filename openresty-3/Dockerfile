FROM openresty/openresty:1.19.3.1-1-centos

COPY qrencode /qrencode

CMD ["/usr/local/openresty/bin/openresty", "-g", "daemon off;"]
STOPSIGNAL SIGQUIT