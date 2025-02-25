# FastAPI Events Management API

A RESTful API built with FastAPI for managing events, organizers, and attendees. This application provides endpoints for creating, reading, updating, and deleting events, as well as filtering events and analyzing attendee participation.

## Features

- **Event Management**: Create, read, update, and delete events
- **Filtering**: Filter events by date, organizer, status, or event type
- **Data Persistence**: Store event data in a JSON file
- **Event Analysis**: Identify attendees who have joined multiple events

## Project Structure

```
├── app/
│   ├── main.py              # Application entry point
│   └── src/
│       ├── app.py           # FastAPI application setup
│       ├── event_analyzer.py # Event analysis functionality
│       ├── file_storage.py  # JSON file data persistence
│       ├── models.py        # Pydantic data models
│       └── routes.py        # API endpoints
├── events.json              # Data storage file
├── requirements.txt         # Project dependencies
└── README.md                # Project documentation
```

## API Endpoints

- `GET /`: Welcome message
- `GET /events`: Get all events
- `GET /events/filter`: Filter events by date, organizer, status, or event type
- `GET /events/{event_id}`: Get a specific event by ID
- `POST /events`: Create a new event
- `PUT /events/{event_id}`: Update an existing event
- `DELETE /events/{event_id}`: Delete an event
- `GET /events/joiners/multiple-meetings`: Get a random joiner who has attended multiple events

## Installation

To run this project locally, you need to have Python and pip installed on your machine.

1. Clone this repository:
   ```bash
   git clone https://github.com/2001J/FastAPI-Events-Management-API
   ```

2. Navigate into the project directory:
   ```bash
   cd fastapi-events-management
   ```

3. Create a virtual environment:
   ```bash
   python -m venv venv
   ```

4. If you are using `Windows PowerShell`, it needs to be run first. However, if you are using `CMD`, this step is not necessary:
   ```bash
   Set-ExecutionPolicy Unrestricted -Scope Process
   ```

5. Activate the virtual environment:
   ```bash
   # Windows users run this command:
   .\venv\Scripts\activate

   # Linux or MacOS users run this command:
   source venv/bin/activate
   ```

6. Install the requirements in the current environment:
   ```bash
   pip install -r requirements.txt
   ```

7. Run the application:
   ```bash
   python app/main.py
   ```

## Testing the API

FastAPI provides automatic interactive API documentation. To access it, visit:
```
http://127.0.0.1:8000/docs
```

This interface allows you to explore and test all available endpoints directly from your browser.

## Data Models

- **Event**: Contains information about an event including name, date, organizer, status, type, location, maximum attendees, and joiners
- **Organizer**: Contains name and email of the event organizer
- **Joiner**: Contains name, email, and country of an event attendee

## Dependencies

- FastAPI: Web framework for building APIs
- Uvicorn: ASGI server for running the application
- Pydantic: Data validation and settings management

## License

[MIT License](LICENSE)







