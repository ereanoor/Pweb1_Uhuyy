# Penjelasan Source Kode
## index.html
File ini merupakan struktur utama website portofolio yang berfungsi sebagai pusat navigasi dan interaksi pengguna.

```HTML
<head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
</head 
```
Fungsi: Menggunakan standar HTML5 dan mengintegrasikan library eksternal untuk animasi serta ikon grafis yang mendukung antarmuka.

```HTML
<nav>
    <div class="logo">ereanoor<span>.dev</span></div>
    <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#hobbies">Hobi</a></li>
        <li><a href="#contact">Kontak</a></li>
    </ul>
</nav>```
```
Fungsi: Implementasi navigasi menggunakan anchor links (#) yang memungkinkan perpindahan antar seksi halaman secara halus (SPA style).

```JavaScript
const phrases = ['IT Student', 'AI Enthusiast'];
let phraseIndex = 0; let charIndex = 0; let isDeleting = false;

function type() {
    const currentPhrase = phrases[phraseIndex];
    if (isDeleting) {
        textElement.textContent = currentPhrase.substring(0, charIndex - 1); 
        charIndex--;
    } else {
        textElement.textContent = currentPhrase.substring(0, charIndex + 1); 
        charIndex++;
    }
}
```
Fungsi: Memanipulasi DOM pada elemen #typewriter untuk mensimulasikan efek pengetikan otomatis secara dinamis.

## Detail Pages (membaca.html, bermusik.html, ngoding.html, gaming.html)
Halaman-halaman ini dirancang untuk memberikan informasi mendalam mengenai profil personal dengan struktur yang konsisten.

```HTML
<body class="sub-page">
    <div class="sub-hero">
        <h1>The <span>Gamer</span> Soul</h1>
        <p>Arena ketangguhan mental dan strategi tim.</p>
    </div>
```
Fungsi: Menggunakan kelas .sub-page untuk mengatur tata letak khusus konten detail dan elemen sub-hero sebagai identitas visual yang puitis di setiap halaman hobi.

```HTML
<div class="detail-box">
    <h3><i class="fas fa-trophy"></i> Prestasi Kompetitif</h3>
    <p>Menjuarai turnamen Mobile Legends dan Top Leaderboard Blood Strike.</p>
</div>
```
Fungsi: Menyediakan wadah khusus untuk menonjolkan poin-poin penting seperti prestasi gaming atau ambisi di bidang Artificial Intelligence.

```HTML
<a href="index.html#hobbies" class="btn-back-bottom">
    <i class="fas fa-arrow-left"></i> Kembali ke Beranda
</a>
```
Fungsi: Mengarahkan pengguna kembali tepat ke bagian daftar hobi di halaman utama menggunakan ID selektor #hobbies, sehingga navigasi tetap intuitif.

### Fitur Khusus (bermusik.html)
```JavaScript
playBtn.addEventListener("click", function() {
    if (audio.paused) {
        audio.play();
        diskIcon.classList.add("fa-spin");
    } else {
        audio.pause();
        diskIcon.classList.remove("fa-spin");
    }
});
```
Fungsi: Mengontrol pemutaran file audio lagu.mp3 secara dinamis dan memberikan animasi pada ikon piringan hitam saat musik aktif.

Siap, Noor! Ini bagian terakhir untuk style.css. Bagian ini sangat penting karena menjelaskan bagaimana tampilan "high-tech" dan blueprint pada portofolio kamu terbentuk.

Seperti biasa, pastikan ada baris kosong setelah tanda penutup kotak kode agar tulisan penjelasannya tidak ikut masuk ke dalam kotak.

## style.css
File ini berfungsi sebagai otak visual yang mengatur estetika, tata letak responsif, dan pengalaman pengguna di seluruh halaman website.

```CSS
* { 
    margin: 0; padding: 0; box-sizing: border-box; 
    font-family: 'Inter', sans-serif; scroll-behavior: smooth; 
}
```
Fungsi: Menghilangkan margin bawaan browser dan menggunakan box-sizing: border-box agar perhitungan dimensi elemen tetap akurat, serta mengaktifkan pergerakan halaman yang halus saat navigasi diklik.

```CSS
body { 
    background-color: #0f172a; 
    background-image: 
        linear-gradient(rgba(56, 189, 248, 0.03) 1px, transparent 1px),
        linear-gradient(90deg, rgba(56, 189, 248, 0.03) 1px, transparent 1px);
    background-size: 40px 40px;
}
```
Fungsi: Menciptakan suasana "high-tech" dengan warna biru gelap dan pola grid halus yang menyerupai kertas desain teknis atau papan sirkuit.

```CSS
.hobbies-grid { 
    display: grid; 
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); 
    gap: 25px; 
}
```
Fungsi: Mengatur kartu hobi agar secara otomatis menyesuaikan jumlah kolom berdasarkan lebar layar (responsif) tanpa memerlukan banyak baris kode tambahan.

```CSS
header { 
    background: rgba(15, 23, 42, 0.9); 
    backdrop-filter: blur(12px);
    position: fixed; 
}
```
Fungsi: Menciptakan efek kaca transparan yang buram pada bagian navigasi atas, memberikan kesan modern dan menjaga keterbacaan menu saat menimpa konten halaman.
