FROM node:22-alpine

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

EXPOSE 3000

CMD ["node", "index.js"]



docker login

docker build -t <username>/docker-test-app:latest .

docker build -t samaysamrat/docker-test-app:latest .


docker push <username>/docker-test-app:latest

