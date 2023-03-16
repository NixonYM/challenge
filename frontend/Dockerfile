FROM node:18.12.0-alpine

WORKDIR /app

COPY package.json yarn.lock ./
RUN yarn --frozen-lockfile --non-interactive

COPY . .
RUN yarn build --mode production

EXPOSE 80

CMD ["yarn", "serve", "dist"]
