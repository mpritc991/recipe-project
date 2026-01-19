# Recipe Project API

A production-style Django REST Framework API built to demonstrate modern backend development practices, including authentication, relational data modeling, filtering, automated testing, and containerized workflows.

This project implements a complete recipe management API with support for users, recipes, tags, ingredients, image uploads, and query-based filtering. The focus is on clean architecture, test coverage, and deployment readiness.

## Overview

The goal of this project is to showcase backend engineering skills through a realistic, production-oriented API. Emphasis is placed on maintainability, correctness, and portability across environments rather than UI or frontend concerns.

The application is designed to be environment-agnostic and suitable for deployment in a containerized cloud environment.

## Key Features

- Token-based authentication and per-user data isolation
- CRUD operations for recipes, tags, and ingredients
- Many-to-many relationships with query-parameter filtering
- Image upload handling for recipe objects
- Reusable base viewsets to reduce duplication
- Comprehensive automated test suite
- OpenAPI schema documentation using drf-spectacular

## Tech Stack

- Python
- Django
- Django REST Framework
- PostgreSQL
- Docker and Docker Compose
- drf-spectacular
- pytest

## Containerization

The application is fully containerized using Docker and Docker Compose.

Docker Compose is used for local development and testing, providing a consistent environment across machines. Services are configured via environment variables, allowing the same containers to be used across development, staging, and production environments with minimal changes.

## Deployment

This application is designed to be deployable to cloud infrastructure such as AWS (e.g., EC2 or ECS), but cloud resources and secrets are intentionally excluded from this repository.

The codebase is deployment-ready and environment-agnostic. All environment-specific configuration, including credentials, database URLs, and secret keys, is injected at runtime via environment variables.

## Production Considerations

- Environment variables are expected to be configured externally
- Secrets are never committed to source control
- Static assets and media storage should be configured per environment
- Infrastructure concerns are intentionally decoupled from application code

This separation ensures the repository remains clean, secure, and portable across environments.

## Environment Variables

Environment-specific configuration is managed via environment variables.

A sample configuration file is provided:

```bash
cp env.sample .env
