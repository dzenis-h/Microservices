# React uses node during development
FROM node
# Let's set up a working driectory
WORKDIR /app
# First we need to copy this file in order not to run 'npm i' over and over again
COPY package.json .
# After the 'package.json' file has been copied, we'll run this on our initial build
RUN npm install
# After that, we'll copy this working directory '.' into the one we've setup earlier '.' = '/app'
COPY . .
# We also need to expose this port for the browser to use
EXPOSE 3000
# ... and finally, we'll run this command, as ususal
CMD [ "npm", "start" ]