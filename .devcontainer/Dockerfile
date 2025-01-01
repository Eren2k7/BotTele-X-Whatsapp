# Menggunakan Alpine Linux sebagai base image
FROM alpine:latest

USER root

# Instalasi dasar
RUN apk update && apk add --no-cache \
    bash \
    curl \
    wget \
    git \
    gh \
    nodejs \
    npm

# Instalasi NVM
ENV NVM_DIR=/usr/local/nvm
RUN mkdir -p $NVM_DIR && \
    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash && \
    . $NVM_DIR/nvm.sh && \
    nvm install 18 && \
    nvm alias default 18

# Menetapkan user default sebagai root
USER root

# Set bash sebagai default shell
CMD ["bash"]
