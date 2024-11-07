
MathPower
MathPower is a serverless web application that calculates the power of a number using AWS services such as Lambda, API Gateway, DynamoDB, and IAM roles. The application takes a base and an exponent as input, retrieves them from DynamoDB, and calculates the result using a POST request to an API endpoint.
Features
•	Frontend: Built with HTML, CSS, and JavaScript to provide a user-friendly interface.
•	Backend: Uses AWS Lambda for the business logic and API Gateway for handling HTTP requests.
•	Database: Stores base and exponent values in AWS DynamoDB for easy retrieval and processing.
•	IAM Role: LambdaDynamoDB-role to provide Lambda function with full access to DynamoDB.
Technologies Used
•	Frontend:
o	HTML/CSS: Used to design and structure the web application.
o	JavaScript: Used to handle user input and make requests to the API Gateway endpoint.
•	Backend:
o	Python: The Lambda function (lambda_function.py) is written in Python and handles the business logic for calculating the power of the number.
o	AWS Lambda: A serverless compute service that runs the Python function without the need for provisioning servers.
o	API Gateway: Handles HTTP requests, connects the frontend to the Lambda function, and processes the data.
•	Database:
o	DynamoDB: A NoSQL database used to store the base and exponent values for calculation.
•	IAM Role:
o	LambdaDynamoDB-role: A custom IAM role that grants Lambda function the necessary permissions to access DynamoDB.
How It Works
1.	User Input: The user enters the base and exponent values on the frontend.
2.	API Request: When the user submits the data, a POST request is sent to the API Gateway endpoint.
3.	Lambda Function: The API Gateway triggers the Lambda function, which retrieves the base and exponent values from DynamoDB, performs the calculation, and returns the result.
4.	Result Display: The result is displayed back on the frontend, showing the calculated power of the number.
How to Use
Step 1: Clone the Repository
Clone the project to your local machine:
bash
Copy code
git clone https://github.com/SunnySangle/MathPower.git
Step 2: Set Up the Project
1.	Ensure you have the necessary AWS services set up:
o	AWS Lambda for running the function.
o	API Gateway to expose the API endpoint.
o	DynamoDB for storing the base and exponent values.
o	IAM Role with permissions for Lambda and DynamoDB.
2.	Open the index.html file in your browser to see the frontend in action.
Step 3: Make a Request
When the user enters the base and exponent values and submits the form, a POST request will be sent to the API Gateway endpoint. The backend will calculate the result and display it.
API Endpoint
The API is deployed using AWS API Gateway and can be accessed at the following endpoint:
bash
Copy code
POST https://ohop3fqi40.execute-api.ap-south-1.amazonaws.com/dev
Example Request:
json
Copy code
{
  "base": 2,
  "exponent": 3
}
Example Response:
json
Copy code
{
  "statusCode": 200,
  "body": "Your result is 8.0"
}
Screenshots:
[Screenshot](assets/images/screenshot1.png)
[Screenshot](assets/images/screenshot2.png)
[Screenshot](assets/images/screenshot3.png)
[Screenshot](assets/images/screenshot4.png)
[Screenshot](assets/images/screenshot5.png)
[Screenshot](assets/images/screenshot6.png)
[Screenshot](assets/images/screenshot7.png)
[Screenshot](assets/images/screenshot8.png)
[Screenshot](assets/images/screenshot9.png)
[Screenshot](assets/images/screenshot10.png)
[Screenshot](assets/images/screenshot11.png)
[Screenshot](assets/images/screenshot12.png)
[Screenshot](assets/images/screenshot13.png)


Deployment
The app is deployed on AWS Amplify, which simplifies the deployment of serverless applications.
Steps to Deploy:
1.	Set up your AWS account and configure the necessary services (Lambda, API Gateway, DynamoDB, IAM roles).
2.	Deploy the frontend using AWS Amplify for a fully managed deployment pipeline.

