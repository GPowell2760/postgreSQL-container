# PostgreSQL Container

## Project Structure

```shell
.
├── .env
├── README.md
└── docker-compose.yaml
```

## Install

Change the default username and password in the .env file.

```shell
POSTGRES_USER=postgres
POSTGRES_PW=postgres
```

Run the following command to pull and run the image

```shell
docker compose up -d
```

## Connect pgAdmin

[pgAdmin4](https://www.pgadmin.org/download/)

After logging in with your credentials of the .env file, you can add your database to pgAdmin.

1. Right-click "Servers" in the top-left corner and select "Create" -> "Server..."
2. Name your connection
3. Change to the "Connection" tab and add the connection details:

- Hostname: "postgres" (this would normally be your IP address of the postgres database - however, docker can resolve this container ip by its name)
- Port: "5432"
- Maintenance Database: $POSTGRES_DB (see .env)
- Username: $POSTGRES_USER (see .env)
- Password: $POSTGRES_PW (see .env)
