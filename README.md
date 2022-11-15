# Docker Testing NodeJS
## Building Docker image
Go to the directory that has your Dockerfile and run the following command to build the Docker image. The -t flag lets you tag your image so it's easier to find later using the docker images command:<br>
``
docker build . -t node-web-app
``
<br>
<br>
## Check created docker image
``
$ docker images
``
## Run the image
Running your image with -d runs the container in detached mode, leaving the container running in the background. The -p flag redirects a public port to a private port inside the container. Run the image you previously built: <br>

``
docker run -p 49160:8080 -d node-web-app
``

## Print the output of my app


Get container ID : 
`` $ docker ps ``

Print app output : 
`` $ docker logs <container id> ``

After check logs you can see log as this 
`` Running on http://localhost:8080 ``

