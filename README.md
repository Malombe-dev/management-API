# management-API
Employee Management REST API
This project is a RESTful API for managing employee records, built using Python’s Flask framework and the Flask-RESTful library. The API provides endpoints to perform CRUD (Create, Read, Update, Delete) operations on an employee database, with a MySQL database hosted on PythonAnywhere.

Features
Create Employees: Add a new employee to the database.
Retrieve Employees: Get a list of all employees.
Update Employees: Update existing employee details.
Delete Employees: Remove an employee from the database.

Requirements
.Python 3.x
.Flask
.Flask-RESTful
.pymysql
.Installation


1.Clone the Repository
bash
Copy code:
git clone https://github.com/your-username/employee-management-api.git
cd employee-management-api

2.Set Up a Virtual Environment (optional)
bash
Copy code:

python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`

3.Install Dependencies

bash
Copy code
pip install -r requirements.txt
Configure Database

4.Update the database connection in app.py:

python
Copy code
connection = pymysql.connect(
    host='your_host',
    user='your_username',
    password='your_password',
    database='your_database'
)
Endpoints
The following endpoints are available:

POST /employees: Adds a new employee.

Payload:
json
Copy code
{
  "first_name": "John",
  "others": "Doe",
  "salary": 50000,
  "department": "Engineering"
}
GET /employees: Retrieves all employees.

PUT /employees: Updates an employee's first name.

Payload:
json
Copy code
{
  "id": 1,
  "first_name": "Jane"
}
DELETE /employees: Deletes an employee.

Payload:
json
Copy code
{
  "id": 1
}
Running the Application
To start the application, use the following command:

bash
Copy code
python app.py
The API will run in development mode at http://127.0.0.1:5000.

Error Handling
Each endpoint provides error handling to ensure that appropriate responses are returned for missing or invalid data, failed database transactions, and other issues.

Contributions
Feel free to fork this repository, make improvements, and create pull requests. Your contributions are welcome!

License
This project is licensed under the MIT License.
