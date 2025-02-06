# Number Classification API

## Overview

The Number Classification API is a web-based service that classifies a given number based on its mathematical properties. It determines whether a number is prime, perfect, or an Armstrong number and also provides additional attributes such as digit sum and parity (odd/even). A fun fact about the number is also retrieved from the Numbers API.

## Features

- Accepts a number as a query parameter.
- Determines if the number is prime, perfect, or an Armstrong number.
- Identifies whether the number is odd or even.
- Calculates the sum of the digits.
- Fetches a fun fact from the Numbers API.
- Returns responses in JSON format.
- Implements CORS support for cross-origin requests.

## Technologies Used

- Node.js
- Express.js
- Axios
- CORS

## API Endpoint

### Request

```text
GET /api/classify-number?number=<num>
```

### Response (200 OK)

```json
{
  "number": 371,
  "is_prime": false,
  "is_perfect": false,
  "properties": ["armstrong", "odd"],
  "digit_sum": 11,
  "fun_fact": "371 is an Armstrong number because 3^3 + 7^3 + 1^3 = 371"
}
```

### Response (400 Bad Request)

```json
{
  "number": "invalid_input",
  "error": true
}
```

## How to Run the API Locally

1. Clone the repository:

   ```sh
   git clone https://github.com/your-username/number-classification-api.git
   ```

2. Navigate to the project directory:

   ```sh
   cd number-classification-api
   ```

3. Install dependencies:

   ```sh
   npm install
   ```

4. Start the server:

   ```sh
   npm run server
   ```

5. Access the API in a browser or via Postman:

   ```sh
   http://localhost:3000/api/classify-number?number=371
   ```

## Deployment

The API is deployed and publicly accessible at:
[Live API Link](https://x-line-api-stage1.onrender.com/api/classify-number?number=371)

## Project Structure

```text
|-- index.js
|-- package.json
|-- README.md
```

## Acknowledgments

- [Numbers API](http://numbersapi.com) for providing fun facts.
- [HNG Internship](https://hng.tech) for the project challenge.
