# 1. Chọn môi trường chạy (Node.js phiên bản 20 trên Alpine Linux cho nhẹ)
FROM node:20-alpine

# 2. Tạo thư mục làm việc trong container
WORKDIR /app

# 3. Copy file quản lý thư viện vào trước để tận dụng cache
COPY package*.json ./

# 4. Cài đặt thư viện
RUN npm install

# 5. Copy toàn bộ code còn lại vào container
COPY . .

# 6. Mở cổng mà ứng dụng Node.js của bạn chạy (ví dụ 3000)
EXPOSE 3000

# 7. Lệnh khởi chạy ứng dụng
CMD ["npm", "start"]
