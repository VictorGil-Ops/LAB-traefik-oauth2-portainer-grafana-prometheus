# traefik-portainer-grafana-prometheus

Docker Compose para desplegar Traefik + Portainer + Grafana + Prometheus

## Necesario

- [Cloudflare](<https://dash.cloudflare.com/login>)
- [OAUTH2](https://developers.google.com/identity/protocols/oauth2)

## Preparación

1. Crear las carpetas, ejecutar en la consola:

```bash

  for i in grafana-db portainer-db prometheus traefik; do mkdir -p "./folders/${i}"; done;

```

2. Prometheus usa el UID 99, dar los permisos a la carpeta.

```bash

  sudo chown 99:99 ./folders/prometheus

```

3. Ejecutar docker-compose

```bash

  sudo docker-compose up --remove-orphans -d

```
