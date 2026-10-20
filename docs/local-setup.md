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
2. Setting up pgAdmin (already added to docker-compose.yaml)\
   i). Visit http://localhost:5050 and log in with the email and password given in .env.\
   ii). To set up the server,\
   &emsp;&emsp;a).Servers → Register → Server…\
   &emsp;&emsp;b).On the General tab, enter a name, ex: finance-api (Docker)\
   &emsp;&emsp;c).On the Connection tab:\
   &emsp;&emsp;d).Host: postgres\
   &emsp;&emsp;e).Host: localhost
   &emsp;&emsp;f).Port: 5432\
   &emsp;&emsp;g).Maintenance database: finance_db\
   &emsp;&emsp;h).Username / Password: the values from the .env\
   &emsp;&emsp;i).Save

**Running the Spring Boot application**
1. _./mvnw spring-boot:run_