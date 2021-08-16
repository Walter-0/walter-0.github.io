# Walter Augustine - SNHU Computer Science Capstone - 2021

## Professional Self-Assessment

This portfolio represents a wide range of the skills I have developed during my time in the computer science bachelor's degree program at SNHU, which include collaborating in an agile software lifecycle, using data structures and algorithms, developing with a security-first mindset, and software testing.

In this project, I used a modern technology stack to build an application that follows industry best-practices and is both maintainable and extensible. The artifacts in this portfolio are all part of the same software project. I used my final project from CS-340 as a starting point, which was a backend API written in Java that connected to a MongoDB database of stock information.

In a nutshell, this project replaced Java with Python as the backend language, added a user interface, and added a realtime search capability.

Tech stack:

* Docker
* MongoDB Atlas
* FastAPI
* Python
* React
* TypeScript
* Bootstrap
* NextJS

## Code Review

[Source code](https://github.com/Walter-0/CS-340-Final-Project)

<iframe width="560" height="315" src="https://www.youtube.com/embed/OPCBDHjs6pQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Artifacts

[Source code](https://github.com/Walter-0/capstone-project)

### Software Design and Engineering

This artifact is a full stack stock application that I built with the new FARM stack, which includes FastAPI, React, and MongoDB. I reused the stock database from the previous project from CS-340, since the data source is the same. This artifact builds on the previous project in that there is less duplication, a more flexible REST API, and a front end to interact with the back end service. I think this artifact is a strong inclusion to my portfolio, considering that the remaining two artifacts will build on the first, improving the whole system. One challenge I had was Dockerizing the project. I was able to get the back end and the database running in Docker containers, but the front end had an error that I was unable to debug at first. Although this project is not deployed, I wanted to provide an initial setup for deploying a Docker container. I enjoyed working with Python, because it's less cumbersome than Java. The latest version of Python has optional typing, which I found to be a useful inclusion when building an API.

### Data Structures and Algorithms

For this artifact, I added the ability to send custom queries to the database that would return a list of stocks that matched. For example, a query can be sent that returns any number of stocks in a particular industry sorted by any field, ascending or descending. This artifact was not part of the original plan, which was to hard-code database queries to return lists of stocks, but is a big improvement over anything hard-coded because it's less limiting. This artifact is important because searching is an important aspect of many database systems. While the third artifact adds full-text search to only return a single stock, this artifact provides a simple way to perform min/max analyses on the stocks in the database by sorting on any of the fields present on the stock documents. The biggest challenge in this artifact was using query strings in the request to the back end, as opposed to using the request body, which I had used for POST and PUT requests.

### Database

This artifact adds full-text search to the MongoDB database by indexing two fields, ticker and company name, on the stock documents. I then wrote database queries in the Python back end so that the front end could search the database for stocks and receive immediate, real-time suggestions based on the input query. Additionally, there is an API route to return a list of all the industries present in the database. The biggest challenge was in building the front end component that would send a new request on every change event that the search box handled, and update a list of suggestions received from the database in response to the user typing, without having to press <kbd>Enter</kbd> or click a submit button.
