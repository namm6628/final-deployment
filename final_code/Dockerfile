FROM node:20-alpine

WORKDIR /app

# copy dependency trước để cache đúng
COPY package*.json ./

# dùng lock file → tránh vuln cũ
RUN npm ci --omit=dev

# copy source code
COPY . .

EXPOSE 3000
CMD ["node", "main.js"]