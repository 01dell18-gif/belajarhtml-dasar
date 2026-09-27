# Product Requirement Document (PRD)
## WebCraft: Interactive Web Development Platform & Studio
- **Versi Dokumen:** 1.2.0 (Ramah Pemula & Panduan Step-by-Step)
- **Status:** Approved & Ready for Implementation
- **Target Rilis:** Single-file Standalone Web Application (`index.html`) & Zero Configuration
- **Target Deployment:** GitHub Pages / Local Browser / Shared Classroom Drive
- **Author:** Principal Product Designer & Lead Web Architect

---

## 1. Executive Summary & Product Vision

### 1.1 Visi Produk
Menciptakan media pembelajaran web dasar yang **sangat ramah pemula (super beginner-friendly)**, mudah dimengerti tanpa istilah rumit, serta mengajarkan pembuatan web dari nol secara bertahap (*step-by-step*).
Pemula diperkenalkan dengan analogi nyata:
- **HTML:** Sebagai **Kerangka / Dinding Rumah** (menentukan ada kamar, pintu, dan jendela).
- **CSS:** Sebagai **Cat & Dekorasi Rumah** (memberi warna, mengatur kerapian, dan memperindah tampilan).
- **JavaScript:** Sebagai **Aliran Listrik & Saklar Rumah** (membuat bel berbunyi saat dipencet, dan lampu menyala saat ditekan).

Pengguna dapat melihat langsung evolusi satu proyek web sederhana:
1. Dimulai dari kode **HTML polos** saja (tampilannya hitam putih sederhana).
2. Diberi sentuhan **CSS** (langsung berubah menjadi indah, berwarna, dan rapi di tengah).
3. Diberi logika **JavaScript sederhana** (tombol menjadi bisa diklik dan merespons aksi pengguna).
4. Disatukan menjadi **1 Contoh File HTML Lengkap** yang siap disalin dan dijalankan langsung di komputer!

---

## 2. Fitur Baru: Lab Step-by-Step Pemula (HTML ➔ CSS ➔ JS ➔ File Lengkap)

Fitur ini diletakkan di halaman muka agar pemula tidak merasa bingung atau kewalahan saat pertama kali membuka website:

### Langkah 1: Struktur HTML Saja
- **Konsep:** Membuat judul, paragraf, dan satu tombol sapaan.
- **Kode:**
  ```html
  <div class="kartu">
    <h2>Halo, Saya Budi!</h2>
    <p>Saya baru mulai belajar membuat website.</p>
    <button id="tombolSapa">Klik Saya</button>
  </div>
  ```
- **Tampilan:** Teks polos standar browser, tanpa warna, tanpa gaya.
- **Pesan Edukasi:** *"Lihat, HTML hanya membuat kerangka tulisan. Belum ada warna maupun hiasan."*

### Langkah 2: Menambahkan CSS (Mempercantik Tampilan)
- **Konsep:** Memberikan warna latar belakang, kartu melayang dengan bayangan halus, dan tombol warna ungu modern.
- **Kode Tambahan:**
  ```css
  body {
    background-color: #f1f5f9;
    font-family: sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
  }
  .kartu {
    background: #ffffff;
    padding: 24px;
    border-radius: 16px;
    box-shadow: 0 10px 25px rgba(0,0,0,0.1);
    text-align: center;
  }
  button {
    background-color: #6366f1;
    color: white;
    border: none;
    padding: 10px 20px;
    border-radius: 8px;
    cursor: pointer;
  }
  ```
- **Tampilan:** Kartu langsung berubah menjadi estetik, berada persis di tengah layar, dan tombol tampak modern.
- **Pesan Edukasi:** *"Hebat! Dengan CSS, kerangka polos tadi berubah menjadi kartu yang menarik dipandang."*

### Langkah 3: Menambahkan JavaScript (Memberikan Interaksi Nyata)
- **Konsep:** Membuat tombol bereaksi saat diklik dengan memunculkan pesan sapaan ramah.
- **Kode Tambahan:**
  ```javascript
  const tombol = document.getElementById("tombolSapa");
  
  tombol.addEventListener("click", function() {
    alert("Halo teman! Selamat datang di dunia Web Development 🎉");
    tombol.innerText = "Sudah Diklik ✓";
    tombol.style.backgroundColor = "#10b981"; // Berubah warna hijau
  });
  ```
- **Tampilan:** Tombol sekarang aktif dan dapat diklik secara interaktif.
- **Pesan Edukasi:** *"Sekarang website kita hidup! Tombol merespons sentuhan pengunjung."*

### Langkah 4: Hasil Akhir 1 File HTML Lengkap
- Menyatukan tag `<!DOCTYPE html>`, `<style>`, konten `<body>`, dan `<script>` menjadi satu file utuh yang rapi dan siap dijalankan cukup dengan klik 2x di komputer pengguna:
```html
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Website Sederhana Pertama Saya</title>
  <style>
    body {
      background-color: #f1f5f9;
      font-family: Arial, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      margin: 0;
    }
    .kartu {
      background: white;
      padding: 30px;
      border-radius: 16px;
      box-shadow: 0 10px 25px rgba(0,0,0,0.1);
      text-align: center;
      max-width: 350px;
    }
    h2 { color: #1e293b; margin-top: 0; }
    p { color: #64748b; line-height: 1.5; }
    button {
      background-color: #6366f1;
      color: white;
      border: none;
      padding: 12px 24px;
      border-radius: 8px;
      font-size: 16px;
      cursor: pointer;
      font-weight: bold;
      transition: background 0.2s;
    }
    button:hover { background-color: #4f46e5; }
  </style>
</head>
<body>

  <div class="kartu">
    <h2>Halo, Saya Pemula Web! 👋</h2>
    <p>Ini adalah kartu web pertama saya yang menggabungkan HTML, CSS, dan JavaScript.</p>
    <button id="tombolAksi">Klik Saya</button>
  </div>

  <script>
    const tombol = document.getElementById("tombolAksi");
    let sudahDiklik = false;

    tombol.addEventListener("click", function() {
      if (!sudahDiklik) {
        alert("Selamat! Kode JavaScript Anda berhasil berjalan! 🎉");
        tombol.innerText = "Terima Kasih! ✨";
        tombol.style.backgroundColor = "#10b981"; // warna hijau
        sudahDiklik = true;
      } else {
        alert("Tombol ini sudah pernah Anda klik sebelumnya.");
      }
    });
  </script>
</body>
</html>
```

---

## 3. Kurikulum yang Disederhanakan Bahasa & Konsepnya

1. **Modul 1: HTML5 (Kerangka Web)**
   - Bahasa sehari-hari: Menjelaskan tag seperti `<p>` untuk paragraf cerita, `<h1>` untuk judul utama, dan `<button>` untuk tombol klik.
   - Tanpa istilah rumit: Menjelaskan peran `head` sebagai kartu identitas website dan `body` sebagai panggung tampilan utama.
2. **Modul 2: CSS3 (Dekorasi & Tata Letak)**
   - Bahasa sehari-hari: Mengapa `margin` adalah jarak ke tetangga sebelah, dan `padding` adalah jarak bantal di dalam baju.
   - Flexbox dijelaskan sebagai "rak gantung" yang bisa menata benda ke samping atau ke bawah secara rapi otomatis.
3. **Modul 3: JavaScript (Logika & Reaksi)**
   - Bahasa sehari-hari: Mengenalkan event klik seperti memencet saklar bel rumah.
4. **Modul 4: Formulir & Google Sheets (Database Gratis)**
   - Menyimpan data form langsung ke tabel Google Spreadsheet tanpa biaya server sepeser pun.
5. **Modul 5: Publikasi ke GitHub Pages**
   - 4 langkah mudah meng-online-kan website ke seluruh dunia secara gratis.

---

## 4. UI/UX & Desain Antarmuka

- Teks bahasa Indonesia yang ramah, hangat, dan mudah dimengerti oleh anak sekolah/pemula umum.
- Visualizer interaktif dengan tombol "Langkah 1", "Langkah 2", "Langkah 3", "Langkah 4 (Lengkap)" yang memperlihatkan transformasi secara langsung.
- 1-Click Salin Kode & 1-Click Unduh File `.html`.
