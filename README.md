# Project: Ambassador Product Platform

## Overview
This project is a full-stack Ambassador Product Platform that allows users to register as ambassadors, generate custom referral links, and earn commissions on referred product purchases. The system is built using Laravel for backend microservices, Angular for the frontend applications, and orchestrated with Docker and Kubernetes for deployment and scaling. Communication between services is efficiently handled through Apache Kafka for asynchronous messaging.

## Microservice Architecture

### 1. Users Microservice
- **Framework:** Laravel
- **Role:** Handles user authentication, registration, and profile management.
- **Security:** Includes secure authentication mechanisms.
- **Database:** MySQL
- **Deployment:** Docker container

### 2. Admin Microservice
- **Framework:** Laravel
- **Role:** Backend management for administrators to oversee ambassadors, products, and transactions.
- **Frontend:** Admin Panel built with Angular (or Vue/React alternatives).
- **Database:** MySQL
- **Deployment:** Docker container

### 3. Ambassador Microservice
- **Framework:** Laravel
- **Role:** Enables ambassadors to manage their profiles, view commissions, and generate custom product referral links.
- **Caching:** Uses Redis for efficient link management and caching frequently accessed data.
- **Frontend:** Ambassador Panel built with Angular (or Vue/React).
- **Database:** MySQL
- **Deployment:** Docker container

### 4. Checkout Microservice
- **Framework:** Laravel
- **Role:** Handles product checkout, order processing, and commission allocation for ambassadors.
- **Payment Gateway:** Integrated with Stripe.
- **Database:** MySQL
- **Deployment:** Docker container

### 5. Email Microservice
- **Framework:** Laravel
- **Role:** Manages the sending of transactional emails, such as order confirmations and notifications to users and ambassadors.
- **Deployment:** Docker container

## Communication
- **Message Broker:** Apache Kafka for asynchronous communication between microservices.

## Orchestration
- **Containerization:** Docker
- **Orchestration and Scaling:** Kubernetes
