FROM node:16

RUN mkdir -p /home/node/app && chown -R node:node /home/node/app
WORKDIR /home/node/app
COPY ../web.js ./
RUN npm install
COPY . .
COPY --chown=node:node . .
USER node
EXPOSE 8080

CMD [ "npm", "start" ]