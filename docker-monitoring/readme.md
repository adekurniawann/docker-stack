1. change docker config json, see `config/daemon.json `
2. restart docker service
3. add stack deploy using portainer
4. append prometheus config file in prometheus volume  with 
```` 
- job_name: devops_central
  scrape_interval: 5s
  static_configs:
  - targets:
    - xxxxxxxx:9080
````
5. install loki plugin
```` 
docker plugin install grafana/loki-docker-driver:latest --alias loki --grant-all-permissions
````
