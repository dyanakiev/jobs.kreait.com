# jobs.kreait.com

## Local development

### Requirements

```bash
$ brew install docker-machine
$ brew install docker-compose
```

### Setup your Docker environment

You can also use an already existing machine - on a new machine, all Docker images will have to be freshly pulled.

```bash
$ docker-machine create -d virtualbox kreait-jobs
$ # point the docker client to the new machine
$ eval "$(docker-machine env kreait-jobs)"
$ # Show the machine's IP address, will return something like
$ # 192.168.99.100
$ docker-machine ip
```

### Start the local website

```bash
$ docker-compose up
```

or in detached mode

```bash
$ docker-compose up -d
```

The website will now be available at the address that `docker-machine ip` gave you, so e.g. http://192.168.99.100/
