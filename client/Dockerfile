FROM node:16 as build

WORKDIR /app
COPY  . .

RUN npm install

FROM node:18-alpine

COPY --from=build /app /
EXPOSE 3000
CMD [ "npm", "start" ]