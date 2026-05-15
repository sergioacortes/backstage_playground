# backstage
backstage playground projects

## Backstage projects 

* playground

## Environment configuration

To start using the backstage projects you most configure the following dependencies.

## dotenv

The package dotenv is used to load the .env file as environment variables before the application start, run the following command to instal dotenv from npm.

```
npm install -g dotenv
```

## Environment variables

Create a .env file on the root of the repository to store the environment variables that are going to be used by docker-compose and backstage projects

```
POSTGRES_HOST=localhost
POSTGRES_PORT=5432
POSTGRES_USER=backstage
POSTGRES_PASSWORD=your_postgres_password
POSTGRES_DB=backstage
GITHUB_APPLICATION_CLIENT_ID=your_github_client_id
GITHUB_APPLICATION_CLIENT_SECRET=your_github_client_secret
```
NOTE: If you have an instance of Postgres on your local machine you must set the environment variables with the values of your instance.

## Postgres

If you have an instance of Postgres on your local machine you can skip this step, otherwise run the following command to run a docker instance of postgres

```
docker-compose up -d
```

# Run backstage project

To run a backstage application go to application folder ej. playground, and run the following command 

```
cd playground
dotenv -e ../.env yarn start
```