# scylla-cluster

**Scylladb cluster with Docker Swarm** 

Using Docker Swarm to setup a scylladb cluster.

## Docker Compose template of Scylladb cluster
```
version: '3'

services:
  scylla:
    image: scylla
    ports:
        - 9042:9042
    command: --seeds auto
```

## Play with it
Build the scylladb Docker image

```
docker build -t 'scylla' scylla
```

Start the scylladb cluster
```
docker stack deploy --compose-file docker-compose.yml scylladb
```

Scale out the instance number of scylladb
```
docker service scale scylladb_scylla=<num>
```

## References

https://github.com/scylladb/scylla

## Contributors
Herber (<herber523@gmail.com>)
