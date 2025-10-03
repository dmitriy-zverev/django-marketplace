# Puddle - Django Marketplace Application

A Django-based online marketplace where users can buy and sell items, communicate through a messaging system, and manage their product listings.

## Features

- **User Authentication**: Sign up, login, and logout functionality
- **Item Listings**: Browse, search, and view detailed item information
- **Categories**: Organize items by categories
- **User Dashboard**: Manage your posted items
- **Messaging System**: Communicate with buyers/sellers through an inbox
- **Image Uploads**: Upload images for item listings
- **Responsive Design**: User-friendly interface

## Project Structure

```
puddle/
├── conversation/     # Messaging system between users
├── core/            # Main app with authentication and home page
├── dashboard/       # User dashboard for managing items
├── item/            # Item listings and categories
├── puddle/          # Project settings and configuration
├── media/           # User-uploaded files (images)
└── manage.py        # Django management script
```

## Requirements

- Python 3.8+
- Django 5.2.7
- Pillow (for image handling)

## Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd django-marketplace
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install django pillow
   ```

4. **Navigate to the project directory**
   ```bash
   cd puddle
   ```

5. **Run migrations**
   ```bash
   python manage.py migrate
   ```

6. **Create a superuser** (optional, for admin access)
   ```bash
   python manage.py createsuperuser
   ```

7. **Run the development server**
   ```bash
   python manage.py runserver
   ```

8. **Access the application**
   - Open your browser and go to: `http://127.0.0.1:8000/`
   - Admin panel: `http://127.0.0.1:8000/admin/`

## Usage

### For Sellers
1. Sign up for an account
2. Login to your account
3. Navigate to "Add Item" to create a new listing
4. Fill in item details (name, description, price, category, image)
5. Manage your items from the dashboard

### For Buyers
1. Browse available items on the homepage
2. Use search and filter by category
3. View item details
4. Contact sellers through the messaging system

### Messaging
- Start a conversation with an item seller
- View all conversations in your inbox
- Reply to messages

## Apps Description

### Core
Main application handling:
- Homepage with featured items
- User authentication (signup, login, logout)
- Contact page
- Base templates

### Item
Item management functionality:
- Item model with categories
- Create, read, update, delete operations
- Item browsing and search
- Image upload for listings

### Dashboard
User dashboard features:
- View your posted items
- Quick access to item management

### Conversation
Messaging system:
- Create conversations about items
- Send and receive messages
- Inbox view for all conversations

## Database

The project uses SQLite database (`db.sqlite3`) for development. For production, consider using PostgreSQL or MySQL.

## Media Files

User-uploaded images are stored in the `media/` directory. Make sure this directory has appropriate permissions.

## Security Notes

⚠️ **Important for Production**:
- Change the `SECRET_KEY` in settings.py
- Set `DEBUG = False`
- Configure `ALLOWED_HOSTS`
- Use environment variables for sensitive data
- Set up proper database (PostgreSQL/MySQL)
- Configure static files serving
- Enable HTTPS

## Development

To contribute or modify:

1. Make changes to the code
2. Run tests (if available):
   ```bash
   python manage.py test
   ```
3. Create migrations if models changed:
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

## License

This project is for educational purposes.

## Support

For issues or questions, please open an issue in the repository.
