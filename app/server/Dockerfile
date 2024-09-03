# Single-stage Dockerfile for Express.js

FROM node:20-alpine

# Set working directory
WORKDIR /app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install --only=production

# Copy the rest of the application files
COPY . .

# Set default environment variables
ENV ATLAS_URI=mongodb://localhost:27017/mydatabase
ENV PORT=5050

# Expose the port the app runs on
EXPOSE 5050

# Start the application
CMD ["node", "server.js"]  
