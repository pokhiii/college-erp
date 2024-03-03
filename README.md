# College ERP

An ERP system for educational institutes. Built with [Frappe](https://frappeframework.com/).

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

1. Clone the repository
   ```sh
   git clone https://github.com/pokhiii/college-erp.git
   ```
2. Move inside the cloned repository
   ```sh
   cd college-erp
   ```
3. Create and start containers defined in `college-erp/docker-compose.yml`.
   ```sh
   docker compose -f college-erp/docker-compose.yml up
   ```
4. Start interactive shell session within the Frappe container
   1. Find the name of container
      ```sh
      docker ps
      ```
      ![image](https://github.com/pokhiii/college-erp/assets/11808845/4374419c-217c-42eb-b6e9-38020221c022)
   2. Start interactive shell
      ```sh
      docker exec -it college-erp-frappe-1 /bin/sh
      ```
5. Inside the container
   ```sh
   cd frappe-bench
   ```
6. Start the app
   ```sh
   bench start
   ```