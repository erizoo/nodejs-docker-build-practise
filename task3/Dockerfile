FROM node:16-alpine

WORKDIR /home/ilovedocker/app
COPY package*.json ./
# Флаг --omit=dev означает - "не ставить devDependencies"
# они не нужны нам в продакшен-окружении
RUN npm i --omit=dev
# копируем исходный код
COPY . .

EXPOSE 3032
CMD [ "node", "main.js" ] 