FROM node:14

# set working directory
WORKDIR /usr/src/app

# add `/app/node_modules/.bin` to $PATH
ENV PATH /app/node_modules/.bin:$PATH

# install app dependencies
COPY rails-react-app/package.json ./
COPY rails-react-app/package-lock.json ./
RUN npm install --silent
RUN npm install react-scripts@3.4.1 -g --silent

# add app
COPY ./rails-react-app/ ./

# start app
CMD ["npm", "start"]
