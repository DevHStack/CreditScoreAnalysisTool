# Credit Score Analysis Tool

A microservices-based prototype platform built with Spring Boot to analyze and manage credit score data. The system demonstrates how enterprise-grade services communicate and 
integrate using modern backend technologies.

## 🚀 Project Overview

This project is composed of multiple Spring Boot microservices communicating through REST APIs and routed using a Spring Cloud Gateway.

Main services included:

- Credit Scoring Service
- User Management Service
- Spring Cloud Gateway

The system simulates a credit score calculation and management platform with caching, messaging, and authentication mechanisms.

---
Client / UI
      ↓
Spring Cloud Gateway
      ↓
 ┌────────────────────────────┐
 │        Microservices        │
 │                              │
 │  UserManagement Service     │
 │  CreditScoring Service      │
 └────────────────────────────┘
      ↓
Supporting Systems
- Redis Cache
- Kafka Messaging
- Email Service
- Database


## 🧱 Architecture

### 1. CreditScoringServiceMS
Responsible for:
- Calculating credit scores
- Caching results using Redis
- Sending notifications using Kafka
- Logging and monitoring integrations

Technologies used:
- Spring Boot
- Redis Cache
- Apache Kafka
- Email notifications
- Log4j2 logging
- Splunk logging integration

---

### 2. UserManagementMS
Handles:
- User registration
- User login
- OAuth2 authentication
- Token validation

Technologies:
- Spring Security
- OAuth2
- JWT authentication
- REST APIs

---

### 3. SpringCloudGateway
Acts as an API gateway that:
- Routes requests to microservices
- Applies authentication filters
- Handles cross-origin requests

Technologies:
- Spring Cloud Gateway
- Spring Security

---

## 🔄 Microservice Communication

Services communicate using REST APIs.  
For example, the credit scoring service consumes user data from the user management service to process credit scores.

---

## ⚙️ Tech Stack

- Java
- Spring Boot
- Spring Cloud Gateway
- Spring Security
- OAuth2 & JWT
- Apache Kafka
- Redis Cache
- Maven
- REST APIs
- Log4j2
- Splunk logging

---

## 📂 Project Structure

## Each microservice contains:

src/main/java → Application source code
src/main/resources → Configuration files
src/test/java → Unit tests
pom.xml → Maven dependencies

---

## ▶️ Running the Project

### Requirements
- Java 17+
- Maven
- Redis (optional for caching)
- Kafka (optional for messaging)

### Run services
For each microservice:

```bash
mvn spring-boot:run

## START SERVICES IN ORDER

UserManagementMS

CreditScoringServiceMS

SpringCloudGateway


