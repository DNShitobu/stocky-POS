# Quick Start Guide (2026 Update)

Below are the exact steps we followed to get Stocky running on a new Windows machine with PHP 8.5:

## 1. Install PHP and Extensions

- Download PHP (8.5+) and extract to a folder (e.g., `C:\Users\yourname\php-8.5.4`).
- Add the PHP folder to your system PATH.
- Enable these extensions in your `php.ini` (remove `;`):
    - extension=openssl

    # Version 5.0 Release Notes

    Highlight Features

    Dynamic Appearance Settings
    - Customize logo, favicon, page title without touching code.

    Database-Powered Translations
    - Add and manage languages directly from the admin panel — no coding required.

    Recurring Invoices
    - Automatically generate and send invoices at scheduled intervals.

    Added More Languages
    - Expanded language support with additional African and global languages for a better multilingual experience.

    Added Termii SMS Gateway
    - Seamless integration with Termii for reliable and regional SMS delivery.

    Added Category Filter in Count Stock
    - Easily filter stock counts by product category for more precise inventory tracking.

    Instant Sale Notifications
    - Automatically send sales details via email or SMS during the transaction process.

    Payment Method Management
    - Easily create and edit payment methods directly from the interface.

    Opening Stock Import
    - Easily import initial product quantities across multiple warehouses using Excel.

    Sales by Category Report
    - Analyze total sales grouped by product categories.

    Sales by Brand Report
    - Analyze total sales grouped by product Brands.

    All Payment Transactions Report
    - View a complete history of customer and supplier payments.

    Sales by Payment Method Report
    - Breakdown of transactions by cash, card, transfer, or other methods.

    SMS Delivery Status Report
    - Log of all outgoing SMS messages and their delivery results.

    Error Logs for Communication Failures
    - Error logs have been added to record any failures during email or SMS sending, helping you track and debug communication issues easily.

    Bug Fixes and Improvements
    - Updated the documentation for better clarity.
    - Resolved several other bugs to improve performance and stability.

Follow these steps to set up and run Stocky on Windows with PHP 8.5:

1. **Install PHP 8.5+**
    - Download PHP and extract to a folder (e.g., `C:\Users\yourname\php-8.5.4`).
    - Add the PHP folder to your system PATH.
    - Enable these extensions in your `php.ini` (remove `;`):
        - extension=openssl
        - extension=pdo_mysql
        - extension=fileinfo
    - Save `php.ini` and restart your terminal.
    - Run `php -m` to confirm extensions are loaded.

2. **Install Composer**
    - Download and install Composer from https://getcomposer.org/
    - In the project directory, run:
        ```sh
        composer install
        ```

3. **Database Setup**
    - Create a new MySQL/MariaDB database (e.g., `stocky`).
    - Edit `.env` and set:
        - DB_DATABASE=your_database_name
        - DB_USERNAME=your_db_user
        - DB_PASSWORD=your_db_password

4. **Generate App Key**
    - Run:
        ```sh
        php artisan key:generate
        ```

5. **Run Migrations**
    - Run:
        ```sh
        php artisan migrate
        ```

6. **Suppress Deprecated Warnings (Optional)**
    - Add this at the top of `public/index.php`:
        ```php
        error_reporting(E_ALL & ~E_DEPRECATED & ~E_USER_DEPRECATED);
        ```

7. **Start the Server**
    - Run:
        ```sh
        php artisan serve
        ```
    - Open [http://127.0.0.1:8000](http://127.0.0.1:8000) in your browser.

---

**This guide reflects the exact steps to get Stocky running as of April 2026.**

# Version 5.0 Release Notes

Highlight Features

Dynamic Appearance Settings

- Customize logo, favicon, page title without touching code.

Database-Powered Translations

- Add and manage languages directly from the admin panel — no coding required.

Recurring Invoices

- Automatically generate and send invoices at scheduled intervals.

Added More Languages

- Expanded language support with additional African and global languages for a better multilingual experience.

Added Termii SMS Gateway

- Seamless integration with Termii for reliable and regional SMS delivery.

Added Category Filter in Count Stock

- Easily filter stock counts by product category for more precise inventory tracking.

Instant Sale Notifications

- Automatically send sales details via email or SMS during the transaction process.

Payment Method Management

- Easily create and edit payment methods directly from the interface.

Opening Stock Import

- Easily import initial product quantities across multiple warehouses using Excel.

Sales by Category Report

- Analyze total sales grouped by product categories.

Sales by Brand Report

- Analyze total sales grouped by product Brands.

All Payment Transactions Report

- View a complete history of customer and supplier payments.

Sales by Payment Method Report

- Breakdown of transactions by cash, card, transfer, or other methods.

SMS Delivery Status Report

- Log of all outgoing SMS messages and their delivery results.

Error Logs for Communication Failures

- Error logs have been added to record any failures during email or SMS sending, helping you track and debug communication issues easily.

Bug Fixes and Improvements

- Updated the documentation for better clarity.
- Resolved several other bugs to improve performance and stability.
