FROM node:16.0.0
WORKDIR /usr/src/app
COPY ["package.json", "yarn.lock", "./"]
RUN yarn install
COPY . .
RUN yarn build
RUN yarn global add serve
ENTRYPOINT [ "serve", "-l", "80", "-s", "build" ]