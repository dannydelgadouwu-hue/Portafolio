<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Brillito🎀 — Portafolio UGC</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;1,400&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  :root {
    --rose:    #E8A4B0;
    --blush:   #F5D6DD;
    --cream:   #FDF8F5;
    --plum:    #2D1B20;
    --muted:   #8C6B73;
    --soft:    #F0E6EA;
    --accent:  #C96A7E;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--cream);
    color: var(--plum);
    font-family: 'DM Sans', sans-serif;
    font-weight: 300;
    line-height: 1.6;
  }

  /* ── HERO ── */
  .hero {
    min-height: 100vh;
    display: grid;
    grid-template-rows: auto 1fr auto;
    padding: 0 clamp(24px, 6vw, 80px);
    position: relative;
    overflow: hidden;
  }

  .hero::before {
    content: '';
    position: absolute;
    top: -120px; right: -120px;
    width: 520px; height: 520px;
    border-radius: 50%;
    background: radial-gradient(circle, #F5D6DD 0%, transparent 70%);
    pointer-events: none;
  }

  .nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 32px 0 24px;
    border-bottom: 1px solid var(--blush);
  }

  .nav-logo {
    font-family: 'Playfair Display', serif;
    font-size: 1.1rem;
    letter-spacing: 0.08em;
    color: var(--accent);
  }

  .nav-tag {
    font-size: 0.72rem;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--muted);
  }

  .hero-center {
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 60px 0 40px;
    max-width: 680px;
  }

  .eyebrow {
    font-size: 0.68rem;
    letter-spacing: 0.3em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 20px;
  }

  h1 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(3rem, 9vw, 6.5rem);
    line-height: 1.02;
    font-weight: 700;
    margin-bottom: 8px;
  }

  h1 em {
    font-style: italic;
    color: var(--accent);
  }

  .hero-sub {
    font-size: clamp(1rem, 2.2vw, 1.15rem);
    color: var(--muted);
    margin-top: 24px;
    max-width: 480px;
  }

  .hero-cta {
    display: inline-block;
    margin-top: 40px;
    padding: 14px 32px;
    background: var(--plum);
    color: var(--cream);
    font-size: 0.78rem;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    text-decoration: none;
    border-radius: 2px;
    transition: background 0.25s;
  }

  .hero-cta:hover { background: var(--accent); }

  .hero-stats {
    display: flex;
    gap: 48px;
    padding: 36px 0;
    border-top: 1px solid var(--blush);
    flex-wrap: wrap;
  }

  .stat-num {
    font-family: 'Playfair Display', serif;
    font-size: 2rem;
    font-weight: 700;
    color: var(--plum);
    line-height: 1;
  }

  .stat-label {
    font-size: 0.7rem;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--muted);
    margin-top: 4px;
  }

  /* ── SECTIONS ── */
  section {
    padding: clamp(64px, 10vw, 120px) clamp(24px, 6vw, 80px);
  }

  .section-label {
    font-size: 0.65rem;
    letter-spacing: 0.3em;
    text-transform: uppercase;
    color: var(--rose);
    margin-bottom: 12px;
  }

  h2 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(1.8rem, 4vw, 2.8rem);
    font-weight: 700;
    line-height: 1.15;
    margin-bottom: 16px;
  }

  h2 em { font-style: italic; color: var(--accent); }

  .section-intro {
    color: var(--muted);
    font-size: 1rem;
    max-width: 560px;
    margin-bottom: 56px;
  }

  /* ── SOBRE MÍ ── */
  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 48px;
    align-items: start;
  }

  @media (max-width: 680px) { .about-grid { grid-template-columns: 1fr; } }

  .about-block {
    background: var(--soft);
    border-radius: 4px;
    padding: 36px 32px;
  }

  .about-block h3 {
    font-family: 'Playfair Display', serif;
    font-size: 1.1rem;
    margin-bottom: 12px;
    color: var(--plum);
  }

  .about-block p {
    font-size: 0.9rem;
    color: var(--muted);
    line-height: 1.75;
  }

  .pill-list {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-top: 16px;
  }

  .pill {
    padding: 5px 14px;
    border: 1px solid var(--rose);
    border-radius: 100px;
    font-size: 0.72rem;
    letter-spacing: 0.06em;
    color: var(--accent);
  }

  /* ── NICHOS ── */
  .nicho-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
    gap: 2px;
  }

  .nicho-card {
    background: var(--soft);
    padding: 40px 28px;
    transition: background 0.2s;
  }

  .nicho-card:hover { background: var(--blush); }

  .nicho-icon {
    font-size: 1.8rem;
    margin-bottom: 16px;
    display: block;
  }

  .nicho-card h3 {
    font-family: 'Playfair Display', serif;
    font-size: 1rem;
    margin-bottom: 8px;
  }

  .nicho-card p {
    font-size: 0.8rem;
    color: var(--muted);
    line-height: 1.65;
  }

  /* ── MÉTRICAS ── */
  .metrics-bg {
    background: var(--plum);
    color: var(--cream);
  }

  .metrics-bg .section-label { color: var(--rose); }
  .metrics-bg h2 { color: var(--cream); }
  .metrics-bg h2 em { color: var(--rose); }
  .metrics-bg .section-intro { color: #B89AA0; }

  .metrics-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
    gap: 2px;
  }

  .metric-card {
    background: rgba(255,255,255,0.05);
    padding: 40px 28px;
    border-top: 2px solid var(--accent);
  }

  .metric-big {
    font-family: 'Playfair Display', serif;
    font-size: 2.6rem;
    font-weight: 700;
    color: var(--rose);
    line-height: 1;
    margin-bottom: 8px;
  }

  .metric-name {
    font-size: 0.72rem;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: #B89AA0;
  }

  /* ── SERVICIOS UGC ── */
  .service-list {
    display: grid;
    gap: 2px;
  }

  .service-row {
    display: grid;
    grid-template-columns: 80px 1fr auto;
    align-items: center;
    gap: 32px;
    padding: 28px 32px;
    background: var(--soft);
    transition: background 0.2s;
  }

  .service-row:hover { background: var(--blush); }

  .service-num {
    font-family: 'Playfair Display', serif;
    font-size: 1.6rem;
    font-weight: 700;
    color: var(--blush);
  }

  .service-row:hover .service-num { color: var(--rose); }

  .service-name {
    font-size: 0.95rem;
    font-weight: 500;
  }

  .service-desc {
    font-size: 0.78rem;
    color: var(--muted);
    margin-top: 4px;
  }

  .service-tag {
    font-size: 0.65rem;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--accent);
    white-space: nowrap;
  }

  @media (max-width: 560px) {
    .service-row { grid-template-columns: 48px 1fr; }
    .service-tag { display: none; }
  }

  /* ── AUDIENCIA ── */
  .audience-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 48px;
    align-items: center;
  }

  @media (max-width: 680px) { .audience-grid { grid-template-columns: 1fr; } }

  .bar-list { display: flex; flex-direction: column; gap: 18px; }

  .bar-item {}

  .bar-label {
    display: flex;
    justify-content: space-between;
    font-size: 0.8rem;
    color: var(--muted);
    margin-bottom: 6px;
  }

  .bar-track {
    height: 4px;
    background: var(--soft);
    border-radius: 2px;
    overflow: hidden;
  }

  .bar-fill {
    height: 100%;
    background: linear-gradient(90deg, var(--rose), var(--accent));
    border-radius: 2px;
    transition: width 1s ease;
  }

  .audience-text h3 {
    font-family: 'Playfair Display', serif;
    font-size: 1.4rem;
    margin-bottom: 12px;
  }

  .audience-text p {
    font-size: 0.88rem;
    color: var(--muted);
    line-height: 1.75;
    margin-bottom: 16px;
  }

  /* ── CONTACTO ── */
  .contact-section {
    background: var(--blush);
    text-align: center;
  }

  .contact-section h2 { margin: 0 auto 16px; }

  .contact-section .section-intro {
    margin: 0 auto 48px;
  }

  .contact-links {
    display: flex;
    justify-content: center;
    gap: 16px;
    flex-wrap: wrap;
  }

  .contact-link {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 14px 28px;
    font-size: 0.78rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    text-decoration: none;
    border-radius: 2px;
    transition: all 0.2s;
  }

  .contact-link.primary {
    background: var(--plum);
    color: var(--cream);
  }

  .contact-link.primary:hover { background: var(--accent); }

  .contact-link.secondary {
    background: transparent;
    color: var(--plum);
    border: 1px solid var(--rose);
  }

  .contact-link.secondary:hover {
    background: var(--rose);
    color: white;
  }

  /* ── FOOTER ── */
  footer {
    padding: 24px clamp(24px, 6vw, 80px);
    border-top: 1px solid var(--blush);
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 12px;
  }

  footer p {
    font-size: 0.72rem;
    color: var(--muted);
    letter-spacing: 0.06em;
  }

  /* ── DIVIDER ── */
  .divider {
    width: 40px;
    height: 2px;
    background: var(--rose);
    margin: 24px 0;
  }

  /* ── TESTIMONIAL / QUOTE ── */
  .quote-section {
    background: var(--soft);
  }

  blockquote {
    font-family: 'Playfair Display', serif;
    font-size: clamp(1.3rem, 3vw, 2rem);
    font-style: italic;
    line-height: 1.4;
    color: var(--plum);
    max-width: 700px;
  }

  blockquote::before {
    content: '"';
    font-size: 4rem;
    color: var(--rose);
    line-height: 0.5;
    display: block;
    margin-bottom: 16px;
  }

  cite {
    display: block;
    margin-top: 20px;
    font-size: 0.72rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--muted);
    font-style: normal;
  }

  /* ── HERO PHOTOS ── */
  .hero-two-col {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: auto 1fr auto;
    gap: 0 48px;
  }

  .hero-two-col .nav {
    grid-column: 1 / -1;
  }

  .hero-two-col .hero-stats {
    grid-column: 1 / -1;
  }

  .hero-photo-wrap {
    display: flex;
    flex-direction: column;
    justify-content: center;
    gap: 16px;
    padding: 40px 0;
  }

  .hero-photo {
    width: 100%;
    border-radius: 4px;
    object-fit: cover;
    height: 320px;
    filter: brightness(1.02) contrast(1.02);
  }

  .hero-photo-2 {
    height: 320px;
  }

  @media (max-width: 720px) {
    .hero-two-col {
      grid-template-columns: 1fr;
    }
    .hero-photo-wrap {
      flex-direction: row;
      height: 200px;
    }
    .hero-photo, .hero-photo-2 {
      height: 100%;
      flex: 1;
    }
  }

  /* ── EXPERIENCIA ── */
  .exp-grid {
    display: grid;
    gap: 2px;
  }

  .exp-card {
    display: flex;
    gap: 24px;
    align-items: flex-start;
    padding: 32px;
    background: var(--soft);
    transition: background 0.2s;
  }

  .exp-card:hover { background: var(--blush); }

  .exp-icon {
    font-size: 1.8rem;
    flex-shrink: 0;
    margin-top: 2px;
  }

  .exp-brand {
    font-family: 'Playfair Display', serif;
    font-size: 1.1rem;
    font-weight: 700;
    color: var(--plum);
    margin-bottom: 2px;
  }

  .exp-role {
    font-size: 0.7rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 10px;
  }

  .exp-desc {
    font-size: 0.88rem;
    color: var(--muted);
    line-height: 1.7;
  }
</style>
</head>
<body>

<!-- HERO -->
<section class="hero hero-two-col">
  <nav class="nav">
    <span class="nav-logo">Brillito🎀</span>
    <span class="nav-tag">Portafolio UGC · 2025</span>
  </nav>

  <div class="hero-center">
    <p class="eyebrow">Creadora de contenido UGC</p>
    <h1>Brigi<em>tte</em></h1>
    <div class="divider"></div>
    <p class="hero-sub">Creo contenido auténtico para marcas de belleza, skincare y lifestyle que conecta con mujeres jóvenes latinas. Con base en Pasto, Colombia — universitaria, real, cercana.</p>
    <a href="mailto:brillitoou__@gmail.com" class="hero-cta">Quiero colaborar →</a>
  </div>

  <div class="hero-stats">
    <div>
      <div class="stat-num">822</div>
      <div class="stat-label">Seguidores Instagram</div>
    </div>
    <div>
      <div class="stat-num">373</div>
      <div class="stat-label">Seguidores TikTok</div>
    </div>
    <div>
      <div class="stat-num">19k</div>
      <div class="stat-label">Vistas/mes TikTok</div>
    </div>
    <div>
      <div class="stat-num">2541</div>
      <div class="stat-label">Me Gusta TikTok</div>
    </div>
  </div>

  <!-- FOTO HERO -->
  <div class="hero-photo-wrap">
    <img src="https://via.placeholder.com/400x320/E8A4B0/ffffff?text=Foto+1" alt="Brig - Brillito" class="hero-photo">
    <img src="https://via.placeholder.com/400x320/F5D6DD/ffffff?text=Foto+2" alt="Brig - Brillito 2" class="hero-photo-2">
  </div>
</section>

<!-- SOBRE MÍ -->
<section>
  <p class="section-label">Sobre mí</p>
  <h2>Quien soy <em>Brillito</em></h2>
  
  <div class="about-grid">
    <div class="about-block">
      <h3>Mi historia</h3>
      <p>Soy Brigitte, creadora de contenido UGC desde Pasto, Colombia. Mi contenido se caracteriza por ser auténtico, relatable y enfocado en marcas que resuenan con mi comunidad. No hago marketing artificial — creo historias que la gente realmente quiere escuchar.</p>
      <div class="pill-list">
        <div class="pill">Auténtico</div>
        <div class="pill">UGC Experto</div>
        <div class="pill">Comunidad Leal</div>
      </div>
    </div>
    
    <div class="about-block">
      <h3>Mi estilo</h3>
      <p>Mi contenido destaca por su naturalidad. Utilizo paletas de colores cálidas, lenguaje cercano y narrativas que conectan emocionalmente. Sigo tendencias sin perder mi identidad — lo que me hace diferente en un mercado saturado.</p>
      <div class="pill-list">
        <div class="pill">Estilo visual</div>
        <div class="pill">Storytelling</div>
        <div class="pill">Tendencias</div>
      </div>
    </div>
  </div>
</section>

<!-- NICHOS -->
<section>
  <p class="section-label">Especialidades</p>
  <h2>Nichos donde <em>domino</em></h2>
  
  <div class="nicho-grid">
    <div class="nicho-card">
      <div class="nicho-icon">💄</div>
      <h3>Belleza & Makeup</h3>
      <p>Tutoriales, reseñas y tendencias makeup. Mi comunidad confía en mis recomendaciones.</p>
    </div>
    <div class="nicho-card">
      <div class="nicho-icon">✨</div>
      <h3>Skincare</h3>
      <p>Rutinas diarias, ingredientes clave y resultados reales sin filtros falsos.</p>
    </div>
    <div class="nicho-card">
      <div class="nicho-icon">👗</div>
      <h3>Moda & Lifestyle</h3>
      <p>Outfits, estilo de vida y tendencias que mis seguidores aman replicar.</p>
    </div>
    <div class="nicho-card">
      <div class="nicho-icon">🌸</div>
      <h3>Wellness</h3>
      <p>Salud mental, autocuidado y bienestar desde una perspectiva real y cercana.</p>
    </div>
  </div>
</section>

<!-- MÉTRICAS -->
<section class="metrics-bg">
  <p class="section-label">Alcance</p>
  <h2>Números que <em>hablan</em></h2>
  <p class="section-intro">Mi comunidad crece constantemente con engagement genuino. Aquí están las cifras que importan.</p>
  
  <div class="metrics-grid">
    <div class="metric-card">
      <div class="metric-big">822</div>
      <div class="metric-name">Seguidores Instagram</div>
    </div>
    <div class="metric-card">
      <div class="metric-big">373</div>
      <div class="metric-name">Seguidores TikTok</div>
    </div>
    <div class="metric-card">
      <div class="metric-big">19k+</div>
      <div class="metric-name">Vistas/mes TikTok</div>
    </div>
    <div class="metric-card">
      <div class="metric-big">12%</div>
      <div class="metric-name">Engagement Rate Promedio</div>
    </div>
  </div>
</section>

<!-- SERVICIOS UGC -->
<section>
  <p class="section-label">Servicios</p>
  <h2>Qué <em>ofrezco</em></h2>
  <p class="section-intro">Creo contenido UGC profesional diseñado para convertir. Cada video cuenta una historia que resonará con tu audiencia.</p>
  
  <div class="service-list">
    <div class="service-row">
      <div class="service-num">01</div>
      <div>
        <div class="service-name">Vídeos UGC 15-30s</div>
        <div class="service-desc">Contenido corto y punchy perfecto para ads, Reels y TikTok. Enfocado en conversión.</div>
      </div>
      <div class="service-tag">Más Popular</div>
    </div>
    <div class="service-row">
      <div class="service-num">02</div>
      <div>
        <div class="service-name">Testimonial Authentico</div>
        <div class="service-desc">Mi genuine opinion sobre tu producto. Perfecto para generar confianza en audiencias.</div>
      </div>
      <div class="service-tag">Personal</div>
    </div>
    <div class="service-row">
      <div class="service-num">03</div>
      <div>
        <div class="service-name">Contenido Long-Form</div>
        <div class="service-desc">Videos 1-3 minutos con narrativa completa. Ideal para YouTube, Reels y más contexto.</div>
      </div>
      <div class="service-tag">Storytelling</div>
    </div>
    <div class="service-row">
      <div class="service-num">04</div>
      <div>
        <div class="service-name">Series de Contenido</div>
        <div class="service-desc">Paquetes de 3-5 videos con temáticas relacionadas. Máximo impacto, mejor precio.</div>
      </div>
      <div class="service-tag">Paquete</div>
    </div>
  </div>
</section>

<!-- AUDIENCIA -->
<section>
  <p class="section-label">Mi Audiencia</p>
  <h2>Quienes me <em>siguen</em></h2>
  
  <div class="audience-grid">
    <div>
      <div class="bar-list">
        <div class="bar-item">
          <div class="bar-label">
            <span>Mujeres 18-24</span>
            <span>65%</span>
          </div>
          <div class="bar-track">
            <div class="bar-fill" style="width: 65%"></div>
          </div>
        </div>
        <div class="bar-item">
          <div class="bar-label">
            <span>Mujeres 25-34</span>
            <span>25%</span>
          </div>
          <div class="bar-track">
            <div class="bar-fill" style="width: 25%"></div>
          </div>
        </div>
        <div class="bar-item">
          <div class="bar-label">
            <span>Otros</span>
            <span>10%</span>
          </div>
          <div class="bar-track">
            <div class="bar-fill" style="width: 10%"></div>
          </div>
        </div>
      </div>
    </div>
    
    <div class="audience-text">
      <h3>Comunidad Leal</h3>
      <p>Mi audiencia es principalmente mujeres jóvenes latinas que buscan contenido auténtico. Son universitarias, trabajadoras, influenciadas por tendencias pero mantienen su identidad.</p>
      <p>Les interesa belleza, moda, wellness y marcas que sean accesibles y que reflejen sus valores. Valoran la honestidad por encima de la perfección.</p>
    </div>
  </div>
</section>

<!-- EXPERIENCIA -->
<section>
  <p class="section-label">Experiencia</p>
  <h2>Marcas con las que he <em>colaborado</em></h2>
  
  <div class="exp-grid">
    <div class="exp-card">
      <div class="exp-icon">💅</div>
      <div>
        <div class="exp-brand">BeautyBrand X</div>
        <div class="exp-role">Creadora UGC</div>
        <div class="exp-desc">Produje 5 videos UGC para su línea de nail art. Obtuvo 3.2x ROI en conversiones.</div>
      </div>
    </div>
    <div class="exp-card">
      <div class="exp-icon">✨</div>
      <div>
        <div class="exp-brand">SkinCare Colombiana</div>
        <div class="exp-role">Embajadora de Contenido</div>
        <div class="exp-desc">Series de 8 videos mostrando mi rutina real. Generó comunidad 40% mas engaged.</div>
      </div>
    </div>
    <div class="exp-card">
      <div class="exp-icon">👗</div>
      <div>
        <div class="exp-brand">Tienda de Ropa Online</div>
        <div class="exp-role">Creadora UGC</div>
        <div class="exp-desc">Hauls y lookbooks. Alcanzó audiencia de 50k visualizaciones en primera semana.</div>
      </div>
    </div>
  </div>
</section>

<!-- QUOTE -->
<section class="quote-section">
  <blockquote>
    El contenido auténtico no vende productos, crea conexiones. Y las conexiones son las que generan verdaderas conversiones.
  </blockquote>
  <cite>— Brigitte, Brillito</cite>
</section>

<!-- CONTACTO -->
<section class="contact-section">
  <h2>Hablemos sobre tu <em>marca</em></h2>
  <p class="section-intro">Estoy lista para crear contenido que convierta. ¿Tienes un producto o marca que te encantaría que promocione?</p>
  
  <div class="contact-links">
    <a href="mailto:brillitoou__@gmail.com" class="contact-link primary">📧 Envía un Email</a>
    <a href="https://instagram.com/brillitoou" class="contact-link secondary">💬 Instagram DM</a>
    <a href="https://wa.me/573001234567" class="contact-link secondary">📱 WhatsApp</a>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <p>&copy; 2025 Brillito🎀 • Todos los derechos reservados</p>
  <p>Diseñado con amor en Pasto, Colombia 🌸</p>
</footer>

</body>
</html>
