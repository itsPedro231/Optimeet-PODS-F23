<div align='center'>

```
██████╗  ██████╗ ██████╗     ██╗  ██╗
██╔══██╗██╔═══██╗██╔══██╗    ██║  ██║
██████╔╝██║   ██║██║  ██║    ███████║
██╔═══╝ ██║   ██║██║  ██║    ╚════██║
██║     ╚██████╔╝██████╔╝         ██║
╚═╝      ╚═════╝ ╚═════╝          ╚═╝
```

</div>

# Optimeet - Meetup Facilitation Platform

Optimeet is a web application that helps groups organize meetups by collecting user preferences and generating personalized activity recommendations. The platform uses an intelligent algorithm to suggest optimal meeting times and locations based on group member preferences.

## Architecture

The project consists of two main components:

### Backend API (Django)
- **Framework**: Django 4.2.6 with Django REST Framework 
- **Database**: SQLite (development) / MySQL (production)
- **Key Features**: Group management, user preferences, recommendation generation, voting system

### Frontend (React)
- **Framework**: React with Vite
- **Key Features**: Activity selection, location preferences, time availability, recommendation viewing

## Features

- **Group Creation & Management**: Create meetup groups and invite participants
- **Preference Collection**: Multi-step preference setting for activities, location, and time availability
- **Smart Recommendations**: Algorithm-generated suggestions based on group preferences
- **Voting System**: Democratic selection of final meetup details
- **Location Integration**: Geographic preferences with radius-based search

## Installation

### Backend Setup
```bash
cd api/optimeet
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```

### Frontend Setup
```bash
cd web/meetup-facilitator
npm install
npm run dev
```

## Environment Configuration

Create a `.env` file in the API directory:
```
SECRET_KEY=your_secret_key
DEBUG=True
ALGO_URL=http://your-algorithm-service-url
# Production database settings
DB_HOST=your_db_host
DB_PORT=your_db_port
DB_NAME=your_db_name
DB_USER=your_db_user
DB_PASS=your_db_password
```

## CI/CD

The project includes automated workflows for database migrations: 

- **Migration Testing**: Validates schema changes on pull requests
- **Production Deployment**: Automatically applies migrations to production database

## License

This project is licensed under the GNU General Public License v3.0 
