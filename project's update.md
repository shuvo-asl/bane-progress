# Bane Invoice Backend

## Project Features

1. **User Management**
2. **User Change/Reset Password**
3. **User Login**
4. **Roles and Permissions**
5. **Authentication and Activity Log**
6. **Notifications**
7. **Currency**
8. **Chasing Rule**
9. **Billing Flights**
10. **Email Template**
11. **Invoice**
12. **Charges**
13. **Data Source**


# Bane Invoice Frontend

## Project Features

1. **Authentication**
2. **User Management**
3. **Roles and Permissions**
4. **Aggregator Flight**
5. **Bill Generation**
6. **Invoice**
7. **Data Source**
8. **Chasing Rule**



Certainly! Here's a simplified version:

### ADSB BACKEND

#### Features

#### API Endpoints:

1. **Fetch All Airports**
   - **Endpoint:** `/airport`
   - **Method:** GET
   - **Output:** All National or International Airports
   - **Remarks:** Fetches all international airports

2. **Get Individual Flight**
   - **Endpoint:** `/flight/<flight_status>`
   - **Method:** GET
   - **Output:** Individual Flight (All flights if status not specified)
   - **Remarks:** Specify status to filter results

3. **Get All Live Flights**
   - **Endpoint:** `/live`
   - **Method:** GET
   - **Output:** All Captured Flights
   - **Remarks:** Gets all flights accessed by sensors in real-time

#### SOCKETS Connected With MLAT-WEB-VIEW

> Events triggering data exchange between client and server

1. **Running Flights**
   - **Client Event:** `running flights`
   - **Server Event:** `data`
   - **Output:** List of running flights
   - **Remarks:** Filters and streams data for running flights

2. **Completed Flights**
   - **Client Event:** `completed flights`
   - **Server Event:** `data`
   - **Output:** List of completed flights
   - **Remarks:** Filters and streams data for completed flights

3. **Get Flight Data and Position History**
   - **Client Event:** `flight_no`
   - **Server Event:** `flight_data`
   - **Output:** Flight data and position history
   - **Remarks:** Gets data and history when flight number is passed

4. **Stream Live Positions of Flights**
   - **Client Event:** `live_position`
   - **Server Event:** `live_position_data`
   - **Output:** Live positions of currently active flights
   - **Remarks:** Streams positions when flights are running





# Bane Aggregator

## Features

### 1. Get Individual Flight

- **Endpoint:** `/flights/<flight_id>`
- **Method:** GET
- **Output:** Individual Flight
- **Remarks:** Retrieves a flight by its ID

### 2. Create a New Flight

- **Endpoint:** `/flights/`
- **Method:** POST
- **Output:** Newly Created Flight
- **Remarks:** Creates a new flight

### 3. Get All Flights

- **Endpoint:** `/flights/`
- **Method:** GET
- **Output:** All Flights (When date is not specified)
- **Remarks:** Fetches all flights stored

### 4. Get Filtered Flights by Date

- **Endpoint:** `/flights/`
- **Method:** GET
- **Output:** All Flights of the Given Date
- **Remarks:** Fetches filtered flights for a specific date

### 5. Get Data from Cache

- **Endpoint:** `/cache-data-sources/`
- **Method:** GET
- **Output:** Data Sources
- **Remarks:** Gets data from the cache

### 6. Store Data to Cache

- **Endpoint:** `/cache-data-sources/`
- **Method:** POST
- **Output:** Data Sources
- **Remarks:** Stores data to the relevant cache

### 7. Update Individual Flight

- **Endpoint:** `/flights/<unique_id>`
- **Method:** PATCH
- **Output:** Updated Individual Flight
- **Remarks:** Updates a particular flight by either callsign or ID when at least one of them is passed