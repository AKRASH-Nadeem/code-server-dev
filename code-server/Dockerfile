FROM codercom/code-server:latest

# Update and install dependencies
RUN sudo apt-get update && sudo apt-get install -y \
    # Install PHP
    php-cli php-mysql php-curl php-mbstring php-xml php-zip \
    # Install Node.js and npm
    nodejs npm \
    # Install Python
    python3 python3-pip \
    && sudo apt-get clean && sudo rm -rf /var/lib/apt/lists/*

# Install VS Code extensions
RUN code-server --install-extension formulahendry.code-runner && \
    code-server --install-extension ms-python.python && \
    code-server --install-extension esbenp.prettier-vscode

WORKDIR /config/workspace