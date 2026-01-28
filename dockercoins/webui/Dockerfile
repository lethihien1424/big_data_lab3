FROM node:18-slim

# Thiết lập thư mục làm việc
WORKDIR /app

# Khởi tạo file package.json nếu chưa có và cài đặt thư viện
RUN npm init -y && \
    npm install express redis@3 --no-audit --prefer-offline

# Copy mã nguồn vào container
COPY files/ /files/
COPY webui.js /

# Lệnh chạy ứng dụng
CMD ["node", "/webui.js"]