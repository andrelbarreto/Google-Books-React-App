# Google Books Search

### Overview

In this activity, we created a new React-based Google Books Search app. This assignment required creation of React components, work with helper/util functions, and utilize React lifecycle methods to query and display books based on user searches. It also uses Node, Express and MongoDB so that users can save books to review or purchase later.

### User Story

As an user I am looking for books that interest me. I would like to search for Books using Google and to be able to save them for future purchase. 

## Installation

RUN: NPM START
--starts the server and the react app concurrently.

NPM Used

Server

"axios": "^0.19.2",
    "concurrently": "^5.1.0",
    "cors": "^2.8.5",
    "dotenv": "^8.2.0",
    "express": "^4.17.1",
    "if-env": "^1.0.4",
    "mongoose": "^5.9.5"

    React App

    "react": "^16.13.0",
    "react-dom": "^16.13.0",
    "react-scripts": "3.4.0",
    "react-router-dom": "^5.0.1"


## Usage

```Javascript/React/Node.JS

    "start": "if-env NODE_ENV=production && npm run start:prod || npm run start:dev",
    "start:prod": "node server.js",
    "start:dev": "concurrently -k \"nodemon --ignore 'client/*'\" \"npm run client\"",
    "client": "cd client && npm run start",
    "install": "cd client && npm install",
    "build": "cd client && npm run build"

Deployed - https://google-books-nu.herokuapp.com/
Github - https://github.com/andrelbarreto/Book_search


### Instructions


. Using mongoose, then create a Book schema.

. At a minimum, books should have each of the following fields:

* `title` - Title of the book from the Google Books API

* `authors` - The books's author(s) as returned from the Google Books API

* `description` - The book's description as returned from the Google Books API

* `image` - The Book's thumbnail image as returned from the Google Books API

* `link` - The Book's information link as returned from the Google Books API

* Creating `documents` in your `books` collection similar to the following:

    ```js
    {
      authors: ["Suzanne Collins"]
      description: "Set in a dark vision of the near future, a terrifying reality TV show is taking place. Twelve boys and twelve girls are forced to appear in a live event called The Hunger Games. There is only one rule: kill or be killed. When sixteen-year-old Katniss Everdeen steps forward to take her younger sister's place in the games, she sees it as a death sentence. But Katniss has been close to death before. For her, survival is second nature."
      image: "http://books.google.com/books/content?id=sazytgAACAAJ&printsec=frontcover&img=1&zoom=1&source=gbs_api"
      link: "http://books.google.com/books?id=sazytgAACAAJ&dq=title:The+Hunger+Games&hl=&source=gbs_api"
      title: "The Hunger Games"
    }
    ```

. Created a layout similar to the mockups required. This should be a SPA (Single Page Application) that uses [`react-router-dom`](https://github.com/reactjs/react-router) to navigate, hide and show your React components without changing the route within Express.

* The layout includes at least two React Components for each page `Search` and `Saved`.


It uses the following Express routes for app:

* `/api/books` (get) - Should return all saved books as JSON.

* `/api/books` (post) - Will be used to save a new book to the database.

* `/api/books/:id` (delete) - Will be used to delete a book from the database by Mongo `_id`.

* `*` (get) - Will load your single HTML page in `client/build/index.html`. Make sure you have this _after_ all other routes are defined.

* App was sucessfuly deployed to Heroku

- - -


### Reminder: Submission on BCS

* **This assignment must be deployed.** * Please submit both the deployed Heroku link to your homework AND the link to the Github Repository!
Deployed - https://google-books-nu.herokuapp.com/
Github - https://github.com/andrelbarreto/Book_search

- - -

### Add To Your Portfolio

It is linked to my new portfolio.

- - -

### Hosting on Heroku
Despite all the complications that it presents, this app was deployed and works properly.
- - -

Final Assignment for Northwestern University Coding Bootcamp is done !
