FROM node:18-alpine

ENV NODE_PATH=/app/node_modules
ENV PATH=$PATH:$NODE_PATH/.bin/


WORKDIR /app

COPY package.json /app
RUN npm install
RUN echo "module.exports = {extends: ['@commitlint/config-conventional']};" > /app/commitlint.config.js

ENTRYPOINT ["commitlint", "--config", "/app/commitlint.config.js"]
