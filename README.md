# Express + Typescript + Prisma boilerplate

This is an opinionated express + typescript boilerplate. Prisma is being used as an ORM to have the flexibility of switching databases with minimal code change.
This repo is created as a [template repo](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template).

## Stack

[![My Tech Stack](https://github-readme-tech-stack.vercel.app/api/cards?fontWeight=normal&align=left&titleAlign=center&lineCount=4&theme=github_dark&hideTitle=true&line1=node.js,node.js,ddbfef;typescript,typescript,543e05;&line3=eslint,eslint,3663f5;prettier,prettier,2ef01c;husky,husky,9d8ed0;commitlint,commitlint,b2f3e7;&line2=express,express,bd3ea6;prisma,prisma,09acb9;&line4=jest,jest,de5bd6;supertest,supertest,cb1288;swagger,swagger,172770;)](https://github-readme-tech-stack.vercel.app/api/cards?align=center&titleAlign=center&lineCount=4&theme=github_dark&hideTitle=true&line1=node.js,node.js,ddbfef;typescript,typescript,543e05;&line3=eslint,eslint,3663f5;prettier,prettier,2ef01c;husky,husky,9d8ed0;commitlint,commitlint,b2f3e7;&line2=express,express,bd3ea6;prisma,prisma,09acb9;&line4=jest,jest,de5bd6;supertest,supertest,cb1288;swagger,swagger,172770;)

| Tool | Description |
| --- | --- |
| Node.js | A JavaScript runtime built on Chrome's V8 JavaScript engine that allows for server-side JavaScript execution |
| Express | A popular web framework for Node.js that provides a variety of features for building web applications |
| TypeScript | A superset of JavaScript that adds optional static typing, classes, and other features to the language |
| Prisma | A database toolkit and ORM that allows for type-safe database access and schema management |
| ESLint | A tool for identifying and reporting on patterns found in ECMAScript/JavaScript code |
| Prettier | A tool for automatically formatting code to enforce consistent style |
| Husky | A tool for running scripts in response to Git events, such as commits or pushes |
| ts-node-dev | A development tool for running TypeScript code with automatic restarts and fast compilation times |
| Swagger | A tool for designing, building, and documenting RESTful APIs |
| Commitizen | A tool for making it easier to follow the conventional commit format for Git commits |
| Jest | A JavaScript testing framework with a focus on simplicity and ease of use |
| Supertest | A library for testing Node.js HTTP servers using a fluent API |

## Features

:white_check_mark: Prisma integrated

:white_check_mark: Swagger for api documentation

:white_check_mark: Linting and formatting with eslint and prettier

:white_check_mark: e2e/unit testing with jest and supertest

:white_check_mark: Commit hooks with husky

:white_check_mark: Multiple environment support

:white_check_mark: Advanced logging with winston

:white_check_mark: env validation

:white_check_mark: Preconfigured error handlers

:white_check_mark: Ensures consitent file naming convention

## Required Stack

| Tool       | Required version |
|------------|------------------|
| NodeJS     | >=16             |
| Typescript | >=4\.9\.4        |

## Clone

Clone the project

```bash
  git clone https://github.com/akhil-neoito/expressjs-typescript-prisma-boilerplate.git
```

Go to the project directory

```bash
  cd expressjs-typescript-prisma-boilerplate
```

## Environment setup

Multiple enviroments are supported namely `development`, `test`, `staging`, `production` as defined in `envirornment.enum.ts`

```ts
  Environments {
    PRODUCTION = 'production',
    DEV = 'development',
    TEST = 'test',
    STAGING = 'staging',
  }
```

1.Development Environment: Used during the development of the application

2.Test Environment: Used to test the application before it is deployed to production

3.Staging Environment: Used to simulate the production environment as closely as possible. It is used to test the application in a live-like environment before it is deployed to production.

4.Production Environment: This environment is where the application is deployed and accessed by end-users.

Multiple env files are also supported according to each environment as below

* `.env`: The default environment file used in all environments, unless a specific custom environment file is present. Contains common configuration variables used across all environments.
* `.env.dev`, `.env.test`, `.env.stage`, `.env.prod`: Custom environment files specific to each environment. Used to customize the configuration of the application for each environment.

**Note**: Custom environment files have priority over the default .env file. Configuration variables in a specific custom environment file take precedence over the ones in the default .env file.

## Run Locally

Run
```bash 
  make setup
```
to setup the project or run each steps individually as below

Install dependencies

```bash
  npm i
```

Create env file from .env.example

```bash
  cp .env.example .env
  # Add env values to .env file after this
```

Start app in dev mode

```bash
  npm run dev
```

## Scripts

Following are the list of predefined scripts available in the app

| Script Name     | Description                                   | Command                   |
|-----------------|-----------------------------------------------|---------------------------|
| dev             | Runs app in development mode with ts-node-dev | `npm run dev`             |
| build           | Builds the app with tsc to dist folder        | `npm run build`           |
| start           | Starts the build                              | `npm run start`           |
| prod            | Builds and runs the app in production mode    | `npm run prod`            |
| prisma:generate | Generates prisma client types                 | `npm run prisma:generate` |
| prisma:migrate  | Runs prisma db migration                      | `npm run prisma:migrate`  |
| prisma:seed     | Seeds db                                      | `npm run prisma:seed`     |
| prisma:studio   | Opens prisma studio                           | `npm run prisma:studio`   |
| lint            | Lints the app with eslint                     | `npm run lint`            |
| lint:fix        | Lints and fixes the app with eslint           | `npm run lint:fix`        |
| format          | Formats the app with eslint                   | `npm run format`          |
| commit          | Opens commitizen                              | `npm run commit`          |
| test            | Runs tests                                    | `npm run test`            |
| clean           | Cleans autogenerated folders and files        | `npm run clean`           |

## Folder structure

```
├── dist
├── logs
├── prisma
├── public
├── src
└── tests
```

| Folder     | Description                                  |
|------------|----------------------------------------------|
| dist       | Build folder. Would be auto generated by tsc |
| logs       | Contains log files                           |
| prisma     | Primsa schema, seeds etc.                    |
| public     | Static resources                             |
| src        | Source folder                                |
| tests      | Contains test files                         |

### src

The source directory contains the following folders

```
├── config
├── dto
├── enums
├── lib
├── middlewares
├── modules
├── types
└── utils
```

Folder | Description
------ | -----------
config | Contains configuration files for the whole app and different libraries.
dto | Contains Data Transfer Objects (DTOs) which are used to transfer data between different layers of the app.
enums | Contains TypeScript enum definitions which can be used throughout the app to ensure type safety and consistency.
lib | Contains any external libraries or modules that the app may depend on, as well as any custom utility functions or classes that you have written yourself. This can include things like a custom logger, validation functions, or other commonly used functionality that doesn't fit neatly into any of the other folders.
middlewares | Contains middleware functions which can be used to modify requests and responses as they pass through the app.
modules | Contains the main modules of the app, each of which can contain submodules, controllers, services, and other components.
types | Contains type definitions which can be used throughout the app to ensure type safety and consistency.
utils | Contains utility functions or classes that can be used throughout the app for common tasks, such as string manipulation, date formatting, or math calculations. These functions may not fit neatly into any of the other folders, but are still useful components of the app.

## License

[MIT](https://choosealicense.com/licenses/mit/)

## Badges

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)
