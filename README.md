# docker_mointoring_apps
# docker has its own mointoring tools
## commands you can use on your docker cli
'<docker logs>'
'<docker top conatiner (id)>'
'<docker stats>'                
this provides the current statistics of all the containers running
'<docker events>'         
this checks the events that occurs in the past on your running containers 

<docker events --since 1h15m --filter container=(id)> can also be used to provide activites in the last hour 

# now we can out source in collecting the metrics, logging and collecting events 

# Open Source Tools for Docker Container Monitoring

### ctop

ctop is a real-time metric tool developed in Golang for monitoring Docker containers. It provides valuable insights into container metrics. To use ctop, run the following command:

```
docker run --rm -ti --name=ctop --volume /var/run/docker.sock:/var/run/docker.sock:ro quay.io/vektorlab/ctop:latest
```

### Lazy Docker

Lazy Docker is another terminal tool for Docker and Docker Compose, also written in Golang. It offers container monitoring capabilities on both Windows and macOS. To install Lazy Docker, execute the following command:

```
docker run --rm -it -v /var/run/docker.sock:/var/run/docker.sock -v C:\Users\USER\Desktop\docker\monitoring\mount:/.config/jesseduffield/lazydocker lazyteam/lazydocker
```

![Screenshot (4)](https://github.com/A-LPHARM/docker_mointoring_apps/assets/123018722/5455712c-8bf2-4984-b8c0-8d1e621c8808)

### cAdvisor

cAdvisor is a container monitoring tool that collects metrics and logs. However, it lacks advanced visualization features. It can send collected data to various destinations like Prometheus, StatD, Elasticsearch, Kafka, InfluxDB, and CollectD.

### Prometheus

Prometheus is a powerful tool for data collection and time-series storage. It gathers and scrapes data while utilizing promQL for querying your data.

### Node Exporter

Node Exporter provides metrics from containers at an endpoint.

### Grafana

Grafana is a versatile tool capable of collecting data from various sources, such as Elastic search, DynamoDB, and AWS. It offers a user-friendly GUI for querying and visualizing data, simplifying the evaluation of logs, data, and metrics in your containers.

Using these open-source tools, monitoring your Docker containers becomes more efficient and streamlined, enabling you to gain valuable insights into their performance.
![Screenshot (5)](https://github.com/A-LPHARM/docker_mointoring_apps/assets/123018722/840e45a0-dcb0-4dcb-81d1-e9f2b085a124)


