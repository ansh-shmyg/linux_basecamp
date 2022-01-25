# SFTP

# Usage

### Build
```
docker build -t sftp-server ./
```
### Docker run
```
docker run -p 22:22 -d sftp-server --name sftp-server user:pass:::

```