

## Working with Docker-Compose

- In the root directory of the project run "**docker-compose up**" command.
- Wait all containers to start.
- To run continuously all containers run  "**docker-compose up -d**" command.
- To shut-down all containers run  "**docker-compose down**" command.



## Table for credentials

|  Container  |        Port         |Username|Password|
|:-----------:|:-------------------:|:------:|:------:|
|  Logstash   |http://localhost:5044| -----  | -----  |
|Elasticsearch|http://localhost:9200| -----  | -----  |
|   Kibana    |http://localhost:5601| -----  | -----  |


## Check containers status

- After containers is up, run "**docker container ls**" to see their status
- run ```telnet localhost 5044``` , ```telnet localhost 9200```  , ```telnet localhost 5601``` to get response from containers

## Updating Logstash Source

- When you make a change to ```logstash/assets/logstash.conf``` you can apply the change by restarting the container: "**docker-compose restart dev_logstash**"

  
## Enabling HTTPS

- You can quickly enable HTTPS on the Nginx container by adding your certs the ```nginx/assets/certs``` directory, updating the ```nginx/assets/default-ssl-example.conf``` file with your certificate names and making it the ```default.conf``` file: run **cp nginx/assets/default-ssl-example.conf nginx/assets/default.conf** then you can apply the change by restarting the container: "**docker-compose restart dev_nginx**"


## Persistent Data - Backup and Restore Named Volume

**Elasticsearch Backup**

- Will be Added

**Elasticsearch Restore**

- Will be Added


## Compose Up Sample Screencast

![compose-up.gif](https://github.com/bilgeadamdev/docker_elasticsearch-logstash-kibana/blob/master/images/up_elasticsearch-logstash-kibana.gif)

## Compose Down Sample Screencast

![compose-down.gif](https://github.com/bilgeadamdev/docker_elasticsearch-logstash-kibana/blob/master/images/down_elasticsearch-logstash-kibana.gif)


