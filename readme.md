# LMS Laravel – Learning Management System

## About

LMS Laravel is an open-source Learning Management System built with the Laravel PHP framework. It provides a platform for creating and managing courses, learning modules, and educational content.

The application supports three main user roles:

* **Admin:** Manages the platform and its resources.
* **Teacher:** Creates and manages courses and learning materials.
* **Student:** Accesses courses and educational content.

The project uses Laravel and various open-source packages to provide its core functionality. It is suitable as a starting point for developers looking to build or customize an online learning platform.

## Features

* Course and learning module management
* Separate roles for administrators, teachers, and students
* API authentication using Laravel Passport
* Google reCAPTCHA configuration
* Email service integration
* WebSocket support for chat functionality
* Database migrations and seeders

## Requirements

* PHP and the required extensions
* Composer
* Node.js and npm
* MySQL or another compatible database
* Git

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/nehafreak/LMS-Laravel-Learning-Management-System.git
cd LMS-Laravel-Learning-Management-System
```

### 2. Install Dependencies

```bash
composer install
```

### 3. Configure Environment Variables

Create the environment configuration file:

```bash
cp .env.example .env
```

Update your `.env` file with the appropriate settings.

**Database configuration**

```env
DB_DATABASE=lms_laravel
DB_USERNAME=root
DB_PASSWORD=root
```

**Google reCAPTCHA configuration**

Obtain your credentials from the [Google reCAPTCHA Admin Console](https://www.google.com/recaptcha/admin/site).

```env
ENABLE_CAPTCHA=true
NOCAPTCHA_SITEKEY=your_site_key
NOCAPTCHA_SECRET=your_secret_key
```

Configure the email settings in `.env` according to your preferred email provider, such as Mailgun or Amazon SES.

### 4. Generate the Application Key

```bash
php artisan key:generate
```

### 5. Run Database Migrations

```bash
php artisan migrate
```

### 6. Configure API Authentication

```bash
php artisan passport:install
```

### 7. Install Frontend Dependencies

```bash
npm install
npm run dev
```

### 8. Seed the Database

```bash
php artisan db:seed
```

### 9. Start the Application

Run the Laravel development server:

```bash
php artisan serve --port=8000
```

Open `http://127.0.0.1:8000` in your browser.

### 10. Start the WebSocket Server

For chat functionality, run the following command in a separate terminal:

```bash
php artisan websockets:serve
```

## Contributing

Contributions, improvements, and feature enhancements are welcome. Developers can extend the existing functionality to meet their project requirements.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
