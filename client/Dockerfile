FROM node:13.12.0-alpine as build
WORKDIR /app
COPY package.json . ./
RUN npm install --only=production
FROM node:13.12.0-alpine as main
COPY --from=build /app /
EXPOSE 3000
CMD [ "npm", "start" ]