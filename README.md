# Application - Petstore Java EE 7

The original application and documentation can be found here https://github.com/agoncal/agoncal-application-petstore-ee7

This version of the application includes Dockerfile and associated files/tools to run the application as 
a container with Postgres.

## Running the Application
To run the application we will execute the following Docker Compose commands.

Step 1:: Run the database container in the background (`-d` or daemon flag). We don't need the database logs to clog our application logs.
```
docker-compose up -d postgres
```

Step 2:: Build out petstore application.
```
docker-compose build petstore
```

Step 3:: Run the application container in the foreground and live stream the logs to stdout. If you hit an error hit `Ctrl+C`, make updates to the Dockerfile and re-build the container using step 2.

```
docker-compose up petstore
```
Step 4:: To preview the application you will need to click *Preview* from the top menu of the Cloud9 environment. This will open a new window and pre-populate the full URL to your preview domain.