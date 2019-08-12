FROM node:8.10-alpine

# install angular-cli as node user
RUN chown -R node:node /usr/local/lib/node_modules \
    && chown -R node:node /usr/local/bin

WORKDIR /node-app

COPY . /node-app

EXPOSE 3000

CMD ["npm","start"]