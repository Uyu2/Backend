# Backend

Moving from the frontend, the backend runs on AWS through a variety of different services to create an API that counts visitors to the website. Every time a visitor goes to the website, the index.html file will reference Javascript file held within S3, which is then turned into an HTTP request to the API Gateway. It will then request the Lambda API with Python code, which increments the visitor count in DynamoDB, and returns the value. The value is then displayed as the visitor # at the top of the website, which is being displayed through the index.html file.

This repository seeks to serve as a restrospective on the creation of the process, and will break down each individual aspect that goes into the backend API.

### Javascript Code

The API Gateway handles requests for the Javascript, and helps communicate with the other tools such as Lambda and DynamoDB that are being used for the API. The Javascript is included in this repository under visitor-counter.js. The index.html file is also included in this repository, as the Javascript file is referenced in it, which is what triggers the API to function when a visitor clicks on the website. 

The Javascript itself operates on the frontend, requesting the number of visitors who have clicked on the page and then returning the value. It is then assigned to the website under "Visitor #: "
