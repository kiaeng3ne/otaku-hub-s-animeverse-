# otaku-hub-s-animeverse-
A colourful anime-themed landing page for posting anime news, reviews, and content.
index.html <!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Otaku Hub</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;800&display=swap" rel="stylesheet">
  <style>
    :root{
      --pink:#ff4ecd;
      --purple:#7c6cff;
      --cyan:#4ef0ff;
      --dark:#0b0b14;
      --glass:rgba(255,255,255,.14);
    }/* THEME STATES */
body.theme-shounen{
  --bg-main: linear-gradient(180deg,#0b0b14,#141428);
  --accent-1:#7c6cff;
  --accent-2:#4ef0ff;
  --card-glass:rgba(255,255,255,.12);
}

body.theme-shojo{
  --bg-main: linear-gradient(180deg,#fff0f7,#ffd6ea);
  --accent-1:#ff7abf;
  --accent-2:#ffb3da;
  --card-glass:rgba(255,255,255,.55);
  color:#3a2a33;
}

*{box-sizing:border-box;margin:0;padding:0;font-family:'Poppins',sans-serif}

body{
  background:
    radial-gradient(1200px 600px at 10% -10%, rgba(124,108,255,.35), transparent 40%),
    radial-gradient(1000px 500px at 90% 10%, rgba(255,78,205,.35), transparent 40%),
    var(--bg-main);
  min-height:100vh;overflow-x:hidden;
  transition:background .5s,color .5s
}

header{
  position:sticky;top:0;z-index:9;
  backdrop-filter: blur(10px);
  background: linear-gradient(180deg, rgba(20,20,40,.75), rgba(20,20,40,.35));
  border-bottom:1px solid rgba(255,255,255,.12)
}

body.theme-shojo header{
  background: linear-gradient(180deg, rgba(255,240,247,.85), rgba(255,214,234,.65));
  border-bottom:1px solid rgba(255,122,191,.35)
}

.nav{max-width:1100px;margin:auto;display:flex;align-items:center;justify-content:space-between;padding:18px}
.logo{font-weight:800;letter-spacing:.5px}
.logo span{color:var(--accent-1)}
.nav a{color:inherit;text-decoration:none;margin-left:16px;opacity:.9}

.hero{
  max-width:1100px;margin:0 auto;display:grid;grid-template-columns:1.1fr .9fr;gap:28px;align-items:center;
  padding:90px 18px 40px
}

.badge{display:inline-flex;gap:8px;align-items:center;background:var(--card-glass);border:1px solid rgba(255,255,255,.18);padding:8px 14px;border-radius:999px}
h1{font-size:3rem;line-height:1.05;margin:14px 0}
h1 em{color:var(--accent-1);font-style:normal}
.lead{opacity:.9;max-width:520px}

.btn{border:none;border-radius:999px;padding:14px 22px;font-weight:600;cursor:pointer}
.btn.primary{background:linear-gradient(135deg,var(--accent-1),var(--accent-2));color:#fff}
.btn.ghost{background:transparent;color:inherit;border:1px solid rgba(255,255,255,.35)}

.hero-art{
  position:relative;border-radius:26px;overflow:hidden;aspect-ratio:4/5;
  background:linear-gradient(135deg, rgba(124,108,255,.25), rgba(78,240,255,.15));
  box-shadow:0 30px 80px rgba(0,0,0,.35)
}

body.theme-shojo .hero-art{
  background:linear-gradient(135deg, rgba(255,122,191,.35), rgba(255,179,218,.45));
}

.section{max-width:1100px;margin:40px auto;padding:0 18px}
.grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:18px}
.card{
  background:var(--card-glass);
  border-radius:22px;overflow:hidden;transition:.25s
}
.thumb{height:140px;background:#111}
.thumb img{width:100%;height:100%;object-fit:cover}

.gallery img{width:100%;height:160px;object-fit:cover;border-radius:18px}

footer{text-align:center;padding:28px;opacity:.7}

@media(max-width:900px){
  .hero{grid-template-columns:1fr}
  h1{font-size:2.3rem}
}

  </style>
</head>
<body class="theme-shounen"><header>
  <div class="nav">
    <button id="themeToggle" style="margin-right:12px;border-radius:999px;padding:8px 14px;border:1px solid rgba(255,255,255,.4);background:transparent;color:#fff;cursor:pointer;font-weight:600">🌸 Shojo Mode</button>
    <div class="logo">Otaku<span>Hub</span></div>
    <nav>
      <a href="#">Home</a>
      <a href="#">News</a>
      <a href="#">Reviews</a>
      <a href="#">Gallery</a>
    </nav>
  </div>
</header><section class="hero">
  <div>
    <div class="badge">✨ <b>Aesthetic Anime Space</b></div>
    <h1>Colorful anime drops, edits & <em>obsessions</em></h1>
    <p class="lead">A vibrant hub for anime news, character spotlights, reviews, and visuals. Built to look good on your phone.</p>
    <div class="cta">
      <button class="btn primary">Explore Now</button>
      <button class="btn ghost">Latest Posts</button>
    </div>
  </div>
  <div class="hero-art">
    <!-- Replace this image URL with any anime image you like -->
    <img src="https://images.unsplash.com/photo-1541560052-77ec1bbc09b7?q=80&w=1200&auto=format&fit=crop" alt="Anime aesthetic" />
    <div class="glow"></div>
  </div>
</section><section class="section">
  <h2>Featured</h2>
  <div class="grid">
    <div class="card">
      <div class="thumb"><img src="https://images.unsplash.com/photo-1549880338-65ddcdfd017b?q=80&w=1200&auto=format&fit=crop" alt=""/></div>
      <div class="content"><span class="tag">NEWS</span><h3>Season highlights</h3><p>What to watch this week.</p></div>
    </div>
    <div class="card">
      <div class="thumb"><img src="https://images.unsplash.com/photo-1529333166437-7750a6dd5a70?q=80&w=1200&auto=format&fit=crop" alt=""/></div>
      <div class="content"><span class="tag">REVIEW</span><h3>Underrated gems</h3><p>Short spoiler-free takes.</p></div>
    </div>
    <div class="card">
      <div class="thumb"><img src="https://images.unsplash.com/photo-1500530855697-b586d89ba3ee?q=80&w=1200&auto=format&fit=crop" alt=""/></div>
      <div class="content"><span class="tag">CHARACTER</span><h3>Icon spotlights</h3><p>Why they hit different.</p></div>
    </div>
  </div>
</section><section class="section">
  <h2>Gallery</h2>
  <div class="gallery">
    <img src="https://images.unsplash.com/photo-1549880338-65ddcdfd017b?q=80&w=1200&auto=format&fit=crop" />
    <img src="https://images.unsplash.com/photo-1529333166437-7750a6dd5a70?q=80&w=1200&auto=format&fit=crop" />
    <img src="https://images.unsplash.com/photo-1500530855697-b586d89ba3ee?q=80&w=1200&auto=format&fit=crop" />
    <img src="https://images.unsplash.com/photo-1519681393784-d120267933ba?q=80&w=1200&auto=format&fit=crop" />
  </div>
</section><footer>© 2026 OtakuHub • Built with love 💖</footer><script>
  const toggleBtn = document.getElementById('themeToggle');
  const body = document.body;

  const themes = {
    shounen: {
      class: 'theme-shounen',
      label: '🌸 Shojo Mode'
    },
    shojo: {
      class: 'theme-shojo',
      label: '🖤 Shounen Mode'
    }
  };

  // LOAD SAVED THEME
  const savedTheme = localStorage.getItem('otaku-theme');
  if (savedTheme && themes[savedTheme]) {
    body.className = themes[savedTheme].class;
    toggleBtn.textContent = themes[savedTheme].label;
  }

  // TOGGLE + SAVE THEME
  toggleBtn.addEventListener('click', () => {
    if (body.classList.contains('theme-shounen')) {
      body.classList.remove('theme-shounen');
      body.classList.add('theme-shojo');
      toggleBtn.textContent = themes.shojo.label;
      localStorage.setItem('otaku-theme', 'shojo');
    } else {
      body.classList.remove('theme-shojo');
      body.classList.add('theme-shounen');
      toggleBtn.textContent = themes.shounen.label;
      localStorage.setItem('otaku-theme', 'shounen');
    }
  });
</script></body>
</html>
