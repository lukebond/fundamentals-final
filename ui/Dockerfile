FROM node:9-alpine
ADD package.json /build/package.json
WORKDIR /build
RUN npm install
ADD . /build
CMD node src/server.js
