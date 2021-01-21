FROM node:latest

WORKDIR /usr/src/app

COPY ./package.json ./

RUN yarn install

COPY . .

RUN yarn build
RUN yarn global add serve

EXPOSE 80

CMD [ "serve", "-s", "build", "-l", "80"]
