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

Here is how to initialize and run the client aspect

```terminal
$ cd client   // go to client folder
$ npm i       // npm install pacakges
$ npm run dev // run it locally

// deployment for client app
$ npm run build
$ npm run start
```

## Server-side usage(PORT: 8000)

Here is how to initialize and run the server aspect

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

| Client-side                   | Server-side           |
| ----------------------------- | --------------------- |
| axios: ^0.15.3                | bcrypt-nodejs: ^0.0.3 |
| babel-preset-stage-1: ^6.1.18 | morgan: ^1.7.0        |
| lodash: ^3.10.1               | cors: ^2.8.1          |
| react: ^16.2.0                | dotenv: ^2.0.0        |
| react-dom: ^16.2.0            | express: ^4.14.0      |
| react-redux: ^4.0.0           | jwt-simple: ^0.5.1    |
| react-router-dom: ^4.2.2      | mongoose: ^4.7.4      |
| redux: ^3.7.2                 |
| redux-thunk: ^2.1.0           |

## Standard

[![JavaScript Style Guide](https://cdn.rawgit.com/standard/standard/master/badge.svg)](https://github.com/standard/standard)

## BUGs or comments

[Create new Issues](https://github.com/samodum/base-mern/issues)
