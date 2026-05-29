# 📊 Databank - Integrated ERP System (PT Intisel)

![Project Status](https://img.shields.io/badge/Status-Active%20Development-boldgreen)
![Tech Stack](https://img.shields.io/badge/Stack-React%20%7C%20NestJS%20%7C%20PostgreSQL-blue)
![Architecture](https://img.shields.io/badge/Architecture-Modular%20Monolith-orange)

**Databank** adalah sistem *Enterprise Resource Planning* (ERP) internal yang dibangun dari nol (*from scratch*) untuk **PT Intisel Prodaktifakom**. Sistem ini dirancang untuk mendigitalisasi proses bisnis manual, meningkatkan efisiensi operasional sebesar **35%**, dan menyediakan manajemen data yang terpusat serta aman.

---

## 📈 Impact & Business Value
* **Efficiency Boost:** Berhasil mengotomatisasi alur kerja manual (PO, Absensi, Payroll), memangkas waktu operasional hingga ~35%.
* **Data Integrity:** Menghilangkan redundansi data melalui sistem database relasional yang terstruktur.
* **Scalability:** Arsitektur modular memungkinkan penambahan modul bisnis baru tanpa mengganggu fungsi yang sudah ada.

## 🚀 Fitur Utama & Modul

### 🔐 Security & Dynamic RBAC
* **Granular Permissions:** Mengimplementasikan *Dynamic Role-Based Access Control* (RBAC) yang memungkinkan admin mengatur izin akses per fitur (misal: `USERS`, `ROLES`, `ADD_DATABANK`) secara real-time.
* **Tiered Access:** Pemisahan akses antara pengguna umum dan manajemen (Role: High) untuk fitur sensitif seperti `Manage Attendance`.

### 📦 PO & Data Management
* **Purchase Order Lifecycle:** Manajemen siklus hidup PO mulai dari pengajuan, persetujuan, hingga invoicing.
* **Databank Suite:** Modul CRUD terintegrasi untuk manajemen data inti perusahaan.

### 🕒 Core Management Suite
* **Attendance System:** Pelacakan kehadiran dengan pemisahan antarmuka pengisian (*Fill*) dan pengelolaan (*Manage*).
* **Automated Payroll:** Sistem penggajian yang terintegrasi langsung dengan data kehadiran dan database internal.
* **Operational Dashboard:** Dasbor real-time yang menyatukan metrik dari procurement, absensi, dan payroll.

### 🎨 Premium UI/UX
* **Dynamic Styling:** Antarmuka responsif dengan dukungan penuh menggunakan Native CSS.
* **Performance:** Menggunakan *Code Splitting* dan *Lazy Loading* (React Suspense) untuk memastikan aplikasi tetap ringan dan cepat saat diakses.

## 🛠️ Analisis Tech Stack

### Backend (databank-backend)
* **Framework:** NestJS (Node.js) untuk arsitektur server-side yang skalabel.
* **ORM:** Prisma ORM dengan pendekatan **Modular Schema** (Base, User, Role, Permission, Attendance, Databank) untuk skalabilitas skema database.
* **Database:** PostgreSQL sebagai database relasional utama.
* **Security:** Bcrypt untuk enkripsi password dan Passport-JWT untuk manajemen token sesi.

### Frontend (databank-frontend)
* **Library:** React.js (Vite).
* **State & Routing:** React Router DOM v7 dengan sistem *Protected Routes* yang berbasis permission.
* **Icons & Animation:** React Icons & Motion untuk elemen UI yang interaktif.
* **API Client:** Axios dengan konfigurasi interceptor untuk komunikasi backend yang efisien.

## 📂 Struktur Proyek
Proyek ini dikelola menggunakan **PNPM Workspace** untuk efisiensi manajemen dependensi di lingkungan monorepo.

```bash
# Setup & Instalasi
$ pnpm install

# Menjalankan Backend (Development)
$ cd databank-backend && pnpm run start:dev

# Menjalankan Frontend (Development)
$ cd databank-frontend && pnpm run dev
