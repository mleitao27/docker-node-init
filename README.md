# Single guide to getting node projects initialized with docker
## 1 - Install [Git](https://git-scm.com/) and [Docker](https://www.docker.com/)
## 2 - Clone this repository
```
git clone git@github.com:mleitao27/docker-node-init.git
```
## 3 - Open a terminal in the docker-node-init directory
```
cd docker-node-init
```
## 4 - Run docker-compose
```
docker-compose -f docker-compose.yml up -d
```
## 5 - Access the containers terminal
```
docker exec -it <CONTAINER ID> /bin/bash
```
Note: You can check the <CONTAINER ID> by running the command below and getting the id associated with the image goparity-challenge-node-init.
```
docker ps
```
Another note: You may need to specify the terminal you want to use **/bin/bash** only works for both Linux and macOS, for Windows try **/bin/sh**.
## 6 - In the container's terminal run the command to create your project
Example for [Vue.js](https://vuejs.org/):
```
npm create vue@latest
```
Example for [React](https://react.dev/):
```
npx create-next-app@latest
```
## 7 - Now you should already see your project in the filetree, copy it to wherever you want
```
cp -R <PROJECT DIR> <DST PATH>
```
## 8 - Stop the container and remove the container
```
docker stop <CONTAINER ID>
```
```
docker rm <CONTAINER ID>
```
