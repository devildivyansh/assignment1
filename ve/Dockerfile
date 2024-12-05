# Step 1: Use an official Node.js image as the base image
FROM node:18-slim

# Step 2: Set the working directory inside the container
WORKDIR /app

# Step 3: Copy package.json and package-lock.json to the container
COPY package*.json ./

# Step 4: Install dependencies inside the container
RUN npm install

# Step 5: Copy the rest of the application code
COPY . .

# Step 6: Build the application for production
RUN npm run build

# Step 7: Expose the port the app will run on
EXPOSE 3000

# Step 8: Set the command to run the application
CMD ["npm", "run", "preview"]
    