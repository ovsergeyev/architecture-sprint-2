Инструкция по развертыванию:

Переход в директорию и запуск контейнеров
  cd mongo-sharding
  docker-compose up -d

Конфигурация сервера конфигурации, шардов и роутера
  docker-compose exec configSrv sh -c "mongosh < /scripts/init-configserver.js"
  docker-compose exec shard1 sh -c "mongosh < /scripts/init-shard1.js"
  docker-compose exec shard2 sh -c "mongosh < /scripts/init-shard2.js"
  docker-compose exec mongos_router sh -c "mongosh < /scripts/init-router.js"