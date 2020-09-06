# Docker Notes

sudo yum update (Get package insatller) 

sudo yum install -y docker

sudo groupadd docker

sudo usermod -aG docker $USER

systemctl start docker   (to start docker)

docker --version

docker info

docker container b117d7befc68 start

docker ps -a (to see all docker containers)

Run Jenkins in docker container

  docker run -p 80:8080 --name=jenkins-master jenkins
  
  first port (ex: 80) is host port (Vm machine; which will be used by browser)
  
  second port (ex:8080) is jenkin container port
  
docker container rm jenkins-master  (remove conatiner)

docker ps -a

docker image list

docker image rm jenkins (remove image)

docker image list

Run Ubuntu container 

  docker container run --rm -i -t ubuntu:latest /bin/bash (Interactive container)
   
   --rm - remove container on exit
   
   -i - interactive container
   
   -t - Allocate a pseudo-TTY
   
 or
 
 docker container run -d --name=ubuntu20 ubuntu:latest (Daemonized)
 
 docker container start/stop/restart ubuntu20 (start conatiner)
 
 docker exec -it ubuntu20 bash (Enterr inti the container shell)
 
 Elastic search:
 
 docker pull elasticsearch:7.9.1
 
 docker run -p 9200:9200 -p 9300:9300 -e "discovery.type=single-node" elasticsearch:7.9.1  (To have elastic search conatiner)



   







