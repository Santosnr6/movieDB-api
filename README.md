# Movie DB API

## Introduction
Local Movie API with just 20 movies, on which you can exercise asynchronous GET, POST, PUT and DELETE calls. The API also has functionality that allows a user to register an account, and use that account to login.

## Instructions

### Installation
Clone this repository and put the **backend**-folder to your project folder (or any other folder). Open a terminal inside the **backend**-folder and run the following command:
```
npm i
```
This you only have to do once. Next, in order to get your backend server 'up and running' you type in the following command:
```
npm start
```
This command you will have to perform each time you want to start your server. Also, in order to 'restart' your backend server, you have to exit the server and run the **npm start**-command again. This will clear all previous changes to the API.

### Documentation

#### Get key
This call will fetch an API-key, which i needed to access the data from the API.
```
GET http://localhost:8080/api/keys
```

#### Get movies
This call will fetch all movies from the API
```
http://localhost:8080/api/movies?key=<API-key>
```

#### Add new movie
In order to add a new movie you will need to send the new movie in the body of your API-call. The new movie must me an object containing the properties **title**, **poster** and **trailer_link**
```
POST http://localhost:8080/api/movies?key=<API-nyckel>
```


#### Toggle favorite movie
In order to toggle a movies favorite-property you need to perform the following API-call where you send the imdbid of the movie as a parameter in the url.
```
PUT http://localhost:8080/api/movies/<imdbid>?key=<API-nyckel>
```

#### Delete a movie
In order to delete a movie you need to perform the following API-call where you send the imdbid of the movie as a parameter in the url.
```
DELETE http://localhost:8080/api/movies/<imdbid>?key=<API-nyckel>
```

#### Log in
In order to log in you need to send the user as an object containing the keys **username** and **password**.
```
POST http://localhost:8080/api/auth/login
```

#### Log out
In order to log out you just have to perform the following POST-call. No data needs to be sent.
```
POST http://localhost:8080/api/auth/logout
```

#### Register user
In order to register you need to send the user as an object containing the keys **username**(only letters and numbers and minimum 5 characters) and **password**(only letters and numbers and minimum 8 characters).
```
POST http://localhost:8080/api/auth/register
```

### Example data
Example data to use when adding a new movie [you can find here](https://santosnr6.github.io/Data/movies.json)
