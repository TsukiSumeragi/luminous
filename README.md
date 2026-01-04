## 🚀 Tech Stack

* PHP ≥ 8.1
* Laravel 10+
* Node.js ≥ 18
* React 18
* Vite 5
* Tailwind CSS
* Laravel Vite Plugin

## 🛠️ Setup Lokal (Development)

### 1️⃣ Clone Repository

```bash
git clone https://github.com/TsukiSumeragi/luminous.git
cd luminous
```

---

### 2️⃣ Install Dependency (WAJIB pakai legacy)

```bash
npm install --legacy-peer-deps
```

### 3️⃣ Install PHP Dependency

```bash
composer install
```

---

### 4️⃣ Environment

```bash
cp .env.example .env
php artisan key:generate
```

---

### 5️⃣ Jalankan Development Server

**Terminal 1 (Laravel):**

```bash
php artisan serve
```

**Terminal 2 (Vite):**

```bash
npm run dev
```

Akses di browser:

```
http://127.0.0.1:8000
```

---

## 🌍 Deployment ke Server (Production)

### 📌 Lokasi Server

```txt
/var/www/luminousstone.com
```

---

### 1️⃣ Upload File (via FileZilla)

Upload **SELURUH ISI PROJECT** ke:

```txt
/var/www/luminousstone.com
```

❌ **JANGAN upload folder `node_modules`**

---

### 2️⃣ Masuk ke Server

```bash
ssh user@72.8.xxx.xxx
cd /var/www/luminousstone.com
```

---

### 3️⃣ Install Dependency Server

```bash
composer install --no-dev --optimize-autoloader
npm install --legacy-peer-deps
npm run build
```

---

### 4️⃣ Laravel Production Setup

```bash
cp .env.example .env
php artisan key:generate
php artisan optimize
php artisan storage:link
```

---

### 5️⃣ Permission (WAJIB)

```bash
chown -R www-data:www-data /var/www/luminousstone.com
chmod -R 775 storage bootstrap/cache
```

---

### 6️⃣ Web Server Configuration

* **Document Root** arahkan ke:

```txt
/var/www/luminousstone.com/public
```

---

## ✅ Hasil Akhir

Website dapat diakses melalui:

```txt
http://72.8.xxx.xxx
atau
https://luminousstone.com
```

---

## 👨‍💻 Catatan Developer

* Routing frontend ditangani **sepenuhnya oleh React**
* Laravel berfungsi sebagai **container & backend**
* Tidak menggunakan Inertia
* Build frontend dilakukan via `npm run build`

---

© Luminous Stone

---

## 🖥️ CMD SERVER 
```bash
cd /var/www/luminousstone.com

composer install --no-dev --optimize-autoloader
npm install --legacy-peer-deps
npm run build

php artisan key:generate
php artisan optimize

chown -R www-data:www-data /var/www/luminousstone.com
chmod -R 775 storage bootstrap/cache
```

Buka:

```
http://72.8.xxx.xxx
```
