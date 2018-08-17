FlashFluent - learning App
============================

This API provides resources for [FlashFluent](https://flashfluent.surge.sh) app which documentation can be found [here](https://github.com/valsakel/spaced-repetition-client).

Live [URL](https://spaced-rep-marjef-server.herokuapp.com/)

## API Documentation
#### `GET /questions/next` - protected
 
Returns value of *propmt* field from document in 'users' collection for a user 
whose *id* obtained from JWT.

Example response:
 
```javascript
  "https://cdn5.kakao.im/wp-content/uploads/2018/07/2-134.jpg"
```

#### `POST /questions/answer` - protected
 
Returns values of *answer*, *correct*, *score*, and *total* fields from document in 
*users* collection for a user whose *id* obtained from JWT.
 
Example response:

```javascript
  {
    answer: "Taj Mahal",
    correct: false,
    score: 1,
    total: 3
  }
```

#### `POST /users/register` - unprotected

Creates a new document in *users* collection

Data parameters:

```javascript
 {
    firstname: "User",
    lastname: "Name",
    username: "username",  
    password: "password"
 } 
```

Example response:

```javascript
 {
    firstname: "User",
    lastname: "Name",
    username: "username",  
    password: "password"
    id: "5b753258a35dac0014b3ef94"
 }
```

 ## Tech Stack
 
 [Node.js](https://nodejs.org/en/)
 
 [Express.js](https://expressjs.com/)
 
 [MongoDB](https://www.mongodb.com/)
 
 [Mongoose](https://mongoosejs.com/)
 
 [Passport](http://www.passportjs.org/)
 
 [passport-jwt](https://www.npmjs.com/package/passport-jwt)
 
 [passport-local](https://www.npmjs.com/package/passport-local)
 
 [bcrypt.js](https://github.com/dcodeIO/bcrypt.js/blob/master/README.md)
 
 [JWT](https://jwt.io/)
 
 [dotenv](https://www.npmjs.com/package/dotenv)
