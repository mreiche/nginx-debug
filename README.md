# Nginx Debug

## Build
```shell
podman build -f Dockerfile --platform linux/amd64 . -t "nginx-debug"
```
## Run

```shell
podman run --rm -p 8080:8080 --name my-nginx nginx-debug nginx-debug -g 'daemon off;'
```

## Test
```shell
curl -H 'H: First' -H 'H: Second' localhost:8080
```

## References
- https://stackoverflow.com/questions/24380123/how-to-log-all-headers-in-nginx
- https://docs.okd.io/latest/networking/routes/route-configuration.html#nw-route-specific-annotations_route-configuration
