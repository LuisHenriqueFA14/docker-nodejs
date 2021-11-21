<h1 align="center"> docker-nodejs </h1>
<p align="center">My first time trying <a href="https://www.docker.com/">docker</a> with nodejs.</p>

### What is that ?

This is a simple project that uses docker to run a nodejs server.

### Requirements

- Docker
- Docker-compose (to run development environment)


### How to use it

After downloading, run this command to build the container:
```
docker build -t <CONTAINER_NAME> . 
```

<br/>

Then, run this command to run the container:
```
docker run -p 3000:3000 -d <CONTAINER_NAME>
```

<br/>

If you want to run it with nodemon (to update files when saving).
Then, run this command:
```
docker ps # to check the container ID
docker stop <CONTAINER_ID> # to stop the docker container
docker-compose up # to start the development container
```

### How to see if works

Run this command with the container running:
```
curl http://localhost:3000/
```
The result should be:
```
{"message":"Hello World!"}
```
