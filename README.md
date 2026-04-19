<h1 align="center" style="color:#B8001F;">☕ TEH TARIK NOMAD ☕</h1>
<p align="center">
  <img width="500" height="500" alt="Nomad Coffee Logo" src="https://github.com/user-attachments/assets/d39c584e-1d94-4598-bff9-bc53c4e82e46" />
</p>

<h2 align="center"> Nama Kelompok: <b>NOMADEN </b></h2>

## 👤 Profil Anggota
| Nayla Camelia Indraswari | Nabila Imtiyaz Agustin | Muhammad Ilyasa’ Izzuddin | Muhammad Reffi Fadillah |
|--------------------------|------------------------|----------------------------|-------------------------|
| **NIM:** 2409116009 <br> **Kelas:** Sistem Informasi A '24 <br> [![Camel](https://img.shields.io/badge/-Camel-FFFFFF?logo=github&logoColor=black)](https://github.com/naylacamelia) | **NIM:** 2409116011 <br> **Kelas:** Sistem Informasi A '24 <br> [![Lala](https://img.shields.io/badge/-Lala-FFFFFF?logo=github&logoColor=black)](https://github.com/nabilaimtiyaz) | **NIM:** 2409116033 <br> **Kelas:** Sistem Informasi A '24 <br> [![Ilyasa'](https://img.shields.io/badge/-Ilyasa'-FFFFFF?logo=github&logoColor=black)](https://github.com/Ilyasa810) | **NIM:** 2409116034 <br> **Kelas:** Sistem Informasi A '24 <br> [![Reffi](https://img.shields.io/badge/-Reffi-FFFFFF?logo=github&logoColor=black)](https://github.com/LuthfiDffa) |

---

## 📚 Daftar Isi
- [📝 Deskripsi Aplikasi](#-deskripsi-aplikasi)
- [⚙️ Fitur Utama](#️-fitur-utama)
- [🌟 Nilai Tambah](#-nilai-tambah)
- [📦 Penjelasan Package yang Digunakan](#-penjelasan-package-yang-digunakan)
- [📊 Use Case Diagram](#-use-case-diagram)
- [🔄 Flowchart Program](#-flowchart-program)
- [🧩 Widget yang Digunakan](#-widget-yang-digunakan)
- [📂 Struktur Folder / Package](#-struktur-folder--package)
- [🧰 Tech Stack](#-tech-stack)

---

## 📝 Deskripsi Aplikasi
**Nomad+** adalah aplikasi digital yang dirancang untuk membantu operasional Cafe Nomad dalam mengelola menu, pesanan, serta interaksi dengan pelanggan secara lebih efisien. Aplikasi ini menyediakan berbagai fitur seperti pemesanan menu, sistem poin, serta voucher promosi yang bertujuan untuk meningkatkan pengalaman dan loyalitas pelanggan.

Melalui aplikasi ini, pengguna dapat dengan mudah melihat menu, melakukan pemesanan, serta memanfaatkan promo yang tersedia. Di sisi lain, admin dapat mengelola data menu, pesanan, dan promo secara terpusat sehingga operasional cafe menjadi lebih terstruktur dan efektif.

---

## ⚙️ Fitur Utama

| No. | Fitur | Deskripsi |
|-----|-------|-----------|
| 1 | **Multi-Branch Selection** | Memungkinkan pengguna memilih cabang toko untuk mendapatkan daftar menu yang sesuai dengan ketersediaan lokal. |
| 2 | **Membership Tiering** | Sistem kasta (Bronze, Silver, Gold, Platinum) yang memberikan *multiplier* poin lebih besar seiring meningkatnya transaksi. |
| 3 | **Point & Rewards** | Pengguna dapat mengumpulkan poin dari setiap pembelian dan menukarkannya sebagai potongan harga (Redeem) saat checkout. |
| 4 | **Advanced Voucher System** | Validasi kode promo unik dengan parameter minimal belanja dan batasan jumlah penggunaan per pengguna. |
| 5 | **Real-time Queue Number** | Pembuatan nomor antrean otomatis setelah transaksi berhasil untuk memudahkan proses pengambilan pesanan. |
| 6 | **Status History** | Pelacakan riwayat pesanan mulai dari *pending*, *confirmed*, hingga *done*. |
| 7 | **Order Management (CRUD)** | Pengguna dapat membuat, melihat, mengubah, dan menghapus pesanan sebelum diproses oleh sistem. |
| 8 | **Admin Dashboard Management** | Admin dapat mengelola menu, pesanan, promo, dan sistem poin secara terpusat melalui dashboard. |
| 9 | **Menu Management System** | Admin dapat menambahkan, mengedit, dan menghapus menu sesuai dengan ketersediaan di setiap cabang. |
| 10 | **Notification System** | Pengguna menerima notifikasi terkait status pesanan, promo terbaru, dan event khusus seperti ulang tahun. |
| 11 | **Birthday Reward System** | Sistem memberikan voucher atau promo khusus kepada pengguna pada hari ulang tahun sebagai bentuk loyalitas. |
| 12 | **Custom Order Request** | Pengguna dapat menambahkan permintaan khusus pada pesanan seperti tingkat gula atau preferensi lainnya. |
| 13 | **Authentication & Validation** | Sistem melakukan validasi data saat registrasi dan login untuk memastikan keamanan dan keakuratan data pengguna. |
---

contoh:

## 📑 Struktur Database
---
### Tabel `branches`
 
Menyimpan data seluruh cabang Cafe Nomad yang tersedia dalam sistem. Informasi ini digunakan untuk menampilkan pilihan cabang kepada pengguna serta menyesuaikan menu dan operasional berdasarkan lokasi cabang.
 
- `id` — Primary key untuk identitas unik setiap cabang
- `name` — Nama cabang cafe
- `location` — Lokasi umum cabang cafe
- `phone` — Nomor telepon cabang yang dapat dihubungi
- `is_open` — Status operasional cabang (buka/tutup)
- `open_time` — Jam buka cabang
- `close_time` — Jam tutup cabang
- `image_url` — URL gambar atau foto cabang untuk ditampilkan di aplikasi
- `created_at` — Waktu data cabang dibuat, biasanya terisi otomatis oleh sistem
- `address` — Alamat lengkap cabang cafe
---

### Tabel `categories`

Menyimpan data kategori menu pada aplikasi Cafe Nomad. Kategori ini digunakan untuk mengelompokkan menu (misalnya minuman dan makanan) agar lebih mudah ditampilkan dan dicari oleh pengguna.
 
- `id` — Primary key untuk identitas unik setiap kategori
- `name` — Nama kategori 
- `icon` — Ikon atau simbol kategori yang digunakan untuk tampilan UI
- `created_at` — Waktu data kategori dibuat, biasanya terisi otomatis oleh sistem

---

### Tabel `menu_items`

Menyimpan data seluruh menu yang tersedia di Cafe Nomad. Tabel ini terhubung dengan kategori dan cabang, sehingga setiap menu dapat ditampilkan sesuai jenis dan lokasi cabang yang dipilih oleh pengguna.

- `id` — Primary key untuk identitas unik setiap menu
- `category_id` — Foreign key yang merujuk ke tabel `categories`, menunjukkan kategori dari menu
- `branch_id` — Foreign key yang merujuk ke tabel `branches`, menunjukkan cabang tempat menu tersedia
- `created_by` — ID admin yang menambahkan menu ke dalam sistem
- `name` — Nama menu (contoh: Teh Tarik, Roti Bakar)
- `description` — Deskripsi singkat mengenai menu
- `price` — Harga menu yang tersedia
- `image_url` — URL gambar menu untuk ditampilkan pada aplikasi
- `is_available` — Status ketersediaan menu (tersedia / tidak tersedia)
- `order_count` — Jumlah berapa kali menu telah dipesan (digunakan untuk analisis atau menu populer)
- `is_featured` — Penanda apakah menu termasuk menu unggulan (highlight di aplikasi)
- `created_at` — Waktu data menu dibuat, biasanya terisi otomatis
- `updated_at` — Waktu terakhir data menu diperbarui

---

### Tabel `order_items`

Menyimpan detail item dari setiap pesanan yang dibuat oleh user.

- `id` — Primary key untuk identitas unik setiap item pesanan
- `order_id` — Foreign key yang merujuk ke tabel `orders`, menunjukkan pesanan utama
- `menu_item_id` — Foreign key yang merujuk ke tabel `menu_items`, menunjukkan menu yang dipesan
- `quantity` — Jumlah item menu yang dipesan
- `notes` — Catatan atau request khusus dari user (misalnya tingkat gula, tanpa es, dll)
- `price` — Harga satuan menu saat dipesan
- `menu_name_snapshot` — Nama menu yang disimpan saat transaksi (untuk menjaga konsistensi data jika nama menu berubah di masa depan)
- `subtotal` — Total harga untuk item tersebut (quantity × price)

---

### Tabel `orders`

Menyimpan data utama dari setiap transaksi atau pesanan yang dilakukan oleh user. Tabel ini menjadi pusat relasi dengan tabel lain seperti `users`, `branches`, `vouchers`, dan `order_items`.

- `id` — Primary key untuk identitas unik setiap pesanan
- `user_id` — Foreign key yang merujuk ke tabel `users`, menunjukkan pemilik pesanan
- `branch_id` — Foreign key yang merujuk ke tabel `branches`, menunjukkan cabang tempat pesanan dibuat
- `voucher_id` — Foreign key yang merujuk ke tabel `vouchers`, menunjukkan voucher yang digunakan (jika ada)
- `queue_number` — Nomor antrean yang dihasilkan sistem untuk proses pengambilan pesanan
- `payment_method` — Metode pembayaran yang digunakan (cash / non-cash)
- `status` — Status pesanan (misalnya: *pending*, *confirmed*, *done*)
- `subtotal` — Total harga sebelum diskon dan biaya tambahan
- `discount_amount` — Jumlah potongan harga dari voucher atau promo
- `service_fee` — Biaya tambahan layanan
- `grand_total` — Total akhir yang harus dibayar oleh user
- `points_earned` — Jumlah poin yang didapat user dari transaksi ini
- `points_used` — Jumlah poin yang digunakan dalam transaksi
- `order_type` — Jenis pesanan (misalnya: dine-in, take-away)
- `notes` — Catatan tambahan untuk pesanan
- `created_at` — Waktu pesanan dibuat
- `voucher_code` — Kode voucher yang digunakan
- `is_reward_redeem` — Penanda apakah pesanan menggunakan penukaran reward
- `reward_menu_item_id` — Foreign key ke `menu_items` jika user menukar reward berupa menu
- `updated_at` — Waktu terakhir data pesanan diperbarui

---

### Tabel `users`

Menyimpan data seluruh pengguna aplikasi. Tabel ini juga mendukung sistem loyalty dengan menyimpan poin dan tingkatan membership pengguna.

- `id` — Primary key untuk identitas unik setiap user
- `auth_id` — ID autentikasi dari sistem auth (misalnya Supabase Auth) yang digunakan untuk login
- `name` — Nama lengkap pengguna
- `email` — Email pengguna yang digunakan untuk login
- `phone` — Nomor telepon pengguna
- `role` — Peran pengguna dalam sistem (user / admin)
- `loyalty_points` — Jumlah poin yang dimiliki user saat ini
- `total_earned_points` — Total keseluruhan poin yang pernah didapatkan user (tidak berkurang meskipun digunakan)
- `membership_tier` — Tingkatan membership user (misalnya: Bronze, Silver, Gold, Platinum)
- `created_at` — Waktu akun pengguna dibuat

---

### Tabel `voucher_usages`
### Tabel `vouchers`

## 🔒 Keamanan Database (RLS)
 
### Tabel `articles`
 
- Semua user dapat membaca semua artikel yang dipublikasikan (oleh semua user)
- User hanya dapat membuat artikel menggunakan akunnya sendiri
- User hanya dapat mengubah dan menghapus artikel miliknya sendiri

## 📦 Penjelasan Package yang Digunakan

Aplikasi ini menggunakan beberapa package untuk mendukung pengembangan fitur, pengelolaan data, serta peningkatan tampilan dan pengalaman pengguna.

### 🔹 Package Utama 

1. **GetX (`get`)**  
   Digunakan sebagai *state management* untuk mengatur data dan logika aplikasi secara efisien.  
   GetX membantu dalam mengelola perubahan data secara real-time, navigasi antar halaman, serta menampilkan notifikasi seperti snackbar.

2. **Supabase (`supabase_flutter`)**  
   Digunakan sebagai backend service yang menyediakan database dan autentikasi.  
   Supabase memungkinkan aplikasi untuk menyimpan data seperti user, menu, pesanan, dan voucher secara online serta melakukan operasi CRUD.

3. **Environment Config (`flutter_dotenv`)**  
   Digunakan untuk menyimpan konfigurasi penting seperti API URL dan API Key agar lebih aman dan tidak ditulis langsung di dalam kode.

---

### 🌟 Package Nilai Tambah 

4. **Google Fonts (`google_fonts`)**  
   Digunakan untuk menerapkan jenis font kustom sehingga tampilan aplikasi menjadi lebih menarik, konsisten, dan memiliki identitas visual yang kuat.

5. **Font Awesome Icons (`font_awesome_flutter`)**  
   Digunakan untuk menampilkan ikon-ikon yang lebih variatif dan profesional pada menu, tombol, dan fitur aplikasi.

6. **Data Formatting (`intl`)**  
   Digunakan untuk memformat data seperti mata uang (Rupiah) dan tanggal agar lebih mudah dibaca dan sesuai dengan format lokal Indonesia.

7. **Loading Animation (`flutter_spinkit`)**  
   Digunakan untuk menampilkan animasi loading yang lebih interaktif saat aplikasi mengambil data, sehingga meningkatkan pengalaman pengguna.

8. **Image Picker (`image_picker`)**  
   Digunakan untuk mengambil gambar dari galeri atau kamera perangkat.  
   Pada aplikasi ini, image_picker dimanfaatkan untuk mendukung fitur seperti upload foto profil pengguna atau gambar menu oleh admin, sehingga data yang ditampilkan menjadi lebih interaktif dan menarik.

---

Penggunaan package-package tersebut membantu dalam:
- Mempermudah pengelolaan state dan data
- Menghubungkan aplikasi dengan database secara efisien
- Meningkatkan tampilan UI/UX aplikasi
- Memberikan pengalaman pengguna yang lebih baik dan interaktif

---

## 📈 Use Case Diagram

<details>
  <summary><b>Use Case</b></summary>
  <img width="1915" height="747" alt="Image" src="https://github.com/user-attachments/assets/e82eebd9-d0e7-4258-aef2-2d8ac1aa1479" />
</details>

## 🔁 Flowchart Program

<details>
  <summary><b>1. Menu Login</b></summary>
  <img width="446" height="755" alt="Image" src="https://github.com/user-attachments/assets/102e23b9-e9cc-455d-b436-6221ef21394c" />
</details>

<details>
  <summary><b>2. Menu Register</b></summary>
  <img width="197" height="521" alt="Image" src="https://github.com/user-attachments/assets/f8b4c209-c1f4-4c5b-9e02-c824c19a737e" />
</details>

<details>
  <summary><b>3. Menu User</b></summary>
  <img width="774" height="858" alt="Image" src="https://github.com/user-attachments/assets/9b28dfae-9cc4-4288-aef3-43bbccac9a64" />
</details>

<details>
  <summary><b>4. Menu Admin</b></summary>
  <img width="496" height="853" alt="Image" src="https://github.com/user-attachments/assets/2e4f72b7-fb8c-4284-9a91-ae97e2cf5ade" />
</details>

---

## ⚙️ Fitur Program

Aplikasi **Nomad+** memiliki beberapa fitur utama yang dibedakan berdasarkan peran pengguna: **Admin**, **User (Pelanggan)**, dan **Fitur Umum**.

---

### 🧑‍💼 1. Fitur untuk Admin
Admin memiliki kontrol penuh terhadap sistem untuk mengelola operasional Cafe Nomad.

- **Kelola Menu (CRUD)**  
  Admin dapat menambahkan, mengedit, dan menghapus menu sesuai dengan ketersediaan di setiap cabang.

- **Kelola Pesanan**  
  Admin dapat melihat seluruh pesanan yang masuk dari user dan memprosesnya.

- **Update Status Pesanan**  
  Admin dapat mengubah status pesanan seperti *pending*, *confirmed*, hingga *done*.

- **Kelola Promo & Voucher**  
  Admin dapat membuat dan mengatur berbagai promo yang berlaku.

- **Kelola Sistem Poin**  
  Admin dapat mengatur skema poin yang didapatkan user dari setiap transaksi.

---

### 👤 2. Fitur untuk User (Pelanggan)
User dapat menggunakan aplikasi untuk melakukan pemesanan dan mendapatkan berbagai keuntungan.

- **Registrasi & Login**  
  User dapat membuat akun dan masuk ke dalam sistem dengan validasi data.

- **Mendapat Voucher Member Baru**  
  User yang baru registrasi otomatis mendapatkan voucher sebagai bentuk promosi awal.

- **Melihat Menu & Detail Menu**  
  User dapat melihat daftar menu serta informasi detail dari setiap cabang.

- **Membuat Pesanan (CRUD)**  
  User dapat:
  - Membuat pesanan  
  - Melihat pesanan  
  - Mengubah pesanan  
  - Menghapus pesanan  

- **Custom Request Pesanan**  
  User dapat menambahkan permintaan khusus seperti tingkat gula, topping, dll.

- **Menggunakan Voucher**  
  User dapat menggunakan voucher saat melakukan pembelian.

- **Sistem Poin & Rewards**  
  User mendapatkan poin dari setiap pembelian yang bisa digunakan sebagai potongan harga.

- **Melihat Status Pesanan**  
  User dapat memantau status pesanan secara real-time.

---

### 🖥️ 3. Fitur Umum
Fitur yang berlaku untuk seluruh sistem aplikasi.

- **Authentication & Validasi Data**  
  Sistem melakukan validasi saat login dan registrasi untuk menjaga keamanan data.

- **Multi-Branch Menu**  
  Sistem menampilkan menu berdasarkan cabang yang dipilih user.

- **Manajemen Database Terpusat**  
  Semua data (user, menu, pesanan, voucher) tersimpan dalam database secara terstruktur.

- **Antarmuka Interaktif & User-Friendly**  
  Tampilan aplikasi dirancang agar mudah digunakan dan menarik bagi pengguna.

---

## 🧩 Widget yang Digunakan
Aplikasi ini menggunakan berbagai widget Flutter untuk membangun UI yang responsif:

* **Layouting**: `Scaffold`, `Stack`, `Column`, `Row`, `Padding`, dan `SizedBox`.
* **Scrolling**: `ListView.builder` dan `GridView` untuk efisiensi render daftar menu dan riwayat.
* **Styling**: `LinearGradient` (digunakan pada kartu member) dan `BoxDecoration` untuk kustomisasi kartu menu.
* **Stateful UI**: `Obx` dari GetX untuk mendengarkan perubahan pada keranjang belanja dan poin secara reaktif.
* **Feedback**: `Get.snackbar` untuk menampilkan pesan sukses/gagal pada proses update profil dan voucher.

---
## 🔍 Tampilan Aplikasi
 
---
 ### 1. Register Page

 

## 📂 Struktur Folder / Package
Proyek ini menggunakan pola arsitektur yang terorganisir:
* `lib/core/`: Berisi konfigurasi warna, gaya teks, dan state global (`AppStateController`).
* `lib/data/datasources/`: Berisi logic komunikasi langsung ke Supabase (`RemoteDatasource`).
* `lib/data/models/`: Definisi data (User, Menu, Order, Voucher) dan factory methods `fromMap`.
* `lib/controllers/`: Logic bisnis aplikasi (Auth, Profile, Cart, Voucher).
* `lib/presentation/`: Berisi folder `screens` dan `widgets` untuk komponen UI.

---

## 🧰 Tech Stack
* **Framework**: [Flutter](https://flutter.dev/)
* **State Management**: [GetX](https://pub.dev/packages/get)
* **Backend**: [Supabase](https://supabase.com/)
* **Database**: PostgreSQL
* **Library Lainnya**: Google Fonts, Font Awesome Flutter, Intl, Flutter Dotenv.

<p align="center">
  <b>Developed for Teh Tarik Nomad © 2024</b>
</p>
