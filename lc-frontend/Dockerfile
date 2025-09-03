# Stage 1: Build the Next.js application
FROM node:18-alpine AS builder

# Set the working directory
WORKDIR /app

# Copy package.json and package-lock.json to leverage Docker cache
COPY package.json package-lock.json ./

# Install dependencies
RUN npm ci

# Copy the rest of the application code
COPY . .

# Build the Next.js app for production
RUN npm run build

# Stage 2: Create the production-ready image
FROM node:18-alpine AS runner

# Set the working directory
WORKDIR /app

# Copy the standalone output from the builder stage
COPY --from=builder /app/.next/standalone ./

# Copy public and .next/static folders
COPY --from=builder /app/public ./public
COPY --from=builder /app/.next/static ./.next/static

# Expose the port
EXPOSE 3000

# Set environment variables for production
ENV NODE_ENV production

# Start the Next.js server
CMD ["node", "server.js"]