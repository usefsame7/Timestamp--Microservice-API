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

   - To convert a date string into Unix and UTC timestamps and store it in the database :

     ```
     POST /api/:date_string
     ```

     The API will respond with the stored timestamp object :

     ```json
     {
       "_id": "609f19c2625e6776d8fc5d88",
       "unix": 1621824000000,
       "utc": "Mon, 24 May 2021 00:00:00 GMT",
     }
   ```

  
   
   The API will return the current time in a JSON object with a unix key :

     ```shell
     GET '/'   => ( empty date parameter )
     ```

     
     
