
# BIG DATA ECOSYSTEM WITH DOCKER

Environment for studying the main big data frameworks in docker.
<br>  This setup will create dockers withthe HDFS, HBase, Hive, Presto, Spark, Jupyter, Hue, Mongodb, Metabase, Nifi, kafka, Mysql and Zookeeper frameworks

<br>  

## SETUP

*NOTE: This step must be performed only once. After the environment is created, use docker-compose to start the containers as shown in the topic STARTING THE ENVIRONMENT*

#### Docker directory creation:

*NOTE: The creation of the directory is important for the necessary mappings*
   * No Linux:
      * Create the directory in the user's home
        ex: /home/user/docker

#### In a terminal/DOS, inside the docker directory, clone the project on github

          git clone https://github.com/rodrigo-reboucas/docker-bigdata.git

## STARTING THE ENVIRONMENT

### In the terminal, in the directory bigdata_docker, run docker-compose

          docker-compose up -d        

### Check images

          docker image ls

### Check containers

          docker container ls

## SOLVING PROBLEMS

### Stop a containers

         docker stop [name of container]      

### Stop all containers

         docker stop $(docker ps -a -q)

  

### Remove a container

         docker rm [name of container]

### Remove all containers

         docker rm $(docker ps -a -q)         

### Container data

         docker container inspect [name of container]

### Start a container

         docker-compose up -d [name of container]

### Start all containers

         docker-compose up -d 

### Access container log

         docker container logs [name of container] 

## Frameworks WebUI Access

* HDFS *http://localhost:50070*

* Presto *http://localhost:8080*

* Hbase *http://localhost:16010/master-status*

* Mongo Express *http://localhost:8081*

* Kafka Manager *http://localhost:9000*

* Metabase *http://localhost:3000*

* Nifi *http://localhost:9090*

* Jupyter Spark *http://localhost:8889*

* Hue *http://localhost:8888*

* Spark *http://localhost:4040*


## Shell Access

   ##### HDFS
          docker exec -it datanode bash      
   ##### HBase
          docker exec -it hbase-master bash
   ##### Sqoop
          docker exec -it datanode bash
   ##### Kafka
          docker exec -it kafka bash
          
## Acess JDBC

   ##### MySQL
          jdbc:mysql://database/employees
   ##### Hive
          jdbc:hive2://hive-server:10000/default
   ##### Presto
          jdbc:presto://presto:8080/hive/default

## Users and passwords

   ##### Hue

    User: admin
    Password: admin

   ##### Metabase

    User: bigdata@class.com
    Password: bigdata123

   ##### MySQL

    User: root
    Password: secret

   ##### MongoDB
    User: root
    Password: root

    Authentication Database: admin

## Images   

[Docker Hub](https://hub.docker.com/u/fjardim)

## Official Documentation

* https://zookeeper.apache.org/
* https://kafka.apache.org/
* https://nifi.apache.org/
* https://prestodb.io/
* https://spark.apache.org/
* https://www.mongodb.com/
* https://www.metabase.com/
* https://jupyter.org/
* https://hbase.apache.org/
* https://sqoop.apache.org/
* https://hadoop.apache.org/
* https://hive.apache.org/
* https://gethue.com/
* https://github.com/yahoo/CMAK
* https://www.docker.com/


​
