FROM node:14

WORKDIR /usr/src/app/demo

COPY package.json .
COPY yarn.lock .


RUN yarn

EXPOSE 8080

CMD ["yarn", "serve"]