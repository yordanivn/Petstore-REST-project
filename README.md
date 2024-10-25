# Overview
Petstore is a sample API that simulates a pet shop management server. The API allows you to access Petstore data using a set of individual calls. There are three endpoint groups: Pet, Store, and User. Playing around with this API documentation can help you understand how APIMatic docs provide value to you.

## Features

### Manage Pets
- **Overview**: This group contains every endpoint needed to manage pet records.
- **Capabilities**:
  - Add new pets to the database.
  - Remove pets from the records.
  - Retrieve pet information.
  - Update existing pet records.
- **Data Generation**:
  - The Pet collection includes predefined arrays for animal categories (e.g., "Dogs," "Cats"), animals within those categories (e.g., "Labrador," "Siamese"), and descriptive tags (e.g., "friendly," "energetic"). This ensures that each new pet created is unique, with random combinations of these attributes.

### Manage Store
- **Overview**: This group contains endpoints required to manage your orders.
- **Capabilities**:
  - Create order records.
  - Update order statuses.
  - Retrieve inventory details.

### Manage Users
- **Overview**: Manage your customer records through this endpoint group.
- **Capabilities**:
  - Log in and log out users.
  - Update user profile information.
  - Retrieve user activity history.
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