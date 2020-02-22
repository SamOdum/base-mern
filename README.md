<h1 align="center">
BASE-MERN
</h1>
<p align="center">A robust but light starter/boilerplate for mern development</p>
<p align="center">
MongoDB, Expressjs, React/Redux, Nodejs
</p>

> MERN is the utilisation of JavaScript in handling the different aspects of a fullstack app.

MERN stack is an implementation of MongoDB, Expressjs, React, Nodejs.

## clone or download

```terminal
$ git clone https://github.com/samodum/base-mern.git
$ npm i
```

## project structure

```terminal
LICENSE
package.json
server/
   package.json
   .env (to create .env, check [prepare your secret session])
client/
   package.json
...
```

# Local usage

## Prerequirements

You will need to have the following installed to able to run this project locally.

- [MongoDB](https://gist.github.com/nrollr/9f523ae17ecdbb50311980503409aeb3)
- [Node](https://nodejs.org/en/download/) ^10.0.0
- [npm](https://nodejs.org/en/download/package-manager/)

## Client-side usage(PORT: 3000)

Here is how to initialize and run the client side

```terminal
$ cd client   // go to client folder
$ npm i       // npm install pacakges
$ npm run dev // run it locally

// deployment for client app
$ npm run build
$ npm run start
```

## Server-side usage(PORT: 8000)

Here is how to initialize and run the server side

### Prepare your secret

Because you need to add a JWT_SECRET in .env to connect to MongoDB, first run the following script

```terminal
// in the root level
$ echo "JWT_SECRET=YOUR_JWT_SECRET" >> ./server/src/.env
```

Then get into the server folder and take the following steps

```terminal
$ cd server   // go to server folder
$ npm i       // npm install pacakges
$ npm run dev // run it locally
$ npm run build // this will build the server code to es5 js codes and generate a dist file
```

## Deploy Server to [Heroku](https://dashboard.heroku.com/)

```terminal
$ npm i -g heroku
$ heroku login
...
$ heroku create
$ npm run heroku:add <what-youd-like-to-name-your-heroku-app>

// remember to run this command in the root level, not the server level, so if you follow the documentation along, you may need to do `cd ..`
$ pwd
/Users/<your-name>/mern
$ npm run deploy:heroku
```

### After creating heroku

remember to update the file of [client/webpack.prod.js](https://github.com/samodum/base-mern/blob/master/client/webpack.prod.js)

```javascript
 'API_URI': JSON.stringify('https://what-youd-like-to-name-your-heroku-app.herokuapp.com')
```

# Dependencies(tech-stacks)

| Client-side              | Server-side               |
| ------------------------ | ------------------------- |
| axios: ^0.19.2           | bcryptjs: ^2.4.3          |
| react: ^16.12.0          | cors: ^2.8.5              |
| react-dom: ^16.12.0      | cross-env: ^7.0.0         |
| react-redux: ^7.2.0      | dotenv: ^2.0.0            |
| react-router: ^5.1.2     | express: ^4.17.1          |
| react-router-dom: ^5.1.2 | express-validator: ^6.4.0 |
| redux: ^4.0.5            | jsonwebtoken: ^8.5.1      |
| redux-thunk: ^2.3.0      | mongoose: ^5.9.1          |
| webpack: ^4.41.6         | morgan: ^1.9.1            |
| @babel/core: ^7.8.4      | babel-core: ^6.26.3       |

## Standard

[![JavaScript Style Guide](https://cdn.rawgit.com/standard/standard/master/badge.svg)](https://github.com/standard/standard)

## BUGs or comments

[Create new Issues](https://github.com/samodum/base-mern/issues)
