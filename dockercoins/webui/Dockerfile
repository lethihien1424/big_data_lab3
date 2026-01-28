FROM node:18-slim
WORKDIR /app
RUN npm init -y && npm install express redis@3 --no-audit
COPY files/ /files/
COPY webui.js /
CMD ["node", "/webui.js"]