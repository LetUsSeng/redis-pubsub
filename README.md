# Redis-PubSub

Redis-PubSub uses Redis as a PubSub server and Grafana to view data. Grafana base off [grafana-redis-datasource](https://github.com/RedisGrafana/grafana-redis-datasource).

## Setup

To set up the server.

```bash
docker-compose up -d
```

## Usage

### SUB
```bash
docker run -it \
--network redis-pubsub_redis-pubsub \
--rm redis \
redis-cli -h redis-server SUBSCRIBE <REPLACE WITH YOUR CHANNEL>
```

### PUB
```bash
docker run -it \
--network redis-pubsub_redis-pubsub \
--rm redis \
redis-cli -h redis-server PUBLISH <REPLACE WITH YOUR CHANNEL> "<YOUR MESSAGE>"
```

### View Redis Information
Go to http://localhost:3000 and go to Redis PubSub dashboard.

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)