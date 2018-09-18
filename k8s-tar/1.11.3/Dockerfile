FROM ubuntu:16.04

LABEL maintainer Late Lee(li@latelee.org)

# version here
ENV K8S_VERSION v1.11.3

ENV ETCD_VERSION v3.3.9
ENV FLANNEL_VERSION v0.10.0

RUN apt-get update || true && \
    apt-get install -y \
    wget && \
    rm -rf /var/lib/dpkg/info/* /var/lib/apt/lists/*

RUN wget -c https://dl.k8s.io/${K8S_VERSION}/kubernetes-server-linux-amd64.tar.gz

RUN wget -c https://dl.k8s.io/${K8S_VERSION}/kubernetes-client-linux-amd64.tar.gz

RUN wget -c https://dl.k8s.io/${K8S_VERSION}/kubernetes-node-linux-arm64.tar.gz

RUN wget -c https://github.com/etcd-io/etcd/releases/download/${ETCD_VERSION}/etcd-${ETCD_VERSION}-linux-amd64.tar.gz

RUN wget -c https://github.com/coreos/flannel/releases/download/${ETCD_VERSION}/flannel-${ETCD_VERSION}-linux-amd64.tar.gz

CMD ["/bin/bash"]
