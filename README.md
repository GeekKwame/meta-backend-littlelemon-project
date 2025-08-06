# Little Lemon Restaurant - Backend System 🍋

**Status**: Development (Accessible only in development mode)  
**Disclaimer**: This project is part of the [Meta Back-End Developer Professional Certificate](https://www.coursera.org/professional-certificates/meta-back-end-developer) on Coursera. All rights belong to Meta Platforms, Inc. This repository is for educational/portfolio purposes only.

---

## 🌟 Key Features

### 📍 Public Pages
| Page          | URL          | Template       | Description                                  |
|---------------|--------------|----------------|----------------------------------------------|
| **Home**      | `/`          | `index.html`   | Landing page with branding and key info.     |
| **About**     | `/about`     | `about.html`   | Restaurant story, team, and mission.         |

### 🍽️ Menu System
| Feature               | URL Pattern            | Template         | Description                                |
|-----------------------|------------------------|------------------|--------------------------------------------|
| Full Menu            | `/menu`                | `menu.html`      | Paginated list of all menu items.          |
| Single Item Details  | `/menu_item/<int:id>`  | `menu_item.html` | Detailed view (price, description, etc.). |

### 📅 Booking System
| Feature               | URL/Endpoint           | Method | Data Format | Description                                |
|-----------------------|------------------------|--------|-------------|--------------------------------------------|
| Booking Form         | `/book`                | GET    | HTML        | User-facing reservation form.              |
| View Reservations    | `/reservations?date=`  | GET    | HTML+JSON   | Embedded JSON of bookings for a date.      |
| **API Endpoint**     | `/bookings`            | POST   | JSON        | Submit new reservations (CSRF exempt).     |
|                       | `/bookings?date=`      | GET    | JSON        | Retrieve bookings for a specific date.     |

---

## ⚙️ Tech Stack

### Backend
- **Python 3.11+**
- **Django 4.x** (MVT architecture)
- **SQLite** (Default database)

### Frontend
- **HTML Templates** (Django templating engine)
- **Bootstrap 5** (Responsive styling - optional)
- **JSON API** (For booking system integration)

### Development Tools
- Django Admin Panel (For data management)
- SQLite Browser (For DB inspection)

---

## 🛠️ Installation & Setup

```bash
# 1. Clone the repository
git clone https://github.com/yourusername/little-lemon-django.git
cd little-lemon-django

# 2. Set up virtual environment (Recommended)
python -m venv venv
source venv/bin/activate  # Linux/Mac
# venv\Scripts\activate  # Windows

# 3. Install dependencies
pip install -r requirements.txt

# 4. Run migrations
python manage.py migrate

# 5. Start development server
python manage.py runserver
