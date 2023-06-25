# Shardeum Installation Guide

## Official Documentation
https://docs.shardeum.org/node/run/validator

## Basics

```
passwd
sudo apt update
sudo apt upgrade -y
sudo apt autoremove -y
```

## SSH keys
```
mkdir ~/.ssh
echo "XXXX PUBLIC KEY" > ~/.ssh/authorized_keys
sed -i 's/^#ChallengeResponseAuthentication.*/ChallengeResponseAuthentication no/' /etc/ssh/sshd_config
sed -i 's/^#PasswordAuthentication.*/PasswordAuthentication no/' /etc/ssh/sshd_config
sed -i 's/^UsePAM.*/UsePAM no/' /etc/ssh/sshd_config
sudo reboot
```

## Packages
```
apt install -y \
curl \
docker.io
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
```

## Install
```
curl -O https://gitlab.com/shardeum/validator/dashboard/-/raw/main/installer.sh && chmod +x installer.sh && ./installer.sh
```
