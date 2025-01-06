FROM rust:1.83-bookworm AS builder

RUN apt update && apt install -y libwebkit2gtk-4.0-dev \
  build-essential \
  curl \
  wget \
  file \
  libssl-dev \
  libgtk-3-dev \
  libayatana-appindicator3-dev \
  librsvg2-dev

RUN apt install -y nodejs npm

RUN npm install -g pnpm
RUN pnpm config set registry https://registry.npmmirror.com/
WORKDIR /app