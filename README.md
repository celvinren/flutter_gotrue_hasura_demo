
Docker:
pull images:
docker-compose up -d
docker compose up --build


check running containers:
docker ps

stop and remove containers:
docker-compose down
docker-compose up -d

If gotrue schema is not created, run:
docker exec -it flutter_gotrue_hasura_demo-postgres-1 psql -U postgres -d app_db
CREATE SCHEMA auth;
\dn

check docker logs:
docker logs flutter_gotrue_hasura_demo-gotrue-1

curl -X POST http://localhost:9999/signup \
  -H "Content-Type: application/json" \
  -d '{
    "email": "test@example.com",
    "password": "12345678"
  }'