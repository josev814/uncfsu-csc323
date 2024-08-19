# POSTEGRES Server with PGAdmin

## Requirements
- [Docker Desktop](https://docs.docker.com/desktop/install/windows-install/)

## Usage
Go to the BuildTools directory
and copy postgres.env.example to postgres.env

Change the values for
- POSTGRES_PASSWORD
- PGADMIN_DEFAULT_EMAIL
- PGADMIN_DEFAULT_PASSWORD

Ensure that Docker Desktop is running by opening Docker Desktop from your Start menu

Open a Powershell Command Line (Powershell in your start menu)

Change to the directory where these files exist

### Stand up the containers
Run the following command to stand up postgres with pgadmin
```powershell
docker compose up -d
```

You can then open your browser to [http://localhost:8888](http://localhost:8888) to access pgadmin using your email and password that you set.

When looking at Docker Desktop you will now see the containers running as well

![Running Images](image.png)

### Stop containers
If you want to stop the containers, but plan on going back to use them later
```powershell
docker compose stop
```

### Start containers
If you want to start the containers after stopping them
```powershell
docker compose start
```

### Teardown containers
To remove the containers run this in powershell
```powershell
docker compose down
```

To also remove the data associated with the pgsql database
#### This will remove any data you have stored in your database!!
```powershell
docker compose down -v
```

