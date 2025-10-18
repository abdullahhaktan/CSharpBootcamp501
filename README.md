# CSharp-WinForms-Dapper-CRUD

[TR]

**C# Windows Form ve Dapper Kütüphanesi ile Temel CRUD (Ekleme/Listeleme/Silme/Güncelleme) Uygulaması**

[![C#](https://img.shields.io/badge/Language-C%23-blue.svg)](https://docs.microsoft.com/en-us/dotnet/csharp/)
[![Windows Forms](https://img.shields.io/badge/Platform-Windows%20Forms-blue.svg)](https://docs.microsoft.com/en-us/dotnet/desktop/winforms/)
[![Dapper](https://img.shields.io/badge/ORM-Dapper-red.svg)](https://dapper-tutorial.net/)
[![SQL Server](https://img.shields.io/badge/Database-SQL%20Server-lightgrey.svg)](https://www.microsoft.com/en-us/sql-server)

---

## 💻 Proje Hakkında

Bu depo, **C# Windows Form (WinForms)** kullanılarak geliştirilmiş ve veri erişimi için hafif bir ORM olan **Dapper** kütüphanesinin uygulandığı basit bir **Ürün/Stok Yönetimi** (kodda "Kitap" olarak da geçiyor) uygulamasıdır. Proje, veritabanı işlemlerinde saf SQL sorgularını Dapper ile hızlıca çalıştırma yeteneğini göstermektedir. İşlemler **asenkron** (`async/await`) olarak yönetilir.

### ⚙️ Teknik Altyapı

* **Platform:** C# Windows Forms
* **Veri Erişim Kütüphanesi:** Dapper ORM
* **Veritabanı:** SQL Server
* **Bağlantı Dizesi:** `Server=DESKTOP-R7AR1ND;initial Catalog=EgitimKampi501Db;integrated security=true`
* **Veri Transferi:** `ResultProductDto` gibi **DTO (Data Transfer Object)** yapıları kullanılmıştır.

---

## ✨ Ana Özellikler (CRUD ve İstatistikler)

Uygulama, `TblProduct` tablosu üzerinde aşağıdaki temel CRUD (Create, Read, Update, Delete) işlemlerini ve ek istatistikleri sunar:

| İşlev | Açıklama | SQL Sorgu Tipi |
| :--- | :--- | :--- |
| **Listeleme** (`btnList_Click`) | Tüm ürünleri `TblProduct` tablosundan çekerek `DataGridView`'de gösterir. | `SELECT` |
| **Ekleme** (`btnAdd_Click`) | Yeni ürün kaydını (Ad, Stok, Fiyat, Kategori) veritabanına ekler. | `INSERT` |
| **Silme** (`btnDelete_Click`) | Belirtilen `ProductId` değerine sahip ürünü siler. | `DELETE` |
| **Güncelleme** (`btnUpdate_Click`) | Var olan bir ürünün bilgilerini `ProductId`'ye göre günceller. | `UPDATE` |

### 📊 İstatistikler (Form Yüklendiğinde)

Uygulama açıldığında (Form1_Load), aşağıdaki istatistikleri Dapper ve SQL sorguları kullanarak hesaplar:

* **Toplam Ürün Sayısı:** `lblTotalProductCount`
* **En Yüksek Fiyatlı Ürün Adı:** `lblMaxPriceProductName`
* **Farklı Kategori Sayısı:** `lblDistinctCategoryCount`

---

## 🚀 Nasıl Çalıştırılır?

1.  **Projeyi Klonlama:**
    ```bash
    git clone [repo-adresiniz]
    cd CSharpEgitimKampi501
    ```

2.  **Veritabanı Kurulumu:**
    * Bir SQL Server örneği üzerinde `EgitimKampi501Db` adında bir veritabanı oluşturun.
    * Bu veritabanı içinde `TblProduct` tablosunu gerekli sütunlarla (`ProductId`, `ProductName`, `ProductStock`, `ProductPrice`, `ProductCategory`) oluşturun.

3.  **Bağlantı Dizesini Güncelleme:**
    * `Form1.cs` dosyasındaki bağlantı dizesini (`SqlConnection` tanımı) kendi SQL Server sunucu adınıza göre güncelleyin:
      ```csharp
      SqlConnection connection = new SqlConnection("Server=SİZİN-SUNUCU-ADINIZ;initial Catalog=EgitimKampi501Db;integrated security=true");
      ```

4.  **Çözümü Derleme ve Çalıştırma:**
    * Visual Studio'da çözümü açın.
    * Çözümü derleyin (Build Solution).
    * Uygulamayı çalıştırın (**F5**).
