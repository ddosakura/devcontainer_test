# System Dependencies

```bash
# https://tauri.app/v1/guides/getting-started/prerequisites
sudo apt update
sudo apt install libwebkit2gtk-4.0-dev \
    build-essential \
    curl \
    wget \
    libssl-dev \
    libgtk-3-dev \
    libayatana-appindicator3-dev \
    librsvg2-dev

# dpkg -l
apt list --installed | grep -E -i -w 'libwebkit2gtk-4.0-dev|build-essential|curl|wget|libssl-dev|libgtk-3-dev|libayatana-appindicator3-dev|librsvg2-dev'

# build-essential/now 12.8ubuntu1.1 amd64 [installed,local]
# curl/now 7.68.0-1ubuntu2.15 amd64 [installed,local]
# libssl-dev/now 1.1.1f-1ubuntu2.16 amd64 [installed,local]
# wget/now 1.20.3-1ubuntu2 amd64 [installed,local]

docker exec -ti <id> /bin/bash
apt update
#  --no-install-recommends 参数来避免安装非必须的文件，从而减小镜像的体积
apt install -y --no-install-recommends libwebkit2gtk-4.0-dev \
    libgtk-3-dev \
    libayatana-appindicator3-dev \
    librsvg2-dev
```
