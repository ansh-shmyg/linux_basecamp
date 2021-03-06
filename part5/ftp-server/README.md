#
The source repo:
```https://github.com/delfer/docker-alpine-ftp-server```

## Usage

### Build
```
docker build -t ftp-server ./
```
### Docker run
```
docker run -d -p 21:21 -p 21000-21010:21000-21010 -e ADDRESS=ftp.site.domain --name ftp-server ftp-server
```

## Configuration

Environment variables:
- `USERS` - space and `|` separated list (optional, default: `ftp|alpineftp`)
  - format `name1|password1|[folder1][|uid1] name2|password2|[folder2][|uid2]`
- `ADDRESS` - external address witch clients can connect passive ports (optional)
- `MIN_PORT` - minimum port number to be used for passive connections (optional, default `21000`)
- `MAX_PORT` - maximum port number to be used for passive connections (optional, default `21010`)

## USERS examples

- `user|password foo|bar|/home/foo`
- `user|password|/home/user/dir|10000`
- `user|password||10000`
