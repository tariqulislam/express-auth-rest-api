
# express-auth-api-example
THis framework and boilerplat, which contains the different features, those are helps the developer to start web api development easily. Developer can easily code, test, documented the api during the development process. It also have good architecture, which helps the developer to maintain the code.

## Installation

Installation process is easy, you can only download or clone application from git

1. clone from git `git clone https://github.com/tariqulislam/express-auth-rest-api.git`
2. then go to express-starter-kit by `cd express-starter-kit`
3. Install Yarn package `npm install -g yarn`
4. run command `yarn install`
5. configure the `database` from `config/config.json` directory
```javascript
{
  "development": {
    "username": "<username>",
    "password": "<password>",
    "database": "interview",
    "host": "127.0.0.1",
    "dialect": "mysql"
  },
  "test": {
    "username": "<username>",
    "password": "<password>",
    "database": "interview",
    "host": "127.0.0.1",
    "dialect": "mysql"
  },
  "production": {
    "username": "<username>",
    "password": "<password>",
    "database": "interview",
    "host": "127.0.0.1",
    "dialect": "mysql"
  }
}

```
6. create the database at mysql
    for command line:
        `> mysql -u <user> -p <password>`
        `> create database interview`
        `> exit()`
    You can also create database from phpmyadmin

7. Migrate the Database with `node_modules/.bin/sequelize db:migrate`
8. run the command `yarn nodemon`
9. To browse the site use `http://localhost:3000`
10. To brows the swagger api documentation `http://localhost:3000/api-docs

## Project Structure
```
--------------------
|--| bin
|----| www (express generate application runner)
|--| config
|----| config.js (Database configuration file for sequelize)
|----| swaggerconfig.js (Swagger configuration file for project(customized))
|--| core (Custom function and helper function folder)
|--| middleware(express router middleware to protect the server from unwanted client request)
|--| migrations(sequelize created migration folder and it contains the database and model mapping files)
|----| 202020202-created-admin.js (migration file)
|--| model (sequelize created model folder and customer model folder also)
|--| route (express routes or api endpoint folder)
|----| admins.js (routes end point file)
|--| seeders (sequelize created seed folder for database)
|--| services (customer folder which contains all the business logic for application)
|----| admin (module wise service)
|------| AdminService.js (service file)
|--| test (Mocha, chai and chai http testing folder, api testing and test automation folder)
|--| public (Assets folder fro project)
|--| views (client side view folder contains ejs view engine file)
|--| .env (dotenv configuration file to control node environment)
|--| .editorconfig (fixing the code style in different editor)
|--| .eslintrc (eslint for javascript standard)
|--| .gitignore (git ignore definition file)
|--| app.js (main file for express js to run application)
|--| ecosystem.config.js (pm2 server configuration file)
|--| package.json (node js package configuration file)
```

## developer must have knowledge about

1. Node.js
2. express.js
3. Mocha & chai
4. sequelize-cli
5. sequelize
6. Swagger
7. Swagger UI
8. JWT(JSON web token)
9. Nodemon
10. ES6 and ES5
11. Express Router
12. Dotenv
13. Bcrypt
14. pm2
15. dotenv

## Usage and instructions

1. Hot reload the development environment with Nodemon plugins.


    No need to restart node project every time when it is at development stage.

    The project has Nodemon server to auto lookup the changes at working directory of project.



**For PM2 Installation**
This project also provide you command which will help developer to install the pm2 and deploy the site to hosting server

  For Install the pm2 to hosting server (`yarn` or `npm` command)
  ```
     yarn pm2:install
     npm run pm2:install
  ```
  For Production and developer deployment
  ```
    yarn pm2:prod
    yarn pm2:dev
    
    npm run pm2:prod
    npm run pm2:dev
  ```
  
  For monitor the process 
  ```
    yarn pm2:monitor
    npm run pm2:monitor
  ```
  
  For reload and stop and kill the pm2 process
  ```
    yarn pm2:reload
    yarn pm2:stop
    yarn pm2:kill
    
    npm run pm2:reload
    npm run pm2:stop
    npm run pm2:kill
  ```