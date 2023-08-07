FROM node

RUN apt-get update
RUN apt-get upgrade -y

RUN mkdir /usr/app
RUN git clone https://github.com/jkjh8/bs_be.git /usr/app

WORKDIR /usr/app

RUN yarn
RUN yarn global add nodemon
RUN yarn global add pm2


EXPOSE 3000

ENV TZ=Asia/Seoul

# CMD [ "pm2-runtime", "start", "config.json" ]
CMD [ "yarn", "start"]
