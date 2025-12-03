## Hello Prisma

Demo of how to get Prisma up and running with a postgres database using docker.

```
# create .env file from .env.example
# this has the DATABASE_URL
cp .env.example .env

# start db with docker compose detached
docker-compose up -d

# install dependencies
npm install

# generate prisma client
npx prisma generate

# run migrations
npx prisma migrate dev

# run prisma studio
npx prisma studio

# see 2 empty tables for User and Post
# at http://localhost:51212/

# run script to populate data
npx tsx script.ts

# see populated data in prisma studio
# at http://localhost:51212/
```
