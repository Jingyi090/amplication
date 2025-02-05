FROM node:18.20.6 AS base

WORKDIR /app

COPY ./dist/ee/packages/amplication-git-pull-service/package.json .

RUN npm i --omit=dev

COPY ./dist/ee/packages/amplication-git-pull-service .

ENV PORT=3333
EXPOSE $PORT

ENTRYPOINT ["node", "./main.js"]