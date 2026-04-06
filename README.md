# WordPress Docker Compose Setup

## 📌 Deskripsi

Project ini menggunakan Docker Compose untuk menjalankan WordPress CMS dengan MySQL sebagai database dan Redis sebagai object cache.

---

## 🚀 Services

* WordPress (http://localhost:8000)
* MySQL (Database)
* Redis (Cache)

---

## ⚙️ Cara Menjalankan

1. Jalankan Docker:
   docker-compose up -d

2. Buka browser:
   http://localhost:8000

---

## ✅ Hasil Testing

* WordPress berhasil diakses
* Bisa membuat post (MySQL bekerja)
* Redis berjalan dengan baik
* Data tetap ada setelah container restart

---

## 📸 Screenshot

### 🔹 WordPress Dashboard

![WordPress Dashboard](WordPress%20Dashboard.png)

### 🔹 Docker Container Running

![Docker Dashboard](Docker%20Dashboard.png)

---

## ❓ Jawaban Pertanyaan

### 1. Kenapa perlu volume untuk MySQL?

Volume digunakan agar data database tidak hilang saat container dihentikan atau dihapus.

---

### 2. Apa fungsi depends_on?

depends_on digunakan untuk mengatur urutan startup container, sehingga WordPress berjalan setelah MySQL.

---

### 3. Bagaimana WordPress connect ke MySQL?

WordPress menggunakan hostname service yaitu "mysql" pada Docker network internal.

---

### 4. Apa keuntungan Redis untuk WordPress?

Redis digunakan untuk caching sehingga:

* Mempercepat loading website
* Mengurangi beban database
* Meningkatkan performa aplikasi

---
