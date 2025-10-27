# Use an official lightweight Node.js base image
FROM node:18-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy package files first (for better build caching)
COPY package*.json ./

# Install production dependencies
RUN npm install --production

# Copy the rest of the application code
COPY . .

# Expose the app port (adjust if different)
EXPOSE 3000

# Run the app
CMD ["npm", "start"]
