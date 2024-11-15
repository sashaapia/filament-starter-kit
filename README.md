# Filament Laravel Application (version française plus bas)

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

---

# Application Laravel avec Filament

Il s'agit d'une application Laravel utilisant Filament pour le panneau d'administration. Suivez les étapes ci-dessous pour configurer le projet sur un nouvel ordinateur après avoir cloné le dépôt.

---

## Guide d'installation

### 1. Cloner le dépôt
Clonez ce dépôt sur votre machine locale :
```bash
git clone https://github.com/sashaapia/filament-starter-kit.git
```

Accédez au répertoire du projet :
```bash
cd filament-starter-kit
```

---

### 2. Installer les dépendances

#### Dépendances PHP
Exécutez Composer pour installer tous les paquets PHP requis :
```bash
composer install
```

---

### 3. Configurer le fichier d'environnement
Créez un fichier `.env` en copiant l'exemple fourni :
```bash
cp .env.example .env
```

Mettez à jour le fichier `.env` avec les informations suivantes (si vous utilisez MySQL) :
- **Configuration de la base de données** :
  ```env
  DB_CONNECTION=mysql
  DB_HOST=127.0.0.1
  DB_PORT=3306
  DB_DATABASE=nom_de_votre_base_de_donnees
  DB_USERNAME=utilisateur_de_la_base
  DB_PASSWORD=mot_de_passe_de_la_base
  ```

Utilisez ceci à la place si vous prévoyez d'utiliser SQLite :
- **Configuration de la base de données** :
  ```env
  DB_CONNECTION=sqlite
  ```

Mettez également à jour les autres configurations (comme `APP_NAME`, `APP_URL`) si nécessaire.

---

### 4. Générer la clé de l'application
Exécutez la commande suivante pour générer la clé `APP_KEY` :
```bash
php artisan key:generate
```

---

### 5. Configurer la base de données
1. Assurez-vous que la base de données existe (créez-la en utilisant votre outil de gestion préféré).
2. Lancez les migrations pour configurer le schéma de la base :
   ```bash
   php artisan migrate
   ```

---

### 6. Créer un utilisateur administrateur (pour le panneau Filament)
Exécutez la commande suivante pour créer un utilisateur administrateur :
```bash
php artisan make:filament-user
```

Suivez les instructions pour configurer un compte administrateur.

---

### 7. Lancer le serveur de développement
Démarrez le serveur de développement :
```bash
php artisan serve
```

Accédez à l'application dans votre navigateur à l'adresse [http://localhost:8000](http://localhost:8000).

---

## Notes

- Assurez-vous que votre fichier `.gitignore` inclut les entrées suivantes pour éviter de commettre des fichiers sensibles :
  ```gitignore
  /vendor
  /node_modules
  /storage
  .env
  ```
- Pour un déploiement en production, des étapes supplémentaires, telles que la configuration d'un serveur web, HTTPS et des paramètres spécifiques à l'environnement, peuvent être nécessaires.

---

Profitez de votre application Laravel avec Filament !