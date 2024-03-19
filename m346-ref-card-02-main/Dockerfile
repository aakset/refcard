FROM node:20-alpine AS build
ENV NODE_ENV=development

WORKDIR /app
COPY package*.json ./
RUN npm ci --verbose
COPY . .
RUN npm run build

FROM nginx:1.21-alpine as prod
COPY --from=build /app/build /usr/share/nginx/html
EXPOSE 80
