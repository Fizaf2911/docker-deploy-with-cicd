FROM node:18

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

RUN adduser --disabled-password appuser

RUN chown -R appuser:appuser /app

USER appuser

EXPOSE 3000

CMD ["node", "app.js"]
