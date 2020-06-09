FROM node:12.16.3-alpine3.9

RUN mkdir -p /var/www/blowstack/blowstack
WORKDIR /var/www/blowstack/blowstack

COPY package*.json ./
RUN npm install

COPY . .

RUN npm run build
#RUN firebase deploy

EXPOSE 3000

ENV NUXT_HOST=0.0.0.0

ENV NUXT_PORT=3000

CMD [ "npm", "start" ]

