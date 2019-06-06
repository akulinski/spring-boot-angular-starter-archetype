
Spring Boot 2.1 And Angular 8 starter

-----

This is a multi-module Spring Boot Angular Maven project that allows to create archetype.
The frontend Angular app is built using [angular-cli](https://cli.angular.io/). The project packages Angular application code as a [WebJar](https://www.webjars.org/). This project is geared towards building monolithic applications. I have also written [a blog that explains step by step how to create this starter project](https://shekhargulati.com/2017/11/08/a-minimalist-guide-to-building-spring-boot-angular-5-applications/).


1. `backend`: This contains Java code of the application.
2. `frontend`: This contains source code for the Angular based frontend.

This project uses following versions:

1. Spring Boot v2.1.5
2. Angular v8.0.0
3. Node v12.4.0
4. Npm v6.9.0

#Create new project

### 1. Generating archetype

In root of project run
```
1. mvn archetype:create-from-project -Darchetype.filteredExtensions=java
2. cd target/generated-sources/archetype/
3. mvn install
```

### 2. Use generated archetype to create new project

```
1. Create folder for your project example: mkdir /tmp/archetype/
2. Change directory to created folder example: cd /tmp/archetype/
3. mvn archetype:generate -DarchetypeCatalog=local
4. Choose com.akulinski.springbootstarter:spring-boot-angular-starter-archetype 
5. Enter data needed for project generation 
6. Voilà 
```

## Features

This starter comes bundled with the following features:

1. Multi module Maven project: A multi module project to modularize backend and frontend code separately.
2. Maven wrapper: So, you don't need to install Maven on your machine.
3. ErrorProne: Find errors in your code.
4. Frontend packaged as a WebJar.
5. CORS enabled: A global configuration is added to enable CORS so that frontend can work seamlessly with backend during development.
6. REST API base path: Sets the base REST API path to `/api`. You can configure it by changing `rest.api.base.path` property.
7. Maven release plugin
8. CI: The project is preconfigured to use TravisCI as continuous integration server.

## Running the backend for development mode

There are multiple ways to run the backend. For development, you can use your favorite IDE and run the
`com.example.app.Application`. As soon as your code compiles, Spring Boot DevTools will reload the code.

You can also run the application using Maven.

```bash
$ cd backend
$  ../mvnw spring-boot:run
```

## Running the frontend for development mode
```
$ cd frontend
$ ng serve 
```
## Hot reloading

Both the front-end and back-end modules support hot reloading.
