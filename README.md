# Express + Typescript + Prisma boilerplate

This is an opiniated express + typescript boilerplate. Prisma is being used as an ORM to have the flexibility of switching databases with minimal code change.
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

## Clone

Clone the project

```bash
  git clone https://github.com/akhil-neoito/expressjs-typescript-prisma-boilerplate.git
```

Go to the project directory

```bash
  cd expressjs-typescript-prisma-boilerplate
```

## Scripts

Following are the list of predefined scripts available in the app

| Script Name     | Description                                   | Command                 |
|-----------------|-----------------------------------------------|-------------------------|
| dev             | Runs app in development mode with ts-node-dev | npm run dev             |
| build           | Builds the app with tsc to dist folder        | npm run build           |
| start           | Starts the build                              | npm run start           |
| prod            | Builds and runs the app in production mode    | npm run prod            |
| prisma:generate | Generates prisma client types                 | npm run prisma:generate |
| prisma:migrate  | Runs prisma db migration                      | npm run prisma:migrate  |
| prisma:seed     | Seeds db                                      | npm run prisma:seed     |
| prisma:studio   | Opens prisma studio                           | npm run prisma:studio   |
| lint            | Lints the app with eslint                     | npm run lint            |
| lint:fix        | Lints and fixes the app with eslint           | npm run lint:fix        |
| format          | Formats the app with eslint                   | npm run format          |
| commit          | Opens commitizen                              | npm run commit          |
| test            | Runs tests                                    | npm run test            |
| clean           | Cleans autogenerated folders and files        | npm run clean           |

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
| tests      | Containes test files                         |

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

| Folder      | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| ----------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| nodejs      | An open-source, cross-platform JavaScript runtime environment that executes JavaScript code outside of a web browser.                                                                                                                                                                                                                                                                                                                                             |
| express     | A popular and widely used web framework for building server-side applications with Node.js. It provides a lot of utility methods for HTTP requests and responses, routing, middleware, and more.                                                                                                                                                                                                                                                                   |
| typescript  | An open-source language that builds on JavaScript by adding static type definitions. It can help catch errors and bugs at compile time, and provides better tooling and editor support for large codebases.                                                                                                                                                                                                                                                       |
| prisma      | An open-source database toolkit for TypeScript and Node.js. It provides a type-safe and scalable ORM (Object-Relational Mapping) for working with databases, as well as a powerful schema migration system.                                                                                                                                                                                                                                                         |
| eslint      | A pluggable and configurable linter tool for identifying and reporting on patterns in JavaScript code. It can help enforce coding standards and best practices, and catch potential bugs and issues before they become a problem.                                                                                                                                                                                                                                |
| prettier    | An opinionated code formatter that can automatically format code to follow consistent style rules. It can help improve code readability and consistency, and save time by avoiding manual formatting.                                                                                                                                                                                                                                                                |
| husky       | A Git hook manager that can run scripts before or after certain Git events, such as committing code. It can be used to enforce code quality standards and run automated tests before a commit is made.                                                                                                                                                                                                                                                              |
| ts-node-dev | A development tool that can automatically compile and restart TypeScript files as they are changed. It provides a fast and efficient development experience for TypeScript projects, without the need for manually compiling code or restarting the server.                                                                                                                                                                                                            |
| swagger     | An open-source framework for building and documenting APIs. It provides a way to define API endpoints, data models, and documentation in a standardized way, making it easier for developers to understand and work with the API.                                                                                                                                                                                                                                      |
| commitizen  | A command-line tool that helps enforce a consistent commit message format across a team or organization. It can help improve code documentation and readability, and make it easier to track changes over time.                                                                                                                                                                                                                                                     |
| jest        | A popular and widely used testing framework for JavaScript and TypeScript code. It provides a way to write and run automated tests, and includes features like test runners, assertions, and mocking.                                                                                                                                                                                                                                                               |
| supertest   | A testing library that can be used to test HTTP servers and API endpoints. It provides an easy-to-use API for making HTTP requests and asserting the responses, making it a popular choice for testing Node.js web applications.                                                                                                                                                                                                                                      |
|

## License

[MIT](https://choosealicense.com/licenses/mit/)

## Badges

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)
