Python RESTful API for Expense Management
This is a simple RESTful API developed in Python using Flask, Marshmallow, and Docker. The API manages personal expenses and incomes, providing the ability to add, delete, and fetch both expenses and incomes.

## Features
Developed using Flask and Marshmallow for data serialization/deserialization.
Fully dockerized for easy setup and deployment.
API endpoints for managing expenses and incomes.
Getting Started
These instructions will help you to run this project on your local machine for development and testing purposes.

## Prerequisites
Python 3.8 or later
Docker (if you want to run the project in a Docker container)
install pipenv

## Installation
Clone the repository: git clone https://github.com/fabian416/python-restful-api.git
Move into the project directory: cd python-restful-api
Install dependencies: pipenv install
  
## Running the Application
- Without Docker
You can start the application by running the bootstrap.sh script:
  ./bootstrap.sh
- With Docker
You can also run the application in a Docker container. First, you need to build the Docker image:
  docker build -t cashman .

## Usage
Here are some sample CURL commands you can use to interact with the API:

Get Expenses
curl http://localhost:5000/expenses
  
Add a New Expense
curl -X POST -H "Content-Type: application/json" -d '{
    "amount": 20,
    "description": "lottery ticket"
}' http://localhost:5000/expenses
  
Get Incomes
curl http://localhost:5000/incomes
  
Add a New Income
curl -X POST -H "Content-Type: application/json" -d '{
    "amount": 300.0,
    "description": "loan payment"
}' http://localhost:5000/incomes
## Future Work
Implement Database persistence with SQLAlchemy.
Add authorization using JWT.
