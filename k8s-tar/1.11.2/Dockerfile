FROM ubuntu:16.04

LABEL maintainer Late Lee(li@latelee.org)

# version here
ENV K8S_VERSION v1.11.2

RUN apt-get update || true && \
    apt-get install -y \
    wget && \
    rm -rf /var/lib/dpkg/info/* /var/lib/apt/lists/*

RUN wget -c https://dl.k8s.io/${K8S_VERSION}/kubernetes-server-linux-amd64.tar.gz

RUN wget -c https://dl.k8s.io/${K8S_VERSION}/kubernetes-client-linux-amd64.tar.gz

RUN wget -c  https://dl.k8s.io/${K8S_VERSION}/kubernetes-node-linux-arm64.tar.gz

CMD ["/bin/bash"]
