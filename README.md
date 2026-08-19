# Config Server

Centralized configuration management component for the Pet Clinic microservices platform.

## Student Information
- **Student Name:** Isuri Gamage
- **Student Number:** 241722008
- **Slack Handle:** 
- **GCP Project ID:** 

## Project Description
The `config-server` externalizes and centralizes configuration properties for all microservices in the Pet Clinic system. Instead of each service managing its own configuration in isolation, they fetch shared and environment-specific configuration from this server at startup, simplifying configuration management across the distributed system.

## Technology Stack
- **Language:** Java 25
- **Framework:** Spring Boot, Spring Cloud Config Server
- **Build Tool:** Maven
- **Cloud Platform:** Google Cloud Platform (GCP) — deployed as IaaS on Compute Engine VM Instance Groups (multi-zone for high availability)
- **Process Management:** PM2

## Setup / Getting Started

### Prerequisites
- Java 25 (JDK)
- Maven

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/Isuri15/config-server.git
   cd config-server
   ```
2. Build and run the service:
   ```bash
   mvn clean install
   mvn spring-boot:run
   ```
3. The Config Server will start on port `8888`.
4. Start this service **before** the business microservices (owner-service, pet-service, appointment-service, api-gateway).

## Cloud Deployment
Deployed on Google Cloud Platform with multiple instances distributed across different zones within the region to ensure high availability and fault tolerance, as required by the platform's high-availability architecture.

## Related Repositories
This service is part of the Pet Clinic platform components. See the parent repository:
- [backend-microservices-platform](https://github.com/Isuri15/backend-microservices-platform)
