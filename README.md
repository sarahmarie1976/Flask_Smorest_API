
# FIRST_REST_API

This is a REST API built with Flask. It provides endpoints for user authentication and managing items, stores, and tags.

## Table of Contents

- [Setup](#setup)
- [Running the Application](#running-the-application)
- [API Endpoints](#api-endpoints)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

## Setup

### Prerequisites

- Python 3.8 or higher
- Docker (optional, for containerized deployment)

### Installation

1. **Clone the repository**:

   ```bash
   git clone https://github.com/yourusername/first_rest_api.git
   cd first_rest_api
Create and activate a virtual environment:

bash

python -m venv .apivenv
source .apivenv/bin/activate
Install dependencies:

bash

pip install -r requirements.txt
Set up the database:

bash

flask db init
flask db migrate
flask db upgrade
Using Docker
Build the Docker image:

bash

docker build -t first_rest_api .
Run the Docker container:

bash

docker run -p 5005:5005 first_rest_api
Running the Application
Activate the virtual environment:

bash

source .apivenv/bin/activate
Run the Flask application:

bash

flask run
The application will be available at http://127.0.0.1:5005.

#API Endpoints
1. Authentication
   - POST /register - Register a new user
   - POST /login - Authenticate a user and return a JWT
   - POST /logout - Revoke the current JWT
2. Items
   - GET /item/<string:item_id> - Get an item by ID
   - POST /item - Create a new item
   - PUT /item/<string:item_id> - Update an item by ID
   - DELETE /item/<string:item_id> - Delete an item by ID
3. Stores
   - GET /store/<string:store_id> - Get a store by ID
   - POST /store - Create a new store
   - PUT /store/<string:store_id> - Update a store by ID
   - DELETE /store/<string:store_id> - Delete a store by ID
4. Tags
   - GET /tag/<string:tag_id> - Get a tag by ID
   - POST /tag - Create a new tag
   - PUT /tag/<string:tag_id> - Update a tag by ID


#first_rest_api/
   - ├── .apivenv/
   - ├── instance/
   - │   ├── data.db
   - ├── migrations/
   - │   ├── versions/
   - ├── models/
   - │   ├── __init__.py
   - │   ├── item.py
   - │   ├── item_tags.py
   - │   ├── store.py
   - │   ├── tag.py
   - │   ├── user.py
   - ├── resources/
   - │   ├── __init__.py
   - │   ├── item.py
   - │   ├── store.py
   - │   ├── tag.py
   - │   ├── user.py
   - ├── .flaskenv
   - ├── .gitignore
   - ├── app.py
   - ├── blocklist.py
   - ├── conftest.py
   - ├── db.py
   - ├── Dockerfile
   - ├── README.md
   - ├── requirements.txt
   - ├── schemas.py
##Contributing
   - Contributions are welcome! Please fork the repository and submit a pull request with your changes.

License
This project is licensed under the MIT License.

### How to Add the README.md in VSCode

1. **Open VSCode**:
   - Open your project folder in VSCode.

2. **Create the README.md File**:
   - Right-click on the root directory of your project in the Explorer panel on the left side.
   - Select "New File".
   - Name the file `README.md`.

3. **Add Content to the README.md File**:
   - Copy the content provided above.
   - Paste it into the `README.md` file in VSCode.

4. **Save the File**:
   - Save the `README.md` file by clicking on File > Save or pressing `Ctrl + S` (Windows) or `Cmd + S` (Mac).

Your `README.md` file is now created and formatted to be clear and visually appealing. This file provides useful information about your project, setup instructions, API endpoints, and more.
