# Laravel Literature

An educational web application for Bulgarian literature exam preparation. The app provides a comprehensive database of authors, books, literary characters, and genres from the Bulgarian literature curriculum.

## Tech Stack

| Technology | Version | Description |
|------------|---------|-------------|
| PHP | >= 5.6.4 | Server-side language |
| Laravel | 5.4 | PHP Framework |
| MySQL | 5.7+ | Database |
| Blade | - | Templating engine |
| Bootstrap | - | CSS Framework |

## Features

- Browse Bulgarian literature authors and their biographies
- Explore books with detailed information and introductions
- View literary characters and their descriptions
- Filter content by literary genres
- User authentication system
- Responsive design for all devices

## Prerequisites

- PHP >= 5.6.4
- Composer
- MySQL 5.7+
- Node.js & npm (for frontend assets)

## Installation

1. Clone the repository:
```bash
git clone https://github.com/nikolaykolibarov/laravel-literature.git
cd laravel-literature
```

2. Install PHP dependencies:
```bash
composer install
```

3. Install JavaScript dependencies:
```bash
npm install
# or
yarn install
```

4. Create environment file:
```bash
cp .env.example .env
```

5. Generate application key:
```bash
php artisan key:generate
```

6. Configure your database in `.env`:
```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=laravel_literature
DB_USERNAME=your_username
DB_PASSWORD=your_password
```

7. Run database migrations:
```bash
php artisan migrate
```

8. (Optional) Seed the database:
```bash
php artisan db:seed
```

## How to Run

Start the development server:
```bash
php artisan serve
```

The application will be available at `http://localhost:8000`

For frontend asset compilation:
```bash
npm run dev
# or for production
npm run production
```

## Project Structure

```
laravel-literature/
├── app/
│   ├── Author.php           # Author model
│   ├── Book.php             # Book model
│   ├── Character.php        # Character model
│   ├── Genre.php            # Genre model
│   ├── Introduction.php     # Introduction model
│   ├── User.php             # User model
│   └── Http/
│       └── Controllers/
│           ├── AuthorsController.php
│           ├── BooksController.php
│           ├── CharactersController.php
│           ├── GenresController.php
│           └── HomeController.php
├── database/
│   └── migrations/          # Database migrations
├── resources/
│   └── views/               # Blade templates
│       ├── authors.blade.php
│       ├── books.blade.php
│       ├── characters.blade.php
│       ├── genres.blade.php
│       └── layouts/
├── routes/
│   └── web.php              # Web routes
└── public/                  # Public assets
```

> **Note:** This project was created for educational/course purposes to help students prepare for the Bulgarian literature matriculation exam.
