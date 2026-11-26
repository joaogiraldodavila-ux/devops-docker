FROM ubuntu:22.04

ENV DEBIAN_FRONTEND=noninteractive

WORKDIR /usr/src/app

RUN apt-get update && apt-get install -y curl && \
    curl -sL https://deb.nodesource.com/setup_16.x | bash - && \
    apt-get install -y nodejs && \
    rm -rf /var/lib/apt/lists/*

COPY . .

RUN npm install && npm run build && npm install -g serve

CMD ["serve", "-s", "-l", "5001", "build"]