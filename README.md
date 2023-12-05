# Nginx Debug

## Build
```shell
podman build -f Dockerfile . -t "nginx-debug"
```
## Run

```shell
podman run --rm -p 8080:8080 --name my-nginx nginx-debug nginx-debug -g 'daemon off;'
```
