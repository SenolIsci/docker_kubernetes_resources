# Specify a base image
FROM node:alpine

#add work directory
WORKDIR /usr/app

# Install some depenendencies
#first copy json conf file which is needed by npm isntall
COPY ./package.json ./
RUN npm install

#then copy all to prevent "npm install" to rerun each time a program file changed.
COPY ./ ./

# Default command
CMD ["npm", "start"]