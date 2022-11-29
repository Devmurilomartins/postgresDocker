# postgresDocker
Docker com  Postgres basico para testes

docker-compose:

version: "3"
services:
  postges-apline:
    image: postgres:15-alpine
    container_name: "postgres"
    environment:
      - POSTGRES_USER=postgres
      - POSTGRES_PASSWORD=postgres
      - TZ=GMT
    volumes:
      - "/var/lib/postgresql/data"
    ports:
      - 5431:5432
