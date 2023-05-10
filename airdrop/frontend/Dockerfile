# Use an official Node.js runtime as a parent image
FROM node:18-alpine

# Set the working directory to /app
WORKDIR /airdropui

# Copy the package.json and package-lock.json files to the container
COPY ./airdropui/package*.json ./

# Install the dependencies
RUN npm install

# Copy the rest of the application code to the container
COPY ./airdropui .

# Build the Angular application for production
RUN npm run build --prod

# Expose the port that the application will run on
EXPOSE 80

# Set the command to run when the container starts
CMD ["npm", "start"]
