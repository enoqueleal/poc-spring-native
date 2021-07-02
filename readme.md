# Overview
Spring Native provides support for compiling Spring applications to native executables using the [GraalVM native-image compiler](https://www.graalvm.org/reference-manual/native-image/).

# Getting Started
Download [GraalVM 21.1.0](https://www.graalvm.org/downloads/)

Set JAVA_HOME and PATH appropriately.

Run ```gu install native-image``` to bring in the native-image extensions to the JDK



# Build the native application
```
$ ./mvnw -Pnative -DskipTests package
```

# Run the native application
```
$ open target/rest-service
```

## or

# Build the native application for docker image
````
$ ./mvnw spring-boot:build-image -DskipTests
````

# Run the native application in docker container
````
$ docker run --rm -p 8080:8080 rest-service:0.0.1-SNAPSHOT
````

# Reference:
[Spring Native documentation](https://docs.spring.io/spring-native/docs/current/reference/htmlsingle/#overview)