# UnraidFactorio [![](https://images.microbadger.com/badges/image/aeonlucid/unraidfactorio.svg)](https://microbadger.com/images/aeonlucid/unraidfactorio) [![Docker Pulls](https://img.shields.io/docker/pulls/aeonlucid/unraidfactorio.svg)](https://hub.docker.com/r/aeonlucid/unraidfactorio/) [![Docker Stars](https://img.shields.io/docker/stars/aeonlucid/unraidfactorio.svg)](https://hub.docker.com/r/aeonlucid/unraidfactorio/)

* `latest` - most up-to-date version (may be experimental).

> This is a fork of https://github.com/dtandersen/docker_factorio_server.  
> Usage should be the same.  
> Only change is [PUID / PGID](https://www.linuxserver.io/docs/puid-pgid/) environment variable support.

# Usage

## Quick Start

Run the server to create the necessary folder structure and configuration files. For this example data is stored in `/opt/factorio`.

```
sudo mkdir -p /opt/factorio
sudo chown 845:845 /opt/factorio
sudo docker run -d \
  -p 34197:34197/udp \
  -p 27015:27015/tcp \
  -v /opt/factorio:/factorio \
  -e PUID=1000 \
  -e PGID=1000 \
  --name factorio \
  --restart=always \
  aeonlucid/unraidfactorio
```
