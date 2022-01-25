# SFTP

# Usage

### Build
```
docker build -t ssh-server ./
```
### Docker run
```
docker run -d \
  --name=openssh-server \
  -e PUID=1000 \
  -e PGID=1000 \
  -e TZ=UTC \
  -e SUDO_ACCESS=true \
  -e PASSWORD_ACCESS=true \
  -e USER_PASSWORD=pass \
  -e USER_NAME=user \
  -p 2222:2222 \
  --restart unless-stopped \
  ssh-server

```

### Docker run alternative
```
docker run -d \
  --name=openssh-server \
  -e PUID=1000 \
  -e PGID=1000 \
  -e TZ=UTC \
  -e SUDO_ACCESS=true \
  -e PASSWORD_ACCESS=true \
  -e USER_PASSWORD=pass \
  -e USER_NAME=user \
  -p 2222:2222 \
  --restart unless-stopped \
  lscr.io/linuxserver/openssh-server

```