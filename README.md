# EduCase Assignment API

## Endpoints

Render Hosted Link : https://educaseassignment-1awn.onrender.com
request may take some time due to render inactivity policy , request may take up to 50 seconds

### 1️⃣ **Add School API**
**Endpoint:** `/addSchool`
- **Method:** `POST`
- **Request Body:**
  ```json
  {
    "name": "name",
    "address": "address",
    "latitude": "xx",
    "longitude": "yy"
  }
  ```
  - `latitude` and `longitude` are float data type.
- **Response (Success - 201 Created):**
  ```json
  {
    "message": "School added successfully",
    "schoolId": "1,2,3....."
  }
  ```
---

### 2️⃣ **List Schools API**
**Endpoint:** `/listSchools`
- **Method:** `GET`
- **Query Parameters:**
  - `latitude` (required)
  - `longitude` (required)
  
  **Example Request:**
  ```
  GET /listSchools?latitude=xx&longitude=yy
  change the xx and yy accordingly
  ```
- **Response (Success - 200 OK):**
  ```json
  {
    "schools": [
      {
        "id": 1,
        "name": "name",
        "address": "address",
        "distance": "x km"
      }
    ]
  }
  ```
- **Response (Error - 400 Bad Request):**
  ```json
  {
    "error": "Missing latitude or longitude"
  }
  ```

## Testing with Postman
- Send requests to `/addSchool` and `/listSchools`.

## Deployment
- Hosted on **Render** (or your chosen platform).
- MySQL database hosted on **Railway**.
