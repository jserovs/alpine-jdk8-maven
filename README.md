# Alpine + OpenJDK8 + Maven build envriment

https://hub.docker.com/r/jserovs/alpine-jdk8-maven

https://github.com/jserovs/alpine-jdk8-maven


This is a lightweight linux machine with JDK8 and Maven ready to build java projects

## Tools included

- OpenJDK8
- Maven 3.6.3 (alpine package)
- Git 2.30

## Directories

Container starts in `/home/developer/` 

## Volumes

you can mount host folder to container using following command
```
-v "$(pwd):/home/developer
```

## Example
```
git clone https://github.com/paul-pop/java8-crud-shop
cd java8-crud-shop
mvn clean install
```

## Running container

```
docker container run -it --rm -v "$(pwd):/home/developer" jserovs/alpine-jdk8-maven
```

### Flags used in command

> -it interactive session with a tty attached

> --rm removes container after stop

> -v mounts current folder to /home/developer in container
