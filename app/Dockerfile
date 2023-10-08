FROM node:16

# Create app directory
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

# Install app dependency
# This allows you to take advantage of cached Docker layers.
COPY package*.json ./

RUN npm install
# If you are building your code for production
# RUN npm ci --omit=dev
# Reference: https://blog.npmjs.org/post/171556855892/introducing-npm-ci-for-faster-more-reliable

# Bundle app source
COPY . .

# Expose Bind Port
EXPOSE 3000

# To start your servre
CMD [ "npm", "run", "dev" ]
