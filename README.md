

### Setup Memory
Run this command in your host.
```
sysctl -w vm.max_map_count=262144
```

### Run Docker Compose
```
docker-compose up -d
```

### Make Everyone can connect
elasticsearch.yml

``` yml
network.host: 0.0.0.0
http.cors.enabled: true
http.cors.allow-origin: "*"
```

### Setting in docker-compose.yml

Name of cluster for elasticsearch

```yml
cluster.name=elasticsearch
```

Upper limit for memory

```yml
mem_limit: 2g
```

