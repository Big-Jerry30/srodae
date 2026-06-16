# Church of Pentecost - New Juaben District
## Website & Church Management System

### Overview
A comprehensive website and church management system for the Church of Pentecost, New Juaben District managing 7 local assemblies with role-based access control.

---

## 🚀 Setup Instructions

### Prerequisites
- XAMPP (with Apache and MySQL)
- Modern web browser (Chrome, Firefox, Edge)
- Basic knowledge of web hosting (for production deployment)

### Installation Steps

#### 1. Install XAMPP
- Download and install XAMPP from https://www.apachefriends.org/
- Start Apache and MySQL from the XAMPP Control Panel

#### 2. Copy Files
- Copy the entire `new_juaben_cms` folder to `C:\xampp\htdocs\`
- Final path should be: `C:\xampp\htdocs\new_juaben_cms\`

#### 3. Setup Database
- Open your web browser
- Navigate to: `http://localhost/new_juaben_cms/database/setup_db.php`
- This will automatically create the database, tables, and sample data
- **IMPORTANT**: Save the login credentials displayed after setup

#### 4. Access the Website
- **Public Website**: `http://localhost/new_juaben_cms/index.html`
- **Admin Login**: `http://localhost/new_juaben_cms/login.html`

---

## 🔑 Default Login Credentials

### District Administrator
- **Username**: `district_admin`
- **Password**: `district123`
- **Access**: Full access to all assemblies and district-wide data

### Local Assembly Admins
Format: `[assembly_code]_admin` / `[assembly_code]123`

Examples:
- **Bethel Assembly**: `bethel_admin` / `bethel123`
- **Srodae**: `srodae_admin` / `srodae123`
- **Holy Ghost**: `hga_admin` / `hga123`
- **Ahenbronum**: `ahen_admin` / `ahen123`
- **Beautiful Gate**: `bgate_admin` / `bgate123`
- **Emmanuel**: `emman_admin` / `emman123`
- **Mount Zion**: `mtzion_admin` / `mtzion123`

> **Security Note**: Change all passwords after first login in production!

---

## 📁 Project Structure

```
new_juaben_cms/
├── index.html                 # Homepage
├── about.html                 # About page
├── contact.html               # Contact page
├── login.html                 # Admin login
├── district-dashboard.html    # District admin portal
├── local-dashboard.html       # Local assembly portal
│
├── css/
│   ├── main.css              # Main stylesheet
│   └── dashboard.css         # Dashboard styles
│
├── js/
│   ├── main.js               # Public site JavaScript
│   └── dashboard.js          # Dashboard JavaScript
│
├── api/                       # Backend PHP APIs
│   ├── config.php            # Database configuration
│   ├── auth.php              # Authentication
│   ├── members.php           # Member management
│   └── assemblies.php        # Assembly list
│
├── database/
│   └── setup_db.php          # Database setup script
│
├── images/                    # Static images
└── uploads/                   # User-uploaded files
```

---

## ✨ Features

### Public Website
- ✅ Homepage with district information
- ✅ About page with mission, vision, and leadership
- ✅ Contact page with all assembly locations
- ✅ Modern, responsive design
- ✅ Mobile-friendly navigation

### District Admin Dashboard
- ✅ View all members across 7 assemblies
- ✅ Add, edit, and delete members
- ✅ Filter by assembly
- ✅ Search functionality
- ✅ Member statistics and reports
- ✅ Complete data access across district

### Local Assembly Dashboard
- ✅ View only local assembly members
- ✅ Add, edit, and delete local members
- ✅ Local statistics
- ✅ Data isolation (cannot access other assemblies)
- ✅ Search and filter local members

### Security Features
- ✅ Password hashing (bcrypt)
- ✅ Session-based authentication
- ✅ Role-based access control
- ✅ Data isolation between assemblies
- ✅ SQL injection prevention

---

## 🎯 Key Functionalities

### 1. Member Management
- Full CRUD operations (Create, Read, Update, Delete)
- Member profiles with:
  - Personal information (name, gender, DOB)
  - Contact details (phone, email, address)
  - Church information (baptism status, membership type)
  - Ministry assignments

### 2. Multi-Branch Architecture
- **1 District Office** with full oversight
- **7 Local Assemblies** with isolated data access
- Each assembly manages only their members
- District can view and manage all assemblies

### 3. Role-Based Access Control
- **District Admin**: Access to all assemblies and members
- **Local Admin**: Access only to their own assembly
- Automatic role-based redirects after login
- Session validation on all requests

---

## 🗄️ Database Schema

### Tables Created:
1. **local_assemblies** - 7 local assemblies information
2. **users** - Admin user accounts (district + local)
3. **members** - Church membership records
4. **ministries** - 9 ministry definitions
5. **ministry_members** - Member-ministry assignments
6. **inventory** - Church assets and equipment
7. **financial_records** - Offerings and expenses
8. **events** - Event scheduling
9. **event_attendance** - Event participation
10. **sermons** - Sermon recordings
11. **news** - News and announcements
12. **reports** - Custom reports

---

## 🔧 Configuration

### Database Settings
Edit `api/config.php` to change database credentials:
```php
define('DB_HOST', 'localhost');
define('DB_USER', 'root');
define('DB_PASS', '');
define('DB_NAME', 'cop_new_juaben');
```

### File Upload Settings
- Maximum file size: 10MB
- Allowed image types: JPEG, PNG, GIF, WebP
- Allowed document types: PDF, DOC, DOCX
- Upload directory: `uploads/`

---

## 📱 Browser Compatibility
- ✅ Chrome/Edge (Latest)
- ✅ Firefox (Latest)
- ✅ Safari (Latest)
- ✅ Mobile browsers (iOS/Android)

---

## 🚨 Troubleshooting

### Database Connection Error
1. Ensure XAMPP MySQL is running
2. Check database credentials in `api/config.php`
3. Verify database was created by running `setup_db.php`

### Login Not Working
1. Clear browser cache and cookies
2. Ensure database setup completed successfully
3. Verify credentials are correct
4. Check browser console for errors

### Members Not Loading
1. Check browser console for JavaScript errors
2. Verify API files are in correct location
3. Ensure user is properly logged in
4. Check database has member records

---

## 🎨 Customization

### Changing Colors
Edit `css/main.css` variables:
```css
:root {
    --primary-navy: #1a2c5b;
    --primary-gold: #d4af37;
    --accent-blue: #2563eb;
    /* Modify as needed */
}
```

### Adding New Pages
1. Create HTML file in root directory
2. Include standard header and footer
3. Link to `css/main.css` and `js/main.js`

---

## 📞 Support

For technical support or questions:
- Email: admin@copnewjuaben.org
- Phone: +233 24 412 3456

---

## 📜 License

Copyright © 2026 Church of Pentecost - New Juaben District. All rights reserved.

---

## 🎯 Coming Soon

Future features under development:
- Ministry assignment management
- Inventory tracking
- Financial reporting
- Event management
- Advanced analytics and reports
- SMS/Email notifications
- File upload for member photos
- Bulk member import (Excel/CSV)

---

## ⚡ Quick Start Guide

1. **Start XAMPP** → Start Apache and MySQL
2. **Setup Database** → Visit `http://localhost/new_juaben_cms/database/setup_db.php`
3. **Login** → Use `district_admin` / `district123`
4. **Add Members** → Go to Members section, click "+ Add Member"
5. **Test Local Access** → Login as `bethel_admin` / `bethel123` to see data isolation

---

**Built with ❤️ for the Church of Pentecost - New Juaben District**
