# Ardalo Digital Platform Overview
The Ardalo Digital Platform is a blueprint how a modern digital platform may be implemented
using multiple teams and a Microservice approach.

Prerequisites for running the Ardalo Digital Platform:
* Kubernetes
* [Traefik](https://traefik.io/traefik/) as Ingress Controller

The Platform consists of the following components:
* [Guidelines and FAQ](https://github.com/ardalo/digital-platform-development-guide) for the development of the Ardalo Digital Platform
* The [Customer Account Service](https://github.com/ardalo/adp-customer-account-service) taking care of the customer account domain
  * [API Documentation](http://35.193.141.187/internal/adp-customer-account-service/swagger-ui/)
  * Provides also the global 404 page

The Platform utilizes the following external services:
* [GitHub](https://github.com/ardalo?tab=repositories) - Source Code Hosting, Version Control System and CI/CD pipeline
* [SonarCloud](https://sonarcloud.io/organizations/ardalo/projects) - Static Code Analysis
* [Docker Hub](https://hub.docker.com/u/ardalo) - Docker Container Registry
* [Google Cloud Platform](https://cloud.google.com/?hl=de) - Infrastructure / Runtime environment

## Open Issues
* 404 page returns `HTTP 200 OK` instead of `HTTP 404 Not Found`
  * In case a 404 occurs, the Ingress Controller requests a 404 page from a service. This 404 page is
    returned with status code 200 and needs to be mapped to 404 within the Ingress Controller. Traefik
    has no middleware out of the box yet which performs that mapping. Thus the status code remains 200
    for the 404 page. For a production environment this is not suitable.
