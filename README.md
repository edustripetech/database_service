# database_service

## Getting Started

This application simply handles and tracks all changes to the database through migration files.
The instructions to get it up and running is listed below:

### Installing
- run `yarn install` to install all dependencies
- run `cp .env.sample .env` to copy the environment variables and replace their descriptions with actual values


### DB Operations

- To run migrations, use the following commands
`npx sequelize-cli db:migrate` OR `yarn migrate`

- To create a new model/migration file, run
`npx sequelize-cli model:generate --name <model-name> --attributes <attribute-name>:<attribute-type>` OR `yarn generate:model --name <model-name> --attributes <attribute-name>:<attribute-type>`
For Example `yarn generate:model --name Todos --attributes title:string`

- To undo migrations, run
`npx sequelize-cli db:migrate:undo:all` OR `yarn migrate:undo` # This will undo all migrations
`npx sequelize-cli db:migrate:undo` OR `yarn migrate:undo:last` # This will undo the last migration

- To seed the table with dummy data, create a seed file as described [here](http://docs.sequelizejs.com/manual/migrations.html) and then run
`npx sequelize-cli db:seed:all` OR `yarn seed`

- To rollback and delete seed data run
`npx sequelize-cli db:seed:undo` OR `yarn seed:undo`
