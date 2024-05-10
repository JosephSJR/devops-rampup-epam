# Use the official Node.js image as base
FROM node:14-alpine

# Set the working directory in the container
WORKDIR /usr/src/app

# Set the BACKEND_URL environment variable
ENV BACKEND_URL="internal-alb-frontend-backend-qa-2000162512.us-east-1.elb.amazonaws.com:3000"

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application files
COPY . .

# Expose the port your app runs on
EXPOSE 80

# Command to run your app
CMD ["node", "server.js"]

