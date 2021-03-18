## This is Docker Test ##
-----------------------------------------------------
#### git clone https://github.com/HcwXd/docker-tutorial.git ####

#### cd docker-Test/docker-demo-app/ ####

#### vim Dockerfile ####
-----------------------------------------------------
###### #FROM node:10.15.3-alpine    * 這行會載入 Node.js 需要的執行環境，每個不同的程式需要的環境可能都不同，這裏下載的是 node:10.15.3-alpine #######
###### #WORKDIR /app                * 在這個 Docker 的環境之中建立一個工作目錄 /app ######
###### #ADD . /app                  * 把跟 Dockerfile 同個資料夾的程式加到剛建立的工作目錄 /app 中 ######
###### #RUN npm install             * 運行 npm install，讓 npm 透過讀取 package.json 下載相依的 package ######
###### #EXPOSE 3000                 * 指定 container 對外開放的 port ######
###### #CMD node index.js           * 我們透過 node index.js 來執行我們的 Server ######
-----------------------------------------------------

#### docker build . -t docker-demo-app ####

#### docker images ####

#### docker run -p 3000:3000 -it "Repository"

#### docker ps ####

#### docker stop "Reposoitory" ####

