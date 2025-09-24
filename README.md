# Laravel 11 Starter Kit

Aplikasi web modern yang dibangun dengan Laravel 11, dilengkapi dengan tools dan teknologi terkini untuk pengembangan yang efisien dan performa tinggi.

## Tech Stack

- **Backend**: Laravel 11.31 (PHP 8.2+)
- **Frontend**: Vite + TailwindCSS + Laravel Echo
- **Database**: SQLite (default), MySQL/PostgreSQL support
- **Queue**: Laravel Horizon
- **Performance**: Laravel Octane (FrankenPHP)
- **Real-time**: Laravel Reverb (WebSocket)
- **Testing**: Pest PHP + Playwright Browser Testing
- **Monitoring**: Laravel Telescope
- **Code Quality**: Laravel Pint, Enlightn, PHPStan (Larastan)

## Requirements

- PHP 8.2 atau lebih tinggi
- Composer
- Node.js & NPM
- SQLite (atau database lain sesuai konfigurasi)

## Installation

1. Clone repository ini:
```bash
git clone https://github.com/kungfufafa/l11.git
cd l11
```

2. Install dependencies PHP:
```bash
composer install
```

3. Install dependencies JavaScript:
```bash
npm install
```

4. Setup environment:
```bash
cp .env.example .env
php artisan key:generate
```

5. Setup database:
```bash
php artisan migrate
```

## Development

### Quick Start
Jalankan semua services development sekaligus:
```bash
composer run dev
```

Command ini akan menjalankan:
- Laravel development server (http://localhost:8000)
- Queue worker dengan auto-retry
- Log monitoring (Pail) dengan real-time output
- Vite development server dengan hot reload

### Manual Commands

**Backend Development:**
```bash
# Laravel server dengan Octane (FrankenPHP)
php artisan octane:start

# Atau server development biasa
php artisan serve
```

**Frontend Development:**
```bash
npm run dev
```

**Real-time WebSocket:**
```bash
php artisan reverb:start
```

**Queue Management:**
```bash
# Queue worker
php artisan queue:work

# Horizon dashboard (http://localhost:8000/horizon)
php artisan horizon
```

**Monitoring & Debugging:**
```bash
# Real-time logs
php artisan pail

# Telescope dashboard (http://localhost:8000/telescope)
php artisan telescope:install
```

## Testing

Jalankan test suite menggunakan Pest:
```bash
./vendor/bin/pest
```

Atau dengan coverage:
```bash
./vendor/bin/pest --coverage
```

## Code Quality

**Format code dengan Pint:**
```bash
./vendor/bin/pint
```

**Analisis code dengan Enlightn:**
```bash
php artisan enlightn
```

## Production

**Build assets untuk production:**
```bash
npm run build
```

**Optimize aplikasi:**
```bash
php artisan optimize
php artisan config:cache
php artisan route:cache
php artisan view:cache
```

## Features

- ⚡ **High Performance**: Laravel Octane dengan FrankenPHP untuk performa maksimal
- 🔄 **Queue Management**: Laravel Horizon untuk background jobs dengan dashboard
- � ***Real-time Communication**: Laravel Reverb untuk WebSocket connections
- 🎨 **Modern UI**: TailwindCSS dengan Vite untuk fast development
- 🧪 **Comprehensive Testing**: Pest PHP + Playwright untuk unit & browser testing
- � **CAdvanced Monitoring**: Laravel Telescope untuk debugging & profiling
- � ***Code Quality**: Enlightn, PHPStan (Larastan), dan Laravel Pint
- 📝 **Real-time Logs**: Laravel Pail untuk monitoring aplikasi
- 🚀 **Production Ready**: Optimized untuk deployment dengan caching strategies

## Environment Variables

Konfigurasi utama di `.env`:

```env
# Application
APP_NAME=Laravel
APP_ENV=local
APP_DEBUG=true
APP_URL=http://localhost

# Database
DB_CONNECTION=sqlite

# Performance
OCTANE_SERVER=frankenphp
QUEUE_CONNECTION=database
CACHE_STORE=database

# Real-time (Reverb)
REVERB_APP_ID=your_app_id
REVERB_APP_KEY=your_app_key
REVERB_APP_SECRET=your_app_secret
REVERB_HOST="localhost"
REVERB_PORT=8080
```

Lihat `.env.example` untuk konfigurasi lengkap.

## Available Dashboards

Setelah menjalankan aplikasi, Anda dapat mengakses:

- **Application**: http://localhost:8000
- **Horizon (Queue)**: http://localhost:8000/horizon
- **Telescope (Debug)**: http://localhost:8000/telescope
- **Reverb (WebSocket)**: ws://localhost:8080

## Useful Commands

```bash
# Static analysis
./vendor/bin/phpstan analyse

# Security & performance audit
php artisan enlightn

# Clear all caches
php artisan optimize:clear

# Generate IDE helper files
php artisan ide-helper:generate
```

## Project Structure

```
├── app/                    # Application logic
├── config/                 # Configuration files
├── database/              # Migrations, seeders, factories
├── public/                # Web server document root
├── resources/             # Views, CSS, JS, lang files
│   ├── css/              # Stylesheets
│   ├── js/               # JavaScript files
│   └── views/            # Blade templates
├── routes/               # Route definitions
├── storage/              # Logs, cache, sessions
├── tests/                # Test files (Pest)
└── vendor/               # Composer dependencies
```

## Contributing

1. Fork repository ini
2. Buat feature branch (`git checkout -b feature/amazing-feature`)
3. Commit perubahan (`git commit -m 'Add amazing feature'`)
4. Push ke branch (`git push origin feature/amazing-feature`)
5. Buat Pull Request

## Troubleshooting

**Permission Issues:**
```bash
chmod -R 775 storage bootstrap/cache
```

**Clear Cache Issues:**
```bash
php artisan config:clear
php artisan cache:clear
php artisan view:clear
php artisan route:clear
```

**Database Issues:**
```bash
php artisan migrate:fresh --seed
```

## License

Aplikasi ini menggunakan lisensi [MIT](https://opensource.org/licenses/MIT).
