# Timestamp Microservice API with MongoDB

This repository contains a microservice API for timestamp functionality, utilizing MongoDB as the database. The API accepts a date string as input, stores it in a MongoDB collection, and returns a JSON object containing both the Unix timestamp and the UTC timestamp of the provided date.

## Prerequisites

- Node.js and npm installed on your system.
- MongoDB installed and running.

## Installation

1. Clone the repository:

   ```shell
   git clone https://github.com/usefsame7/Timestamp--Microservice-API.git
   ```

2. Navigate to the project directory:

   ```shell
   cd Timestamp--Microservice-API
   ```

3. Install the dependencies:

   ```shell
   npm install
   ```

4. Set up MongoDB:

   - Ensure that MongoDB is installed and running.
   - Update the MongoDB connection URL in `config.js` if necessary.

## Usage

1. Start the server:

   ```shell
   npm start
   ```

   This will start the server on `http://localhost:3000`.

2. Access the API:

   The API provides several endpoints for timestamp functionality.

   - To convert a date string into Unix and UTC timestamps and store it in the database:

     ```
     POST /api/timestamp
     ```

     Example request body:

     ```json
     {
       "dateString": "2021-05-24"
     }
     ```

     The API will respond with the stored timestamp object:

     ```json
     {
       "_id": "609f19c2625e6776d8fc5d88",
       "dateString": "2021-05-24",
       "unix": 1621824000000,
       "utc": "Mon, 24 May 2021 00:00:00 GMT",
       "createdAt": "2023-05-24T10:00:00.000Z"
     }
     ```

   - To retrieve all stored timestamp objects:

     ```
     GET /api/timestamp
     ```

     The API will respond with an array of timestamp objects:

     ```json
     [
       {
         "_id": "609f19c2625e6776d8fc5d88",
         "dateString": "2021-05-24",
         "unix": 1621824000000,
         "utc": "Mon, 24 May 2021 00:00:00 GMT",
         "createdAt": "2023-05-24T10:00:00.000Z"
       },
       {
         "_id": "609f1a0f625e6776d8fc5d89",
         "dateString": "2023-05-24",
         "unix": 1671824000000,
         "utc": "Wed, 24 May 2023 00:00:00 GMT",
         "createdAt": "2023-05-24T10:05:00.000Z"
       }
     ]
     ```

   - To retrieve a specific stored timestamp object by ID:

     ```
     GET /api/timestamp/:id
     ```

     Example usage:

     ```
     GET /api/timestamp/609f19c2625e6776d8fc5d88
     ```

     The API will respond with the timestamp object matching the provided ID.

   - To delete a specific stored timestamp object by ID:

     ```
     DELETE /api/timestamp/:id
     ```

     Example usage:

     ```
     DELETE /api/timestamp/609f19c2625e6776d8fc5d88
     ```

     The API will

