<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Canchas Encanto Campestre — Reserva en segundos</title>
<meta name="description" content="Complejo deportivo campestre con canchas de fútbol sintético y voleibol playa. Reserva online, disponibilidad inmediata, horario de 6 AM a 11 PM." />
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;800&family=Inter:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root{
    --primary:#1f5132;          /* verde profundo */
    --primary-foreground:#ffffff;
    --accent:#f5c518;           /* amarillo hora valle */
    --accent-foreground:#1a1a1a;
    --bg:#fbfaf6;
    --fg:#1a1a1a;
    --muted:#6b7280;
    --card:#ffffff;
    --border:#e6e6e0;
    --success:#16a34a;
    --destructive:#dc2626;
    --shadow:0 12px 32px -12px rgba(31,81,50,.35);
    --gradient-hero:linear-gradient(135deg,#1f5132 0%,#2d7a48 100%);
    --gradient-accent:linear-gradient(135deg,#f5c518 0%,#f59e0b 100%);
  }
  *{box-sizing:border-box;margin:0;padding:0}
  html,body{background:var(--bg);color:var(--fg);font-family:'Inter',system-ui,sans-serif;line-height:1.5}
  h1,h2,h3,.display{font-family:'Poppins',sans-serif;font-weight:800;letter-spacing:-.02em}
  a{color:inherit;text-decoration:none}
  img{max-width:100%;display:block}
  .container{max-width:1200px;margin:0 auto;padding:0 1rem}

  /* NAVBAR */
  .nav{position:sticky;top:0;z-index:40;background:var(--primary);color:#fff;box-shadow:var(--shadow)}
  .nav-inner{display:flex;align-items:center;justify-content:space-between;padding:.85rem 1rem;max-width:1200px;margin:0 auto}
  .brand{display:flex;align-items:center;gap:.5rem;font-family:'Poppins';font-weight:800;font-size:1.05rem}
  .brand .dot{width:10px;height:10px;border-radius:999px;background:var(--accent)}
  .nav-links{display:none;gap:.25rem}
  .nav-links a{padding:.5rem .85rem;border-radius:.5rem;font-size:.9rem;font-weight:500}
  .nav-links a:hover{background:rgba(255,255,255,.1)}
  .btn{display:inline-flex;align-items:center;gap:.5rem;padding:.6rem 1.1rem;border-radius:.6rem;font-weight:600;font-size:.95rem;cursor:pointer;border:none;transition:transform .15s,box-shadow .15s}
  .btn:hover{transform:translateY(-1px)}
  .btn-accent{background:var(--accent);color:var(--accent-foreground)}
  .btn-primary{background:var(--primary);color:#fff}
  .btn-outline{background:rgba(255,255,255,.1);color:#fff;border:1px solid rgba(255,255,255,.4)}
  @media(min-width:900px){.nav-links{display:flex}}

  /* HERO */
  .hero{position:relative;min-height:85vh;display:flex;align-items:center;overflow:hidden;isolation:isolate}
  .hero img.bg{position:absolute;inset:0;width:100%;height:100%;object-fit:cover;z-index:-2}
  .hero::after{content:"";position:absolute;inset:0;background:linear-gradient(180deg,rgba(0,0,0,.4) 0%,rgba(31,81,50,.6) 50%,rgba(31,81,50,.92) 100%);z-index:-1}
  .hero-content{padding:5rem 1rem;color:#fff;max-width:1200px;margin:0 auto;width:100%}
  .chip{display:inline-flex;align-items:center;gap:.4rem;background:var(--accent);color:var(--accent-foreground);padding:.4rem 1rem;border-radius:999px;font-size:.85rem;font-weight:600}
  .hero h1{font-size:clamp(2.5rem,6vw,4.5rem);margin-top:1.5rem;max-width:46rem;line-height:1.05}
  .hero h1 span{color:var(--accent)}
  .hero p{margin-top:1.5rem;max-width:34rem;font-size:1.1rem;color:rgba(255,255,255,.9)}
  .hero-ctas{margin-top:2rem;display:flex;flex-wrap:wrap;gap:.75rem}

  /* FEATURES */
  .section{padding:4rem 0}
  .grid-3{display:grid;gap:1.5rem;grid-template-columns:1fr}
  @media(min-width:768px){.grid-3{grid-template-columns:repeat(3,1fr)}}
  .card{background:var(--card);border:1px solid var(--border);border-radius:1rem;padding:1.5rem;box-shadow:0 1px 3px rgba(0,0,0,.04)}
  .card .icon{width:42px;height:42px;display:flex;align-items:center;justify-content:center;background:rgba(31,81,50,.1);color:var(--primary);border-radius:.6rem;font-size:1.3rem}
  .card h3{margin-top:1rem;font-size:1.25rem}
  .card p{margin-top:.5rem;color:var(--muted);font-size:.92rem}

  /* INSTALACIONES */
  .section h2{font-size:clamp(2rem,4vw,2.5rem);color:var(--primary)}
  .section .lead{margin-top:.5rem;color:var(--muted)}
  .grid-2{display:grid;gap:1.5rem;grid-template-columns:1fr;margin-top:2rem}
  @media(min-width:768px){.grid-2{grid-template-columns:1fr 1fr}}
  .tile{position:relative;overflow:hidden;border-radius:1.25rem;box-shadow:var(--shadow)}
  .tile img{height:20rem;width:100%;object-fit:cover;transition:transform .5s}
  .tile:hover img{transform:scale(1.05)}
  .tile::after{content:"";position:absolute;inset:0;background:linear-gradient(0deg,rgba(31,81,50,.95) 0%,rgba(31,81,50,.3) 50%,transparent 100%)}
  .tile-text{position:absolute;bottom:0;left:0;padding:1.5rem;color:#fff;z-index:2}
  .tile-text h3{font-family:'Poppins';font-size:1.5rem;font-weight:800}
  .tile-text p{font-size:.9rem;color:rgba(255,255,255,.85);margin-top:.25rem}

  /* CTA */
  .cta{max-width:900px;margin:0 auto;padding:3rem 1rem 5rem}
  .cta-box{background:var(--gradient-accent);border-radius:1.5rem;padding:3rem 2rem;text-align:center;box-shadow:var(--shadow);color:var(--accent-foreground)}
  .cta-box h2{font-size:clamp(1.75rem,3.5vw,2.25rem)}
  .cta-box p{margin-top:.5rem;color:rgba(26,26,26,.75)}
  .cta-box .btn{margin-top:1.5rem}

  /* FOOTER */
  footer{background:var(--primary);color:#fff;padding:2.5rem 1rem;text-align:center;margin-top:4rem}
  footer .name{font-family:'Poppins';font-weight:800;font-size:1.1rem}
  footer .tag{opacity:.75;margin-top:.25rem}
  footer .legal{opacity:.55;font-size:.85rem;margin-top:1rem}

  /* WhatsApp button */
  .wa{position:fixed;right:1.25rem;bottom:1.25rem;width:56px;height:56px;border-radius:999px;background:#25D366;color:#fff;display:flex;align-items:center;justify-content:center;box-shadow:0 8px 24px rgba(37,211,102,.4);z-index:50}
  .wa svg{width:28px;height:28px}
</style>
</head>
<body>

<header class="nav">
  <div class="nav-inner">
    <a class="brand" href="#"><span class="dot"></span> Encanto Campestre</a>
    <nav class="nav-links">
      <a href="#">Inicio</a>
      <a href="#reservar">Reservar Cancha</a>
      <a href="#">Mis Reservas</a>
      <a href="#promociones">Promociones</a>
      <a href="#contacto">Contacto</a>
    </nav>
    <a href="#" class="btn btn-accent">Iniciar Sesión</a>
  </div>
</header>

<section class="hero">
  <img class="bg" src="assets/hero-banner.jpg" alt="Complejo deportivo Encanto Campestre" />
  <div class="hero-content">
    <span class="chip">✨ Complejo campestre</span>
    <h1>Reserva tu espacio<br/><span>deportivo</span> en segundos.</h1>
    <p>Canchas de fútbol sintético y voleibol playa en un entorno natural único. Disponibilidad en tiempo real, todos los días de 6:00 AM a 11:00 PM.</p>
    <div class="hero-ctas">
      <a href="#reservar" class="btn btn-accent">📅 Reservar Cancha</a>
      <a href="#promociones" class="btn btn-outline">Ver Promociones</a>
    </div>
  </div>
</section>

<section class="section container">
  <div class="grid-3">
    <div class="card"><div class="icon">⏰</div><h3>Horario amplio</h3><p>Todos los días de 06:00 AM a 11:00 PM.</p></div>
    <div class="card"><div class="icon">📍</div><h3>4 canchas profesionales</h3><p>2 sintéticas y 2 de voleibol playa.</p></div>
    <div class="card"><div class="icon">✨</div><h3>Hora Valle</h3><p>Tarifas especiales L-V de 11 AM a 3 PM.</p></div>
  </div>
</section>

<section class="section container" id="reservar">
  <h2>Nuestras instalaciones</h2>
  <p class="lead">Cuatro canchas listas para tu próximo partido.</p>
  <div class="grid-2">
    <div class="tile">
      <img src="assets/cancha-sintetica.jpg" alt="Cancha de fútbol sintético" />
      <div class="tile-text">
        <h3>Canchas Sintéticas</h3>
        <p>Cancha N°1 (6 personas) y N°2 (4 personas) — grama profesional.</p>
      </div>
    </div>
    <div class="tile">
      <img src="assets/voley-playa.jpg" alt="Cancha de vóley playa" />
      <div class="tile-text">
        <h3>Voley Playa</h3>
        <p>Cancha N°1 y N°2 — arena fina entre palmeras.</p>
      </div>
    </div>
  </div>
</section>

<section class="cta" id="promociones">
  <div class="cta-box">
    <h2>¿Listo para jugar?</h2>
    <p>Reserva ahora y asegura tu horario favorito.</p>
    <a href="#" class="btn btn-primary">Reservar ahora</a>
  </div>
</section>

<footer id="contacto">
  <p class="name">Canchas Encanto Campestre</p>
  <p class="tag">Reserva tu espacio deportivo en segundos.</p>
  <p class="legal">© 2026 Encanto Campestre. Todos los derechos reservados.</p>
</footer>

<a class="wa" href="https://wa.me/" target="_blank" aria-label="WhatsApp">
  <svg viewBox="0 0 24 24" fill="currentColor"><path d="M20.5 3.5A11.9 11.9 0 0 0 12 0C5.4 0 0 5.4 0 12c0 2.1.5 4.1 1.6 5.9L0 24l6.3-1.6A12 12 0 0 0 12 24c6.6 0 12-5.4 12-12 0-3.2-1.2-6.2-3.5-8.5zM12 22a10 10 0 0 1-5.1-1.4l-.4-.2-3.7 1 1-3.6-.2-.4A10 10 0 1 1 22 12c0 5.5-4.5 10-10 10zm5.5-7.5c-.3-.2-1.8-.9-2-1s-.5-.2-.7.2-.8 1-1 1.2-.4.2-.7 0a8 8 0 0 1-2.4-1.5 9 9 0 0 1-1.6-2c-.2-.3 0-.5.1-.7l.5-.5.3-.5c.1-.2 0-.4 0-.5l-.7-1.7c-.2-.4-.4-.4-.6-.4h-.5c-.2 0-.5 0-.7.3a3 3 0 0 0-1 2.3c0 1.3 1 2.6 1.1 2.8s2 3 4.7 4.2c.6.3 1.1.5 1.5.6.7.2 1.3.2 1.7.1.5-.1 1.6-.7 1.8-1.3.2-.7.2-1.2.2-1.4l-.6-.3z"/></svg>
</a>

</body>
</html>
