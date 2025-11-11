# Micro-project-fullstack-team_number_11

#Members
Prem vatage      [4MC23IS079]
Shivraj S M      [4MC23IS099]
Tejas kumar D H  [4MC23IS115]
Vidyasagar M N   [4MC23IS124]

#Interview Portal

A production-ready Django web application for interview preparation with MCQ questions, performance tracking, and gamification features.

## Features

- **60 MCQs** (20 Aptitude, 20 Technical, 20 HR) with 4 options each
- **Study Mode** and **Quiz Mode** for practice
- **Aptitude Quiz** with timer and auto-submit
- **HR Practice** with audio recording support
- **Performance Dashboard** with charts (Chart.js)
- **Gamification** with badges and points system
- **Dark Mode** toggle with localStorage persistence
- **Responsive UI** with Tailwind CSS

## Setup Instructions

### 1. Activate Virtual Environment

```bash
source .venv/bin/activate
```

### 2. Run Migrations (if not already done)

```bash
python manage.py makemigrations
python manage.py migrate
```

### 3. Load Sample Questions

```bash
python manage.py loaddata fixtures/sample_questions.json
```

### 4. Create Superuser (Optional)

```bash
python manage.py createsuperuser
```

### 5. Run Development Server

```bash
python manage.py runserver
```

Visit http://127.0.0.1:8000/ in your browser.

## Project Structure

- `core/` - Home dashboard and main views
- `preparations/` - Question models, views, and templates
- `performance/` - Performance tracking and charts
- `gamification/` - Badges and points system
- `accounts/` - User authentication and profiles
- `templates/` - HTML templates
- `static/` - JavaScript and CSS files
- `fixtures/` - Sample question data

## Key Features

### Gamification

- **Points System**: +10 per correct MCQ, +20 for quiz completion, +5 for daily streak
- **Badges**:
  - Algorithm Ace (≥20 technical correct)
  - HR Master (≥10 HR recordings)
  - Streak Keeper (7-day streak)
  - Speed Runner (avg time < 60s on 10 aptitude Qs)

### Performance Tracking

- Score history chart
- Topic proficiency radar chart
- Time analysis bar chart
- Weakness detection with practice recommendations

## Technologies Used

- Django 4.2+
- SQLite (default database)
- Tailwind CSS (CDN)
- Chart.js (CDN)
- Monaco Editor (CDN)
- Pillow (for image handling)

## Notes

- Uses SQLite for simplicity (can be changed to PostgreSQL/MySQL for production)
- All static assets loaded via CDN (no bundlers required)
- Dark mode persists in localStorage
- CSRF protection enabled for all POST requests

