# **3-Month Server Engineer Learning Plan**

A focused plan to transition from an experienced Android developer to an intermediate Server Engineer.

## **Month 1: Core Backend Foundation**

**Project:** Build a REST API for a simple blogging platform.

### **Week 1: Spring Boot & REST APIs**

* \[ \] Set up a Spring Boot project (Kotlin, Spring Web, Spring Data JPA) using Spring Initializr.  
* \[ \] Implement a @RestController with full CRUD endpoints (GET, POST, PUT, DELETE) for a Post resource.  
* \[ \] Test all endpoints using Postman or Insomnia.  
* \[ \] Refactor logic into a dedicated @Service class.

\<br\>  
Resources:

* [Official Guide: Building a RESTful Web Service](https://spring.io/guides/gs/rest-service/)  
* [Baeldung: Spring Boot with Kotlin](https://www.baeldung.com/kotlin/spring-boot-kotlin)

### **Week 2: Databases & Persistence**

* \[ \] Set up a PostgreSQL database and configure the Spring application to connect to it.  
* \[ \] Define data models as JPA @Entity classes and create JpaRepository interfaces for them.  
* \[ \] Integrate a migration tool (Flyway or Liquibase) and create an initial schema script.  
* \[ \] Use the @Transactional annotation on service methods to ensure data consistency.

\<br\>  
Resources:

* [Official Guide: Accessing Data with JPA](https://spring.io/guides/gs/accessing-data-jpa/)  
* [Baeldung: Intro to Spring Data JPA](https://www.google.com/search?q=https://www.baeldung.com/spring-data-jpa-tutorial)  
* [Flyway: Getting Started](https://flywaydb.org/documentation/getstarted/)

### **Week 3: Advanced APIs & Best Practices**

* \[ \] Add and apply jakarta.validation annotations for request validation.  
* \[ \] Create a global exception handler with @ControllerAdvice for structured error responses.  
* \[ \] Use the DTO pattern to separate API data from internal database entities.  
* \[ \] Implement @OneToMany and @ManyToOne entity relationships.

\<br\>  
Resources:

* [Baeldung: Spring Boot Validation](https://www.baeldung.com/spring-boot-bean-validation)  
* [Baeldung: DTO Pattern in Spring](https://www.baeldung.com/java-dto-pattern)

### **Week 4: Testing & Basic Security**

* \[ \] Write unit tests (JUnit 5, Mockito) and integration tests (@SpringBootTest).  
* \[ \] Add Spring Security and configure a basic username/password authentication provider.  
* \[ \] Secure write endpoints (POST, PUT, DELETE) to require authentication.

\<br\>  
Resources:

* [Official Guide: Spring Security Architecture](https://spring.io/guides/topicals/spring-security-architecture)  
* [Baeldung: Testing in Spring Boot](https://www.baeldung.com/spring-boot-testing)

## **Month 2: Architecture & Scalability**

**Project:** Decompose the monolith into microservices.

### **Week 5: Intro to Microservices**

* \[ \] Research Monolith vs. Microservices architectures.  
* \[ \] Create a separate user-service Spring Boot project and migrate all user-related logic to it.  
* \[ \] Implement a REST call from the blog-service to the user-service using WebClient.

\<br\>  
Resources:

* [Microservices.io: Microservice Architecture Pattern](https://microservices.io/patterns/microservices.html)  
* [Baeldung: Spring 5 WebClient](https://www.google.com/search?q=https://www.baeldung.com/spring-webclient-tutorial)

### **Week 6: Asynchronous Communication & Caching**

* \[ \] Use RabbitMQ for asynchronous communication between services (e.g., a UserCreated event).  
* \[ \] Integrate Redis to cache frequently accessed data using Spring's @Cacheable annotation.

\<br\>  
Resources:

* [Official Guide: Messaging with RabbitMQ](https://spring.io/guides/gs/messaging-rabbitmq/)  
* [Official Guide: Caching](https://spring.io/guides/gs/caching/)

### **Week 7: Containerization with Docker 🐳**

* \[ \] Write Dockerfiles to containerize the blog-service and user-service.  
* \[ \] Create a docker-compose.yml file to define and run the entire application stack (services, DB, cache, message queue).

\<br\>  
Resources:

* [Official Guide: Spring Boot with Docker](https://spring.io/guides/gs/spring-boot-docker/)  
* [Docker Compose Overview](https://docs.docker.com/compose/)

### **Week 8: API Gateways & JWT Authentication**

* \[ \] Set up Spring Cloud Gateway to route requests to the appropriate microservice.  
* \[ \] Implement JWT issuance in the user-service upon login.  
* \[ \] Configure the gateway to validate JWTs on incoming requests, centralizing authentication.

\<br\>  
Resources:

* [Official Guide: Spring Cloud Gateway](https://spring.io/projects/spring-cloud-gateway)  
* [Baeldung: Spring Security and JWT](https://www.baeldung.com/spring-security-oauth-jwt)

## **Month 3: Operations & The Cloud (DevOps)**

**Project:** Deploy and Monitor your Application on AWS.

### **Week 9: Introduction to the Cloud (AWS)**

* \[ \] Sign up for an AWS Free Tier account.  
* \[ \] Provision core services: an EC2 instance, an RDS PostgreSQL database, and an S3 bucket.  
* \[ \] Update application configuration to use the new cloud resources.

\<br\>  
Resources:

* [AWS Free Tier](https://aws.amazon.com/free/)  
* [AWS Docs: Getting Started Guides](https://aws.amazon.com/getting-started/)

### **Week 10: CI/CD & Container Orchestration**

* \[ \] Create a GitHub Actions workflow to run tests and build Docker images on every push.  
* \[ \] Push built images to AWS ECR (Elastic Container Registry).  
* \[ \] Deploy and run your containers on an AWS ECS (Elastic Container Service) cluster.

\<br\>  
Resources:

* [GitHub Actions Documentation](https://docs.github.com/en/actions)  
* [AWS Docs: Getting Started with Amazon ECS](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/getting-started-fargate.html)

### **Week 11: Monitoring & Logging**

* \[ \] Use Spring Boot Actuator to expose application health and metrics.  
* \[ \] Configure services to send structured logs to AWS CloudWatch.  
* \[ \] Create CloudWatch Dashboards and Alarms to monitor key application metrics.

\<br\>  
Resources:

* [Baeldung: Spring Boot Actuator](https://www.baeldung.com/spring-boot-actuators)  
* [AWS Docs: What is Amazon CloudWatch?](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/WhatIsCloudWatch.html)

### **Week 12: Infrastructure as Code & Review**

* \[ \] Learn the basics of Terraform by writing a script to provision a simple AWS resource.  
* \[ \] Run the init, plan, apply, and destroy commands.  
* \[ \] Review all concepts from the past three months and update your professional profiles (GitHub, resume) with new skills.

\<br\>  
Resources:

* [Terraform on AWS: Get Started](https://developer.hashicorp.com/terraform/tutorials/aws-get-started)
