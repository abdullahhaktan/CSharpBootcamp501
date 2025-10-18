# Online Ticari Otomasyon Sistemi

[TR]

**ASP.NET MVC ile Geliştirilmiş Online Ticari Otomasyon Sistemi**

[![C#](https://img.shields.io/badge/Language-C%23-blue.svg)](https://docs.microsoft.com/en-us/dotnet/csharp/)
[![ASP.NET MVC](https://img.shields.io/badge/Framework-ASP.NET%20MVC-brightgreen.svg)](https://dotnet.microsoft.com/apps/aspnet/mvc)
[![Entity Framework](https://img.shields.io/badge/ORM-Entity%20Framework-blueviolet.svg)](https://docs.microsoft.com/en-us/ef/)
[![GitHub repo size](https://img.shields.io/github/repo-size/abdullahhaktan/OnlineTicariOtomasyonSistemi)](https://github.com/abdullahhaktan/OnlineTicariOtomasyonSistemi)

---

## 💻 Proje Hakkında

Bu proje, **ASP.NET MVC** mimarisi kullanılarak geliştirilmiş, web tabanlı kapsamlı bir **Online Ticari Otomasyon Sistemi**'dir. Sistem, ticari süreçlerin yönetimi, stok takibi, satış raporlama ve kullanıcı etkileşimi gibi temel işlevleri modern bir arayüzle sunar.

### ⚙️ Teknik Altyapı

* **Mimari:** ASP.NET MVC
* **Programlama Dili:** C#
* **Veri Erişim:** Entity Framework (`Code First` Yaklaşımı ile oluşturulmuştur.)
* **Sorgulama:** LINQ Sorguları kullanılarak Entity Framework ile gerçekleştirilmiştir.
* **Arayüz:** AdminLTE Template kullanılarak modern ve duyarlı bir kullanıcı deneyimi sağlanmıştır.
* **Modülerlik:** "Hızlı Bakış" tabloları gibi önemli bileşenler **Partial View** yapısıyla modüler ve yeniden kullanılabilir şekilde tasarlanmıştır.
* **Grafikler:** ASP.NET'in sunduğu yerleşik grafik yapıları kullanılarak dinamik ve görsel raporlama sağlanmıştır (Örn: Ürün - Stok Grafiği).

---

## ✨ Ana Özellikler

Sistem, yetki seviyelerine göre farklı işlevler sunar:

### 1. Kullanıcı Girişi ve Yetkilendirme
Sisteme iki ana yetki seviyesinde giriş yapılabilir:
* **Admin Girişi:** Tüm yönetimsel ve raporlama işlevlerine erişim sağlar.
* **Cari Girişi (Müşteri/Tedarikçi):** Kendi siparişlerini, kargo takibini ve profil bilgilerini yönetebilir.

### 2. Yönetim ve Raporlama (Admin Paneli)
* **Hızlı Bakış Tabloları:** Kategori, Müşteri/Şehir ve Departman/Personel bazlı anlık özet verileri gösteren Partial View'ler.
* **Dinamik Stok/Satış Grafikleri:** Ürün bazında stok durumunu gösteren pasta grafik gibi görsel raporlama araçları.
* **CRUD İşlemleri:** Ürün, kategori, cari, personel ve giderler üzerinde Silme (`Emin misiniz?` onayı ile), Güncelleme ve Satış yapma.

### 3. Cari Hesap İşlemleri (Cari Paneli)
* **Profil Yönetimi:** Cari, kendi ad-soyad, e-posta, toplam satış ve toplam ürün sayısı gibi bilgilerini görüntüleyebilir.
* **Sipariş ve Kargo Takibi:** Mevcut siparişlerini listeleyebilir ve kargolarının durumunu takip edebilir.
* **Duyurular:** Sistemden gelen önemli duyuruları kontrol edebilir.
* **Mesajlaşma:** Sistemdeki diğer carilerle mesaj gönderebilme şansı vardır.

---

## 🚀 Nasıl Çalıştırılır?

1.  **Projeyi Klonlama:**
    ```bash
    git clone [https://github.com/abdullahhaktan/OnlineTicariOtomasyonSistemi](https://github.com/abdullahhaktan/OnlineTicariOtomasyonSistemi)
    cd OnlineTicariOtomasyonSistemi
    ```

2.  **Projeyi Açma:**
    * Visual Studio kullanarak kök dizindeki `.sln` (Solution) dosyasını açın.

3.  **Veritabanı Ayarları:**
    * Entity Framework Code First yaklaşımı kullanıldığı için, bağlantı dizgesini (`Connection String`) kontrol edin.
    * Veritabanı sunucunuzu (`web.config` veya ilgili yapılandırma dosyasında) doğru şekilde ayarlayın ve migrasyonları uygulayarak tabloların oluşmasını sağlayın.

4.  **Çözümü Derleme ve Çalıştırma:**
    * Visual Studio'da çözümü derleyin (`Build Solution` veya F6).
    * Uygulamayı çalıştırın (**F5**). Uygulama, öncelikle yetki seçme ekranı (**GİRİŞ FORMU**) ile başlayacaktır.

---
---

[EN]

# Online Commercial Automation System

**Online Commercial Automation System Developed with ASP.NET MVC**

---

## 💻 About the Project

This project is a comprehensive **Online Commercial Automation System** developed using the **ASP.NET MVC** architecture. The system provides essential functions such as managing commercial processes, inventory tracking, sales reporting, and user interaction through a modern interface.

### ⚙️ Technical Stack

* **Architecture:** ASP.NET MVC
* **Language:** C#
* **Data Access:** Entity Framework (using the `Code First` approach)
* **Querying:** Implemented with LINQ Queries via Entity Framework.
* **UI:** AdminLTE Template is used for a modern and responsive user experience.
* **Modularity:** Key components like the "Quick Look" tables are designed as **Partial Views** for a modular and reusable structure.
* **Charts:** Dynamic and visual reporting is provided using ASP.NET's built-in charting structures (e.g., Product - Stock Chart).

---

## ✨ Core Features

The system offers different functionalities based on authorization levels:

### 1. User Login and Authorization
The system supports two main authorization levels:
* **Admin Login:** Provides access to all administrative and reporting functions.
* **Current Account (Customer/Supplier) Login:** Can manage their own orders, cargo tracking, and profile information.

### 2. Administration and Reporting (Admin Panel)
* **Quick Look Tables:** Partial Views displaying instant summary data based on Category, Customer/City, and Department/Personnel.
* **Dynamic Stock/Sales Charts:** Visual reporting tools like pie charts showing product-based stock status.
* **CRUD Operations:** Create, Read, Update, and Delete operations on products, categories, current accounts, personnel, and expenses (with a "Are you sure?" confirmation for deletion).

### 3. Current Account Operations (Client Panel)
* **Profile Management:** Current accounts can view their personal information, total sales, and total product count.
* **Order and Cargo Tracking:** They can list their existing orders and track the status of their shipments.
* **Announcements:** Can check important announcements from the system.
* **Messaging:** Users have the ability to send messages to other current accounts within the system.

---

## 🚀 How to Run

1.  **Cloning the Project:**
    ```bash
    git clone [https://github.com/abdullahhaktan/OnlineTicariOtomasyonSistemi](https://github.com/abdullahhaktan/OnlineTicariOtomasyonSistemi)
    cd OnlineTicariOtomasyonSistemi
    ```

2.  **Opening the Project:**
    * Open the root directory's **`.sln`** (Solution) file using Visual Studio.

3.  **Database Configuration:**
    * Check the `Connection String`.
    * Configure your database server and apply migrations to create the tables.

4.  **Building and Running:**
    * Build the solution in Visual Studio.
    * Start the application (**F5**).

---

## 📸 Ekran Görüntüleri

<img width="1233" height="568" alt="Ekran görüntüsü 2025-10-18 192025" src="https://github.com/user-attachments/assets/404b235f-8d79-4e32-a584-5c3e2c474b94" />

---

<img width="1240" height="586" alt="Ekran görüntüsü 2025-10-18 192040" src="https://github.com/user-attachments/assets/37487135-0917-48ba-9381-5aeca30be117" />

---

<img width="1237" height="589" alt="Ekran görüntüsü 2025-10-18 192053" src="https://github.com/user-attachments/assets/667c8d4f-4c7a-4f89-9d79-191fae7ad7fb" />

---

<img width="1240" height="591" alt="Ekran görüntüsü 2025-10-18 192107" src="https://github.com/user-attachments/assets/7754c50e-5497-427f-b370-e86a2757902e" />

---

<img width="1235" height="588" alt="Ekran görüntüsü 2025-10-18 192121" src="https://github.com/user-attachments/assets/835aa912-545b-43da-9b3a-e7a8b5b43a00" />
