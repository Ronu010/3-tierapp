# Use Node.js base image
FROM node:20

# Set the working directory
WORKDIR /app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy all project files
COPY . .

# Expose the backend port
EXPOSE 5000

# Command to run the app
CMD ["node", "server.js"]
