# Overview
Petstore is a sample API that simulates a pet shop management server. The API allows you to access Petstore data using a set of individual calls. There are three endpoint groups: Pet, Store, and User. 

## Features

### Manage Pets
- **Capabilities**:
  - Add new pets to the database.
  - Retrieve pet information.
  - Find pets by status.
  - Update existing pet records.
  - Delete a pet.
  
- **Data Generation**:
  - The Pet collection includes predefined arrays for animal categories (e.g., "Mammal," "Bird"), animals within those categories (e.g., "Dog," "Cat"), and descriptive tags (e.g., "Playful," "Cuddly"). This ensures that each new pet created is unique, with random combinations of these attributes.

### Manage Store
- **Capabilities**:
  - Create order records.
  - Find purchased order.
  - Retrieve inventory details.
  - Delete purchase order.

### Manage Users
- **Capabilities**:
  - Create single user or list of users
  - Log in and log out users.
  - Update user profile information.
  - Retrieve user activity history.
  - Delete user.

- **Data Generation**:
  - Each user in the User collection has a randomly generated unique ID, username, first name, last name, and email address to ensure uniqueness.

### Authorization
- Some of the API requests require authorization using an API key. The API key must be included in the header of those requests to authenticate the user and gain access to specific resources.

### Collection Variables
- To streamline API calls, part of the response data from previous requests (such as user IDs, order numbers, etc.) is stored as collection variables. These variables help in dynamically chaining requests without the need for manual data input, allowing smoother workflows and more efficient testing.

### Testing
Each request in the collection is equipped with automated tests to ensure the integrity and reliability of the API. Below are some of the key tests implemented:
- **Status Code Validation**: Verifying that the correct status code is returned for each request.
- **Response Structure Validation**: Ensuring that the response contains the expected fields and data types.
- **Response Code Validation**: Checking that the correct response code is returned based on the input.
- **ID Matching**: Ensuring that the correct ID is returned or updated in the response.

### Visual Reports with Newman
- The API tests are executed using Newman, which generates detailed visual reports. These reports provide insights into the test results, including pass/fail status, response times, and any errors encountered during testing, ensuring comprehensive coverage and transparency.