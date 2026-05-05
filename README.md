<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Kurangi Kantong Plastik – Mulai Dari Kita</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700;900&family=DM+Sans:ital,wght@0,300;0,400;0,600;1,300&display=swap" rel="stylesheet">
<style>
  :root {
    --hijau: #1a6b3c;
    --hijau-muda: #2d9e5f;
    --hijau-terang: #4fc97f;
    --krem: #f5f0e8;
    --coklat: #3d2b1f;
    --kuning: #e8c84a;
    --merah: #c0392b;
    --putih: #fafaf7;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--putih);
    color: var(--coklat);
    overflow-x: hidden;
  }

  /* NAV */
  nav {
    position: fixed; top: 0; width: 100%; z-index: 100;
    background: rgba(245,240,232,0.92);
    backdrop-filter: blur(10px);
    border-bottom: 2px solid var(--hijau);
    display: flex; align-items: center; justify-content: space-between;
    padding: 14px 40px;
  }
  .nav-logo {
    font-family: 'Playfair Display', serif;
    font-size: 1.2rem; font-weight: 900;
    color: var(--hijau);
    letter-spacing: -0.5px;
  }
  .nav-logo span { color: var(--coklat); }
  nav ul { list-style: none; display: flex; gap: 30px; }
  nav ul li a {
    text-decoration: none; font-size: 0.85rem; font-weight: 600;
    color: var(--coklat); letter-spacing: 0.5px;
    transition: color 0.2s;
  }
  nav ul li a:hover { color: var(--hijau-muda); }

  /* HERO */
  .hero {
    min-height: 100vh;
    background: var(--hijau);
    display: flex; align-items: center; justify-content: center;
    flex-direction: column;
    text-align: center;
    padding: 100px 40px 60px;
    position: relative;
    overflow: hidden;
  }
  .hero::before {
    content: '';
    position: absolute; inset: 0;
    background:
      radial-gradient(ellipse at 20% 50%, rgba(77,201,127,0.18) 0%, transparent 60%),
      radial-gradient(ellipse at 80% 20%, rgba(232,200,74,0.12) 0%, transparent 50%);
  }
  .leaf-bg {
    position: absolute; inset: 0;
    background-image: url("data:image/svg+xml,%3Csvg width='60' height='60' viewBox='0 0 60 60' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='none' fill-rule='evenodd'%3E%3Cg fill='%234fc97f' fill-opacity='0.07'%3E%3Cpath d='M36 34v-4h-2v4h-4v2h4v4h2v-4h4v-2h-4zm0-30V0h-2v4h-4v2h4v4h2V6h4V4h-4zM6 34v-4H4v4H0v2h4v4h2v-4h4v-2H6zM6 4V0H4v4H0v2h4v4h2V6h4V4H6z'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E");
  }
  .hero-emoji {
    font-size: 5rem; margin-bottom: 20px;
    animation: float 3s ease-in-out infinite;
    position: relative; z-index: 1;
  }
  @keyframes float {
    0%,100%{transform:translateY(0)} 50%{transform:translateY(-12px)}
  }
  .hero h1 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2.5rem, 6vw, 4.5rem);
    color: var(--krem);
    line-height: 1.1;
    max-width: 800px;
    position: relative; z-index: 1;
    animation: fadeUp 0.8s ease both;
  }
  .hero h1 em { color: var(--kuning); font-style: normal; }
  .hero p {
    color: rgba(245,240,232,0.82);
    font-size: 1.1rem; max-width: 560px;
    margin: 22px auto 0;
    line-height: 1.7; position: relative; z-index: 1;
    animation: fadeUp 0.8s 0.2s ease both;
    font-weight: 300;
  }
  .hero-cta {
    display: flex; gap: 16px; flex-wrap: wrap; justify-content: center;
    margin-top: 36px; position: relative; z-index: 1;
    animation: fadeUp 0.8s 0.4s ease both;
  }
  .btn-utama {
    background: var(--kuning); color: var(--coklat);
    border: none; padding: 14px 32px;
    font-family: 'DM Sans', sans-serif;
    font-size: 0.95rem; font-weight: 600;
    border-radius: 50px; cursor: pointer;
    text-decoration: none;
    transition: transform 0.2s, box-shadow 0.2s;
    box-shadow: 0 4px 20px rgba(232,200,74,0.4);
  }
  .btn-utama:hover { transform: translateY(-2px); box-shadow: 0 8px 30px rgba(232,200,74,0.5); }
  .btn-outline {
    background: transparent; color: var(--krem);
    border: 2px solid rgba(245,240,232,0.5);
    padding: 14px 32px; border-radius: 50px;
    font-family: 'DM Sans', sans-serif;
    font-size: 0.95rem; font-weight: 600;
    cursor: pointer; text-decoration: none;
    transition: border-color 0.2s, background 0.2s;
  }
  .btn-outline:hover { border-color: var(--krem); background: rgba(255,255,255,0.08); }
  .scroll-arrow {
    position: absolute; bottom: 30px; left: 50%;
    transform: translateX(-50%);
    color: rgba(245,240,232,0.5); font-size: 1.6rem;
    animation: bounce 2s infinite;
  }
  @keyframes bounce { 0%,100%{transform:translateX(-50%) translateY(0)} 50%{transform:translateX(-50%) translateY(8px)} }
  @keyframes fadeUp { from{opacity:0;transform:translateY(30px)} to{opacity:1;transform:translateY(0)} }

  /* STATS STRIP */
  .stats-strip {
    background: var(--coklat);
    display: flex; flex-wrap: wrap; justify-content: center;
    gap: 0; overflow: hidden;
  }
  .stat-item {
    padding: 28px 40px; text-align: center;
    border-right: 1px solid rgba(245,240,232,0.12);
    flex: 1; min-width: 200px;
    transition: background 0.3s;
  }
  .stat-item:hover { background: rgba(77,201,127,0.12); }
  .stat-item:last-child { border-right: none; }
  .stat-num {
    font-family: 'Playfair Display', serif;
    font-size: 2.4rem; color: var(--kuning); font-weight: 900;
  }
  .stat-label { color: rgba(245,240,232,0.7); font-size: 0.8rem; margin-top: 4px; font-weight: 300; }

  /* SECTION BASE */
  section { padding: 80px 40px; }
  .section-tag {
    display: inline-block;
    background: var(--hijau);
    color: var(--krem); font-size: 0.72rem;
    font-weight: 600; letter-spacing: 2px;
    padding: 6px 14px; border-radius: 50px;
    text-transform: uppercase; margin-bottom: 16px;
  }
  .section-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2rem, 4vw, 3rem);
    line-height: 1.15; color: var(--coklat);
    max-width: 640px;
  }
  .section-title em { color: var(--hijau); font-style: normal; }
  .section-desc {
    color: #6b5b4e; font-size: 1rem; max-width: 560px;
    line-height: 1.8; margin-top: 14px; font-weight: 300;
  }

  /* DAMPAK */
  .dampak-section { background: var(--krem); }
  .dampak-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 24px; margin-top: 48px;
  }
  .dampak-card {
    background: var(--putih);
    border-radius: 20px; padding: 32px 28px;
    border: 1px solid rgba(26,107,60,0.1);
    transition: transform 0.3s, box-shadow 0.3s;
    position: relative; overflow: hidden;
  }
  .dampak-card::before {
    content: ''; position: absolute;
    top: 0; left: 0; right: 0; height: 4px;
    background: var(--hijau-muda);
  }
  .dampak-card:hover { transform: translateY(-6px); box-shadow: 0 16px 40px rgba(26,107,60,0.12); }
  .dampak-icon { font-size: 2.4rem; margin-bottom: 16px; }
  .dampak-card h3 {
    font-family: 'Playfair Display', serif;
    font-size: 1.2rem; color: var(--coklat); margin-bottom: 10px;
  }
  .dampak-card p { color: #7a6b60; font-size: 0.9rem; line-height: 1.7; font-weight: 300; }

  /* SURVEY RESULTS */
  .survey-section { background: var(--hijau); }
  .survey-section .section-tag { background: var(--kuning); color: var(--coklat); }
  .survey-section .section-title { color: var(--krem); }
  .survey-section .section-title em { color: var(--kuning); }
  .survey-section .section-desc { color: rgba(245,240,232,0.7); }

  .survey-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 24px; margin-top: 48px;
  }
  .survey-card {
    background: rgba(255,255,255,0.07);
    border: 1px solid rgba(255,255,255,0.15);
    border-radius: 20px; padding: 28px;
    backdrop-filter: blur(8px);
  }
  .survey-card h4 {
    font-family: 'DM Sans', sans-serif;
    font-size: 0.88rem; font-weight: 600;
    color: rgba(245,240,232,0.75); margin-bottom: 18px;
    letter-spacing: 0.3px; line-height: 1.5;
  }
  .bar-item { margin-bottom: 12px; }
  .bar-label-row {
    display: flex; justify-content: space-between;
    margin-bottom: 5px;
  }
  .bar-label { font-size: 0.8rem; color: rgba(245,240,232,0.8); }
  .bar-pct { font-size: 0.8rem; color: var(--kuning); font-weight: 600; }
  .bar-track {
    background: rgba(255,255,255,0.1);
    border-radius: 10px; height: 8px; overflow: hidden;
  }
  .bar-fill {
    height: 100%; border-radius: 10px;
    background: linear-gradient(90deg, var(--hijau-terang), var(--kuning));
    transition: width 1.2s cubic-bezier(.4,0,.2,1);
    width: 0;
  }
  .bar-fill.animated { width: var(--target-width); }

  /* PERBANDINGAN */
  .perbandingan-section { background: var(--putih); }
  .pasar-grid {
    display: grid; grid-template-columns: 1fr 1fr; gap: 28px;
    margin-top: 48px;
  }
  @media(max-width:640px){ .pasar-grid { grid-template-columns: 1fr; } }
  .pasar-card {
    border-radius: 24px; padding: 36px 30px;
    position: relative; overflow: hidden;
  }
  .pasar-card.tradisional { background: #fff8ee; border: 2px solid #e8c84a; }
  .pasar-card.modern { background: #edf7f2; border: 2px solid var(--hijau-muda); }
  .pasar-badge {
    display: inline-flex; align-items: center; gap: 8px;
    font-size: 0.78rem; font-weight: 600; letter-spacing: 1px;
    text-transform: uppercase; padding: 6px 14px;
    border-radius: 50px; margin-bottom: 20px;
  }
  .tradisional .pasar-badge { background: #fdeec3; color: #7a5a00; }
  .modern .pasar-badge { background: #c5edd9; color: var(--hijau); }
  .pasar-card h3 {
    font-family: 'Playfair Display', serif;
    font-size: 1.6rem; margin-bottom: 20px;
  }
  .tradisional h3 { color: var(--coklat); }
  .modern h3 { color: var(--hijau); }
  .pasar-stat {
    display: flex; gap: 10px; align-items: flex-start;
    margin-bottom: 14px;
  }
  .pasar-stat-icon { font-size: 1.2rem; margin-top: 2px; }
  .pasar-stat p { font-size: 0.9rem; color: #5a4e45; line-height: 1.6; font-weight: 300; }
  .pasar-stat p strong { font-weight: 600; color: var(--coklat); }
  .big-pct {
    font-family: 'Playfair Display', serif;
    font-size: 3.5rem; font-weight: 900; line-height: 1;
    margin: 20px 0 6px;
  }
  .tradisional .big-pct { color: var(--kuning); }
  .modern .big-pct { color: var(--hijau-muda); }
  .big-pct-label { font-size: 0.85rem; color: #7a6b60; font-weight: 300; }

  /* TIPS */
  .tips-section { background: var(--krem); }
  .tips-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 20px; margin-top: 48px;
  }
  .tip-card {
    background: var(--putih); border-radius: 20px;
    padding: 30px 24px; text-align: center;
    border: 1px solid rgba(26,107,60,0.1);
    transition: transform 0.3s, border-color 0.3s;
    cursor: default;
  }
  .tip-card:hover { transform: translateY(-4px); border-color: var(--hijau-muda); }
  .tip-card .tip-emoji { font-size: 2.6rem; margin-bottom: 14px; display: block; }
  .tip-card h4 {
    font-family: 'Playfair Display', serif;
    font-size: 1.05rem; color: var(--coklat); margin-bottom: 8px;
  }
  .tip-card p { font-size: 0.85rem; color: #7a6b60; line-height: 1.6; font-weight: 300; }
  .tip-num {
    display: inline-block;
    background: var(--hijau); color: var(--krem);
    width: 28px; height: 28px; border-radius: 50%;
    font-size: 0.8rem; font-weight: 600;
    line-height: 28px; text-align: center;
    margin-bottom: 12px;
  }

  /* PLEDGE */
  .pledge-section {
    background: var(--coklat);
    text-align: center; padding: 80px 40px;
  }
  .pledge-section .section-title { color: var(--krem); margin: 0 auto; text-align: center; }
  .pledge-section .section-title em { color: var(--kuning); }
  .pledge-section p {
    color: rgba(245,240,232,0.65); font-size: 1rem;
    max-width: 520px; margin: 16px auto 36px;
    line-height: 1.8; font-weight: 300;
  }
  .pledge-actions { display: flex; gap: 16px; justify-content: center; flex-wrap: wrap; }

  /* FOOTER */
  footer {
    background: #1a1208;
    padding: 40px;
    display: flex; flex-wrap: wrap;
    align-items: center; justify-content: space-between;
    gap: 20px;
  }
  .footer-brand {
    font-family: 'Playfair Display', serif;
    color: var(--krem); font-size: 1.1rem; font-weight: 700;
  }
  .footer-brand span { color: var(--hijau-terang); }
  footer p {
    color: rgba(245,240,232,0.4);
    font-size: 0.8rem; text-align: center; flex: 1;
    line-height: 1.6;
  }
  .footer-credit {
    color: rgba(245,240,232,0.35); font-size: 0.75rem;
  }

  /* RESPONSIVE */
  @media(max-width: 768px) {
    nav ul { display: none; }
    nav { padding: 14px 20px; }
    section { padding: 60px 20px; }
    .hero { padding: 100px 24px 60px; }
    .stats-strip .stat-item { padding: 20px 24px; }
    footer { padding: 30px 20px; }
  }

  /* SCROLL REVEAL */
  .reveal {
    opacity: 0; transform: translateY(30px);
    transition: opacity 0.7s ease, transform 0.7s ease;
  }
  .reveal.visible { opacity: 1; transform: translateY(0); }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-logo">Bijak<span>Plastik</span></div>
  <ul>
    <li><a href="#dampak">Dampak</a></li>
    <li><a href="#survei">Data Survei</a></li>
    <li><a href="#tips">Solusi</a></li>
    <li><a href="#janji">Komitmen</a></li>
  </ul>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="leaf-bg"></div>
  <div class="hero-emoji">🛍️</div>
  <h1>Saatnya Kita <em>Bijak</em><br>Soal Kantong Plastik</h1>
  <p>Setiap hari, jutaan kantong plastik berakhir di lingkungan kita. Mulai dari pasar tradisional hingga supermarket modern — saatnya kita berubah bersama.</p>
  <div class="hero-cta">
    <a href="#survei" class="btn-utama">Lihat Data Survei</a>
    <a href="#tips" class="btn-outline">Tips Mengurangi Plastik</a>
  </div>
  <div class="scroll-arrow">↓</div>
</section>

<!-- STATS -->
<div class="stats-strip">
  <div class="stat-item">
    <div class="stat-num">12,4 Jt</div>
    <div class="stat-label">Ton sampah diproyeksikan 2025 (KLHK)</div>
  </div>
  <div class="stat-item">
    <div class="stat-num">80%</div>
    <div class="stat-label">Berasal dari kemasan & kantong belanja</div>
  </div>
  <div class="stat-item">
    <div class="stat-num">500 th</div>
    <div class="stat-label">Waktu terurai plastik di alam</div>
  </div>
  <div class="stat-item">
    <div class="stat-num">42</div>
    <div class="stat-label">Responden dalam survei ini</div>
  </div>
</div>

<!-- DAMPAK -->
<section class="dampak-section" id="dampak">
  <div class="section-tag">⚠ Dampak Lingkungan</div>
  <h2 class="section-title">Mengapa Kantong Plastik <em>Berbahaya?</em></h2>
  <p class="section-desc">Plastik sekali pakai merusak ekosistem darat, sungai, dan laut. Dampaknya nyata dan bisa dirasakan generasi mendatang.</p>

  <div class="dampak-grid">
    <div class="dampak-card reveal">
      <div class="dampak-icon">🌊</div>
      <h3>Mencemari Perairan</h3>
      <p>Kantong plastik mencemari sungai dan laut, mengancam kehidupan biota air. Ikan dan penyu kerap memakan plastik yang terlihat seperti makanan mereka.</p>
    </div>
    <div class="dampak-card reveal">
      <div class="dampak-icon">🌍</div>
      <h3>Merusak Tanah</h3>
      <p>Plastik yang terkubur di tanah menghambat penyerapan air dan nutrisi. Mikroplastik dari plastik yang terurai masuk ke dalam rantai makanan kita.</p>
    </div>
    <div class="dampak-card reveal">
      <div class="dampak-icon">💨</div>
      <h3>Emisi Karbon</h3>
      <p>PBB memperkirakan plastik menyumbang lebih dari 15% emisi karbon metana dari sampah global, mempercepat perubahan iklim yang sudah mengkhawatirkan.</p>
    </div>
    <div class="dampak-card reveal">
      <div class="dampak-icon">🐾</div>
      <h3>Ancam Keanekaragaman Hayati</h3>
      <p>Satwa liar kerap terjerat atau menelan sampah plastik. Lebih dari 800 spesies hewan terdampak oleh polusi plastik di seluruh dunia.</p>
    </div>
  </div>
</section>

<!-- SURVEI -->
<section class="survey-section" id="survei">
  <div class="section-tag">📊 Hasil Survei</div>
  <h2 class="section-title">Data Nyata dari <em>Masyarakat Kita</em></h2>
  <p class="section-desc">Survei dilakukan terhadap 42 responden dari berbagai usia dan latar belakang pekerjaan mengenai kebiasaan penggunaan kantong plastik saat berbelanja.</p>

  <div class="survey-grid">
    <!-- P2: Kantong plastik pasar tradisional -->
    <div class="survey-card reveal">
      <h4>🏪 Penggunaan kantong plastik saat belanja di Pasar Tradisional</h4>
      <div class="bar-item">
        <div class="bar-label-row"><span class="bar-label">Sangat Sering</span><span class="bar-pct">33%</span></div>
        <div class="bar-track"><div class="bar-fill" style="--target-width:33%"></div></div>
      </div>
      <div class="bar-item">
        <div class="bar-label-row"><span class="bar-label">Sering</span><span class="bar-pct">33%</span></div>
        <div class="bar-track"><div class="bar-fill" style="--target-width:33%"></div></div>
      </div>
      <div class="bar-item">
        <div class="bar-label-row"><span class="bar-label">Kadang-Kadang</span><span class="bar-pct">17%</span></div>
        <div class="bar-track"><div class="bar-fill" style="--target-width:17%"></div></div>
      </div>
      <div class="bar-item">
        <div class="bar-label-row"><span class="bar-label">Jarang</span><span class="bar-pct">14%</span></div>
        <div class="bar-track"><div class="bar-fill" style="--target-width:14%"></div></div>
      </div>
      <div class="bar-item">
        <div class="bar-label-row"><span class="bar-label">Tidak Pernah</span><span class="bar-pct">2%</span></div>
        <div class="bar-track"><div class="bar-fill" style="--target-width:2%"></div></div>
      </div>
    </div>

    <!-- P5: Kantong plastik pasar modern -->
    <div class="survey-card reveal">
      <h4>🏬 Penggunaan kantong plastik saat belanja di Pasar Modern</h4>
      <div class="bar-item">
        <div class="bar-label-row"><span class="bar-label">Sering</span><span class="bar-pct">33%</span></div>
        <div class="bar-track"><div class="bar-fill" style="--target-width:33%"></div></div>
      </div>
      <div class="bar-item">
        <div class="bar-label-row"><span class="bar-label">Sangat Sering</span><span class="bar-pct">24%</span></div>
        <div class="bar-track"><div class="bar-fill" style="--target-width:24%"></div></div>
      </div>
      <div class="bar-item">
        <div class="bar-label-row"><span class="bar-label">Kadang-Kadang</span><span class="bar-pct">21%</span></div>
        <div class="bar-track"><div class="bar-fill" style="--target-width:21%"></div></div>
      </div>
      <div class="bar-item">
        <div class="bar-label-row"><span class="bar-label">Jarang</span><span class="bar-pct">14%</span></div>
        <div class="bar-track"><div class="bar-fill" style="--target-width:14%"></div></div>
      </div>
      <div class="bar-item">
        <div class="bar-label-row"><span class="bar-label">Tidak Pernah</span><span class="bar-pct">7%</span></div>
        <div class="bar-track"><div class="bar-fill" style="--target-width:7%"></div></div>
      </div>
    </div>

    <!-- P7: Setuju plastik cemari lingkungan -->
    <div class="survey-card reveal">
      <h4>♻️ Kantong plastik dapat mencemari lingkungan</h4>
      <div class="bar-item">
        <div class="bar-label-row"><span class="bar-label">Sangat Setuju</span><span class="bar-pct">60%</span></div>
        <div class="bar-track"><div class="bar-fill" style="--target-width:60%"></div></div>
      </div>
      <div class="bar-item">
        <div class="bar-label-row"><span class="bar-label">Setuju</span><span class="bar-pct">29%</span></div>
        <div class="bar-track"><div class="bar-fill" style="--target-width:29%"></div></div>
      </div>
      <div class="bar-item">
        <div class="bar-label-row"><span class="bar-label">Netral</span><span class="bar-pct">10%</span></div>
        <div class="bar-track"><div class="bar-fill" style="--target-width:10%"></div></div>
      </div>
      <div class="bar-item">
        <div class="bar-label-row"><span class="bar-label">Tidak Setuju</span><span class="bar-pct">2%</span></div>
        <div class="bar-track"><div class="bar-fill" style="--target-width:2%"></div></div>
      </div>
    </div>

    <!-- P10: Setuju pembatasan di pasar modern -->
    <div class="survey-card reveal">
      <h4>🚫 Setuju pembatasan kantong plastik di Pasar Modern</h4>
      <div class="bar-item">
        <div class="bar-label-row"><span class="bar-label">Sangat Setuju</span><span class="bar-pct">43%</span></div>
        <div class="bar-track"><div class="bar-fill" style="--target-width:43%"></div></div>
      </div>
      <div class="bar-item">
        <div class="bar-label-row"><span class="bar-label">Setuju</span><span class="bar-pct">29%</span></div>
        <div class="bar-track"><div class="bar-fill" style="--target-width:29%"></div></div>
      </div>
      <div class="bar-item">
        <div class="bar-label-row"><span class="bar-label">Netral</span><span class="bar-pct">24%</span></div>
        <div class="bar-track"><div class="bar-fill" style="--target-width:24%"></div></div>
      </div>
      <div class="bar-item">
        <div class="bar-label-row"><span class="bar-label">Sangat Tidak Setuju</span><span class="bar-pct">5%</span></div>
        <div class="bar-track"><div class="bar-fill" style="--target-width:5%"></div></div>
      </div>
    </div>
  </div>
</section>

<!-- PERBANDINGAN -->
<section class="perbandingan-section" id="perbandingan">
  <div class="section-tag">🆚 Perbandingan</div>
  <h2 class="section-title">Pasar Tradisional vs <em>Pasar Modern</em></h2>
  <p class="section-desc">Pola penggunaan kantong plastik berbeda di antara dua jenis tempat belanja. Yuk kenali datanya!</p>

  <div class="pasar-grid">
    <div class="pasar-card tradisional reveal">
      <div class="pasar-badge">🛒 Pasar Tradisional</div>
      <h3>Kebiasaan di Pasar Tradisional</h3>
      <div class="big-pct">66%</div>
      <p class="big-pct-label">responden sering atau sangat sering pakai kantong plastik</p>
      <br>
      <div class="pasar-stat">
        <span class="pasar-stat-icon">📦</span>
        <p><strong>45%</strong> responden hanya kadang-kadang berbelanja di pasar tradisional</p>
      </div>
      <div class="pasar-stat">
        <span class="pasar-stat-icon">👜</span>
        <p>Hanya <strong>19%</strong> yang sering atau sangat sering membawa tas belanja sendiri</p>
      </div>
      <div class="pasar-stat">
        <span class="pasar-stat-icon">✅</span>
        <p><strong>62%</strong> setuju atau sangat setuju pembatasan kantong plastik di sini</p>
      </div>
    </div>

    <div class="pasar-card modern reveal">
      <div class="pasar-badge">🏬 Pasar Modern</div>
      <h3>Kebiasaan di Pasar Modern</h3>
      <div class="big-pct">57%</div>
      <p class="big-pct-label">responden sering atau sangat sering pakai kantong plastik</p>
      <br>
      <div class="pasar-stat">
        <span class="pasar-stat-icon">🛍️</span>
        <p><strong>55%</strong> responden sering atau sangat sering berbelanja di pasar modern</p>
      </div>
      <div class="pasar-stat">
        <span class="pasar-stat-icon">👜</span>
        <p>Sebanyak <strong>33%</strong> sudah sering atau sangat sering bawa tas sendiri</p>
      </div>
      <div class="pasar-stat">
        <span class="pasar-stat-icon">✅</span>
        <p><strong>72%</strong> setuju atau sangat setuju pembatasan di pasar modern</p>
      </div>
    </div>
  </div>
</section>

<!-- TIPS -->
<section class="tips-section" id="tips">
  <div class="section-tag">💡 Solusi</div>
  <h2 class="section-title">Langkah Kecil, Dampak <em>Besar</em></h2>
  <p class="section-desc">Mengurangi kantong plastik tidak harus rumit. Berikut cara mudah yang bisa langsung kamu terapkan mulai hari ini.</p>

  <div class="tips-grid">
    <div class="tip-card reveal">
      <span class="tip-num">1</span>
      <span class="tip-emoji">👜</span>
      <h4>Bawa Tas Sendiri</h4>
      <p>Siapkan tas kain (tote bag), spunbond, atau paperbag di tas kamu. Letakkan di tempat yang mudah dijangkau agar tidak terlupa.</p>
    </div>
    <div class="tip-card reveal">
      <span class="tip-num">2</span>
      <span class="tip-emoji">🧺</span>
      <h4>Gunakan Keranjang Belanja</h4>
      <p>Keranjang belanja rotan atau plastik reusable sangat praktis untuk berbelanja di pasar tradisional dan tahan lama digunakan bertahun-tahun.</p>
    </div>
    <div class="tip-card reveal">
      <span class="tip-num">3</span>
      <span class="tip-emoji">📣</span>
      <h4>Ajak Orang Sekitar</h4>
      <p>Bagikan kebiasaan baik ini kepada keluarga, teman, dan tetangga. Perubahan kolektif dimulai dari percakapan kecil di rumah.</p>
    </div>
    <div class="tip-card reveal">
      <span class="tip-num">4</span>
      <span class="tip-emoji">🏪</span>
      <h4>Dukung Pedagang Ramah Lingkungan</h4>
      <p>Beli di toko atau pedagang yang menggunakan kemasan daun pisang, kertas, atau menyediakan pilihan tanpa plastik.</p>
    </div>
    <div class="tip-card reveal">
      <span class="tip-num">5</span>
      <span class="tip-emoji">♻️</span>
      <h4>Daur Ulang Plastik Lama</h4>
      <p>Jika masih punya kantong plastik, cuci dan gunakan kembali beberapa kali sebelum membuangnya. Setiap penggunaan ulang berarti!</p>
    </div>
    <div class="tip-card reveal">
      <span class="tip-num">6</span>
      <span class="tip-emoji">📱</span>
      <h4>Sebarkan Kesadaran</h4>
      <p>Bagikan informasi ini di media sosial. Satu postingan bisa menjangkau ratusan orang dan menginspirasi perubahan nyata.</p>
    </div>
  </div>
</section>

<!-- PLEDGE -->
<section class="pledge-section" id="janji">
  <div class="section-tag" style="background:var(--hijau-muda)">🤝 Komitmen Kita</div>
  <h2 class="section-title">Mulai Hari Ini,<br><em>Kurangi Plastikmu</em></h2>
  <p>Bersama-sama kita bisa menciptakan lingkungan yang lebih bersih. Tidak perlu sempurna, yang penting mulai dan konsisten. Satu kantong tas kain sudah menyelamatkan banyak kantong plastik dari alam kita.</p>
  <div class="pledge-actions">
    <a href="#tips" class="btn-utama">Lihat Cara Memulai</a>
    <a href="#survei" class="btn-outline">Baca Data Selengkapnya</a>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-brand">Bijak<span>Plastik</span></div>
  <p>Berdasarkan survei penggunaan kantong plastik saat berbelanja<br>oleh Muhammad Alaudin Ad'ari · Teknik Industri · Universitas Ma'arif Hasyim Latief · 2026</p>
  <div class="footer-credit">Dosen: Dr. Gusti Andriansyah, S.T., M.T.</div>
</footer>

<script>
  // Scroll reveal
  const reveals = document.querySelectorAll('.reveal');
  const observer = new IntersectionObserver((entries) => {
    entries.forEach((entry, i) => {
      if (entry.isIntersecting) {
        setTimeout(() => {
          entry.target.classList.add('visible');
        }, 80 * (Array.from(reveals).indexOf(entry.target) % 4));
        observer.unobserve(entry.target);
      }
    });
  }, { threshold: 0.12 });
  reveals.forEach(el => observer.observe(el));

  // Bar fill animation on scroll
  const bars = document.querySelectorAll('.bar-fill');
  const barObserver = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        setTimeout(() => entry.target.classList.add('animated'), 300);
        barObserver.unobserve(entry.target);
      }
    });
  }, { threshold: 0.2 });
  bars.forEach(b => barObserver.observe(b));
</script>
</body>
</html>
