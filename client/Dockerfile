FROM node:14.2.0-alpine3.11 as build

WORKDIR /app/client

COPY ./package.json /app/client

RUN npm install

COPY . /app/client/

RUN npm run build

FROM nginx

EXPOSE 3000

COPY ./nginx/default.conf /etc/nginx/conf.d/default.conf

COPY --from=build /app/client/build /usr/share/nginx/html