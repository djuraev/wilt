### March Log
#### One of the worst ways to use your time is to do something well that you didn't need to do at all.

## 03-26
* Git pull without commiting local changes: ```git checkout .``` then you can pull ```git pull```
* Spring Argument too long to run error solution: 
     * <b>Run -> Edit Configurations -> Environment</b> set VM Options to ```-Dspring.profiles.active=local```
* Run RabbitMQ in Docker
* * ```docker run --name rabbitmq -d -p 5672:5672 -p 15672:15672 -e RABBITMQ_DEFAULT_USER=jeff -e RABBITMQ_DEFAULT_PASS=jeff1! rabbitmq```

* RSQL JPA Specifation - usefull library for querying : [link to github repo](https://github.com/perplexhub/rsql-jpa-specification)