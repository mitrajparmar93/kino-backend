# DEVELOPMENT.md

## Development Guide

### Environment Setup

1. **Python Environment**: Use `poetry` for dependency management. 

`poetry install`

2. **Database Setup**: Install PostgreSQL on WSL and create a new database.

`CREATE DATABASE mydatabase;`

3. **Database Migration**: Run the Django migration commands to initialize your database schema.

`python manage.py migrate`

### Code Structure

- **Models**: Located in `models/` - Defines the data models related to `User`, `Movie`, `Rating`, etc.
- **Views**: Located in `views/` - Handles the business logic and data manipulation.
- **Templates**: Located in `templates/` - Houses the HTML templates.
- **Static**: Located in `static/` - Contains all static files like CSS and JS.

### Testing

1. **Unit Testing**: Use Django's built-in testing framework. 

python manage.py test

### Version Control

- Branching Strategy: Follow Git Flow
- `master` for production
- `develop` for active development

### CI/CD Pipeline

- **Linting**: Pylint, Flake8
- **Testing**: Automated testing with GitHub Actions
- **Deployment**: Docker for containerization, Kubernetes for orchestration

### API Documentation

- Utilize DRF Spectacular to automatically generate the API documentation. 
- Swagger UI accessible at `/api/docs/`

### Troubleshooting

- If psycopg2 fails to install, ensure you've installed its dependencies:

`sudo apt-get install libpq-dev`