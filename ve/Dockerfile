# Use Node.js base image for building the frontend
FROM node:16-alpine AS build

# Set working directory
WORKDIR /app

# Copy package files and install dependencies
COPY package*.json ./
RUN npm install

# Copy the rest of the code
COPY . .

# Build the app
RUN npm run build

# Serve the app with Nginx
FROM nginx:1.21-alpine
COPY --from=build /app/dist /usr/share/nginx/html

# Expose the frontend port (e.g., 80)
EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]