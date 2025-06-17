Pizza Restaurant API

Setup & Run

Install dependencies:

pipenv install
pipenv shell

Set up database:

export FLASK_APP=server.app
flask db init
flask db migrate
flask db upgrade

Add sample data:

python server/seed.py

Start server:

flask run

API Endpoints

Restaurants

GET /restaurants
List all restaurants
curl http://localhost:5000/restaurants

GET /restaurants/
Get specific restaurant with its pizzas
curl http://localhost:5000/restaurants/1

DELETE /restaurants/
Delete a restaurant
curl -X DELETE http://localhost:5000/restaurants/1

Pizzas

GET /pizzas
List all pizza types
curl http://localhost:5000/pizzas