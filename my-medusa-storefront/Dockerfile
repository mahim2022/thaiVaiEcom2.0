FROM node:20-alpine
WORKDIR /app

ENV NODE_ENV=production
ENV PORT=8000

COPY package.json yarn.lock .yarnrc.yml ./
COPY .yarn/releases .yarn/releases

RUN yarn install

COPY . .

EXPOSE 8000

CMD ["sh", "-c", "yarn build && yarn start -p 8000"]
