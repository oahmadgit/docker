# Use the official Node.js image.
# https://hub.docker.com/_/node
FROM node:14

# Create and change to the app directory.
WORKDIR /usr/src/app

# Install app dependencies using the `npm ci` command instead of `npm install`.
# This command uses the package-lock.json file to ensure the exact same dependencies are installed.
COPY package*.json ./
RUN npm ci --only=production

# Copy the rest of the application code.
COPY . .

# Expose the port the app runs on.
EXPOSE 3000

# Run the application.
CMD ["node", "server.js"]
