# College ERP

An ERP system for educational institutes. Built with Frappe.

## Setup

### Development environment

#### Pre-requisites

1. Docker
   ```sh
   docker -v   # Check if Docker is installed.
   ```
2. [Docker Compose](https://docs.docker.com/compose/)
   ```sh
   docker compose version  # Check if Docker Compose is installed.
   ```
3. Git
   ```sh
   git -v # Check if Git is installed.
   ```

#### Installation

1. Clone the `frappe_docker` repository
   ```sh
   git clone https://github.com/frappe/frappe_docker.git
   ```
2. Move inside the cloned repository
   ```sh
   cd frappe_docker
   ```
3. Create and start containers defined in `devcontainer-example/docker-compose.yml`.
   ```sh
   docker compose -f devcontainer-example/docker-compose.yml up
   ```
4. Start interactive shell session within the Frappe container
   1. Find the name of container
      ```sh
      docker ps
      ```
      ![image](https://github.com/pokhiii/college-erp/assets/11808845/1b81ee46-800c-4765-a605-5e05914a5b46)
   2. Start interactive shell
      ```sh
      docker exec -it devcontainer-example-frappe-1 /bin/sh
      ```