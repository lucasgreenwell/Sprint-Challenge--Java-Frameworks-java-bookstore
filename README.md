# Java Frameworks Sprint Challenge

**Read these instructions carefully. Understand exactly what is expected _before_ starting this Sprint Challenge.**

This challenge allows you to practice the concepts and techniques learned over the past sprint and apply them in a concrete project. This sprint explored **using Frameworks in Java**. During this sprint, you studied **SQL, Spring Data, JPA, and Hibernate**. In your challenge this week, you will demonstrate your mastery of these skills by creating **a Java Spring REST API Application**.

This is an individual assessment. All work must be your own. Your challenge score is a measure of your ability to work independently using the material covered through this sprint. You need to demonstrate proficiency in the concepts and objectives introduced and practiced in preceding days.

You are not allowed to collaborate during the sprint challenge. However, you are encouraged to follow the twenty-minute rule and seek support from your TL if you need direction.

_You have **three hours** to complete this challenge. Plan your time accordingly._

## Introduction

This is a basic bookstore database scheme with books which have authors. The book can be found in a section of the store.

Your final results should look like (not counting user authentication related endpoints, just the bookstore endpoints) You can also use the data below to help test your endpoints:

### MVP

<details>
<summary>GET /books/books - returns a JSON object list of all the books, their section, and their authors.</summary>

```JSON
```

</details>

<details>
<summary>GET /authors/authors - returns a JSON object list of all the authors, their books, and the book's section.</summary>

```JSON
```

</details>

<details>
<summary>POST /books/book - add a new book.</summary>

DATA

```JSON
```

OUTPUT

```TEXT
```

</details>

<details>
<summary>PUT /books/book/{bookid} - replace the book, associated section, and associated authors with the given information</summary>

DATA

```JSON
```

OUTPUT

```TEXT
```

</details>

<details>
<summary>DELETE /data/books/{id} - deletes a book and the book author combinations - but does not delete the author records.</summary>

OUTPUT

```TEXT
```

</details>

### Commits

Commit your code regularly and meaningfully. This helps both you (in case you ever need to return to old code for any number of reasons) and your team lead as the evaluate your solution.

Be prepared to demonstrate your understanding of this week's concepts by answering questions on the following topics. You might prepare by writing down your own answers before hand.

1. Can you explain exception handling in your application?
2. Can you explain your user authentication flow?
3. Can you show me your unit tests and describe how they work?
4. Can you show how you deployed your application to a cloud service with a persistent database?

## Instructions

### Task 1: Project Set Up

- [ ] Create a forked copy of this project
- [ ] Add your team lead as collaborator on Github
- [ ] Clone your OWN version of the repository (Not Lambda's by mistake!)
- [ ] Create a new branch: git checkout -b `<firstName-lastName>`.
- [ ] Create a new Java Spring Application using IntelliJ.
- [ ] Push commits: `git push origin <firstName-lastName>`
- [ ] Implement the project on your newly created `<firstName-lastName>` branch, committing changes regularly
- [ ] Push commits: git push origin `<firstName-lastName>`

### Task 2: Project Requirements

- [ ] You will be creating a REST api service to store and read data from a database. You should be able to switch between an H2 database and a PostgreSQL database by using an application.properties setting.

- [ ] Please fork and clone this repository. This repository does have a starter project. The provided initial application has the basics in place for

- Auditing fields
- Exception Handling
- User Oauth2 Authentication
  - Endpoints to handle (know how these work)
    - Creating a new user
    - Updating a user
    - Deleting a user
    - Authenticated user logging out
    - plus many more!
- Swagger
- Unit / Integration testing (at least the POM file entries)
- Deployment to Heroku
- Conversion to Postgresql

- [ ] Create the models, repositories, and services needed to model the following suggested table layout:

- Note these are the minimum fields required. More is okay.

- [ ] section
  - `sectionid` - long primary key
  - `sectionname` - String the name of section. Cannot be null. Must be unique
  
- [ ] book
  - `bookid` - long primary key
  - `booktitle` - String the title of the book. Cannot be null.
  - `ISBN` - String the ISBN number of the book. Cannot be null. Must be unique
  - `copy` - Int the year the book was published (copyright date)
  
- [ ] authors
  - `authorid` - long primary key
  - `lastname` - String last name of the author
  - `firstname` - String first name of the author

- [ ] There is a many to many relationship between authors and books. A book may have many authors while an author may write many books.

- [ ] The is a one to many relationship between sections and books. One section can hold many books while a book can only be in one section.

- [ ] add the standard four auditing fields to all tables
- [ ] The SeedData.java class contains sample data to test your application
- [ ] Appropriate Exception handling should be in place for each bookstore endpoint
- [ ] Expose the following endpoints
  - [ ] List the data
    - [ ] GET /books/books - returns a JSON object list of all the books, their section, and their authors.
    - [ ] GET /authors/authors - returns a JSON object list of all the authors, their books, and the book's section.

  - [ ] Manage the data
    - [ ] POST /books/book - add a new book.
    - [ ] PUT /books/book/{bookid} - replace the book, associated section, and associated authors with the given information
    - [ ] DELETE /data/books/{id} - deletes a book and the book author combinations - but does not delete the author records.

- [ ] Your system will have authentication in place. The following are the roles you need to handle:
  - [ ] User - people who can look up books, authors, sections
  - [ ] Data - people who can update data on books, authors, sections. The can also read books, authors, sections.
  - [ ] ADMIN - people who can update data on users and otherwise have full access to the system.

- [ ] Required Unit Testing
  - [ ] Write at least 2 unit tests for the book service
  - [ ] Write at least 2 unit tests for the book controller

- [ ] Deploy the system to Heroku using PostgreSQL

### Task 3: Stretch Goals

- [ ] Unit Testing
  - [ ] Write tests to achieve 100% line coverage in book service
  - [ ] Write tests to achieve 100% line coverage in book controller

- [ ] Expose the following endpoint
  - [ ] POST /data/books/{bookid}/authors/{authorid} - assigns a book already in the system (bookid) to an author already in the system (authorid) (see how roles are handled for users)

### Required best practices

- [ ] Consistent naming. Examples: variables, functions, Components, and file/folder organization.
- [ ] Consistent spacing. Examples: line breaks, around arguments and before/after functions.
- [ ] Consistent quotation usage.
- [ ] Spell-check.
- [ ] Schedule time to review, refine and reassess your work.

It is better to submit a challenge that meets [MVP](https://en.wikipedia.org/wiki/Minimum_viable_product) than one that attempts too much and fails.

### Tips and Gotchas

In your solution, it is essential that you follow best practices and produce clean and professional results. You will be scored on your adherence to proper code style and good organization. Schedule time to review, refine, and assess your work and perform basic professional polishing including spell-checking and grammar-checking on your work. It is better to submit a challenge that meets MVP than one that attempts too much and does not.
