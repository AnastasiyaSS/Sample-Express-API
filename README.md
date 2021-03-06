# SkillCrucial React Redux boilerplate

## Quick start

1. Clone this repo using:
  ```shell
  $ git clone git@github.com:ovasylenko/skillcrucial-react-redux-boilerplate.git
  ```

2. To install dependencies and clean the git repo run:

  ```shell
  $ yarn install
  ```

  *We recommend using `yarn` for installing packages, but you can use `npm` instead*:

  ```shell
  $ npm install
  ```
3. Create first build

  ```shell
  $ yarn run build:prod
  ```
4. Copy .env.example file to .env and make the necessary changes there

5. Run project in Dev mode

  ```shell
  $ yarn run dev
  ```

## Project Structure

#### `server/server.js`

In this file I worte a code, which works with API. Using this app in postman you can:
1. GET the list of users.
2. Create a new user with POST method.
3. Fix data with PATCH method.
4. DELETE the user you don't need anymore.
5. DELETE the entire file from the boilerplate.

Learned how to work with Node.js, Express, practiced with Postman. Diven into understanding API methods.

Issues I faced during working on this project:
1. How to build the structure of the code. For example such functions as saveFile and readWrite. These functions could be written as one, but I decided that this way is more convinient for me.
2. Had some difficulties with async/await.

#### `client/`

You will write your app in this folder. You will spend most of your time in here.

#### `client/components`

This folder contains all your components

#### `dist/assets`
This directory contains compiled project files

#### `webpack.development.config.js` `and webpack.production.frontend.config.js`
Project environment configs. Webpack uses proper config depending on defined application environment.
By default `webpack.development.config.js` is used unless you build the application with --config webpack.production.frontend.config.js variable.


## Command Line Commands

#### Installation

```Shell
yarn install
```
Installs the dependencies.

#### Development

```Shell
yarn run dev
```

Starts the development server running on `http://localhost:8080` using the webpack.development.config.js with Hot Module Replacement (HMR) (Changes in the application code will be hot-reloaded)

```Shell
yarn run dev:server
```

Starts the development server and makes your application accessible at http://localhost:8080.

```Shell
yarn run clean
```
Removes a directory "dist" from a project

#### Building

```Shell
yarn build:prod
```

Prepares your app for deployment to production environment (using the webpack.production.frontend.config.js) (does not run tests). Optimizes and minifies all files, piping them to the `dist` folder.


#### Testing

```Shell
yarn run test
```

Tests your application modern JavaScript Testing Framework - Jest with the unit tests specified in the `**/__tests__/*.spec.js` files
throughout the application.

```Shell
yarn run test:watch
```

Watches changes to your application and re-runs tests whenever a file changes.

```Shell
yarn run coverage
```

Generates test coverage.


It???s also possible to leave out the run in this command, each script can be executed with its name, e.g:
yarn test:watch
yarn test:coverage

#### Linting

```Shell
yarn run lint
```
Will analyse your code for potential errors. Will check both: `./client/**/**.js` and `./server/**/**.js` files.
Code linting is a type of static analysis that is frequently used to find problematic patterns or code that doesn???t adhere to certain style guidelines.


```Shell
yarn run lint:server
```

Will analyse only  `server/**/**.js` files