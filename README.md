# Full-Stack-Recipe-Sharing-Website

**Live Website:** [http://240391269.cs2410-web01pvm.aston.ac.uk](http://240391269.cs2410-web01pvm.aston.ac.uk)

---

## Overview

This is a full-stack recipe sharing platform built using the **Laravel PHP framework**. Users can register, log in, add recipes with images, search recipes by name or type, and view detailed recipes. The application follows the **MVC (Model-View-Controller)** architecture, separating logic from layout for easier maintenance.

---

## Technologies Used

- **Server-side:** PHP 8.x, Laravel Framework  
- **Client-side:** Blade templates, HTML, Bootstrap 5, inline custom CSS  
- **Database:** MySQL (hosted via Virtualmin/phpMyAdmin)  
- **Authentication:** Laravel UI with email/password login  
- **Image Uploads:** Handled via Laravel file upload (`public_html/uploads`)  
- **Security Features:** CSRF protection, input validation, password hashing, session management, authorization  

---

## Features

| Feature | Description | Main Source File(s) |
|---------|-------------|-------------------|
| View all recipes | Displays all recipes in styled cards with image, name, and description | `resources/views/recipes/index.blade.php` |
| View recipe details | Shows full recipe details including ingredients, steps, and image | `resources/views/recipes/show.blade.php` |
| Search recipes | Search by recipe name or type | `RecipeController@index()` |
| Register | User registration using Laravel UI | `register.blade.php` |
| Login | User login via email/password | `login.blade.php` |
| Add recipe | Authenticated users can add recipes with image upload | `recipes.create`, `RecipeController@store` |
| Update recipe | Users can edit their own recipes | `RecipeController.php` |
| Logout | Users can securely log out | Laravel default auth |

---

## Security Implementation

- **Authentication:** Only logged-in users can access create/edit/delete functions  
- **Authorization:** Only recipe owners can modify their entries  
- **CSRF Protection:** All forms use `@csrf` in Blade templates  
- **Input Validation:** Fields validated using Laravel's validation system  
- **Password Hashing:** Passwords hashed using bcrypt  
- **Session Management:** Laravel default session file driver  

---

## User Account for Testing

| Username | Password |
|----------|----------|
| amirahbegum652@gmail.com | helloworld |

---


