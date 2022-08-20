# Containerization Python Flask

Flask is a common python framework for web api development. And it is not exemption to be deployed in conainerized package.

## To build, run:
```
docker build -t flask .
```
**flask** being the image tag name.

## Note:

--host=0.0.0.0 is included in the command inside **Dockerfile** because flask only make port 5000 available locally - inside the container.
Thus, to access it on the host machine, **host** with internet ip wildcard (0.0.0.0) argument needs to be supplied.

## To build, run:
```
docker run -d --rm --name app -p 80:5000 flask 
```

Making port 80 accessible on the host machine.

