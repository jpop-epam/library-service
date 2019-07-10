## Library-Service
Library Service REST API

## Author
Arnab Mondal

### This Rest API supports the following endpoints

|   Endpoint      | HTTP Method | Description                          |  Access |                   Comments                     |
|-----------------|-------------|--------------------------------------|---------|------------------------------------------------|
|/lib                 | GET     | Login                    | GENERAL | Calls user service **GET /users/{user_id}**        |
|/lib/books           | GET     | List of all books                       | GENERAL | Calls book service **GET /books URL**             |
|/lib/books/{book_id} | GET     | Get a book's details | GENERAL | Calls book service **GET /books/{book_id} URL**    |
|/lib/books/{book_id} | POST    | Add a new book                        | ADMIN  | Calls book service **POST /books/{book_id} URL**   |
|/lib/books/{book_id}	| DELETE  | Delete a book                        | ADMIN   | Delete book association with user in library table and calls book service **DELETE /books/{book_id} URL** |
|/lib/users/{book_id} | GET     | List of all users | GENERAL | Calls user service **GET /users URL**  |
|/lib/users/{user_id} | GET     | View user profile with all issued books    | GENERAL | Calls user service **GET /users/{user_id}**, fetches book ids on user_id  from library table and calls **GET /books/{book_id}** for all books. Displays consolidated data |
|/lib/users/{user_id} | POST    | Add a user                       | GENERAL | User Registration, calls user service **POST /users/{user_id}** |
|/lib/users/{user_id} | DELETE  | Release all books for that user_id in library table and delete user.                           | ADMIN   |        Calls **DELETE users/{user_id}**                                       |
|/lib/users/{user_id} | PUT     | Update user's account details | GENERAL |       Calls **PUT users/{user_id}** |
|/lib/users/{user_id}/books/{book_id} | PUT | Issue a book to a user  | GENERAL | Updates library table with book-user association. 


### Reference Documentation
For further reference, please consider the following sections:

* [Official Gradle documentation](https://docs.gradle.org)

### Guides
The following guides illustrate how to use some features concretely:

* [Building a RESTful Web Service](https://spring.io/guides/gs/rest-service/)
* [Serving Web Content with Spring MVC](https://spring.io/guides/gs/serving-web-content/)
* [Building REST services with Spring](https://spring.io/guides/tutorials/bookmarks/)
* [Building a Hypermedia-Driven RESTful Web Service](https://spring.io/guides/gs/rest-hateoas/)
* [Building a RESTful Web Service with Spring Boot Actuator](https://spring.io/guides/gs/actuator-service/)
* [Accessing data with MySQL](https://spring.io/guides/gs/accessing-data-mysql/)

### Additional Links
These additional references should also help you:

* [Gradle Build Scans – insights for your project's build](https://scans.gradle.com#gradle)|                                 |
