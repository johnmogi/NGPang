pagan stands for:
postgresql
angular
docker
nestJs -nnest.md

https://makinhs.medium.com/graphql-nodejs-postgres-made-easy-with-nestjs-and-typeorm-4daff3c516d

DOCKER-
this might sound obvious but clean or at least stop all previous working containers...

docker fires up postgreSQL and graphql
the reason i choose graphql is to improve
inner related queries.

curl https://raw.githubusercontent.com/hasura/graphql-engine/stable/install-manifests/docker-compose/docker-compose.yaml -o docker-compose.yml
docker-compose up -d (need to run DD)
docker ps
http://localhost:8080/console

also -look for docker for the status before trying to cinnect.

nnest - 
yarn add typeorm pg @nestjs/typeorm
npm i @nestjs/graphql





