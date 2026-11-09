# Correspondances

Refonte de la billetterie d'un réseau ferroviaire régional : modélisation, migrations et performance sur PostgreSQL 16.

## Stack

- PostgreSQL 16 (Docker)
- Java 21, Spring Boot 3.5, Spring Data JPA / Hibernate
- Flyway pour les migrations
- Swagger UI (springdoc) pour tester les endpoints

## Prérequis

- Docker et Docker Compose
- JDK 21
- Maven

## Lancement

```bash
docker compose up -d
mvn spring-boot:run
```

Au démarrage, Flyway applique les migrations de `src/main/resources/db/migration` qui ne l'ont pas encore été.

Swagger UI : http://localhost:8080/swagger-ui.html

## Structure

```
docs/        MCD, MLD, MPD, explication des choix, dossier performance
db/          générateur de volumétrie et requêtes commentées
src/         projet Spring Boot, entités et migrations
```

## Documentation

- [Modélisation](docs/modelisation.md)
