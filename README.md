# recipe-project

A production-style API built to demonstrate modern backend development practices.

## Deployment

This application is designed to be deployable to AWS (e.g., EC2 or ECS), but cloud infrastructure and secrets are intentionally excluded from this repository.

The codebase is deployment-ready and environment-agnostic. All environment-specific configuration, including credentials, database URLs, and secret keys, is injected at runtime via environment variables.

## Containerization

The application is fully containerized and developed using Docker and Docker Compose.

Docker Compose is used for local development and testing, providing a consistent environment across machines. Services are configured via environment variables, allowing the same containers to be used across development, staging, and production environments with minimal changes.

### Services
- Web API
- Database
- Supporting services as required

The Docker configuration is intentionally environment-agnostic and can be adapted for production orchestration (e.g., ECS or Kubernetes) without modifying application code.

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
