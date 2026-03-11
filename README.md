# Bitasmbl-Esoterica-Online-Game-Backend-Service-a34e72-19474608cffb

## Description
A Kotlin/Micronaut backend for online games providing high-performance APIs, matchmaking, player session management, and reliable communication via PostgreSQL and RabbitMQ.

## Tech Stack
- Kotlin
- Micronaut
- PostgreSQL
- RabbitMQ

## Requirements
- Expose REST API for creating and fetching player sessions using Kotlin and Micronaut.
- Persist player sessions in PostgreSQL and retrieve them by playerId.
- Publish a RabbitMQ event whenever a new player session is created.
- Implement a consumer that logs or processes the incoming session-created events.
- Secure game backend endpoints with a simple API key header validation.

## Installation
- git clone https://github.com/he1snber8/Bitasmbl-Esoterica-Online-Game-Backend-Service-a34e72-19474608cffb.git
- Configure PostgreSQL and RabbitMQ connection settings in Micronaut configuration.
- ./gradlew build

## Usage
- Run: ./gradlew run
- Set API key header on all requests.

## API Endpoints
- POST /sessions
- GET /sessions/{playerId}

## Implementation Steps
1. Define Micronaut controllers for session REST endpoints.
2. Create PostgreSQL entities and repositories for player sessions.
3. Implement service layer for session creation and retrieval by playerId.
4. Integrate RabbitMQ publisher for session-created events.
5. Implement RabbitMQ consumer to log or process session-created events.
6. Add API key header filter for securing endpoints.
7. Wire configuration for PostgreSQL and RabbitMQ in Micronaut.