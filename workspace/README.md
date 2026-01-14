# Little Lemon Django Starter

A minimal Django 6 project with a single app (`restaurant`) created for the Little Lemon capstone. It currently uses SQLite and includes the default project scaffolding.

## Project structure
- `littlelemon/manage.py` – Django management entrypoint
- `littlelemon/littlelemon/` – project config (`settings.py`, `urls.py`, WSGI/ASGI)
- `littlelemon/restaurant/` – app placeholder (`models.py`, `views.py`, `admin.py`, `tests.py`)

## Getting started
1) Activate the bundled virtual environment:
   - Windows PowerShell: `./Scripts/Activate.ps1`
   - Windows CMD: `Scripts\\activate.bat`
2) Run migrations and start the dev server:
   - `cd littlelemon`
   - `python manage.py migrate`
   - `python manage.py runserver`

## Running tests
From `littlelemon/`: `python manage.py test`

## Notes
- The project uses SQLite by default (`db.sqlite3`).
- Update `ALLOWED_HOSTS` in `littlelemon/settings.py` before deploying.
- The repository `.gitignore` excludes the virtual environment and common Python/Django artifacts.
