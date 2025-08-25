# alx-backend-caching_property_listings

A Django project for property listings with advanced caching using Docker, PostgreSQL, and Redis.

## Features

- Django project and app setup
- PostgreSQL as the database (Dockerized)
- Redis as the cache backend (Dockerized)
- Property list view cached for 15 minutes
- Low-level queryset caching for 1 hour
- Automatic cache invalidation using Django signals
- Redis cache metrics analysis

## Setup

1. Clone the repository:

   ```sh
   git clone https://github.com/kimoban/alx-backend-caching_property_listings.git
   cd alx-backend-caching_property_listings
   ```

2. Start Docker services:

   ```sh
   docker compose -f docker-compose.yaml up -d
   ```

3. Activate the virtual environment and install dependencies:

   ```sh
   # Windows PowerShell
   .venv\Scripts\Activate.ps1
   pip install -r requirements.txt
   ```

4. Run migrations:

   ```sh
   python manage.py makemigrations
   python manage.py migrate
   ```

5. Start the Django server:

   ```sh
   python manage.py runserver
   ```

## Endpoints

- `/properties/` — Returns all properties (cached)

## License

MIT
