FROM node:18

WORKDIR /app

# Copy package files first for better caching
COPY package.json package-lock.json* ./

# Install dependencies with explicit platform flag
RUN npm install --platform=linux --arch=x64

# Copy the rest of the application
COPY . .

# Expose Vite dev server port
EXPOSE 5173

# Command to run the application
CMD ["npm", "run", "dev", "--", "--host", "0.0.0.0"]