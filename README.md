Solution:

We can achieve this with a simple Flask application that exposes three endpoints and utilizes the Flask web framework for handling HTTP requests. Let me explain the code 
in sections:

main.py file
Flask: The main Flask class that is used to create the web application.
jsonify: A Flask function that helps in creating JSON responses.
request: Allows access to incoming request data.
json: Python's built-in module for working with JSON data.
requests: A popular HTTP library for making requests to APIs

data.py
There is a function fetch_data written in data.py 
fetch_data: A function that takes an API URL as a parameter, sends an HTTP GET request to that URL using the requests.get method, and checks if the response status code is 200 (OK).
If the status code is 200, it returns the JSON content of the response using response.json().
If the status code is not 200, it prints an error message and returns None.
Then there is a save_to_file function which will save the data in data.json file that will be used as source of information in the main.py (application)
save_to_file: A function that takes data and a filename as parameters and writes the data to a file in JSON format.
It uses the json.dump method to serialize the data to a JSON-formatted string and writes it to the specified file.
The indent=2 argument adds indentation to make the JSON file more human-readable.


We can now run the main.py file using the following command: #I am using a AWS EC2 instance to test the application.

#python3 main.py
