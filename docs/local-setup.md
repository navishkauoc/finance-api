**Prerequisites**
1. Java 17
2. Maven
3. Docker Desktop

**How to set up**
1. Copy .env.example file to .env and fill in your own values. Never commit the real .env file.

**Running the Docker**
1. Run below commands in the terminal, while inside the project location.\
   i). _docker compose up -d_\
   &emsp;&emsp;a). First time: downloads the image, creates the volume, and starts the container.\
   &emsp;&emsp;b). Next time: If the container is already running, it does nothing. If it's stopped or was removed, it starts or recreates it. (The docker-compose file has restart: unless-stopped).\
   ii). _docker compose ps_\
   &emsp;&emsp;a). To check whether the container is running and to check the health.

**Running the Spring Boot application**
1. _./mvnw spring-boot:run_