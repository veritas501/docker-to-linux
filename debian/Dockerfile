FROM amd64/debian:bullseye
LABEL com.iximiuz-project="docker-to-linux"
RUN apt-get -y update
RUN apt-get -y install --no-install-recommends \
  linux-image-amd64 \
  systemd-sysv
RUN apt-get -y install netcat openssh-server net-tools iproute2 ifupdown wget curl git vim
RUN (echo "root:root" | chpasswd) && \
    (mkdir -p /etc/network) && \
    (printf "\nauto eth0\niface eth0 inet dhcp\n" | tee -a /etc/network/interfaces)

