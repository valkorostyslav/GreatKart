# GreatKart - E-commerce Django Project

E-commerce platform built with Django for online shopping.

## Features

- User authentication and registration
- Product catalog with categories
- Shopping cart functionality
- Product variations (color, size)
- Order management
- Product reviews and ratings
- User dashboard
- Admin panel

## Requirements

- Python 3.8+
- Django 4.2.2
- SQLite (default database)

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/valkorostyslav/GreatKart.git
cd GreatKart
```

### 2. Create virtual environment

```bash
# Windows
python -m venv venv

# Activate virtual environment
# Windows PowerShell
.\venv\Scripts\Activate.ps1

# Windows CMD
venv\Scripts\activate

# Linux/Mac
python3 -m venv venv
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Create .env file

Copy `.env-sample` to `.env` and fill in the required values:

```bash
# Windows
copy .env-sample .env

# Linux/Mac
cp .env-sample .env
```

Edit `.env` file with your settings:

```env
SECRET_KEY=your-secret-key-here
DEBUG=True
EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_HOST_USER=your-email@gmail.com
EMAIL_HOST_PASSWORD=your-app-password
EMAIL_USE_TLS=True
```

**Note:** For Gmail, you need to use an [App Password](https://support.google.com/accounts/answer/185833) instead of your regular password.

### 5. Run migrations

```bash
python manage.py migrate
```

### 6. Create superuser

```bash
python manage.py createsuperuser
```

Follow the prompts to create an admin user.

### 7. Collect static files (optional, for production)

```bash
python manage.py collectstatic
```

### 8. Run the development server

```bash
python manage.py runserver
```

The server will start at `http://127.0.0.1:8000/`

## Access Points

- **Homepage:** http://127.0.0.1:8000/
- **Admin Panel:** http://127.0.0.1:8000/admin/
- **Store:** http://127.0.0.1:8000/store/
- **Cart:** http://127.0.0.1:8000/cart/
- **Accounts:** http://127.0.0.1:8000/accounts/

## Project Structure

```
GreatKart/
├── accounts/          # User authentication and profiles
├── carts/            # Shopping cart functionality
├── category/         # Product categories
├── greatkart/        # Main project settings
├── orders/           # Order management
├── store/            # Product management
├── templates/        # HTML templates
├── static/           # Static files (CSS, JS, images)
├── media/            # User uploaded files
├── manage.py         # Django management script
└── requirements.txt  # Python dependencies
```

## Adding Products with Variations

1. Go to Admin Panel → Store → Products
2. Create or edit a product
3. In the "Variations" section, add color and size variations:
   - **Variation category:** Select `color` or `size`
   - **Variation value:** Enter the value (e.g., "Red", "Blue" for colors or "S", "M", "L" for sizes)
   - **Is active:** Check to make the variation available

## Troubleshooting

### Virtual environment not activating

If you get an error when activating the virtual environment in PowerShell, run:

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```

### Module not found errors

Make sure the virtual environment is activated and all dependencies are installed:

```bash
pip install -r requirements.txt
```

### Database errors

If you encounter database errors, try:

```bash
python manage.py migrate
```

### UserProfile DoesNotExist error

This has been fixed - UserProfile will be created automatically when needed.

## Technologies Used

- Django 4.2.2
- Python 3.8+
- SQLite
- Bootstrap (for frontend)
- Pillow (for image handling)

## License

This project is open source and available under the MIT License.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

