## Ex 01 -Simple Web Server using Spring Boot

## AIM:
To develop a Simple Web Server using Spring Boot that can handle basic HTTP requests and return appropriate responses through RESTful endpoints.

## ALGORITHM:
1. Start a New Spring Boot Project:</br>
Use Spring Initializr (https://start.spring.io/)</br>
2. Select dependencies: Spring Web</br>
3. Create the Main Application Class:</br>
This class contains the main() method with @SpringBootApplication annotation to bootstrap the application.</br>
4. Create a Controller Class:</br>
Create a class annotated with @RestController.</br>
5. Define one or more HTTP request handler methods using @GetMapping, @PostMapping, etc.</br>
6. Write Endpoint Methods:</br>
Inside the controller, define a simple method for handling GET requests (e.g., return “Hello World” when /hello is accessed).</br>
7. Run the Application:</br>
Run the application using your IDE or via the command line (mvn spring-boot:run or ./mvnw spring-boot:run).</br>
8. Test the Endpoint:</br>
* Open a web browser or use Postman to visit:</br>
* http://localhost:8080/hello</br>
* You should see the output (e.g., "Hello World").</br>
* Stop the Server:</br>
Stop the Spring Boot server once testing is complete.</br>


## Program:

simple-web-server/ </br>
├── src/</br>
│   └── main/</br>
│       ├── java/<br>
│       │   └── com.example.demo/</br>
│       │       ├── DemoApplication.java</br>
│       │       └── HelloController.java</br>
│       └── resources/</br>
│           └── application.properties</br>
├── pom.xml</br>

 ### Pom.xml:

```
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 
                             http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>

    <groupId>com.example</groupId>
    <artifactId>simple-web-server</artifactId>
    <version>0.0.1-SNAPSHOT</version>
    <name>Simple Web Server</name>
    <description>Demo project for Spring Boot Web Server</description>

    <parent>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-parent</artifactId>
        <version>3.1.2</version>
        <relativePath/>
    </parent>

    <dependencies>
        <!-- Spring Boot Web -->
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-web</artifactId>
        </dependency>
    </dependencies>

    <build>
        <plugins>
            <plugin>
                <groupId>org.springframework.boot</groupId>
                <artifactId>spring-boot-maven-plugin</artifactId>
            </plugin>
        </plugins>
    </build>
</project>

```

### Experiment1Application.java

```
package com.example.experiment1;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class DemoApplication {
    public static void main(String[] args) {
        SpringApplication.run(DemoApplication.class, args);
    }
}
```

### HelloController.java

```
package com.example.experiment1;

import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RestController;

@RestController
public class HelloController {

    @GetMapping("/hello")
    public String sayHello() {
        return "Hello, Spring Boot! This the First Simple Web Server using Spring Boot";
    }
}
```

### application.properties:
server.port=8080


### Output:

<img width="1910" height="1018" alt="Screenshot 2026-11-19 123402" src="https://github.com/user-attachments/assets/36f9135e-fe8e-450d-8e92-0b25a485283c" />


### Result:
Thus, The Program to develop a Simple Web Server using Spring Boot that can handle basic HTTP requests and return appropriate responses is executed successfully.
