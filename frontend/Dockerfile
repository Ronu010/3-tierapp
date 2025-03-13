# Use Node.js base image for building React app
FROM node:20 AS build

# Set the working directory
WORKDIR /app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy all project files
COPY . .

# Build the React app
RUN npm run build

# Use Nginx for serving the built files
FROM nginx:1.25

# Copy build files to Nginx's html folder
COPY --from=build /app/dist /usr/share/nginx/html

# Expose the frontend port
EXPOSE 80
