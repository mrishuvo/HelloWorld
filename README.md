# Spring Boot Maven Jib Example

This project contains a minimal Spring Boot application that can be deployed as a Docker container via a build with the Maven Jib plugin.

## Getting Started

### Prerequisites

Git, Maven and Docker are required to download,  build and run the project.

### Installing

```
git clone https://github.com/Darkwyng/spring-boot-maven-jib-example.git
cd spring-boot-maven-jib-example
mvn compile jib:dockerBuild
docker run myimagename
```

If all worked, the container will say
```
Hello world
```

As it is written now, it will run on a Raspberry Pi 3. For other systems you may need to adapt the base docker image in [pom.xml](pom.xml).

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
