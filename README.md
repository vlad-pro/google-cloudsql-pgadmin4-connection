# Google CloudSQL local connection + pgadmin4

## Configuration and startup

1. To run the local docker compose environment you will need to populate .env.example file with connection information. You need database and connection credentials to be able to start.

2. Change .env.example to .env and edit the contents with your data

3. `docker-compose --env-file .env up -d` This will bring local environment up for you: cloud sql proxy for connecting to the database and pgadmin4 that you can use for your convinience.

4. To use pgadmin4 open your browser and navigate to localhost:5050, if you did not changed the port in the env file. Use login and password from env file to get in. Use cloudsql container name from the docker-compose.yml file as a "Hostname/address" in pgadmin4 connection tab when creating a server conenction. In this project it's name is sql_proxy.
