FROM amd64/ubuntu:21.10
LABEL com.iximiuz-project="docker-to-linux"
RUN apt-get update -y
RUN apt-get -y install \
  linux-image-virtual \
  systemd-sysv
RUN apt-get -y install socat netcat openssh-server net-tools iproute2 ifupdown wget curl git vim
RUN (echo "root:root" | chpasswd) && \
    (mkdir -p /etc/network) && \
    (printf "\nauto eth0\niface eth0 inet dhcp\n" | tee -a /etc/network/interfaces)

