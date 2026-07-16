# Profiles REST API

A Django REST Framework tutorial project implementing a user-profiles API with authentication: user registration/login, profile management, and a simple activity "feed". Built following common DRF best practices (viewsets, routers, token authentication, custom permissions).

## Tech Stack

- Python
- [Django](https://www.djangoproject.com/) 2.2
- [Django REST Framework](https://www.django-rest-framework.org/) 3.9.2
- SQLite (default local database)

## Prerequisites

- Python 3 (a version compatible with Django 2.2, e.g. Python 3.6–3.8)
- pip

## Installation

```bash
git clone https://github.com/er-shrey/profiles-rest-api.git
cd profiles-rest-api

python3 -m venv myenv
source myenv/bin/activate   # On Windows: myenv\Scripts\activate

pip install -r requirements.txt
```

## Running the app

```bash
python manage.py migrate
python manage.py runserver
```

The API is served at `http://127.0.0.1:8000/`.

## API endpoints

- `GET/POST /hello-view/` — sample `APIView` demonstrating manual HTTP method handling
- `POST /login/` — obtain an auth token
- `/hello-viewset/` — sample `ViewSet` demonstrating router-based endpoints
- `/profile/` — user profile CRUD (`profiles_api.UserProfile`, the custom `AUTH_USER_MODEL`)
- `/feed/` — user profile feed items

## Project structure

- `profiles_project/` — Django project settings and root URL config
- `profiles_api/` — the app: models, serializers, views, permissions, and migrations
- `manage.py` — Django's command-line utility
