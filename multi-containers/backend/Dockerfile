# First we want to use a base image. This will go to Docker Hub and fetch the latest Node image.
FROM node
# Let's set up a working driectory.
WORKDIR /app
# First we need to copy this file in order not to run 'npm i' over and over again.
COPY package.json .
# After the 'package.json' file has been copied, we'll run this on our initial build.
RUN npm install
# After that, we'll copy this working directory '.' into the one we've setup earlier '.' = '/app'.
COPY . .
# We also need to expose a port for the client to use (send http requests to).
EXPOSE 80
# Let's set up some ENV variables (for the DB to connect) 
# -> 'root' & 'secret' are defaults; we'll use the real ones during runtime.
ENV MONGODB_USERNAME=root
ENV MONGODB_PASSWORD=secret
# ... and finally, we'll run this command, as ususal. This will run nodemon.
CMD [ "npm", "start" ]

