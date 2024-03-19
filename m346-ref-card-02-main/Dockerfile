FROM node:20
WORKDIR /app
COPY ./m346-ref-card-02-main/package.json .
RUN npm install
RUN npm i esbuild
COPY ./m346-ref-card-02-main .
EXPOSE 80
CMD ["npm", "run", "dev"]
