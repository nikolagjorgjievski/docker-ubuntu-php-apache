#Docker: Ubuntu 16.04 PHP 7.2 Apache2
This project has a docker development environment ready which you can easily set up the project on your local machine by installing [Docker Community Edition](https://docs.docker.com/engine/installation/) and [Docker Compose](https://docs.docker.com/compose/install/) for the operating system you are using.

After installing Docker CE and Docker Compose, run the following commands to see if everything was installed properly:

```
docker
docker-compose
```

Run the following command to build the project:

```
docker build -t mysite .
```
This command will install everything that the project needs.

After the build is complete, run the following command to start the docker containers:

```
docker run -p 8080:80 -d --name mysite mysite
```

To check if everything works, open your browser and go to:

```
http://localhost:8080/
```
You should see the response:
```
Hello?
```

If you want bash access to the container, run:

```
docker exec -it mysite bash
```

To stop the container, run:

```
docker stop mysite
```
