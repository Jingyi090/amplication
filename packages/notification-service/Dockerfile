FROM node:18.20.4-alpine AS base

WORKDIR /app

COPY ./dist/packages/notification-service/package.json .

RUN npm i --omit=dev

COPY ./dist/packages/notification-service .

ENV PORT=3333
EXPOSE $PORT

ENTRYPOINT ["node", "./main.js"]