FROM nginx:stable

MAINTAINER wmt 'wangmt@firstgrid.cn'

ENV NODE_VERSION 6.9.2

RUN apt-get update \
 && apt-get install --no-install-recommends --no-install-suggests -y \
 && apt-get install --yes wget \
 && wget https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-x64.tar.gz \
 && tar -xvf "node-v$NODE_VERSION-linux-x64.tar.gz" -C /usr/local --strip-components=1 \
 && ln -s /usr/local/bin/node /usr/local/bin/nodejs
 && npm install cnpm -g

CMD [ "node" ]
