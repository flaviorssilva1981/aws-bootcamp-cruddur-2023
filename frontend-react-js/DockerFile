FROM node:16.18

WORKDIR /frontend-react-js

COPY . /frontend-react-js

ENV PORT=3000

RUN npm install

EXPOSE ${PORT}

CMD ["npm", "start"]
# ok agora