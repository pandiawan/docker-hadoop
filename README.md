# Docker Hadoop

Hadoop 3.3.1 with Ubuntu 20.04

## Creating the hadoop image

    $ git clone https://github.com/pandiawan/docker-hadoop.git
    $ cd docker-hadoop
    $ docker build -t hadoop:3.3.1 .

## Creating the container

To run and create a container execute the next command:

    $ docker run -it --name hadoop-3.3.1 -p 9864:9864 -p 9870:9870 -p 8088:8088 --hostname localhost hadoop:3.3.1

## Access Hadoop UI from Browser
Use your preferred browser and navigate to your localhost URL or IP. The default port number 9870 gives you access to the Hadoop NameNode UI:

    http://localhost:9870
     
The default port 9864 is used to access individual DataNodes directly from your browser:

    http://localhost:9864

The YARN Resource Manager is accessible on port 8088:

    http://localhost:8088

## Stopping and re-starting the container

To stop the container execute the following commands, to gratefully shutdown.

    $ stop-dfs.sh
    $ stop-yarn.sh

After that.

    $ exit

To re-start the container, and go back to our Hadoop environment execute:

    $ docker start -i hadoop-3.3.1


