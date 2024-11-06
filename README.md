# Backend

Moving from the frontend, the backend runs on AWS through a variety of different services to create an API that counts visitors to the website. Every time a visitor goes to the website, the table within DynamoDB is to be incremented using the created Lambda function in Python. It will return the Visitor # at the top of the website, from the value held within the visitor count table within DynamoDB. The API Gateway and Lambda function are integrated together referencing the Python and Javascript code, as well as the database to create the API.

### Javascript Code
