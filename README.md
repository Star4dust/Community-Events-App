# Community Events App

A full-stack community events app built during the FNB App Academy 2026.
FastAPI backend serving a JSON API, with a Flet (Python) frontend.

## Features
- Browse local community events and filter them by category
- Save and un-save (bookmark) events
- Event detail view
- Register and log in (passwords are salted and hashed with PBKDF2)
- Loading, empty and error states in the UI

## Tech stack
Python 3.14, FastAPI, Uvicorn, Pydantic, Flet, httpx

## How to run
Requires Python 3.10 or newer.

1. Create and activate a virtual environment, then install dependencies:
   ```
   python -m venv venv
   venv\Scripts\activate
   pip install -r requirements.txt
   ```
2. Start the backend from the project root (API docs at http://127.0.0.1:8000/docs):
   ```
   uvicorn backend.main:app --reload
   ```
3. In a second terminal (venv activated), start the Flet app:
   ```
   flet run Frontend/src/main.py
   ```

## What I built vs. course material
Built as part of the FNB App Academy 2026, following the structure of the course's Community Events lesson (FastAPI backend, Flet frontend).

## Known limitations
- Users and saved events are kept in memory, so they reset when the server restarts
- Login returns the email only; there are no sessions or tokens yet
- CORS allows all origins, which is fine for local development but not for production
