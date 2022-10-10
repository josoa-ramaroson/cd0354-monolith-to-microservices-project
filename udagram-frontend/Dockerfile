FROM beevelop/ionic:latest AS ionic
# Create app directory
WORKDIR /usr/src/app
# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
COPY package*.json ./
RUN npm ci
<<<<<<< HEAD
# Regroupement des sources de l'application
COPY . ../projet3
RUN ionic init udacity-c2-frontend
#RUN ionic build
## Exécuter
FROM nginx:alpine
COPY www /usr/share/nginx/html
#COPY --from=ionic /usr/src/app/www /usr/share/nginx/html
=======
# Bundle app source
COPY . .
RUN ionic build
## Run 
FROM nginx:alpine
#COPY www /usr/share/nginx/html
COPY --from=ionic  /usr/src/app/www /usr/share/nginx/html
>>>>>>> master
