# Monitower
Monitower is a containerized monitoring stack designed to provide observability and alerting for your infrastructure. This project leverages Docker Compose to orchestrate multiple services for metrics collection, visualization, error tracking, alert management, authentication, and container registry management.

## Services

- **Prometheus**: Collects and stores metrics from configured targets.
- **Grafana**: Visualizes metrics and dashboards.
- **Alertmanager**: Handles alerts sent by Prometheus.
- **Node Exporter**: Exposes hardware and OS metrics for Prometheus.
- **Glitchtip**: Provides error tracking and monitoring for your applications.
- **Registry**: A private Docker registry for storing and distributing your container images.
- **Keycloak**: Provides identity and access management, enabling single sign-on (SSO) and secure authentication for your services.
- **(Other services as defined in your `docker-compose.yml`)**

## Getting Started

### Prerequisites

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/)

### Startup Instructions

1. Clone this repository:
    ```sh
    git clone https://github.com/yourusername/monitower.git
    cd monitower
    ```

2. Start all services:
    ```sh
    docker-compose up -d
    ```

3. Access the dashboards and services:
    - **Grafana**: [http://localhost:3000](http://localhost:3000)
    - **Prometheus**: [http://localhost:9090](http://localhost:9090)
    - **Alertmanager**: [http://localhost:9093](http://localhost:9093)
    - **Glitchtip**: [http://localhost:8000](http://localhost:8000)
    - **Registry**: [http://localhost:5000](http://localhost:5000)
    - **Keycloak**: [http://localhost:8080](http://localhost:8080)

4. Stop the stack:
    ```sh
    docker-compose down
    ```

## Configuration

- Edit `prometheus.yml` to add scrape targets.
- Configure Grafana dashboards and data sources as needed.
- Adjust alert rules in Prometheus and Alertmanager configurations.
- Set up projects and configure error reporting in Glitchtip.
- Configure authentication and storage for the Registry as needed.
- Set up realms, clients, and users in Keycloak to manage authentication and authorization for your services.

## Purpose

Monitower provides a quick way to deploy a full-featured monitoring stack using Docker Compose. It is suitable for development, testing, or small-scale production environments, and includes a private registry for managing your container images, as well as integrated authentication with Keycloak.

## License

MIT
