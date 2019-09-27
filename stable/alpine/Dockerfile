FROM python:3.7-alpine

LABEL maintainer="Cleber J Santos <cleber@cleberjsantos.com.br>"
ENV PYTHONUNBUFFERED=1 \ 
    ADDRESS=0.0.0.0 \
    PORT=9999

RUN apk --update add --no-cache --virtual .build-deps \
    build-base \
    python3-dev \
    linux-headers \
    openssl-dev \
    libffi-dev \
  && pip3 install --no-cache-dir webssh \
  && apk del .build-deps \
  && rm -rf /var/cache/apk/* /tmp/* /var/tmp/*

EXPOSE $PORT
ENTRYPOINT wssh --address=$ADDRESS --port=$PORT
