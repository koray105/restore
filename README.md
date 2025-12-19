# ReStore - E-Commerce Platform

[Türkçe okumak için buraya tıklayın (README.tr.md)](./README.tr.md)

A modern, full-stack e-commerce application built with **Next.js 16**, **Supabase**, and **Tailwind CSS**. Designed with a premium feel and focus on user experience.

---

## 🚀 Features

- **Storefront**: Browse products with category filtering and dynamic search.
- **Authentication**: Secure user registration, login, and password management via Supabase Auth.
- **Product Management**: Users can create, edit, and delete their own listings with optimized image uploads (WebP).
- **Admin Panel**: A comprehensive dashboard for admins to manage:
  - Product Moderation (Approve/Reject)
  - User Management (Ban/Unban)
  - Category Management
  - Report Handling (Reviewing reported listings)
- **Messaging System**: Real-time chat between buyers and sellers.
- **Favorites**: Performance-optimized "save to favorites" system with live count updates.
- **Notifications**: 
  - Real-time in-app notifications.
  - Browser Push Notifications (Service Workers) for messages and likes.
- **Settings**: Comprehensive user profile management, notification toggles, and account deletion.

## 🛠 Technologies

- **Frontend**: [Next.js 16](https://nextjs.org/) (App Router), [Tailwind CSS](https://tailwindcss.com/)
- **Backend/Database**: [Supabase](https://supabase.com/) (PostgreSQL, Auth, Storage, Edge Functions, Realtime)
- **Icons**: [Lucide React](https://lucide.dev/)
- **Image Optimization**: [Browser Image Compression](https://www.npmjs.com/package/browser-image-compression) (WebP conversion)
- **Notifications**: Web Push API

---

## 📦 Getting Started

### 1. Prerequisites

- **Node.js**: v18 or later
- **Supabase Account**: A project set up on Supabase.

### 2. Environment Setup

1. Clone the repository.
2. Copy `.env.example` to `.env.local`:
   ```bash
   cp .env.example .env.local
   ```
3. Update `.env.local` with your credentials:
   - `NEXT_PUBLIC_SUPABASE_URL`: Your Supabase Project URL.
   - `NEXT_PUBLIC_SUPABASE_ANON_KEY`: Your Anonymous key.
   - `NEXT_PUBLIC_VAPID_PUBLIC_KEY`: For Push Notifications.

### 3. Database & Storage Setup

1. **Run Migrations**: Use the provided SQL scripts in `supabase/migrations` or run `supabase_admin_migration.sql` in your Supabase SQL Editor to set up tables (products, profiles, reports, notifications, etc.) and RLS policies.
2. **Storage**: Create a bucket named `product-images` in Supabase Storage and set it to **Public**.
3. **Admin Privileges**: To access the Admin Panel, sign up as a user and manually set the `is_admin` column to `true` in the `profiles` table for your user ID.

### 4. Installation & Development

```bash
npm install
npm run dev
```

Visit [http://localhost:3000](http://localhost:3000) to view the app locally.

---

## 🎨 Design System

The app follows a modern, Airbnb-inspired design system with:
- **Responsive Layouts** (Mobile-first design)
- **Dark/Light Mode** support
- **Glassmorphism** effects and subtle micro-animations
- **Custom UI Components** for a premium feel

---

## 🛡 License

This project is licensed under the MIT License - feel free to use it for your own projects!

# ReStore - E-Ticaret Platformu

[Click here for English version (README.md)](./README.md)

**Next.js 16**, **Supabase** ve **Tailwind CSS** ile geliştirilmiş, modern ve premium tasarıma sahip tam donanımlı bir e-ticaret uygulamasıdır. Kullanıcı deneyimine odaklanarak Airbnb tarzı şık bir arayüz ile oluşturulmuştur.

---

## 🚀 Özellikler

- **Ürün Vitrini**: Kategori filtreleme ve dinamik arama ile ürünleri inceleme.
- **Kimlik Doğrulama**: Supabase Auth ile güvenli kayıt olma, giriş yapma ve şifre yönetimi.
- **Ürün Yönetimi**: Kullanıcıların kendi ilanlarını oluşturması, düzenlemesi ve silmesi (WebP formatında optimize edilmiş görsel yükleme ile).
- **Yönetici (Admin) Paneli**: Kapsamlı yönetim özellikleri:
  - İlan Moderasyonu (Onaylama/Reddetme)
  - Kullanıcı Yönetimi (Engelleme/Engel Kaldırma)
  - Kategori Yönetimi
  - Rapor Sistemi (Şikayet edilen ilanların incelenmesi)
- **Mesajlaşma**: Alıcılar ve satıcılar arasında gerçek zamanlı sohbet.
- **Favoriler**: Performans odaklı favorilere ekleme sistemi ve canlı sayaç güncellemeleri.
- **Bildirimler**: 
  - Uygulama içi gerçek zamanlı bildirimler.
  - Mesaj ve beğeniler için Tarayıcı Anlık Bildirimleri (Service Workers).
- **Ayarlar**: Profil yönetimi, bildirim tercihleri ve hesap silme özellikleri.

## 🛠 Kullanılan Teknolojiler

- **Frontend**: [Next.js 16](https://nextjs.org/) (App Router), [Tailwind CSS](https://tailwindcss.com/)
- **Backend/Veritabanı**: [Supabase](https://supabase.com/) (PostgreSQL, Auth, Storage, Edge Functions, Realtime)
- **İkonlar**: [Lucide React](https://lucide.dev/)
- **Görsel Optimizasyon**: [Browser Image Compression](https://www.npmjs.com/package/browser-image-compression) (WebP dönüştürme)
- **Bildirimler**: Web Push API

---

## 📦 Kurulum

### 1. Ön Koşullar

- **Node.js**: v18 veya üzeri
- **Supabase Hesabı**: Supabase üzerinde oluşturulmuş bir proje.

### 2. Ortam Değişkenleri (Environment Variables)

1. Depoyu (repository) klonlayın.
2. `.env.example` dosyasını `.env.local` olarak kopyalayın:
   ```bash
   cp .env.example .env.local
   ```
3. `.env.local` dosyasını kendi Supabase bilgilerinizle güncelleyin:
   - `NEXT_PUBLIC_SUPABASE_URL`: Supabase Proje URL'niz.
   - `NEXT_PUBLIC_SUPABASE_ANON_KEY`: Anonim anahtarınız.
   - `NEXT_PUBLIC_VAPID_PUBLIC_KEY`: Push Bildirimleri için public key.

### 3. Veritabanı ve Depolama Kurulumu

1. **Migrasyonları Çalıştırın**: `supabase/migrations` klasöründeki veya `supabase_admin_migration.sql` dosyasındaki SQL komutlarını Supabase SQL Editor'da çalıştırarak tabloları ve RLS politikalarını oluşturun.
2. **Depolama (Storage)**: Supabase üzerinde `product-images` adında bir bucket oluşturun ve erişimini **Public** (Açık) yapın.
3. **Yönetici Yetkisi**: Admin paneline erişmek için, kayıt olduktan sonra Supabase Table Editor üzerinden `profiles` tablosuna gidin ve kendi kullanıcınızın `is_admin` değerini `true` yapın.

### 4. Yerel Çalıştırma

```bash
npm install
npm run dev
```

Uygulamaya [http://localhost:3000](http://localhost:3000) adresinden erişebilirsiniz.

---

## 🎨 Tasarım Sistemi

Uygulama, modern ve premium bir tasarım çizgisi izler:
- **Duyarlı (Responsive)**: Mobil öncelikli tasarım.
- **Koyu/Açık Tema**: Gece ve gündüz modu desteği.
- **Mikro Etkileşimler**: Akıcı animasyonlar ve şık geçişler.
- **Özel Bileşenler**: Airbnb tarzı temiz ve profesyonel arayüz bileşenleri.

---

## 🛡 Lisans

Bu proje MIT Lisansı ile lisanslanmıştır - kendi projelerinizde dilediğiniz gibi kullanabilirsiniz!

