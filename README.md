# acm
URL-SHORTNER


Description:
This project is a URL shortener application where users can enter a long URL, optionally add a note, and generate a shortened URL. 
The application also provides search functionality to retrieve URLs based on a search query. The shortened URLs are stored in a MongoDB database using the Mongoose ODM.

How to run the project: 
1.if you want to run project locally on computer , change the code in server.js file

mongoose.connect('mongodb+srv://lalit9171:lalit9025@cluster0.enuowoj.mongodb.net/?retryWrites=true&w=majority'

Change the url in above code.
And type code “npm run devStart”  in terminal. 
Install 
 "dependencies": {
    "ejs": "^3.1.9",
    "express": "^4.18.2",
    "mongodb": "^5.6.0",
    "mongoose": "^7.3.0",
    "shortid": "^2.2.16"
  },
  "devDependencies": {
    "nodemon": "^2.0.22"
  }


2.if you want to host the website please setup a database on mondodb atlas.

Connect it to server,js by changing the url.
I hosted my website on rendre application  : https://url-shortner-cls3.onrender.com/
Reference for hosting :https://www.youtube.com/watch?v=AjaGmTVBIfI&t=406s

For database setup : https://www.youtube.com/watch?v=68Jd7GXZPe8

The internal working of your project : 

server.js:

This file is the main entry point of the server-side code.
It includes necessary dependencies such as Express, Mongoose, and the ShortUrl model.
The server connects to the MongoDB database using the provided connection string.
It configures the view engine as EJS and sets up the necessary middleware.
The server defines routes for handling URL search, URL shrinking, and URL redirection.
It listens for incoming HTTP requests on the specified port.

index.ejs:

This file represents the view template for rendering the homepage.
It includes HTML markup along with embedded JavaScript code using EJS syntax.
The template consists of three main sections: search form, shrink form, and URL table.
The search form allows users to search for URLs based on a search query.
The shrink form allows users to enter a URL and an optional note to create a shortened URL.
The URL table displays a list of existing URLs with their full URL, short URL, note, and click count.


shortUrl.js:

This file defines the ShortUrl model using Mongoose.
The model represents a document in the MongoDB collection for storing shortened URLs.
It specifies the schema for the document, including fields like full (full URL), short (short URL), note, and clicks (click count).
The model also defines a pre-save hook to automatically generate a unique short URL before saving the document.

Resources:
For website hosting :https://render.com/
From youtube :https://www.youtube.com/watch?v=AjaGmTVBIfI&t=406s
                       https://www.youtube.com/watch?v=68Jd7GXZPe8
proper explnantion: https://docs.google.com/document/d/1OyHp3hr6-hPnLC1ESUtFQVhlGB7eWeYFlhmKeTo70qs/edit
