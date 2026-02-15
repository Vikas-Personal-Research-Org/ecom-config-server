# E-Commerce Config Server

Spring Cloud Config Server that provides centralized configuration management for the e-commerce microservices platform.

## Overview

This service runs on port **8888** and serves configuration to the following microservices using a native (classpath) profile:

| Service                | Port |
|------------------------|------|
| API Gateway            | 8080 |
| Product Service        | 8081 |
| Inventory Service      | 8082 |
| Order Service          | 8083 |
| User Service           | 8084 |
| Payment Service        | 8085 |
| Notification Service   | 8086 |

## Running

```bash
mvn spring-boot:run
```

## Building

```bash
mvn clean package
```

## Docker

```bash
docker build -t ecom-config-server .
docker run -p 8888:8888 ecom-config-server
```

## Fetching Configuration

Once running, service configurations can be retrieved at:

```
http://localhost:8888/<service-name>/default
```
