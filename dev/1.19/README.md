# djbrain/go:dev-1.19

Image for starting go projects with hot reloading

## Usage
- start project
```
cd /path/to/project
docker run --rm -d \
 -p 8080:8080 \
 -v $(pwd):/var/www \
 djbrain/go:dev-1.19
```
- using in docker-compose
```
version: '3'
services:
  app:
    image: djbrain/go:dev-1.19
    extra_hosts:
      - 'host.docker.internal:host-gateway'
    ports:
      - '${APP_PORT:-8080}:8080'
    volumes:
      - './:/var/www'
```
