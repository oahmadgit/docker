# Use the official Node.js image as the build stage.
FROM node:14 as build

# Set the working directory.
WORKDIR /usr/src/app

# Copy the package.json and package-lock.json files.
COPY package*.json ./

# Install dependencies.
RUN npm install

# Copy the rest of the application code.
COPY . .

# Build the application.
RUN npm run build

# Use an official Nginx image to serve the static files.
FROM nginx:alpine

# Copy the built React app from the build stage.
COPY --from=build /usr/src/app/build /usr/share/nginx/html

# Expose the port the app runs on.
EXPOSE 80

# Start Nginx when the container starts.
CMD ["nginx", "-g", "daemon off;"]
