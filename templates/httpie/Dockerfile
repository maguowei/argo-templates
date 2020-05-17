FROM alpine:3.11

RUN apk add --update --no-cache python3 && \
    pip3 install --upgrade pip setuptools httpie && \
    rm -rf /root/.cache
