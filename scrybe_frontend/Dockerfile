# pull the official base image
FROM node:14-alpine as build

# set work directory
WORKDIR /scrybe_frontend

# install dependencies
COPY package*.json ./
RUN npm install --force

# copy project
COPY . .

EXPOSE 3000

RUN npm run dev

# FROM nginx:1.19

# COPY ./nginx/nginx.conf etc/nginx/nginx.conf

# COPY --from=build /scrybe_frontend/dist /usr/share/nginx/html