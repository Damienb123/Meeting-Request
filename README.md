# Meeting-Request

## Table of Contents

1. [Overview](#Overview)
2. [API Endpoints](#API-Endpoints)
    - Schedule a Meeting
3. [Request Body Format](#Request-Body-Format)
    - Example Request
4. [Setup Instructions](#Setup-Instructions)
5. [Example Usage](#Example-Usage)
6. [Reference](#Reference)
7. [Conclusion](#Conclusion)

## Overview

The Meeting-Request API allows users to schedule meetings by providing details such as time, duration, description, location, reminder time, and invitees. This documentation provides the necessary details to use the API effectively.

## API Endpoints

### Schedule a Meeting

- **Endpoint:** /meeting
- **Method:** POST
- **Content-Type:** application/json
 
## Request Body Format

The request body should be in JSON format and contain the following elements:

- **meeting:** Root element that encapsulates the meeting details.
  - **time:** Specifies the time of the meeting in YYYY-MM-DD HH:MM format.
  - **duration:** Duration of the meeting in minutes.
  - **description:** Description of the meeting.
  - **location:** Location of the meeting.
  - **reminder:** Reminder time in minutes before the meeting.
  - **invitees:** List of email addresses of the invitees.

### Example Request
```
{
    "meeting": {
        "time": "2015-09-01 10:00",
        "duration": 60,
        "description": "2016 Strategic Planning Meeting",
        "location": "Building 23, Room 206",
        "reminder": 15,
        "invitees": ["michael@example.com", "thelma@example.com", "david@example.com", "leon@example.com"]
    }
}
```

## Setup Instructions

1. **Clone the Respository:** Clone the project repository to your local machine.
2. **Install Dependencies:** Run the appropriate command to install dependencies (e.g., mvn install for Maven projects).
3. **Start the Server:** Start the server using your preferred method (e.g., mvn spring-boot:run for Spring Boot projects).

## Example Usage

To schedule a meeting, send a POST request to the /meeting endpoint with the following JSON body:
```
{
    "meeting": {
        "time": "2015-09-01 10:00",
        "duration": 60,
        "description": "2016 Strategic Planning Meeting",
        "location": "Building 23, Room 206",
        "reminder": 15,
        "invitees": ["michael@example.com", "thelma@example.com", "david@example.com", "leon@example.com"]
    }
}
```

## Reference

## Conclusion

The Meeting-Request API provides a straightforward way to schedule meetings by specifying details such as time, duration, description, location, reminder time, and invitees. This documentation outlines the required request format, expected responses, and provides examples to help users get started with the API.
