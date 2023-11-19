FROM nginx
WORKDIR /home/
COPY ./nginx.conf .
COPY ./hello_world.c .
COPY ./run.sh .

RUN apt-get update \
    && apt-get install -y gcc spawn-fcgi libfcgi-dev \
    && rm -rf /var/lib/apt/lists/*

USER nginx

ENTRYPOINT ["sh", "./run.sh"]
