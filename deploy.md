# NGINX 
## DEPLOY
in root folder
```sh
docker compose --env-file .env.local -f nginx/docker-compose.nginx.yaml -f jenkins/docker-compose.jenkins.yaml -f minio/docker-compose.minio.yaml -f registry/docker-compose.registry.yaml up -d

```
## REMOVE
in root folder
```sh
docker compose --env-file .env.local -f nginx/docker-compose.nginx.yaml -f jenkins/docker-compose.jenkins.yaml -f minio/docker-compose.minio.yaml -f registry/docker-compose.registry.yaml down
```

# TRAEFIK 
## DEPLOY
in root folder
```sh
docker compose --env-file .env.local -f traefik/docker-compose.traefik.yaml -f jenkins/docker-compose.jenkins.yaml -f minio/docker-compose.minio.yaml -f registry/docker-compose.registry.yaml up -d
```
## REMOVE
in root folder
```sh
docker compose --env-file .env.local -f traefik/docker-compose.traefik.yaml -f jenkins/docker-compose.jenkins.yaml -f minio/docker-compose.minio.yaml -f registry/docker-compose.registry.yaml down
```

# NGINX-PROXY-MANAGER 
## DEPLOY
in root folder
```sh
docker compose --env-file .env.local -f nginx-proxy-manager/docker-compose.nginx.yaml -f jenkins/docker-compose.jenkins.yaml -f minio/docker-compose.minio.yaml -f registry/docker-compose.registry.yaml up -d
```
## REMOVE
in root folder
```sh
docker compose --env-file .env.local -f nginx-proxy-manager/docker-compose.nginx.yaml -f jenkins/docker-compose.jenkins.yaml -f minio/docker-compose.minio.yaml -f registry/docker-compose.registry.yaml down
```
