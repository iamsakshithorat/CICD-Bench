FROM node:20-slim
WORKDIR /app

# Dependencies first: this layer is cached when package files do not change
COPY package*.json ./
RUN npm ci

# Source code last: changes here do not invalidate the layer above
COPY . .
CMD ["node", "index.js"]
