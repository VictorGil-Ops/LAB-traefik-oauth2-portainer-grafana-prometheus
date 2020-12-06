# traefik-portainer-grafana-prometheus
Docker Compose para desplegar Traefik + Portainer + Grafana + Prometheus

## Preparación
Crear las carpetas

Ejecutar en la consola:

for i in grafana-db portainer-db prometheus traefik; do
  mkdir -p "./folders/${i}"
done

## Prometheus usa el UID 99, dar los permisos a la carpeta

sudo chown 99:99 ./folders/prometheus

## Ejecutar docker-compose

sudo docker-compose up --remove-orphans
