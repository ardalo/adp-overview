# Ardalo Digital Platform Overview
The Ardalo Digital Platform is a blueprint how a modern digital platform may be implemented
using multiple teams and a Microservice approach.

### Prerequisites for running the Ardalo Digital Platform
* Kubernetes
* [Traefik](https://traefik.io/traefik/) as Ingress Controller

### Component Overview
* [Guidelines and FAQ](https://github.com/ardalo/digital-platform-development-guide) for the development of the Ardalo Digital Platform
* The [Customer Account Service](https://github.com/ardalo/adp-customer-account-service) taking care of the customer account domain
  * [API Documentation](http://35.193.141.187/internal/adp-customer-account-service/)
  * Provides also the global 404 page

### Utilized External Services
* [GitHub](https://github.com/ardalo?tab=repositories) - Source Code Hosting, Version Control System and CI/CD pipeline
* [SonarCloud](https://sonarcloud.io/organizations/ardalo/projects) - Static Code Analysis
* [Docker Hub](https://hub.docker.com/u/ardalo) - Docker Container Registry
* [Google Cloud Platform](https://cloud.google.com/?hl=de) - Infrastructure / Runtime environment
