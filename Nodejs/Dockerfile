FROM node:16-alpine
LABEL maintainer="Hoang Bui <mynamebvh@gmail.com>"

WORKDIR /app/backend

RUN mkdir -p /node_modules && chown node:node -R /node_modules /app
RUN npm install -g pm2

USER node

COPY --chown=node:node package.json ./

RUN npm install

COPY --chown=node:node . ./

EXPOSE 3000
