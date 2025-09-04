<php
include 'cekuser.php';
?>

<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Iklan Videotron</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      line-height: 1.6;
    }
    header {
      background: #1a237e;
      color: white;
      padding: 20px;
      text-align: center;
    }
    nav {
      display: flex;
      justify-content: center;
      gap: 20px;
      margin-top: 10px;
    }
    nav a {
      color: white;
      text-decoration: none;
      font-weight: bold;
    }
    .hero {
      background: url("https://images.unsplash.com/photo-1582719478190-4cfba0a3a94d") no-repeat center/cover;
      color: white;
      height: 400px;
      display: flex;
      align-items: center;
      justify-content: center;
      flex-direction: column;
      text-shadow: 2px 2px 5px black;
    }
    .hero h1 {
      font-size: 3rem;
    }
    .container {
      width: 90%;
      max-width: 1100px;
      margin: auto;
      padding: 40px 0;
    }
    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 20px;
    }
    .card {
      border: 1px solid #ccc;
      border-radius: 10px;
      overflow: hidden;
      box-shadow: 0 4px 6px rgba(0,0,0,0.1);
      transition: transform 0.2s;
    }
    .card:hover {
      transform: translateY(-5px);
    }
    .card img {
      width: 100%;
      height: 180px;
      object-fit: cover;
    }
    .card-body {
      padding: 15px;
    }
    .card-body h3 {
      margin: 0 0 10px;
      color: #1a237e;
    }
    .btn {
      display: inline-block;
      background: #1a237e;
      color: white;
      padding: 10px 15px;
      border-radius: 5px;
      text-decoration: none;
      transition: background 0.3s;
    }
    .btn:hover {
      background: #3949ab;
    }
    form {
      display: grid;
      gap: 15px;
    }
    form input, form select, form textarea {
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 5px;
      width: 100%;
    }
    footer {
      background: #1a237e;
      color: white;
      text-align: center;
      padding: 20px;
      margin-top: 30px;
    }
  </style>
</head>
<body>

  <header>
    <h1>Videotron Advertising</h1>
    <nav>
      <a href="#lokasi">Lokasi</a>
      <a href="#pesan">Pesan</a>
      <a href="#kontak">Kontak</a>
    </nav>
  </header>

  <section class="hero">
    <h1>Iklan Anda di Videotron</h1>
    <p>Tingkatkan brand awareness dengan iklan digital luar ruang</p>
    <a href="#pesan" class="btn">Pesan Sekarang</a>
  </section>

  <section class="container" id="lokasi">
    <h2>Lokasi Videotron</h2>
    <div class="grid">
      <div class="card">
        <img src="https://images.unsplash.com/photo-1508057198894-247b23fe5ade" alt="Jakarta">
        <div class="card-body">
          <h3>Jakarta - Sudirman</h3>
          <p>Ukuran: 8x4m<br>Harga: Rp 20.000.000 / bulan</p>
          <a href="#pesan" class="btn">Pesan</a>
        </div>
      </div>
      <div class="card">
        <img src="https://images.unsplash.com/photo-1528909514045-2fa4ac7a08ba" alt="Bandung">
        <div class="card-body">
          <h3>Bandung - Dago</h3>
          <p>Ukuran: 6x3m<br>Harga: Rp 12.000.000 / bulan</p>
          <a href="#pesan" class="btn">Pesan</a>
        </div>
      </div>
      <div class="card">
        <img src="https://images.unsplash.com/photo-1508057198894-247b23fe5ade" alt="Surabaya">
        <div class="card-body">
          <h3>Surabaya - Tunjungan</h3>
          <p>Ukuran: 10x5m<br>Harga: Rp 25.000.000 / bulan</p>
          <a href="#pesan" class="btn">Pesan</a>
        </div>
      </div>
    </div>
  </section>

  <section class="container" id="pesan">
    <h2>Form Pemesanan</h2>
    <form onsubmit="return handleBooking(event)">
      <input type="text" placeholder="Nama Lengkap" required>
      <input type="email" placeholder="Email" required>
      <input type="tel" placeholder="Nomor Telepon" required>
      <select required>
        <option value="">Pilih Lokasi</option>
        <option>Jakarta - Sudirman</option>
        <option>Bandung - Dago</option>
        <option>Surabaya - Tunjungan</option>
      </select>
      <input type="number" placeholder="Durasi (bulan)" required>
      <textarea placeholder="Catatan Tambahan"></textarea>
      <button type="submit" class="btn">Kirim Pemesanan</button>
    </form>
  </section>

  <footer id="kontak">
    <p>© 2025 Videotron Advertising. Semua Hak Dilindungi.</p>
    <p>Hubungi kami: info@videotron.co.id | 0812-3456-7890</p>
  </footer>

  <script>
    function handleBooking(event) {
      event.preventDefault();
      alert("Terima kasih, pemesanan Anda sudah kami terima!");
      event.target.reset();
    }
  </script>

</body>
</html>
