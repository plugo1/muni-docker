FROM jenkins/jenkins:2.479.3

USER root

# Dependencias básicas
RUN apt-get update && apt-get install -y \
    docker.io \
    wget \
    curl \
    software-properties-common \
    apt-transport-https \
    ca-certificates \
    gnupg

# Instalar kubectl
RUN curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl" \
    && chmod +x kubectl \
    && mv kubectl /usr/local/bin/

# Repositorio y SDK .NET
RUN wget https://packages.microsoft.com/config/ubuntu/20.04/packages-microsoft-prod.deb -O packages-microsoft-prod.deb \
    && dpkg -i packages-microsoft-prod.deb \
    && rm packages-microsoft-prod.deb

RUN apt-get update && apt-get install -y dotnet-sdk-8.0

# Limpiar
RUN apt-get clean && rm -rf /var/lib/apt/lists/*

USER jenkins
EXPOSE 8080

