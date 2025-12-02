# ===== Backend Dockerfile =====

# Stage 1: Build
FROM node:18-alpine

# Set working directory
WORKDIR /app

# Copy package.json first (better layer caching)
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the backend code
COPY . .

# Expose backend port
EXPOSE 4000

# Start server
CMD ["npm", "start"]
