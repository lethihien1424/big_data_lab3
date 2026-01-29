FROM node:18-slim

# cài yarn
RUN apt-get update && apt-get install -y --no-install-recommends yarnpkg \
    && rm -rf /var/lib/apt/lists/*

# cài dependencies bằng yarn (né lỗi npm idealTree)
RUN yarnpkg add express redis@3

COPY files/ /files/
COPY webui.js /
CMD ["node", "webui.js"]
EXPOSE 80
