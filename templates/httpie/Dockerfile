FROM alpine:3.11

RUN apk add --update --no-cache python3 && \
    pip3 install -U pip httpie && \
    rm -rf /root/.cache
