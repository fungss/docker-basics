# docker-basics<br/>
reference: [thenewboston](https://www.youtube.com/watch?v=gFjxB0Jn8Wo&list=PL6gx4Cwl9DGBkvpSIgwchk0glHLz7CQ-7&index=1&ab_channel=thenewboston)

## list container/image<br/>
docker container ls -a<br/>
docker image ls -a<br/>


## common command<br/>
docker container run imageID/imageTag *optionalCMD<br/>
docker container create imageID/imageTag            # create only the container but it will not run it<br/>
docker container start -a containerID/containerTag  # -a shows logs<br/>
docker container stop containerID/containerTag<br/>
docker container kill -f containerID/containerTag<br/>
docker container rm containerID/containerTag<br/>
docker container inspect containerID/containerTag<br/>
docker system prune --all                           # clear all containers<br/>


## enable interaction with a running containers<br/>
docker container exec -it containerID CMD<br/>


## build image from Dockerfile<br/>
docker build -t userName/project-name .             # don't forget the .<br/>
docker run -it -p localPortNum:containerPortNum imageID/imageTag<br/>
