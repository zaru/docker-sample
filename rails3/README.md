```
docker-compose run web rails new . --force --database=mysql --skip-bundle
docker-compose up
docker-compose run web rails db:create
```
