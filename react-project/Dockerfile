FROM node:12-stretch AS build
WORKDIR /app
COPY . .
RUN npm ci && npm run build

FROM nginx:latest
COPY --from=build /app/build /usr/share/nginx/html