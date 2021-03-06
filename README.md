# GraphQLProject

This is a small project made for understanding the basics of GraphQL.

This project contains a small web client from which a user can type a graphQL query that is sent through http to a dotnet server. This server send the necessary front-end files to the browser and catch graphQL queries, execute them and send back the requested json object to the client. Then the vuejs framework updates automatically the result section of the webpage with the json object.

## Instalation

1) Create a dotnet solution
```bash
mkdir GraphQLProject
cd GraphQLProject
dotnet new sln
```

2) Create a console app
```bash
dotnet new console -o App
cd App
```

3) Add the GraphQL library to the project
```bash
dotnet add package GraphQL
```

4) Add / Replace files / folders by those in this repository

At the end you should have this tree:
```bash
│   App.csproj
│   Program.cs
│
├───bin
│   │
│
├───obj
│   │   
│
└───webpage
        index.html
        script.js
        style.css
```

## Usage
1) Start the Server
```bash
dotnet run
```

2) Start an instance of your favourite browser and type this URL: http://localhost:8080/

By default the client query everything.

You can change the query to get less data.

For example:
```bash
{movies{title,year,director}}
```

## Project status

For now only GraphQL queries without any argment can be done.

## TODO

- [ ] Add arguments to GraphQL queries
- [ ] Add mutation to graphQL schema
- [ ] Move the Schema in a separate file
- [ ] Move the json data to an external file
