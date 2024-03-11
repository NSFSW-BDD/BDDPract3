# Practice - Autograding Instructions

This repository contains a test suite for an Express.js application. The practice is designed to evaluate your implementation of an Express.js API with specific endpoints and functionality. The following instructions outline the expected behavior that will be tested.

## Instructions

1. **Clone the repository**: Clone this repository to your local machine.

   ```shell
   git clone https://github.com/your-username/your-repository-name.git
   ```

2. **Navigate to the repository**: Change to the repository's directory.

   ```shell
   cd your-repository-name
   ```

3. **Install dependencies**: Install the necessary dependencies by running the following command.

   ```shell
   npm install
   ```

4. **Implement your Express.js application**: Create your Express.js application with the required endpoints and functionality based on the following specifications.

   - **GET /player**: This endpoint should return an array of player objects. The test will check if the response status is 200 (OK) and the response body contains an array with a length of 3.

   - **POST /player**: This endpoint should accept a request body containing `name` and `level` properties. The test will send requests to this endpoint with and without the request body. The response status should be 201 (Created) when the request body is provided, and 400 (Bad Request) when the request body is missing.

   - **GET /player/:id**: This endpoint should retrieve a specific player's information based on the provided `id`. The test will send a GET request to this endpoint after a successful POST request and expect the response status to be 200 (OK). The response body should contain the `name` and `level` properties matching the values provided in the POST request.

   - **PUT /player/:id**: This endpoint should update a specific player's information based on the provided `id`. The test will send requests to this endpoint with different scenarios. It will check if the response status is 400 (Bad Request) when the request body is missing or incomplete, 404 (Not Found) when the player does not exist, and 204 (No Content) when the player is successfully updated.

   - **DELETE /player/:id**: This endpoint should delete a specific player based on the provided `id`. The test will send a DELETE request to this endpoint and expect the response status to be 204 (No Content). After deletion, a subsequent GET request to the same endpoint should return a 404 (Not Found) status.

5. **Run the tests**: Execute the test suite to run the automated tests.

   ```shell
   npm test
   ```

6. **Review the test results**: After running the tests, the test suite will display the results in the console. It will indicate which tests passed and which tests failed. Pay attention to the failure messages to identify any errors in your application.

7. **Debug and iterate**: If any tests fail, review the failure messages and debug your Express.js application accordingly. Make the necessary modifications to fix the issues and rerun the tests to verify your changes.

8. **Repeat steps 5 and 6**: Continue iterating on your application, fixing any failing tests until all the tests pass successfully.

9. **Submit your solution**: Once all the tests pass, you can submit your solution for grading or further evaluation.

Note: Make sure your Express.js application follows the specified endpoint URLs and handles requests and responses correctly according to the given instructions.

Good luck with the autograding process!