FROM adoptopenjdk/openjdk12:jdk-12.0.2_10-slim

LABEL maintainer="silvio.wangler@gmail.com"

ADD endless.sh /endless.sh

RUN apt-get update && \
    apt-get install -y --no-install-recommends git openssh-client tar gzip ca-certificates && \
    rm -rf /var/lib/apt/lists/* && \
    chmod +x /endless.sh

LABEL com.circleci.preserve-entrypoint=true

ENTRYPOINT ["/endless.sh"]