FROM node:14.15.4-alpine3.12

WORKDIR /var/www/app/

COPY ./client-app ./

RUN apk update && \
    apk add python3 && \
    apk add make && \
    apk add g++

RUN npm install --quiet

RUN npm run build

EXPOSE 3000

CMD ["npm", "run" ,"start"]