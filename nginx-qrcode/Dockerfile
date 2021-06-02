FROM alpine:3.8

RUN cat /etc/apk/repositories | sed -e "s/dl-cdn.alpinelinux.org/mirrors.aliyun.com/" | tee /etc/apk/repositories && \
    apk --update add openssl-dev pcre-dev zlib-dev wget build-base autoconf automake libtool libpng-dev libgd pcre pcre-dev pkgconfig gd-dev && \
    cd /tmp && \
    wget https://nginx.org/download/nginx-1.15.5.tar.gz && tar -zxvf nginx-1.15.5.tar.gz && rm -rf nginx-1.15.5.tar.gz && \
    wget https://github.com/dcshi/ngx_http_qrcode_module/archive/master.zip && unzip master.zip && mv ngx_http_qrcode_module-master ngx_http_qrcode_module && rm -rf master.zip && \
    wget https://github.com/fukuchi/libqrencode/archive/master.zip && unzip master.zip && mv libqrencode-master libqrencode && \
    cd libqrencode && ./autogen.sh && ./configure && make && make install && ldconfig || true && \
    cd /tmp/nginx-1.15.5 && ./configure --add-module=../ngx_http_qrcode_module/ && make && make install && \
    apk del build-base autoconf automake pkgconfig && \
    rm -rf /tmp/* && rm -rf /var/cache/apk/*

ADD nginx.conf /usr/local/nginx/conf/nginx.conf

EXPOSE 80

ENTRYPOINT [ "/usr/local/nginx/sbin/nginx", "-g", "daemon off;" ]
