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
```