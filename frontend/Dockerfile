# frontend/Dockerfile
FROM node:22-alpine
WORKDIR /app

# install deps
COPY package*.json ./
RUN if [ -f package-lock.json ]; then npm ci; else npm install; fi

COPY . .

ENV HOST=0.0.0.0
ENV PORT=3000

EXPOSE 3000
CMD ["npm", "start"]
