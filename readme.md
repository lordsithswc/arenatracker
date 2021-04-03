# arena tracker on rpi4 

## Getting started

1. Clone the repo `git clone https://github.com/marx-godfellas/swgoh-arena-tracker-hosting.git`
2. Edit the `docker-variables.env` file.
3. Check the configurations with `docker-compose config`
4. Run `docker-compose up -d`

## .env
Holds environment variables that can be used to in the docker-compose file, e.g. TAG.

If you instead would like to set the TAG from command line, you can do something like this:
```
TAG=0.23.0 docker-compose config
```

This will override anything in the .env file.

## docker-variables.env
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
docker stack deploy -c <(docker-compose config) <name>
```

## references
- https://docs.docker.com/compose/environment-variables/
