# Learning Sql Using Postgres

Companion repository for [postgres course](https://www.udemy.com/course/postgresql-from-zero-to-hero).

## Requirements

- Docker and Docker Compose

## Setup

### Running Containers

`docker-compose up -d`

### Accessing PGAdmin4

To login, the email is test@example.com and the password is "SuperSecret". If you want to change these values they are in the docker-compose.yml file. Change the environment variables PGADMIN_DEFAULT_EMAIL and PGADMIN_DEFAULT_PASSWORD to whatever you want.

Navigate to http://localhost:8888 in your browser and login.

### Adding a Database Server

On the home page, click on “Add New Server”.

The two tabs you need to modify are “General” and “Connection”. Add the name of the database under General. The database name is "postgres". Under the “Connection” tab, fill in the host name which should be "db" unless you changed it in your docker-compose.yml file. Then add your username and password. The username and password is "postgres" for both fields. Then check save password. Finally, click “Save”.

### Adding Databases

The tar files in this repository are test databases for learning.

In PGAdmin, on the left sidebar, hover over "Databases" and right click to create a new database. Create a database for each tar file using the file names (e.g., "northwind", "pagila", "usda", "AdventureWorks"). Next you need to restore the database using the tar file. Right click on a database name, then select "Restore". Change the "Format" at the bottom from "backup" to "All files". Then you want to upload the tar file by clicking the upload icon above and then dragging the tar file into the window. Click the upload icon again to toggle back to the file listing. Select the tar file you uploaded and click "Select", then "Restore". When you do this you will see an error because the public schema is already created. You can safely ignore this popup. Repeat these steps to restore all databases.
