# auth-api

## Author: Neveen Beiram

[Tests](https://github.com/NeveenBeiram/auth-api/actions)

[Heroku Deployment](https://neveen-auth-api.herokuapp.com/)

[Pull Request](https://github.com/NeveenBeiram/auth-api/pulls)

#### Setup

* Clone the repo

* npm init -y.

* npm install.

* Create .env file with PORT=3030.

#### Test

`npm test`

![test](lab8test.PNG)

#### Run the app

`npm start`

<hr>

#### End points

- /signup: POST Method

You can Sign-up by sending post request using postman.
You can signup as:

* user
* writer
* editor
* admin

Example:

```
username: nev
password: 1234
role: editor
```

Example of the data when you sign up :

```
{
    "user": {
        "_id": "60aca5b2b68af15a92b9d924",
        "username": "nev",
        "password": "$2b$12$vd3lLt7kMR9fJk8h3l9BHeB1bbfqhDFSe8ApNtAzYDWzWYFcl9k1W",
        "role":"editor"
        "__v": 0
    },
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6ImIiLCJpYXQiOjE2MjIwNjQ4NjZ9.3EsXeCvUJUjIurs4E5jf-YoIVplarFEKDdtwk7IMrj8"
}
```

- /signin: POST Method

* You can signin by sending post request using postman.


- /users: GET Method

* You can access the /users route and get all the usernames available in the DB by siging in and sending a get request with bearer auth and pass the token after you signin.


- /secret: GET Method


* You can access the /secret route by sending a get request with bearer auth and pass the token after you signin.
You will see the following message when you access the secret route:

`Secret route welcomes you`


- api/v1/clothes
 
 you can:
* add clothes by sending post request using postman.

*  get the data for all the clothes by sending get request.

* get the data for specific clothes using its ID by sending get request http://localhost:3030/api/v1/clothes/1518

* update the data for specific clothes using its ID by sending put request http://localhost:3030/api/v1/clothes/1518

*  delete the data for specific clothes using its ID by sending delete request http://localhost:3030/api/v1/clothes/1518

Authenticated Route
If you signed up as:

user : you can read the data only
writer: you can read and post
editor: you can read , post, update
admin: you can read , post, update and delete

- api/v2/food

You can add food by sending post request using postman.

You can get the data for all the food by sending get request.

You can get the data for specific food using its ID by sending get request http://localhost:3030/api/v2/food/1615

You can update the data for specific food using its ID by sending put request http://localhost:3030/api/v2/food/1615

You can delete the data for specific food using its ID by sending delete request http://localhost:3030/api/v2/food/1615

api/v2/food

You can add food by sending post request using postman.

You can get the data for all the food by sending get request.

You can get the data for specific food using its ID by sending get request http://localhost:3030/api/v2/food/1615

You can update the data for specific food using its ID by sending put request http://localhost:3030/api/v2/food/1615

You can delete the data for specific food using its ID by sending delete request http://localhost:3030/api/v2/food/1615

<hr>

#### UML:

![uml](./uml.png)