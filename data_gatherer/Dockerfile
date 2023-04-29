FROM node:16-alpine

WORKDIR /data_gatherer

COPY package.json .
RUN npm install --quiet

COPY . .

CMD ["npm", "run", "start"]
