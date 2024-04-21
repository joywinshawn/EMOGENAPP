FROM node:21-alpine3.18

WORKDIR /app

RUN npm cache clean --force

RUN rm -rf package-lock.json node_modules

COPY package.json /app/

RUN npm install

RUN npm install -g npm@latest

COPY ../ /app/

EXPOSE 5173

CMD ["npm", "run", "dev"]
