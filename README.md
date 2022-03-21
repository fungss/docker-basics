# docker-basics



# list container/image
docker container ls -a
docker image ls -a


# common command
docker container run imageID/imageTag *optionalCMD
docker container create imageID/imageTag            # create only the container but it will not run it
docker container start -a containerID/containerTag  # -a shows logs
docker container stop containerID/containerTag
docker container kill -f containerID/containerTag
docker container rm containerID/containerTag
docker container inspect containerID/containerTag
docker system prune --all                           # clear all containers


# enable interaction with a running containers
docker container exec -it containerID CMD


# build image from Dockerfile
docker build -t userName/project-name .             # don't forget the .
docker run -it -p localPortNum:containerPortNum imageID/imageTag
