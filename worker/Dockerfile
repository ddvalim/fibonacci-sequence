FROM node:14.18-alpine3.13

WORKDIR /app/server

COPY ./package.json /app/server

RUN npm install

COPY . /app/server

CMD ["npm", "run", "start"]