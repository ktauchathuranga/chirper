# Chirper

A microblogging application built with Laravel 12. Users can post short messages ("chirps"), edit and delete their own posts, and view a public feed of recent chirps from all users.

## Features

- Post chirps up to 255 characters
- Edit and delete your own chirps
- Public feed showing the 50 most recent chirps
- "Edited" indicator for updated chirps
- User registration and login
- Dynamic user avatars

## Tech Stack

**Backend**
- Laravel 12 (PHP 8.2+)
- SQLite / MySQL (configurable via `.env`)

**Frontend**
- Blade templates (server-rendered)
- Tailwind CSS v4
- DaisyUI v5
- Vite 7

**Testing**
- Pest 4

## Requirements

- PHP 8.2+
- Composer
- Node.js and npm

## Installation

1. Clone the repository:

```bash
git clone <repository-url>
cd chirper
```

2. Run the setup script, which installs dependencies, copies `.env`, generates the app key, runs migrations, and seeds the database:

```bash
composer setup
```

3. Start the development servers (Laravel, queue worker, log viewer, and Vite):

```bash
composer dev
```

The application will be available at `http://localhost:8000`.

## Manual Setup

If you prefer to set up manually:

```bash
composer install
cp .env.example .env
php artisan key:generate
php artisan migrate --seed
npm install
npm run dev
```

## Running Tests

```bash
php artisan test
```

## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
