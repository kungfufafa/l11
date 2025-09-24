# Laravel Application

Aplikasi web modern yang dibangun dengan Laravel 11, dilengkapi dengan tools dan teknologi terkini untuk pengembangan yang efisien.

## Tech Stack

- **Backend**: Laravel 11.31 (PHP 8.2+)
- **Frontend**: Vite + TailwindCSS
- **Database**: SQLite (default), MySQL/PostgreSQL support
- **Queue**: Laravel Horizon
- **Performance**: Laravel Octane
- **Testing**: Pest PHP + Browser Testing
- **Monitoring**: Laravel Telescope
- **Code Quality**: Laravel Pint, Enlightn

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
- Laravel development server
- Queue worker
- Log monitoring (Pail)
- Vite development server

### Manual Commands

**Backend Development:**
```bash
php artisan serve
```

**Frontend Development:**
```bash
npm run dev
```

**Queue Worker:**
```bash
php artisan queue:work
```

**Monitoring Logs:**
```bash
php artisan pail
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

- ⚡ **High Performance**: Laravel Octane untuk performa maksimal
- 🔄 **Queue Management**: Laravel Horizon untuk background jobs
- 🎨 **Modern UI**: TailwindCSS untuk styling
- 🧪 **Testing**: Pest PHP dengan browser testing
- 📊 **Monitoring**: Laravel Telescope untuk debugging
- 🔍 **Code Analysis**: Enlightn untuk security & performance insights
- 📝 **Log Monitoring**: Laravel Pail untuk real-time logs

## Environment Variables

Konfigurasi utama di `.env`:

```env
APP_NAME=Laravel
APP_ENV=local
APP_DEBUG=true
APP_URL=http://localhost

DB_CONNECTION=sqlite
QUEUE_CONNECTION=database
CACHE_STORE=database
```

Lihat `.env.example` untuk konfigurasi lengkap.

## License

Aplikasi ini menggunakan lisensi [MIT](https://opensource.org/licenses/MIT).
