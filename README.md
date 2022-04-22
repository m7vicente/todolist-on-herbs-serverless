![Node.js CI](https://github.com/herbsjs/todolist-on-herbs/workflows/Node.js%20CI/badge.svg)

# What's Herbs?

Herbs is an open source library for backend applications. It is focused on achieving faster deliveries and with happier developers, without neglecting the long-term need to constantly evolve your application as requirements change.

See more on the website: [https://herbsjs.org/](https://herbsjs.org/)

# Getting Started with TO DO list on Herbs

Within this repository, you will find a front-end application, made in react consuming a back-end application, using [Herbs](https://github.com/herbsjs), the API is made in graphQL


# Todolist on Herbs

This is a example on how to build a backend application using [Herbs](https://github.com/herbsjs).

### Using

    $ npm install
    $ npm run knex:migrate
    $ npm start

  You should receive this message => 🚀 Server UP and Running in port: 4000

  VSCode launchers (launch.json) are also available.

### Postgresql setup

  1. Change `knexfile.js` and `src\infra\config\dev.json` connection info.

  2. Run migration:

    $ npx knex migrate:latest --env development

### Herbs Shelf

View all the use cases and its steps in just one place.

Herbs Shelf: [http://localhost:4000/herbsshelf](http://localhost:4000/herbsshelf)

Documentation dynamically generated by [herbsshelf](https://github.com/herbsjs/herbsshelf/).

### GraphQL

GraphQL Playground: [http://localhost:4000/graphql](http://localhost:4000/graphql)

GraphQL dynamically generated by [herbs2gql](https://github.com/herbsjs/herbs2gql).

### Rest

Express routes dynamically generated by herbs2rest.

### Herbs REPL

View all the use cases your termnal.

    $ node ./src/infra/repl

REPL dynamically generated by [Herbs REPL](https://github.com/herbsjs/herbs2repl).

### Settings

**Environment:**

`.env.{environment}` files.

Rename one of the files to just `.env`.

Default is `dev`. Also check for `HERBS_EXCEPTION` env variable.

**Config:**

Edit `/backend/infra/config/{environment}.json` files if necessary.

## How to contribute

If you would like to help contribute to this repository, please see [CONTRIBUTING](https://github.com/herbsjs/todolist-on-herbs/blob/master/.github/CONTRIBUTING.md)

### License

- [MIT License](https://github.com/herbsjs/todolist-on-herbs/blob/master/LICENSE)



```
classDiagram
    class User {
        Number ID
        String firstName
        String lastName
        Number age
        User_Account[] accounts
    }
    class User_Account{
        Number ID
        Date expirationDate
        isExpired()
    }
    class Project{
        Number ID
        String name
        User_Account user
        Task[] tasks
    }
    class Task{
        Number ID
        String name
        Date dueDate
    }
    User "1" --> "*" User_Account
    Project "1" --> "1" User_Account
    Project "1" --> "*" Task
```

```mermaid
classDiagram
    class User {
        Number ID
        String firstName
        String lastName
        Number age
        User_Account[] accounts
    }
    class User_Account{
        Number ID
        Date expirationDate
        isExpired()
    }
    class Project{
        Number ID
        String name
        User_Account user
        Task[] tasks
    }
    class Task{
        Number ID
        String name
        Date dueDate
    }
    User "1" --> "*" User_Account
    Project "1" --> "1" User_Account
    Project "1" --> "*" Task
```
