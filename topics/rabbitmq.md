## RabbitMQ

RabbitMQ is a a distributed message broker that is program to exchange messages between producers and consumers.

#### Commands

run RabbitMQ in a docker container and rabbitmq management exposed on localhost 5656. Then open `localhost:5656` with `guest` and password `guest`

```bash
docker run --rm -it --hostname my-rabbit -p 15672:15672 -p 5672:5672 rabbitmq:3-management
```

get the logs

```bash
docker logs some-rabbit
```
