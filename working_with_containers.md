#### tagging a container
  * docker build -t robingautam/redis:latest
  * docker run robingautam/redis
#### Alternative for using Dockerfile (example)
  * docker run -it alpine sh
  * apk add --update redis
  * In another terminal, docker ps {copy the container id}
  * docker commit -c 'CMD["redis-server"]' 862d3c373c6e 
  * Doing this will create a custom redis image out of base image of apline
  * If you want to access the redis image directly from docker hub, you may do--> docker run redis
#### COPY 
  * COPY ./ ./ {Path to folder from your machine && place to copy stuff to inside the container}