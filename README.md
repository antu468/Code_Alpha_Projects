# Mini Social Media

A simple social media platform built with Laravel, allowing users to create profiles, post updates with images, like posts, and comment on them. This is a mini project demonstrating basic CRUD operations for social features using MongoDB as the database.

## Features

- **User Authentication**: Register, login, email verification, password reset.
- **User Profiles**: View and edit user profiles with bio and profile image.
- **Posts**: Create, view, edit, and delete posts with captions and images.
- **Likes**: Like and unlike posts.
- **Comments**: Add and delete comments on posts.
- **Feed**: Authenticated homepage showing all posts in a feed.

## Tech Stack

- **Backend**: Laravel 12.x (PHP 8.2+)
- **Database**: MongoDB (via `mongodb/laravel-mongodb` package)
- **Frontend**: Blade templates, Bootstrap (via Laravel UI), Vite for asset compilation
- **Other**: Composer for PHP dependencies, npm for JS/CSS

## Installation

1. **Clone the Repository**
   ```
   git clone <your-repo-url>
   cd Mini_Social_media
   ```

2. **Install PHP Dependencies**
   ```
   composer install
   ```

3. **Install Node Dependencies**
   ```
   npm install
   ```

4. **Environment Setup**
   - Copy `.env.example` to `.env`:
     ```
     cp .env.example .env
     ```
   - Generate application key:
     ```
     php artisan key:generate
     ```
   - Configure your MongoDB connection in `.env`:
     ```
     DB_CONNECTION=mongodb
     DB_HOST=127.0.0.1
     DB_PORT=27017
     DB_DATABASE=your_database_name
     DB_USERNAME=your_username  # if applicable
     DB_PASSWORD=your_password  # if applicable
     ```
   - Set up mail configuration if needed (e.g., for email verification):
     ```
     MAIL_MAILER=smtp
     MAIL_HOST=mailpit
     MAIL_PORT=1025
     MAIL_USERNAME=null
     MAIL_PASSWORD=null
     MAIL_ENCRYPTION=null
     MAIL_FROM_ADDRESS="hello@example.com"
     MAIL_FROM_NAME="${APP_NAME}"
     ```

5. **Database Setup**
   - Run migrations to create tables:
     ```
     php artisan migrate
     ```
   - Seed the database (optional, for testing):
     ```
     php artisan db:seed
     ```

6. **Build Assets**
   ```
   npm run build
   ```
   Or for development:
   ```
   npm run dev
   ```

7. **Run the Application**
   ```
   php artisan serve
   ```
   Visit `http://127.0.0.1:8000` in your browser.

## Usage

- Register a new account or log in.
- Create a post with a caption and optional image upload.
- View the feed at `/` (requires login).
- Like/unlike posts or add comments.
- Visit `/profile/{username}` to see user profiles.
- Edit your profile at `/profile/{username}/edit`.

## File Structure

- `app/Models/`: Eloquent models for User, Post, Comment, Like.
- `app/Http/Controllers/`: Controllers for auth, posts, profiles, comments, likes.
- `resources/views/`: Blade templates for views (posts, profiles, auth).
- `routes/web.php`: Web routes definition.
- `database/migrations/`: MongoDB migrations for schema.

## Testing

Run PHPUnit tests:
```
php artisan test
```

## Contributing

1. Fork the project.
2. Create a feature branch (`git checkout -b feature/AmazingFeature`).
3. Commit changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the branch (`git push origin feature/AmazingFeature`).
5. Open a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Support

If you encounter issues, check the `storage/logs/laravel.log` file or open an issue on GitHub.
