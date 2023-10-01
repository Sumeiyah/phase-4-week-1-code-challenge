# Pizza Restaurant API

This Flask API provides endpoints for managing pizza restaurants and their associated pizzas. It allows you to create, retrieve, update, and delete restaurants and pizzas, as well as associate pizzas with specific restaurants.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Endpoints](#endpoints)
- [Models](#models)
- [Validations](#validations)
- [Routes](#routes)
- [Author](#author)
- [License](#license)

## Installation

1. Clone the repository:

   ```bash
   $ git clone https://github.com/yourusername/pizza-restaurant.git
   $ cd pizza-restaurant
   ```

2. Set up a virtual environment:

   ```bash
   $ python3 -m venv venv
   $ source venv/bin/activate  # On Windows, use: venv\Scripts\activate
   ```

3. Install the required packages:

   ```bash
   $ pip install -r requirements.txt
   ```

4. Create and initialize the database:

   ```bash
   $ flask db init
   $ flask db migrate
   $ flask db upgrade
   ```

## Usage

1. Start the Flask server:

   ```bash
   $ flask run
   ```

2. Access the API at `http://localhost:5000`.

## Endpoints

- `GET /restaurants`: Get a list of all restaurants.
- `GET /restaurants/:id`: Get details of a specific restaurant.
- `DELETE /restaurants/:id`: Delete a restaurant by ID.
- `GET /pizzas`: Get a list of all pizzas.
- `POST /restaurant_pizzas`: Create a new RestaurantPizza association.

## Models

- `Restaurant`: Represents a pizza restaurant.
- `Pizza`: Represents a type of pizza.
- `RestaurantPizza`: Represents the association between a restaurant and a pizza.

## Validations

- `RestaurantPizza`: Price must be between 1 and 30.
- `Restaurant`: Name must be less than 50 characters in length and must be unique.

## Routes

- `GET /restaurants`: Returns a JSON list of restaurants.
- `GET /restaurants/:id`: Returns details of a specific restaurant, including associated pizzas.
- `DELETE /restaurants/:id`: Deletes a restaurant and its associated RestaurantPizzas.
- `GET /pizzas`: Returns a JSON list of pizzas.
- `POST /restaurant_pizzas`: Creates a new RestaurantPizza association.

## Author

Sumeya Farah

## License

This project is licensed under the [MIT License](LICENSE).

