# Sui Fullnode Installation Guide

## Official Documentation
https://docs.sui.io/build/fullnode

## Prerequisites

### Packages
```
apt-get update \
&& apt-get install -y --no-install-recommends \
tzdata \
ca-certificates \
build-essential \
pkg-config \
cmake
```

### Docker

https://docs.docker.com/
```
apt-get install -y \
docker.io
```

## Sui Installation

### Fullnode template
```
wget https://github.com/MystenLabs/sui/raw/main/crates/sui-config/data/fullnode-template.yaml
```

### Get docker compose file
```
wget https://raw.githubusercontent.com/MystenLabs/sui/main/docker/fullnode/docker-compose.yaml
```

### get latest version of genesis devnet file
```
wget https://github.com/MystenLabs/sui-genesis/raw/main/devnet/genesis.blob
```

### Start / stop fullnode
```
docker compose up -d
```
```
docker compose down
```

### Get fullnode container logs
```
docker ps
docker logs --follow --tail 1 $SUI_CONTAINER_ID
```

## Troubleshoot

Go to https://node.sui.zvalid.com/ -> enter your IP  
or go to https://explorer.devnet.sui.io/ -> custom RPC URL -> enter your IP

## Start fullnode as a service
```
to do
```