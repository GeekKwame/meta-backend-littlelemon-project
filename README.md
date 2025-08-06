
Accessible only in development.

---

## 📦 Features

### ✅ Public Pages
- **Home Page** (`/`)  
  Static landing page (`index.html`) with branding or basic info.

- **About Page** (`/about`)  
  Static description about the Little Lemon restaurant.

### 🍽️ Menu Pages
- **Menu Listing** (`/menu`)  
  Displays all menu items from the database.

- **Single Menu Item View** (`/menu_item/<id>`)  
  View individual menu item details.

### 📆 Booking System
- **Booking Form** (`/book`)  
  A form allowing users to submit reservation requests.

- **Booking Display** (`/reservations?date=YYYY-MM-DD`)  
  Shows existing bookings for a selected date, as JSON embedded in the page.

- **API Booking Endpoint** (`/bookings`)  
  Accepts `POST` requests with JSON to create new reservations (CSRF exempt).  
  Also returns all bookings for a specific date in JSON format on `GET`.

---

## ⚙️ Technologies Used

- Python 3.11+
- Django 4.x
- SQLite (default Django DB)
- HTML (Template rendering)
- JSON (for bookings API)
- Bootstrap (optional frontend styling, if used)

---

## 🗂️ Project Structure (Views Overview)

| View Function         | URL Pattern              | Template               | Description                         |
|----------------------|--------------------------|------------------------|-------------------------------------|
| `home()`             | `/`                      | `index.html`           | Landing page                        |
| `about()`            | `/about`                 | `about.html`           | About Little Lemon                  |
| `menu()`             | `/menu`                  | `menu.html`            | List of menu items                  |
| `display_menu_item()`| `/menu_item/<id>`        | `menu_item.html`       | Detail view of a menu item          |
| `book()`             | `/book`                  | `book.html`            | Reservation form                    |
| `reservations()`     | `/reservations?date=`    | `bookings.html`        | Shows reservations on that date     |
| `bookings()`         | `/bookings` (POST/GET)   | API only               | JSON booking API                    |

---

## 🧪 API Usage

### POST: `/bookings`

```json
{
  "first_name": "Edmund",
  "reservation_date": "2025-08-06",
  "reservation_slot": "18:00"
}

## Disclaimer
This project is part of a course assignment from the Meta Back-End Developer Professional Certificate on Coursera. All rights belong to Meta Platforms, Inc. This repository is for educational and portfolio purposes only.

