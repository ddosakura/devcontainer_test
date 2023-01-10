FROM ddosakura/hakke:1.1.0

USER root

# https://github.com/devcontainers/features/tree/main/src/desktop-lite#installing-a-browser

# https://askubuntu.com/questions/1406527/why-doesnt-ubuntu-provide-firefox-esr-in-its-repositories
# RUN apt-get update && export DEBIAN_FRONTEND=noninteractive && apt-get install -y firefox-esr
# RUN snap install firefox --channel=esr/stable

# https://blog.csdn.net/chengly0129/article/details/72178806
# https://stackoverflow.com/questions/59087200/google-chrome-failed-to-move-to-new-namespace/64460373#64460373
# https://stackoverflow.com/questions/50662388/running-headless-chrome-puppeteer-with-no-sandbox/53975412#53975412
# docker 使用特权容器(或使用 security_opt 进行细粒度配置) --privileged 且使用非根用户
# 或 google-chrome --no-sandbox
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && curl -sSL https://dl.google.com/linux/direct/google-chrome-stable_current_$(dpkg --print-architecture).deb -o /tmp/chrome.deb \
    && apt-get -y install --no-install-recommends /tmp/chrome.deb

USER vscode
