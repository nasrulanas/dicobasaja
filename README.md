<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Undangan Pernikahan</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    body {
      background: #fef8f8;
      font-family: 'Georgia', serif;
    }
    .countdown {
      font-size: 2rem;
      font-weight: bold;
      color: #e63946;
    }
  </style>
</head>
<body>

<!-- Musik Latar -->
<audio autoplay loop>
  <source src="path_to_your_wedding_music.mp3" type="audio/mp3">
  Browser Anda tidak mendukung elemen audio.
</audio>

<!-- Hero Section -->
<section class="min-h-screen flex flex-col items-center justify-center text-center bg-gradient-to-b from-pink-200 to-white text-gray-800 p-6">
  <h1 class="text-4xl md:text-5xl font-bold mb-4">Undangan Pernikahan</h1>
  <p class="text-lg mb-6">Kami mengundang Anda untuk hadir dalam hari bahagia kami</p>
  <h2 class="text-3xl font-semibold text-pink-600">Alya & Raka</h2>
  <p class="mt-4 text-md">Minggu, 21 Desember 2025<br>Gedung Serbaguna, Jakarta</p>
  <a href="#rsvp" class="mt-6 inline-block bg-pink-500 text-white px-6 py-2 rounded-full shadow hover:bg-pink-600 transition">RSVP Sekarang</a>
</section>

<!-- Countdown Timer -->
<section class="py-16 px-6 text-center">
  <h3 class="text-3xl font-bold text-pink-600 mb-8">Hitung Mundur Menuju Hari Bahagia</h3>
  <div id="countdown" class="countdown"></div>
</section>

<!-- Buku Tamu Digital -->
<section id="rsvp" class="py-16 px-6 bg-pink-100 text-center">
  <h3 class="text-3xl font-bold text-gray-800 mb-6">Konfirmasi Kehadiran</h3>
  <p class="mb-4 text-gray-700">Kami akan sangat senang jika Anda dapat hadir di hari istimewa kami.</p>
  <a href="https://wa.me/6281234567890?text=Hai%20Alya%20dan%20Raka,%20saya%20akan%20datang%20ke%20acara%20pernikahanmu!" target="_blank" class="bg-green-500 text-white px-6 py-3 rounded-full shadow hover:bg-green-600 transition">
    Konfirmasi via WhatsApp
  </a>
</section>

<!-- QR Code untuk Akses Cepat -->
<section class="py-16 px-6 text-center">
  <h3 class="text-3xl font-bold text-pink-600 mb-8">Akses Cepat dengan QR Code</h3>
  <img src="path_to_your_qr_code.png" alt="QR Code Undangan" class="mx-auto mb-4">
  <p class="text-lg text-gray-700">Scan QR Code ini untuk mengakses undangan digital kami kapan saja.</p>
</section>

<!-- Footer -->
<footer class="bg-gray-800 text-white text-center py-6">
  <p>&copy; 2025 Alya & Raka | Terima kasih atas doa dan restunya ❤️</p>
</footer>

<script>
  // Countdown Timer
  const countdownDate = new Date("Dec 21, 2025 10:00:00").getTime();
  const countdownElement = document.getElementById("countdown");

  const updateCountdown = () => {
    const now = new Date().getTime();
    const distance = countdownDate - now;

    if (distance < 0) {
      countdownElement.innerHTML = "Hari Bahagia Telah Tiba!";
    } else {
      const days = Math.floor(distance / (1000 * 60 * 60 * 24));
      const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
      const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
      const seconds = Math.floor((distance % (1000 * 60)) / 1000);
      countdownElement.innerHTML = `${days} Hari ${hours} Jam ${minutes} Menit ${seconds} Detik`;
    }
  };

  setInterval(updateCountdown, 1000);
</script>

</body>
</html>
