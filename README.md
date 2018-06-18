# kafka-bootstrap-docker

If you want to run Kafka in you local dev environment using docker or vagrant this project is for you! Welcome!

You can build the image from the Dockerfile supplied. It creates Kafka and Zookeeper in a single container.

Alternatively to bootstrap kafka on your machine using vagrant just:
 1. Clone this repo
 2. Switch current directory to it
 3. and run `vagrant up`
 
Here you are! Now you have running instance of Kafka on the 9092 port of your host!


Part of this project was taken from [spotify/kafka](https://github.com/spotify/docker-kafka).
