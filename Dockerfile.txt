FROM node:16

EXPOSE 3000

WORKDIR /app

RUN npm i npm@latest -g

COPY package.json package-lock.json* ./

RUN npm install --no-optional && npm cache clean --force

COPY . .

CMD ["node", "index.js"]