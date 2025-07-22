3-Month Server Engineer Learning Plan
This plan tracks the journey from experienced Android developer to intermediate Server Engineer over three months.

Month 1: The Core Backend Foundation
Project: Build a REST API for a simple blogging platform (Users, Posts, Comments).

Week 1: Spring Boot & REST APIs
[ ] Set up a Spring Boot project using Spring Initializr (Kotlin, Spring Web, Spring Data JPA).

[ ] Create a @RestController for a Post resource.

[ ] Implement GET /posts and GET /posts/{id} endpoints.

[ ] Implement POST /posts endpoint.

[ ] Implement PUT /posts/{id} endpoint.

[ ] Implement DELETE /posts/{id} endpoint.

[ ] Install and use Postman or Insomnia to test all created endpoints.

[ ] Refactor business logic from the controller into a dedicated @Service class.

<br>
Resources:

Official Guide: Building a RESTful Web Service with Spring Boot

Baeldung: Spring Boot with Kotlin

Postman: Getting Started

Week 2: Databases & Persistence
[ ] Install PostgreSQL locally or run it via Docker.

[ ] Configure your Spring Boot application to connect to the PostgreSQL database.

[ ] Create @Entity classes for User, Post, and Comment.

[ ] Create JpaRepository interfaces for each entity to handle database queries.

[ ] Connect your service layer to the repositories to persist and retrieve data.

[ ] Add a database migration tool (Flyway or Liquibase) to the project.

[ ] Create an initial migration script for your tables.

[ ] Learn and correctly apply the @Transactional annotation on service methods.

<br>
Resources:

Official Guide: Accessing Data with JPA

Baeldung: Introduction to Spring Data JPA

Flyway: Getting Started

PostgreSQL: Official Documentation

Week 3: Advanced APIs & Best Practices
[ ] Add jakarta.validation dependencies to your project.

[ ] Apply validation annotations (@NotNull, @Size, etc.) to request objects.

[ ] Create a global exception handler using @ControllerAdvice to return structured error responses.

[ ] Define DTOs (Data Transfer Objects) for your API's requests and responses.

[ ] Refactor controllers to use DTOs instead of exposing JPA entities directly.

[ ] Implement entity relationships (@OneToMany, @ManyToOne) between Users, Posts, and Comments.

<br>
Resources:

Baeldung: Spring Boot Validation

Baeldung: DTO Pattern in Spring

Baeldung: Error Handling for REST with Spring

Week 4: Testing & Basic Security
[ ] Write unit tests for your @Service classes using JUnit 5 and Mockito.

[ ] Write integration tests for your @RestController using @SpringBootTest and MockMvc.

[ ] Add the Spring Security dependency to your project.

[ ] Configure basic security with an in-memory or JDBC-based user store.

[ ] Secure your POST, PUT, and DELETE endpoints to require authentication.

<br>
Resources:

Official Guide: Spring Security Architecture

Baeldung: Testing in Spring Boot

JUnit 5 User Guide

Mockito Documentation

Month 2: Architecture & Scalability
Project: Decompose the monolith into microservices.

Week 5: Intro to Microservices
[ ] Read an article or watch a video comparing Monolith vs. Microservices architectures.

[ ] Create a new, separate Spring Boot project named user-service.

[ ] Move all user-related code (Entity, Repository, Service, Controller) to the user-service.

[ ] Remove the user code from the original blog-service.

[ ] Implement a REST call from blog-service to user-service using WebClient.

<br>
Resources:

Microservices.io: Pattern: Microservice Architecture

Spring Cloud Documentation

Baeldung: Spring 5 WebClient

Week 6: Asynchronous Communication & Caching
[ ] Run RabbitMQ using a Docker container.

[ ] Add the spring-rabbit dependency to both microservices.

[ ] Make the user-service publish a UserCreated message to a RabbitMQ queue.

[ ] Make the blog-service consume this message to perform a follow-up action.

[ ] Run Redis using a Docker container.

[ ] Add the Spring Data Redis dependency to your blog-service.

[ ] Apply the @Cacheable annotation to a high-traffic method, like fetching a post by its ID.

[ ] Verify that the cache is working by checking logs or using a Redis CLI.

<br>
Resources:

Official Guide: Messaging with RabbitMQ

Official Guide: Caching

Redis: Official Documentation

RabbitMQ: Get Started

Week 7: Containerization with Docker 🐳
[ ] Install Docker Desktop on your computer.

[ ] Write a Dockerfile for your blog-service.

[ ] Write a Dockerfile for your user-service.

[ ] Build Docker images for both services using the docker build command.

[ ] Create a docker-compose.yml file.

[ ] Define all services in the compose file: blog-service, user-service, postgres, rabbitmq, and redis.

[ ] Start your entire multi-container application with a single docker-compose up command.

<br>
Resources:

Docker: Get Started

Official Guide: Spring Boot with Docker

Docker Compose Overview

Week 8: API Gateways & JWT Authentication
[ ] Create a new Spring Boot project with the Spring Cloud Gateway dependency.

[ ] Configure routes in the gateway to forward requests to the correct microservice.

[ ] Add a JWT library dependency to your user-service.

[ ] Create a /login endpoint in the user-service that returns a JWT on success.

[ ] Configure the API Gateway to validate JWTs on incoming requests.

[ ] Update your Postman collection to first log in, save the token, and use it as a Bearer Token on subsequent requests.

<br>
Resources:

Official Guide: Spring Cloud Gateway

Baeldung: Spring Security and JWT

JWT.io: Introduction to JSON Web Tokens

Month 3: Operations & The Cloud (DevOps)
Project: Deploy and Monitor your Application on AWS.

Week 9: Introduction to the Cloud (AWS)
[ ] Sign up for an AWS Free Tier account.

[ ] Launch a small t2.micro EC2 instance and connect to it via SSH.

[ ] Create a managed PostgreSQL database using AWS RDS.

[ ] Update your application configuration to connect to the RDS instance.

[ ] Create a private S3 bucket for storing files.

<br>
Resources:

AWS Free Tier

AWS Docs: Launch an EC2 Instance

AWS Docs: Create a PostgreSQL DB with RDS

AWS Docs: Getting started with S3

Week 10: CI/CD & Container Orchestration
[ ] Create a new GitHub repository for your project.

[ ] Set up a GitHub Actions workflow (.github/workflows/ci.yml).

[ ] Configure the workflow to automatically run tests (./gradlew test) on every push.

[ ] Create an AWS ECR (Elastic Container Registry) repository.

[ ] Add steps to your GitHub Actions workflow to build and push your Docker image to ECR.

[ ] Create an AWS ECS (Elastic Container Service) cluster.

[ ] Create an ECS Task Definition and Service to deploy and run your container from ECR.

<br>
Resources:

GitHub Actions Documentation

AWS Docs: What is Amazon ECR?

AWS Docs: Getting Started with Amazon ECS

Week 11: Monitoring & Logging
[ ] Add the Spring Boot Actuator dependency to your services.

[ ] Explore the /actuator/health and /actuator/metrics endpoints.

[ ] Configure your services to output logs in a structured JSON format.

[ ] Configure your ECS task to send container logs to AWS CloudWatch Logs.

[ ] Find and search your application's logs in the CloudWatch console.

[ ] Create a CloudWatch Dashboard to monitor key metrics like CPU and Memory usage of your service.

[ ] Create a CloudWatch Alarm that sends you a notification if a metric crosses a threshold.

<br>
Resources:

Official Guide: Spring Boot Actuator

Baeldung: Spring Boot Actuator

AWS Docs: What is Amazon CloudWatch?

Week 12: Infrastructure as Code & Review
[ ] Install Terraform on your local machine.

[ ] Write a simple Terraform script to provision a single AWS resource (e.g., an S3 bucket).

[ ] Run terraform init, terraform plan, and terraform apply.

[ ] Clean up the resource using terraform destroy.

[ ] Review all the projects and concepts from the last 3 months.

[ ] Clean up and push all your project code to GitHub.

[ ] Update your resume and LinkedIn profile with your new skills: Spring Boot, Microservices, Docker, AWS (ECS, RDS, S3), CI/CD, and more.

<br>
Resources:

Terraform: Introduction

Terraform on AWS: Get Started
