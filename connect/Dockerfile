FROM alpine:3.21.3

RUN apk add --no-cache \
    bash \
    curl \
    ca-certificates \
    unzip \
    && curl https://rclone.org/install.sh | bash \
    && mkdir -p /config/rclone

VOLUME /config/rclone    

COPY entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh

ENTRYPOINT ["/entrypoint.sh"]