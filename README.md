# Banking-Architect-Platform

A microservices-based trade/order processing system built with Spring Boot, Kafka, and Cassandra.

## Architecture

See `docs/architecture.md`.

## Services

- `order-service` — accepts orders, persists to Cassandra, publishes events
- `risk-service` — consumes order events, computes exposure
- `notification-service` — consumes processed events, notifies downstream

## Local development

See individual service READMEs under `services/`.
