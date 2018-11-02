# Lets use latest LTS version of the node
FROM node:10-alpine

# Create a work directory and copy over our dependency manifest files.
RUN mkdir /app

WORKDIR /app

#COPY ["package.json", "package-lock.json*", "./"]
COPY ./package.json .

RUN npm install

COPY . .

EXPOSE 8081

# Container should end with only one CMD command, which kicks off the process for the container
CMD ["npm", "start"]


