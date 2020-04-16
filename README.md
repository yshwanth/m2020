# Major20 Backend
Start a API quickly using Node, Express & Postgres database

**Dependencies**

We use **express** to serve the API, **body-parser** to parse responses, **postgres** for the database, **knex** as the query engine, **dotenv** to protect environment variables, **helmut** to add proper headers, **cors** to prevent/allow XSS, **morgan** as our logger, and **nodemon** as a dev dependency to watch for changes.

All dependencies are included in the cloned project.

## Instructions

**1. Clone the repo**

```
git clone 
```

**2. CD into the project**

```
cd into directory
```

**3. Install dependencies**

```
npm install
```

**4. Start Postgres**

```
brew services start postgresql
```

**Note:** You can use Postgres or MYSQL. We are using Postgres. If you would like to use MYSQL instead of Postgres you will need to `npm uninstall pg` and `npm install mysql`. Then edit the above command to start MYSQL started on your computer.

**5. Create a database**

Change the database name to whatever you would like to name the database. Be sure to also change the database name in server.js to whatever you name the database.

```
createdb crud-starter-api
```

**6. Create a database table**

Open pSequel and run the following command. Change the table name to whatever you would like to name the table.

```
CREATE TABLE testtable1 (
 id serial PRIMARY KEY,
 first_name VARCHAR(100),
 last_name VARCHAR(100),
 email text UNIQUE NOT NULL,
 phone VARCHAR(100),
 city VARCHAR(100),
 company_name VARCHAR(100),
 added TIMESTAMP NOT NULL
);
```


An important piece that is missing from this API is an authentication API. In that case it is recommended to install bCrypt for password hashing and authentication. Then, more routes should be created for registering, logging in and logging out users. There should also be a scheme for keeping users logged in. The suggested method for persisting logins would be to use JWT for token creation, Redis to store tokens in server memory, and localStorage to save tokens on the frontend. The tokens stored in localStorage will be sent back to the API via authorization headers for protected requests and would need to be verified by the server.

# m2020
