<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>SELEKSI MARGA VETHERA</title>

<!-- ============ GOOGLE FONTS ============ -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@500;700;900&family=Playfair+Display:wght@600;800&family=Poppins:wght@300;400;500;600&display=swap" rel="stylesheet">

<style>
/* ============================================================
   RESET & VARIABEL GLOBAL
============================================================ */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  -webkit-tap-highlight-color: transparent;
}

:root {
  --bg-dark: #0a0410;
  --bg-dark-2: #140820;
  --gold: #d4af37;
  --gold-light: #f4e5a1;
  --gold-bright: #ffd700;
  --purple: #6a1b9a;
  --purple-light: #9c27b0;
  --text-light: #f5f0ff;
  --text-muted: #b8a9c9;
  --card-bg: rgba(20, 8, 32, 0.75);
  --border-gold: rgba(212, 175, 55, 0.4);
  --shadow-gold: 0 0 25px rgba(212, 175, 55, 0.35);
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: 'Poppins', sans-serif;
  background: var(--bg-dark);
  color: var(--text-light);
  min-height: 100vh;
  overflow-x: hidden;
  position: relative;
  line-height: 1.6;
}

/* ============================================================
   BACKGROUND CANVAS (PARTIKEL BINTANG)
============================================================ */
#starCanvas {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 0;
  pointer-events: none;
}

/* Gradient overlay untuk kesan depth */
body::before {
  content: '';
  position: fixed;
  inset: 0;
  background: radial-gradient(ellipse at top, rgba(106, 27, 154, 0.25) 0%, transparent 50%),
              radial-gradient(ellipse at bottom, rgba(212, 175, 55, 0.12) 0%, transparent 50%);
  pointer-events: none;
  z-index: 1;
}

/* ============================================================
   CONTAINER UTAMA (MOBILE-FIRST 9:16)
============================================================ */
.main-wrapper {
  position: relative;
  z-index: 2;
  max-width: 480px;
  margin: 0 auto;
  padding: 40px 20px 80px;
  min-height: 100vh;
}

/* ============================================================
   HEADER / LOGO VETHERA
============================================================ */
.header {
  text-align: center;
  margin-bottom: 30px;
  padding-top: 10px;
}

.crown-icon {
  font-size: 36px;
  margin-bottom: 8px;
  display: inline-block;
  animation: floatCrown 3s ease-in-out infinite;
  filter: drop-shadow(0 0 12px var(--gold-bright));
}

@keyframes floatCrown {
  0%, 100% { transform: translateY(0) rotate(-5deg); }
  50% { transform: translateY(-8px) rotate(5deg); }
}

/* Judul VETHERA dengan efek shine */
.logo-title {
  font-family: 'Cinzel', serif;
  font-weight: 900;
  font-size: clamp(42px, 13vw, 64px);
  letter-spacing: 6px;
  background: linear-gradient(
    120deg,
    var(--gold) 0%,
    var(--gold-light) 25%,
    #ffffff 50%,
    var(--gold-light) 75%,
    var(--gold) 100%
  );
  background-size: 200% auto;
  -webkit-background-clip: text;
  background-clip: text;
  -webkit-text-fill-color: transparent;
  animation: shine 4s linear infinite;
  text-shadow: 0 0 30px rgba(212, 175, 55, 0.4);
  line-height: 1.1;
}

@keyframes shine {
  to { background-position: 200% center; }
}

/* Garis dekorasi bawah judul */
.title-divider {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 10px;
  margin-top: 12px;
}

.title-divider .line {
  height: 1px;
  width: 60px;
  background: linear-gradient(90deg, transparent, var(--gold), transparent);
}

.title-divider .diamond {
  color: var(--gold);
  font-size: 10px;
  animation: pulseDiamond 2s ease-in-out infinite;
}

@keyframes pulseDiamond {
  0%, 100% { opacity: 0.5; transform: scale(1); }
  50% { opacity: 1; transform: scale(1.3); }
}

/* Subjudul dengan efek typing */
.subtitle {
  font-family: 'Poppins', sans-serif;
  font-weight: 300;
  font-size: clamp(11px, 3.2vw, 14px);
  letter-spacing: 4px;
  color: var(--text-muted);
  text-transform: uppercase;
  margin-top: 18px;
  min-height: 20px;
}

/* Cursor typing */
.subtitle .cursor {
  display: inline-block;
  width: 2px;
  height: 1em;
  background: var(--gold);
  margin-left: 2px;
  vertical-align: middle;
  animation: blink 0.8s step-end infinite;
}

@keyframes blink {
  50% { opacity: 0; }
}

/* ============================================================
   COUNTDOWN TIMER
============================================================ */
.countdown-section {
  background: var(--card-bg);
  border: 1px solid var(--border-gold);
  border-radius: 16px;
  padding: 18px 14px;
  margin-bottom: 24px;
  backdrop-filter: blur(12px);
  -webkit-backdrop-filter: blur(12px);
  box-shadow: var(--shadow-gold), inset 0 1px 0 rgba(255,255,255,0.05);
  text-align: center;
}

.countdown-label {
  font-size: 11px;
  letter-spacing: 3px;
  color: var(--gold);
  text-transform: uppercase;
  margin-bottom: 12px;
  font-weight: 500;
}

.countdown-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 8px;
}

.countdown-box {
  background: rgba(106, 27, 154, 0.15);
  border: 1px solid rgba(212, 175, 55, 0.25);
  border-radius: 10px;
  padding: 10px 4px;
}

.countdown-num {
  font-family: 'Cinzel', serif;
  font-weight: 700;
  font-size: 22px;
  color: var(--gold-light);
  display: block;
  text-shadow: 0 0 10px rgba(212, 175, 55, 0.6);
}

.countdown-unit {
  font-size: 9px;
  letter-spacing: 1.5px;
  color: var(--text-muted);
  text-transform: uppercase;
}

/* ============================================================
   FORM PENDAFTARAN
============================================================ */
.form-section {
  background: var(--card-bg);
  border: 1px solid var(--border-gold);
  border-radius: 18px;
  padding: 26px 20px;
  backdrop-filter: blur(12px);
  -webkit-backdrop-filter: blur(12px);
  box-shadow: var(--shadow-gold), inset 0 1px 0 rgba(255,255,255,0.05);
  margin-bottom: 24px;
}

.form-title {
  font-family: 'Cinzel', serif;
  font-size: 18px;
  font-weight: 700;
  letter-spacing: 3px;
  text-align: center;
  color: var(--gold-light);
  margin-bottom: 22px;
  text-transform: uppercase;
}

.form-group {
  margin-bottom: 16px;
}

.form-group label {
  display: block;
  font-size: 11px;
  letter-spacing: 2px;
  text-transform: uppercase;
  color: var(--gold);
  margin-bottom: 8px;
  font-weight: 500;
}

.form-group label .optional {
  color: var(--text-muted);
  font-size: 9px;
  letter-spacing: 1px;
  text-transform: none;
  font-weight: 300;
}

.form-group input,
.form-group textarea {
  width: 100%;
  background: rgba(10, 4, 16, 0.6);
  border: 1px solid rgba(212, 175, 55, 0.3);
  border-radius: 10px;
  padding: 12px 14px;
  color: var(--text-light);
  font-family: 'Poppins', sans-serif;
  font-size: 14px;
  transition: all 0.3s ease;
  outline: none;
}

.form-group input::placeholder,
.form-group textarea::placeholder {
  color: rgba(184, 169, 201, 0.4);
}

.form-group input:focus,
.form-group textarea:focus {
  border-color: var(--gold);
  box-shadow: 0 0 0 3px rgba(212, 175, 55, 0.15), 0 0 20px rgba(212, 175, 55, 0.2);
  background: rgba(10, 4, 16, 0.85);
}

.form-group textarea {
  resize: vertical;
  min-height: 90px;
}

/* Upload foto custom */
.file-upload-wrapper {
  position: relative;
  width: 100%;
}

.file-upload-wrapper input[type="file"] {
  position: absolute;
  opacity: 0;
  width: 100%;
  height: 100%;
  cursor: pointer;
  z-index: 2;
}

.file-upload-display {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 8px;
  padding: 14px;
  border: 1px dashed rgba(212, 175, 55, 0.5);
  border-radius: 10px;
  background: rgba(10, 4, 16, 0.6);
  color: var(--text-muted);
  font-size: 12px;
  transition: all 0.3s ease;
}

.file-upload-wrapper:hover .file-upload-display {
  border-color: var(--gold);
  color: var(--gold-light);
  background: rgba(106, 27, 154, 0.1);
}

/* Tombol Submit */
.submit-btn {
  width: 100%;
  padding: 16px;
  margin-top: 8px;
  border: none;
  border-radius: 12px;
  background: linear-gradient(135deg, var(--gold) 0%, #b8941f 50%, var(--gold-bright) 100%);
  background-size: 200% auto;
  color: #1a0a2a;
  font-family: 'Cinzel', serif;
  font-weight: 900;
  font-size: 14px;
  letter-spacing: 3px;
  text-transform: uppercase;
  cursor: pointer;
  position: relative;
  overflow: hidden;
  transition: all 0.4s ease;
  box-shadow: 0 4px 20px rgba(212, 175, 55, 0.4);
}

.submit-btn:hover {
  background-position: right center;
  transform: translateY(-2px);
  box-shadow: 0 8px 30px rgba(212, 175, 55, 0.7);
}

.submit-btn:active {
  transform: translateY(0);
}

/* Shine sweep pada tombol */
.submit-btn::after {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(255,255,255,0.6), transparent);
  transition: left 0.6s ease;
}

.submit-btn:hover::after {
  left: 100%;
}

.submit-btn:disabled {
  opacity: 0.6;
  cursor: not-allowed;
}

/* Loading spinner */
.spinner {
  display: inline-block;
  width: 16px;
  height: 16px;
  border: 2px solid rgba(26, 10, 42, 0.3);
  border-top-color: #1a0a2a;
  border-radius: 50%;
  animation: spin 0.7s linear infinite;
  vertical-align: middle;
  margin-right: 8px;
}

@keyframes spin {
  to { transform: rotate(360deg); }
}

/* ============================================================
   CARD SYARAT & KETENTUAN
============================================================ */
.terms-section {
  background: var(--card-bg);
  border: 1px solid var(--border-gold);
  border-radius: 18px;
  padding: 24px 20px;
  backdrop-filter: blur(12px);
  -webkit-backdrop-filter: blur(12px);
  box-shadow: var(--shadow-gold), inset 0 1px 0 rgba(255,255,255,0.05);
  margin-bottom: 24px;
}

.terms-title {
  font-family: 'Cinzel', serif;
  font-size: 16px;
  font-weight: 700;
  letter-spacing: 3px;
  color: var(--gold-light);
  text-align: center;
  margin-bottom: 16px;
  text-transform: uppercase;
}

.terms-list {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.terms-list li {
  display: flex;
  align-items: flex-start;
  gap: 10px;
  font-size: 13px;
  color: var(--text-muted);
  line-height: 1.5;
}

.terms-list li::before {
  content: '✦';
  color: var(--gold);
  flex-shrink: 0;
  font-size: 12px;
  margin-top: 2px;
}

/* ============================================================
   FOOTER SOCIAL MEDIA
============================================================ */
.footer {
  text-align: center;
  padding-top: 10px;
}

.footer-text {
  font-size: 11px;
  letter-spacing: 2px;
  text-transform: uppercase;
  color: var(--text-muted);
  margin-bottom: 16px;
}

.social-icons {
  display: flex;
  justify-content: center;
  gap: 14px;
  margin-bottom: 20px;
}

.social-icon {
  width: 44px;
  height: 44px;
  border-radius: 50%;
  border: 1px solid var(--border-gold);
  background: rgba(106, 27, 154, 0.15);
  display: flex;
  align-items: center;
  justify-content: center;
  text-decoration: none;
  color: var(--gold);
  font-size: 18px;
  transition: all 0.3s ease;
}

.social-icon:hover {
  background: var(--gold);
  color: var(--bg-dark);
  box-shadow: 0 0 20px rgba(212, 175, 55, 0.6);
  transform: translateY(-3px);
}

.copyright {
  font-size: 10px;
  color: rgba(184, 169, 201, 0.5);
  letter-spacing: 1px;
}

/* ============================================================
   WATERMARK
============================================================ */
.watermark {
  position: fixed;
  bottom: 14px;
  right: 14px;
  z-index: 100;
  font-family: 'Cinzel', serif;
  font-weight: 700;
  font-size: 12px;
  letter-spacing: 2px;
  color: var(--gold);
  opacity: 0.55;
  text-shadow: 0 0 10px rgba(212, 175, 55, 0.5);
  pointer-events: none;
  animation: watermarkPulse 3s ease-in-out infinite;
}

@keyframes watermarkPulse {
  0%, 100% { opacity: 0.4; }
  50% { opacity: 0.75; }
}

/* ============================================================
   MUSIC TOGGLE BUTTON
============================================================ */
.music-toggle {
  position: fixed;
  top: 14px;
  right: 14px;
  z-index: 100;
  width: 42px;
  height: 42px;
  border-radius: 50%;
  border: 1px solid var(--border-gold);
  background: rgba(20, 8, 32, 0.85);
  backdrop-filter: blur(8px);
  color: var(--gold);
  font-size: 16px;
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.3s ease;
  box-shadow: 0 0 15px rgba(212, 175, 55, 0.3);
}

.music-toggle:hover {
  background: var(--gold);
  color: var(--bg-dark);
}

.music-toggle.playing {
  animation: musicPulse 1.5s ease-in-out infinite;
}

@keyframes musicPulse {
  0%, 100% { box-shadow: 0 0 15px rgba(212, 175, 55, 0.3); }
  50% { box-shadow: 0 0 30px rgba(212, 175, 55, 0.8); }
}

/* ============================================================
   CUSTOM MODAL / ALERT
============================================================ */
.modal-overlay {
  position: fixed;
  inset: 0;
  background: rgba(5, 2, 10, 0.85);
  backdrop-filter: blur(8px);
  -webkit-backdrop-filter: blur(8px);
  z-index: 1000;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 20px;
  opacity: 0;
  visibility: hidden;
  transition: all 0.4s ease;
}

.modal-overlay.active {
  opacity: 1;
  visibility: visible;
}

.modal-box {
  background: linear-gradient(145deg, #1a0a2a, #140820);
  border: 1px solid var(--gold);
  border-radius: 20px;
  padding: 30px 24px;
  max-width: 380px;
  width: 100%;
  text-align: center;
  box-shadow: 0 0 40px rgba(212, 175, 55, 0.5), inset 0 1px 0 rgba(255,255,255,0.08);
  transform: scale(0.85);
  transition: transform 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
}

.modal-overlay.active .modal-box {
  transform: scale(1);
}

.modal-icon {
  font-size: 48px;
  margin-bottom: 14px;
  animation: modalIconPop 0.6s ease;
}

@keyframes modalIconPop {
  0% { transform: scale(0); }
  70% { transform: scale(1.2); }
  100% { transform: scale(1); }
}

.modal-title {
  font-family: 'Cinzel', serif;
  font-size: 20px;
  font-weight: 700;
  letter-spacing: 3px;
  color: var(--gold-light);
  margin-bottom: 10px;
  text-transform: uppercase;
}

.modal-message {
  font-size: 13px;
  color: var(--text-muted);
  line-height: 1.6;
  margin-bottom: 22px;
}

.modal-btn {
  padding: 12px 32px;
  border: none;
  border-radius: 10px;
  background: linear-gradient(135deg, var(--gold), var(--gold-bright));
  color: #1a0a2a;
  font-family: 'Cinzel', serif;
  font-weight: 700;
  font-size: 12px;
  letter-spacing: 2px;
  text-transform: uppercase;
  cursor: pointer;
  transition: all 0.3s ease;
}

.modal-btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 5px 20px rgba(212, 175, 55, 0.6);
}

/* Modal error variant */
.modal-box.error {
  border-color: #ff4d6d;
  box-shadow: 0 0 40px rgba(255, 77, 109, 0.5), inset 0 1px 0 rgba(255,255,255,0.08);
}

.modal-box.error .modal-title {
  color: #ff8fa3;
}

.modal-box.error .modal-btn {
  background: linear-gradient(135deg, #ff4d6d, #ff8fa3);
}

/* ============================================================
   ERROR MESSAGE DI FORM
============================================================ */
.error-text {
  color: #ff6b81;
  font-size: 11px;
  margin-top: 5px;
  display: none;
  letter-spacing: 0.5px;
}

.form-group.invalid input,
.form-group.invalid textarea {
  border-color: #ff4d6d;
  box-shadow: 0 0 0 3px rgba(255, 77, 109, 0.15);
}

.form-group.invalid .error-text {
  display: block;
}

/* ============================================================
   SCROLL FADE-IN ANIMATION
============================================================ */
.reveal {
  opacity: 0;
  transform: translateY(30px);
  transition: opacity 0.8s ease, transform 0.8s ease;
}

.reveal.visible {
  opacity: 1;
  transform: translateY(0);
}

/* ============================================================
   CONFETTI
============================================================ */
#confettiCanvas {
  position: fixed;
  inset: 0;
  z-index: 999;
  pointer-events: none;
  display: none;
}

/* ============================================================
   RESPONSIVE FINE-TUNING
============================================================ */
@media (max-width: 360px) {
  .main-wrapper { padding: 30px 14px 70px; }
  .countdown-num { font-size: 18px; }
  .logo-title { letter-spacing: 4px; }
}

@media (min-height: 800px) {
  .main-wrapper { padding-top: 60px; }
}
</style>
</head>

<body>

<!-- ============ CANVAS PARTIKEL BINTANG ============ -->
<canvas id="starCanvas"></canvas>

<!-- ============ CANVAS CONFETTI ============ -->
<canvas id="confettiCanvas"></canvas>

<!-- ============ WATERMARK ============ -->
<div class="watermark">@vethera</div>

<!-- ============ MUSIC TOGGLE ============ -->
<button class="music-toggle" id="musicToggle" aria-label="Toggle music">♪</button>
<!-- Audio placeholder — ganti src dengan file musik kamu -->
<audio id="bgMusic" loop>
  <source src="" type="audio/mpeg">
</audio>

<!-- ============ MAIN WRAPPER ============ -->
<div class="main-wrapper">

  <!-- HEADER -->
  <header class="header reveal">
    <div class="crown-icon">👑</div>
    <h1 class="logo-title">VETHERA</h1>
    <div class="title-divider">
      <span class="line"></span>
      <span class="diamond">◆</span>
      <span class="line"></span>
    </div>
    <p class="subtitle" id="typingSubtitle"></p>
  </header>

  <!-- COUNTDOWN -->
  <section class="countdown-section reveal">
    <div class="countdown-label">⏳ Pendaftaran Ditutup Dalam</div>
    <div class="countdown-grid">
      <div class="countdown-box">
        <span class="countdown-num" id="cdDays">00</span>
        <span class="countdown-unit">Hari</span>
      </div>
      <div class="countdown-box">
        <span class="countdown-num" id="cdHours">00</span>
        <span class="countdown-unit">Jam</span>
      </div>
      <div class="countdown-box">
        <span class="countdown-num" id="cdMinutes">00</span>
        <span class="countdown-unit">Menit</span>
      </div>
      <div class="countdown-box">
        <span class="countdown-num" id="cdSeconds">00</span>
        <span class="countdown-unit">Detik</span>
      </div>
    </div>
  </section>

  <!-- FORM PENDAFTARAN -->
  <section class="form-section reveal">
    <h2 class="form-title">✦ Form Pendaftaran ✦</h2>
    <form id="registrationForm" novalidate>

      <div class="form-group" id="group-nama">
        <label for="nama">Nama Lengkap</label>
        <input type="text" id="nama" name="nama" placeholder="Masukkan nama lengkap kamu" autocomplete="name">
        <span class="error-text">Nama wajib diisi</span>
      </div>

      <div class="form-group" id="group-tiktok">
        <label for="tiktok">Username TikTok</label>
        <input type="text" id="tiktok" name="tiktok" placeholder="@username" autocomplete="off">
        <span class="error-text">Username TikTok wajib diisi</span>
      </div>

      <div class="form-group" id="group-umur">
        <label for="umur">Umur</label>
        <input type="number" id="umur" name="umur" placeholder="Contoh: 17" min="10" max="99">
        <span class="error-text">Umur wajib diisi (minimal 10 tahun)</span>
      </div>

      <div class="form-group" id="group-alasan">
        <label for="alasan">Alasan Ingin Join</label>
        <textarea id="alasan" name="alasan" placeholder="Ceritakan alasanmu ingin bergabung dengan Marga VETHERA..."></textarea>
        <span class="error-text">Alasan wajib diisi (minimal 20 karakter)</span>
      </div>

      <div class="form-group">
        <label for="foto">Upload Foto <span class="optional">(opsional)</span></label>
        <div class="file-upload-wrapper">
          <input type="file" id="foto" name="foto" accept="image/*">
          <div class="file-upload-display" id="fileDisplay">
            📷 <span>Pilih foto dari galeri</span>
          </div>
        </div>
      </div>

      <button type="submit" class="submit-btn" id="submitBtn">
        DAFTAR SEKARANG
      </button>
    </form>
  </section>

  <!-- SYARAT & KETENTUAN -->
  <section class="terms-section reveal">
    <h2 class="terms-title">✦ Syarat & Ketentuan ✦</h2>
    <ul class="terms-list">
      <li>Minimal umur 10 tahun dan memiliki akun TikTok aktif.</li>
      <li>Wajib follow akun resmi Marga VETHERA.</li>
      <li>Bersedia mengikuti seluruh peraturan marga.</li>
      <li>Tidak terlibat dalam drama atau konflik antar marga lain.</li>
      <li>Aktif dalam kegiatan dan konten marga VETHERA.</li>
      <li>Pendaftaran bersifat gratis, tidak dipungut biaya apapun.</li>
    </ul>
  </section>

  <!-- FOOTER -->
  <footer class="footer reveal">
    <p class="footer-text">Ikuti Kami</p>
    <div class="social-icons">
      <a href="#" class="social-icon" aria-label="TikTok" title="TikTok">
        <!-- SVG TikTok -->
        <svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor"><path d="M19.59 6.69a4.83 4.83 0 0 1-3.77-4.25V2h-3.45v13.67a2.89 2.89 0 0 1-5.2 1.74 2.89 2.89 0 0 1 2.31-4.64 2.93 2.93 0 0 1 .88.13V9.4a6.84 6.84 0 0 0-1-.05A6.33 6.33 0 0 0 5 20.1a6.34 6.34 0 0 0 10.86-4.43v-7a8.16 8.16 0 0 0 4.77 1.52v-3.4a4.85 4.85 0 0 1-1-.1z"/></svg>
      </a>
      <a href="#" class="social-icon" aria-label="Instagram" title="Instagram">
        <!-- SVG Instagram -->
        <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="2" y="2" width="20" height="20" rx="5" ry="5"/><path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"/><line x1="17.5" y1="6.5" x2="17.51" y2="6.5"/></svg>
      </a>
      <a href="#" class="social-icon" aria-label="Discord" title="Discord">
        <!-- SVG Discord -->
        <svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor"><path d="M20.32 4.37a19.8 19.8 0 0 0-4.89-1.52.07.07 0 0 0-.08.04 13.8 13.8 0 0 0-.61 1.25 18.3 18.3 0 0 0-5.48 0 12.7 12.7 0 0 0-.62-1.25.08.08 0 0 0-.08-.04 19.7 19.7 0 0 0-4.88 1.52.07.07 0 0 0-.03.03C.53 9.05-.32 13.58.1 18.06a.08.08 0 0 0 .03.05 19.9 19.9 0 0 0 6 3.03.08.08 0 0 0 .08-.03 14.2 14.2 0 0 0 1.23-2 .07.07 0 0 0-.04-.1 13.1 13.1 0 0 1-1.87-.89.08.08 0 0 1 0-.13c.13-.09.25-.19.37-.29a.07.07 0 0 1 .08-.01c3.93 1.79 8.18 1.79 12.06 0a.07.07 0 0 1 .08.01c.12.1.25.2.37.29a.08.08 0 0 1 0 .13 12.3 12.3 0 0 1-1.87.89.08.08 0 0 0-.04.1 16 16 0 0 0 1.23 2 .08.08 0 0 0 .08.03 19.8 19.8 0 0 0 6.02-3.03.08.08 0 0 0 .03-.05c.5-5.18-.84-9.68-3.55-13.66a.06.06 0 0 0-.03-.03zM8.02 15.33c-1.18 0-2.16-1.08-2.16-2.42s.96-2.42 2.16-2.42c1.21 0 2.18 1.1 2.16 2.42 0 1.34-.96 2.42-2.16 2.42zm7.97 0c-1.18 0-2.16-1.08-2.16-2.42s.96-2.42 2.16-2.42c1.21 0 2.18 1.1 2.16 2.42 0 1.34-.95 2.42-2.16 2.42z"/></svg>
      </a>
    </div>
    <p class="copyright">© 2025 MARGA VETHERA. All Rights Reserved.</p>
  </footer>

</div>

<!-- ============ CUSTOM MODAL ============ -->
<div class="modal-overlay" id="modalOverlay">
  <div class="modal-box" id="modalBox">
    <div class="modal-icon" id="modalIcon">✨</div>
    <h3 class="modal-title" id="modalTitle">Berhasil!</h3>
    <p class="modal-message" id="modalMessage"></p>
    <button class="modal-btn" id="modalBtn">TUTUP</button>
  </div>
</div>

<script>
/* ============================================================
   1. PARTIKEL BINTANG BERGERAK (CANVAS)
============================================================ */
(function initStars() {
  const canvas = document.getElementById('starCanvas');
  const ctx = canvas.getContext('2d');
  let stars = [];
  let w, h;

  function resize() {
    w = canvas.width = window.innerWidth;
    h = canvas.height = window.innerHeight;
    // Jumlah bintang menyesuaikan luas layar
    const count = Math.floor((w * h) / 12000);
    stars = [];
    for (let i = 0; i < count; i++) {
      stars.push({
        x: Math.random() * w,
        y: Math.random() * h,
        r: Math.random() * 1.6 + 0.4,
        speed: Math.random() * 0.3 + 0.08,
        alpha: Math.random() * 0.6 + 0.2,
        twinkle: Math.random() * Math.PI * 2,
        gold: Math.random() > 0.6
      });
    }
  }

  function draw() {
    ctx.clearRect(0, 0, w, h);
    for (const s of stars) {
      // Twinkle effect
      s.twinkle += 0.02;
      const twinkleAlpha = s.alpha * (0.6 + 0.4 * Math.sin(s.twinkle));

      ctx.beginPath();
      ctx.arc(s.x, s.y, s.r, 0, Math.PI * 2);
      ctx.fillStyle = s.gold
        ? `rgba(212, 175, 55, ${twinkleAlpha})`
        : `rgba(200, 180, 255, ${twinkleAlpha})`;
      ctx.shadowBlur = 8;
      ctx.shadowColor = s.gold ? 'rgba(212,175,55,0.8)' : 'rgba(160,120,255,0.7)';
      ctx.fill();

      // Gerak mengapung perlahan
      s.y -= s.speed;
      if (s.y < -5) {
        s.y = h + 5;
        s.x = Math.random() * w;
      }
    }
    ctx.shadowBlur = 0;
    requestAnimationFrame(draw);
  }

  window.addEventListener('resize', resize);
  resize();
  draw();
})();

/* ============================================================
   2. EFEK TYPING DI SUBJUDUL
============================================================ */
(function typeSubtitle() {
  const el = document.getElementById('typingSubtitle');
  const text = 'SELEKSI ANGGOTA MARGA';
  let i = 0;

  function type() {
    if (i < text.length) {
      el.innerHTML = text.substring(0, i + 1) + '<span class="cursor"></span>';
      i++;
      setTimeout(type, 90);
    } else {
      // Cursor berkedip terus setelah selesai
      el.innerHTML = text + '<span class="cursor"></span>';
    }
  }
  setTimeout(type, 800);
})();

/* ============================================================
   3. COUNTDOWN TIMER
============================================================ */
(function countdown() {
  // 👉 UBAH TANGGAL SELEKSI DI SINI
  const targetDate = new Date('2025-12-31T23:59:59').getTime();

  const dEl = document.getElementById('cdDays');
  const hEl = document.getElementById('cdHours');
  const mEl = document.getElementById('cdMinutes');
  const sEl = document.getElementById('cdSeconds');

  function pad(n) { return String(n).padStart(2, '0'); }

  function update() {
    const now = Date.now();
    const diff = targetDate - now;

    if (diff <= 0) {
      dEl.textContent = hEl.textContent = mEl.textContent = sEl.textContent = '00';
      return;
    }

    const days = Math.floor(diff / (1000 * 60 * 60 * 24));
    const hours = Math.floor((diff / (1000 * 60 * 60)) % 24);
    const minutes = Math.floor((diff / (1000 * 60)) % 60);
    const seconds = Math.floor((diff / 1000) % 60);

    dEl.textContent = pad(days);
    hEl.textContent = pad(hours);
    mEl.textContent = pad(minutes);
    sEl.textContent = pad(seconds);
  }

  update();
  setInterval(update, 1000);
})();

/* ============================================================
   4. SCROLL REVEAL ANIMATION
============================================================ */
(function scrollReveal() {
  const reveals = document.querySelectorAll('.reveal');
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.classList.add('visible');
        observer.unobserve(entry.target);
      }
    });
  }, { threshold: 0.15 });

  reveals.forEach((el, i) => {
    el.style.transitionDelay = (i * 0.08) + 's';
    observer.observe(el);
  });
})();

/* ============================================================
   5. FILE UPLOAD DISPLAY
============================================================ */
(function fileUpload() {
  const input = document.getElementById('foto');
  const display = document.getElementById('fileDisplay');

  input.addEventListener('change', function () {
    if (this.files && this.files[0]) {
      const name = this.files[0].name;
      // Potong nama jika terlalu panjang
      const shortName = name.length > 22 ? name.substring(0, 19) + '...' : name;
      display.innerHTML = '✅ <span>' + shortName + '</span>';
      display.style.borderColor = 'var(--gold-bright)';
      display.style.color = 'var(--gold-light)';
    }
  });
})();

/* ============================================================
   6. MUSIC TOGGLE
============================================================ */
(function musicToggle() {
  const btn = document.getElementById('musicToggle');
  const audio = document.getElementById('bgMusic');
  let playing = false;

  btn.addEventListener('click', function () {
    // Jika tidak ada source, beri tahu user
    if (!audio.querySelector('source').src) {
      showModal('info', '🎵', 'Musik Belum Tersedia',
        'Tambahkan file musik pada tag <audio> untuk mengaktifkan fitur ini.');
      return;
    }

    if (playing) {
      audio.pause();
      btn.textContent = '♪';
      btn.classList.remove('playing');
    } else {
      audio.play().catch(() => {
        showModal('info', '🎵', 'Tidak Bisa Memutar',
          'Browser memblokir autoplay. Coba lagi setelah interaksi.');
      });
      btn.textContent = '❚❚';
      btn.classList.add('playing');
    }
    playing = !playing;
  });
})();

/* ============================================================
   7. CUSTOM MODAL
============================================================ */
let modalCallback = null;
function showModal(type, icon, title, message, callback) {
  const overlay = document.getElementById('modalOverlay');
  const box = document.getElementById('modalBox');
  const iconEl = document.getElementById('modalIcon');
  const titleEl = document.getElementById('modalTitle');
  const msgEl = document.getElementById('modalMessage');

  iconEl.textContent = icon;
  titleEl.textContent = title;
  msgEl.innerHTML = message;

  box.classList.remove('error');
  if (type === 'error') box.classList.add('error');

  modalCallback = callback || null;
  overlay.classList.add('active');
}

document.getElementById('modalBtn').addEventListener('click', () => {
  const overlay = document.getElementById('modalOverlay');
  overlay.classList.remove('active');
  if (modalCallback) {
    const cb = modalCallback;
    modalCallback = null;
    setTimeout(cb, 300);
  }
});

// Tutup modal dengan klik overlay
document.getElementById('modalOverlay').addEventListener('click', (e) => {
  if (e.target.id === 'modalOverlay') {
    document.getElementById('modalBtn').click();
  }
});

/* ============================================================
   8. VALIDASI FORM & SUBMIT
============================================================ */
(function formHandler() {
  const form = document.getElementById('registrationForm');
  const submitBtn = document.getElementById('submitBtn');

  // Fungsi set error
  function setError(groupId, message) {
    const group = document.getElementById(groupId);
    group.classList.add('invalid');
    group.querySelector('.error-text').textContent = message;
  }

  function clearError(groupId) {
    const group = document.getElementById(groupId);
    group.classList.remove('invalid');
  }

  // Hapus error saat user mengetik
  ['nama', 'tiktok', 'umur', 'alasan'].forEach(id => {
    const input = document.getElementById(id);
    input.addEventListener('input', () => clearError('group-' + id));
  });

  // Validasi
  function validate() {
    let valid = true;

    const nama = document.getElementById('nama').value.trim();
    const tiktok = document.getElementById('tiktok').value.trim();
    const umur = document.getElementById('umur').value.trim();
    const alasan = document.getElementById('alasan').value.trim();

    if (nama.length < 3) {
      setError('group-nama', 'Nama minimal 3 karakter');
      valid = false;
    } else clearError('group-nama');

    if (tiktok.length < 2) {
      setError('group-tiktok', 'Username TikTok wajib diisi');
      valid = false;
    } else clearError('group-tiktok');

    const umurNum = parseInt(umur, 10);
    if (!umur || isNaN(umurNum) || umurNum < 10 || umurNum > 99) {
      setError('group-umur', 'Umur harus antara 10 - 99 tahun');
      valid = false;
    } else clearError('group-umur');

    if (alasan.length < 20) {
      setError('group-alasan', 'Alasan minimal 20 karakter');
      valid = false;
    } else clearError('group-alasan');

    return valid;
  }

  form.addEventListener('submit', function (e) {
    e.preventDefault();

    if (!validate()) {
      showModal('error', '⚠️', 'Data Belum Lengkap',
        'Mohon periksa kembali form pendaftaran kamu sebelum mengirim.');
      return;
    }

    // Loading state
    submitBtn.disabled = true;
    const originalText = submitBtn.innerHTML;
    submitBtn.innerHTML = '<span class="spinner"></span>MENGIRIM...';

    // Simulasi proses pengiriman (ganti dengan fetch ke server)
    setTimeout(() => {
      submitBtn.disabled = false;
      submitBtn.innerHTML = originalText;

      const nama = document.getElementById('nama').value.trim();

      // Tampilkan modal sukses
      showModal('success', '👑', 'Pendaftaran Berhasil!',
        `Selamat <strong>${nama}</strong>!<br><br>
         Pendaftaranmu telah kami terima.<br>
         Tunggu pengumuman seleksi berikutnya.<br><br>
         <span style="color:var(--gold);font-size:11px;letter-spacing:2px;">— MARGA VETHERA —</span>`,
        () => {
          form.reset();
          document.getElementById('fileDisplay').innerHTML = '📷 <span>Pilih foto dari galeri</span>';
          document.getElementById('fileDisplay').style.borderColor = '';
          document.getElementById('fileDisplay').style.color = '';
        }
      );

      // Konfeti
      launchConfetti();

      // Log data (bisa diintegrasikan ke Google Sheets / server)
      console.log('Data Pendaftar:', {
        nama,
        tiktok: document.getElementById('tiktok').value,
        umur: document.getElementById('umur').value,
        alasan: document.getElementById('alasan').value,
        waktu: new Date().toISOString()
      });
    }, 1800);
  });
})();

/* ============================================================
   9. CONFETTI ANIMATION
============================================================ */
function launchConfetti() {
  const canvas = document.getElementById('confettiCanvas');
  const ctx = canvas.getContext('2d');
  canvas.style.display = 'block';

  let w = canvas.width = window.innerWidth;
  let h = canvas.height = window.innerHeight;

  const colors = ['#d4af37', '#ffd700', '#f4e5a1', '#9c27b0', '#ffffff', '#6a1b9a'];
  const pieces = [];
  const count = 150;

  for (let i = 0; i < count; i++) {
    pieces.push({
      x: Math.random() * w,
      y: Math.random() * -h,
      w: Math.random() * 8 + 4,
      h: Math.random() * 6 + 3,
      color: colors[Math.floor(Math.random() * colors.length)],
      vy: Math.random() * 3 + 2,
      vx: Math.random() * 2 - 1,
      rot: Math.random() * Math.PI * 2,
      vRot: Math.random() * 0.2 - 0.1,
      opacity: 1
    });
  }

  let startTime = Date.now();

  function animate() {
    ctx.clearRect(0, 0, w, h);

    pieces.forEach(p => {
      p.x += p.vx;
      p.y += p.vy;
      p.rot += p.vRot;
      p.vy += 0.05; // gravity

      // Fade out setelah 2.5 detik
      if (Date.now() - startTime > 2500) {
        p.opacity -= 0.02;
      }

      ctx.save();
      ctx.translate(p.x, p.y);
      ctx.rotate(p.rot);
      ctx.globalAlpha = Math.max(p.opacity, 0);
      ctx.fillStyle = p.color;
      ctx.fillRect(-p.w / 2, -p.h / 2, p.w, p.h);
      ctx.restore();
    });

    // Cek apakah perlu berhenti
    const allFaded = pieces.every(p => p.opacity <= 0);
    const allOffScreen = pieces.every(p => p.y > h + 20);

    if (allFaded || allOffScreen) {
      canvas.style.display = 'none';
      ctx.clearRect(0, 0, w, h);
    } else {
      requestAnimationFrame(animate);
    }
  }

  animate();
}

/* ============================================================
   10. HANDLE RESIZE UNTUK CANVAS CONFETTI
============================================================ */
window.addEventListener('resize', () => {
  const canvas = document.getElementById('confettiCanvas');
  canvas.width = window.innerWidth;
  canvas.height = window.innerHeight;
});
</script>

</body>
</html>
