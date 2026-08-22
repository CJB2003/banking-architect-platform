# Banking-Architect-Platform

A microservices-based trade/order processing system built with Spring Boot, Kafka, and Cassandra.

## Architecture

As of right now, the plan is to build the project within Spring Boot, have Kafka be our messenger for producer/consumer services, persist data to Cassandra, and deploy with Kubernetes locally, then AWS EKS to the cloud.

## Services

- `order-service` — accepts orders, persists to Cassandra, publishes events
- `risk-service` — consumes order events, computes exposure
- `notification-service` — consumes processed events, notifies downstream

## Local development

See individual service READMEs under `services/`.
