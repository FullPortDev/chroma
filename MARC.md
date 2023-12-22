# Files of importance
- docker-compose.dev.yml
- docker-compose.prod.yml
- MARC.md
- .env
- .env.dev
- server.htpasswd
- server.dev.htpasswd


# Dev
docker-compose --env-file ./.env.dev -f docker-compose.dev.yml up -d --build
docker-compose --env-file ./.env.dev -f docker-compose.dev.yml down

# Prod
docker-compose --env-file ./.env -f docker-compose.prod.yml up -d --build
docker-compose --env-file ./.env -f docker-compose.prod.yml down


# Things of note
- the PERSIST_DIRECTORY env variable needs to be the same name as the volume
- generate the htpasswd with this command `htpasswd -Bbn username password > server.htpasswd`
- the docker-compose fil