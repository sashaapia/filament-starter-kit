# Filament Laravel Application

This is a Laravel application with Filament for the admin panel. Follow the steps below to set up the project on a new computer after cloning the repository.

---

## Installation Guide

### 1. Clone the Repository
Clone this repository to your local machine:
```bash
git clone https://github.com/sashaapia/filament-starter-kit.git
```

Navigate into the project directory:
```bash
cd filament-starter-kit
```

---

### 2. Install Dependencies

#### PHP Dependencies
Run Composer to install all required PHP packages:
```bash
composer install
```

---

### 3. Set Up the Environment File
Create a `.env` file by copying the example:
```bash
cp .env.example .env
```

Update the `.env` file with the following (if using mySQL):
- **Database Configuration:**
  ```env
  DB_CONNECTION=mysql
  DB_HOST=127.0.0.1
  DB_PORT=3306
  DB_DATABASE=your_database_name
  DB_USERNAME=your_database_user
  DB_PASSWORD=your_database_password
  ```

Use this instead if you plan to use sqlite:
- **Database Configuration:**
  ```env
    DB_CONNECTION=sqlite
  ```

DB_CONNECTION=sqlite

- Update other configurations (like `APP_NAME`, `APP_URL`) as needed.

---

### 4. Generate the Application Key
Run the following command to generate the `APP_KEY`:
```bash
php artisan key:generate
```

---

### 5. Set Up the Database
1. Ensure the database exists (create it using your preferred database management tool).
2. Run migrations to set up the schema:
   ```bash
   php artisan migrate
   ```

---

### 6. Create an Admin User (For Filament Admin Panel)
Run the following command to create an admin user:
```bash
php artisan make:filament-user
```

Follow the prompts to set up an admin account.

---

### 7. Start the Development Server
Run the development server:
```bash
php artisan serve
```

Visit the application in your browser at [http://localhost:8000](http://localhost:8000).

---

## Notes

- Ensure your `.gitignore` file includes the following entries to avoid committing sensitive files:
  ```gitignore
  /vendor
  /node_modules
  /storage
  .env
  ```
- For production deployments, additional steps such as configuring a web server, HTTPS, and environment-specific settings may be required.

---

Enjoy using your Filament-powered Laravel application!
