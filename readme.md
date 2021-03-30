# arena tracker

## .env
Holds environment variables that can be used to in the docker-compose file, e.g. TAG.

## squad.env
Holds all the environment variables that should be passed into the container.

## test/run

Test the configurations:
```
docker-compose config
```

Run or upgrade (same command)
```
docker-compose up -d 
```

## docker swarm

Deploy to docker swarm:
```
docker stack deploy -c <(docker-compose config) squad
```

## references
- https://docs.docker.com/compose/environment-variables/
