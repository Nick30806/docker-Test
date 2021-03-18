## This is Docker Test ##
-----------------------------------------------------
#### git clone https://github.com/HcwXd/docker-tutorial.git ####

#### cd docker-Test/docker-demo-app/ ####

#### vim Dockerfile ####
FROM node:10.15.3-alpine    *這行會載入 Node.js 需要的執行環境，每個不同的程式需要的環境可能都不同，這裏下載的是 node:10.15.3-alpine
WORKDIR /app                *
ADD . /app
RUN npm install
EXPOSE 3000
CMD node index.js
