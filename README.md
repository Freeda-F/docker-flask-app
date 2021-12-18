# docker-flask-app
A Python Flask app in Docker which prints the hostname and IP of the container.

## Requirements

- [Install docker](https://docs.docker.com/engine/install/)
- [Install docker-compose](https://docs.docker.com/compose/install/)

## Prerequisites

1. Python Flask application code - app.py
2. Modules required for the application in file - requirements.txt

## Building the docker Image

For deploying the python flask app, we will be building a custom image using a Dockerfile. 
1. Run the Dockerfile
```
docker build -t freedafrancis/devflask-app:1 .
```
3. You can give the required tags to the docker image
```
docker tag freedafrancis/devflask-app:1 freedafrancis/devflask-app:latest
```
4. Push the image to the repository
```
docker image push freedafrancis/devflask-app:1
docker image push freedafrancis/devflask-app:latest
```
Now, the image is available in the docker repository.

## Download precreated image

You can also just download the existing image from DockerHub.
```
docker image pull freedafrancis/devflask-app:latest
```

## Run the container

Either you can run the container using the docker command 
```
docker container run --name dev-flaskapp -d -p 80:5000 freedafrancis/devflask-app
```
Or create a docker-compose file(docker-compose.yml) and use compose commands to start the container.
```
docker-compose up -d
 ```
 
## Provisioning
1. Clone this repository
```
git clone https://github.com/Freeda-F/docker-flask-app.git
```
2. Switch to the cloned directory
```
cd docker-flask-app
```
3. Start the docker containers using
```
docker-compose up -d
```
4. To stop and remove the containers,networks or volumes associated with this docker, you can use
```
docker-compose down -v
```
 
## Result

![image](https://user-images.githubusercontent.com/93197553/146647512-d083f5bb-e6db-4d23-8ecf-b44a26c212e3.png)
![image](https://user-images.githubusercontent.com/93197553/146647533-e8fbd665-a68b-4ca3-a316-d65bea050941.png)

