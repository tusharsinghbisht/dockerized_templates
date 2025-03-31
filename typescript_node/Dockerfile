FROM node:18-alpine as base 

WORKDIR /app

COPY package.json .
COPY package-lock.json .

RUN npm install

ENV PORT=8000
EXPOSE 8000
COPY . .

FROM base as development
ENV NODE_ENV=developement
CMD ["npm", "run", "dev"]


FROM base as production
ENV NODE_ENV=production
RUN npm run build
RUN npm prune --production
CMD ["npm", "start"]