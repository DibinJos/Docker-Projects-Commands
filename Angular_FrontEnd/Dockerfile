FROM node:8.10-alpine

#install angular-cli as node user
RUN chown -R node:node /usr/local/lib/node_modules \
    && chown -R node:node /usr/local/bin

USER node
RUN npm install -g @angular/cli@6.2.5

#Set npm as the default package manager for the root
USER root
RUN ng set -g packageManager = npm

WORKDIR /app

COPY . .

EXPOSE 4200

CMD ["ng","serve","--host","0.0.0.0"]

