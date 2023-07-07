# Attention: This is a Template Repo

Please fork this repository (or click the `Use this template` button) before attempting to use it to deploy Veramo. This will allow you to maintain your agent and update it to the latest version as you wish. 

# Veramo Agent Deploy

**The official Veramo Docker agent is built from this this source.**

## Environment variables

These are the default environment variables use in the production config.

#### `BASE_URL`

Set this to your base app url. Your default web:did will be based on this when it gets created on first run. Be sure to replace `APP_NAME` with the actual name of your app.

#### `API_KEY`

Used for authorization

#### `SECRET_KEY`

Used for encrypting the database

#### `AGENT_PATH`

The path where the agent will be accessible from, default to `/agent`

#### `MESSAGING_PATH`

The path where the messaging will be accessible from, default to `/messaging`

#### `PORT`

The port to run the server on

#### `DATABASE_URL`

The database connection string for Postgres

## Deploy to Heroku

You will need to fork this repo, then click the button below and follow the Heroku deploy process:

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/zdravko61/veramo-agent-deploy/tree/nickreynolds/mediator)

Be sure to set the `BASE_URL` correctly, with your App name replacing `APP_NAME` in the URL.

You will be able to access your agent at `https://your-app-name.herokuapp.com/agent` and you can find your OpenAPI Schema at `https://your-app-name.herokuapp.com/open-api.json`. 

You can find the required API Key through the Heroku project settings (`Reveal Config Vars`).

The deployment will create a link between your forked repo and the Heroku instance. When you update your repo (e.g. updating the Veramo package version, changing your agent configuration), Heroku will automatically deploy

## Deploy to Heroku using Docker

You will need to fork this repo and add the following key/value pair to the root of `app.json`. You can then use the same deploy button as above or use the Heroku cli.

```json
{
  "stack": "container"
}
```

## Deploy to Azure Pipelines

Coming soon

## Deploy to Azure Pipelines using docker

Coming soon

## Deploy to AWS

Follow the instructions on our docs page: [Veramo.io Docs](https://veramo.io/docs/deployment_tutorials/deployment_aws)
