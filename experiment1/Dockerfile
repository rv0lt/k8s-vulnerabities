#Example of Dockerfile that does NOT run as root

# Use an official Node runtime as a parent image
FROM node:14-alpine

# Set the working directory in the container to /app
WORKDIR /app

# Copy package.json and package-lock.json into the directory
COPY package*.json ./

# Install any needed packages
RUN npm install

# Copy the rest of your app's source code from your host to your image filesystem.
COPY . .

# Run the application with the non-root user
USER node

# Make port 8080 available to the world outside this container
EXPOSE 8080

# Run the app when the container launches
CMD ["node", "index.js"]
