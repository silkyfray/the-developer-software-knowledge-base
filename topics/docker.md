## Docker

### Docker Compose

Docker Compose is a tool for running multi-container setup.

#### Commands

Builds the list of services and starts them as daemon

```bash
docker-compose up -d --build <list of services>
```

The difference between `docker-compose up` and `docker-compose up --build` is that it is forced to build the images even there is no need.

Builds all services in the stack and starts them as daemon

```bash
docker-compose up -d
```

Restart the list of services. Note: build beforehand in order to pick up ENV variables. Also `up` works better as it picks up env changes.

```bash
docker-compose restart <list of services>
```

Execute a script inside a docker container

```bash
docker-compose exec <service name> bash /path/to/file
```
