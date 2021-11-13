# PostgreSQL + pgAdmin 4 + Docker-Compose

This is an example to show how to setup PostgreSQL + pgAdmin 4 + Docker-Compose.

## How to do the set up? ##

**:warning: Warning:** it´s necessarily to developers to have Docker installed in your machine, so please follow the steps below:
- 🐳 [Docker Engine Installation](https://docs.docker.com/engine/install/ubuntu/)  
- 🐳 [Docker Compose Installation](https://docs.docker.com/compose/install/)  
- **💡 Tip:** [For any doubts please use Docker documentation](https://docs.docker.com/)  

### Using the application

After install Docker and Docker-compose, open your terminal and execute:

```sh
sudo docker-compose up
```
For to access the container application, execute in another terminal window:

```sh
sudo docker-compose run --rm postgres bash
```

For reset the application(to drop and on again), execute:

```sh
docker-compose down && docker-compose up
```

#### Setting up

Go to [localhost:5555](http://localhost:5555/) and use the application like the example below:

![Setup](https://raw.githubusercontent.com/claudimf/PostgreSQL_pgAdmin4_Docker-Compose/main/Set_up.gif)

Variables:  

```sh
PGADMIN_DEFAULT_EMAIL: pgadmin4@pgadmin.org
PGADMIN_DEFAULT_PASSWORD: admin
HOSTNAME: postgres
POSTGRES_USER: postgres
POSTGRES_PASSWORD: postgres
```

### Files permissions ###
When you/or application creates some file using the Docker container and you need to edit it you will need to change the file permission executing the following command in terminal first:

```sh
sudo chown -R $USER:$USER .
```

## References used for consultation ##
[1° Docker Engine Installation](https://docs.docker.com/engine/install/ubuntu/)  
[2° Docker Compose Installation](https://docs.docker.com/compose/install/)  
[3° Docker documentation](https://docs.docker.com/)  
[4° PostgreSQL Schema](https://www.postgresqltutorial.com/postgresql-schema/)  
[5° How to Run PostgreSQL Using Docker](https://towardsdatascience.com/how-to-run-postgresql-using-docker-15bf87b452d4)  
