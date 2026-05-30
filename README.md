# Auth System (Nuxt 4 + Laravel 13 Sanctum)

A full-stack authentication application demonstrating secure, session-based SPA authentication using **Nuxt 4** and **Laravel 13** with **Sanctum**.

## 🚀 Features

- **User Registration:** Secure account creation with email uniqueness and password confirmation.
- **SPA Authentication:** Session-based authentication using Laravel Sanctum (no tokens in LocalStorage).
- **Protected Routes:** Nuxt middleware (`sanctum:auth` and `sanctum:guest`) to manage page access.
- **Responsive UI:** Styled with **Tailwind CSS** and **DaisyUI** using the _Synthwave_ theme.
- **Logout:** Secure session invalidation.

## 🛠️ Tech Stack

- **Frontend:** Nuxt 4, Vue 3, Tailwind CSS, DaisyUI.
- **Backend:** Laravel 13, Laravel Sanctum.
- **Database:** SQLite/MySQL (configured in Laravel).

## 📦 Installation & Setup

### 1. Backend (Server)

Navigate to the `server` directory:

```bash
cd server
composer install
cp .env.example .env
php artisan key:generate
```

- Configure your database in `.env`.
- Set `SANCTUM_STATEFUL_DOMAINS=localhost:3000` (or your frontend URL).
- Set `SESSION_DOMAIN=localhost`.

Run migrations:

```bash
php artisan migrate
php artisan serve
```

### 2. Frontend (Client)

Navigate to the `client/app` directory:

```bash
cd client/app
npm install
```

- Create a `.env` file and set your backend URL:
  `NUXT_PUBLIC_SANCTUM_BASE_URL=http://localhost:8000`

Start the development server:

```bash
npm run dev
```

The app will be available at `http://localhost:3000`.
