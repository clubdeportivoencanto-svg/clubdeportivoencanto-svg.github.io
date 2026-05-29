<style>
:root{
  --primary:#164728;
  --primary2:#236b3b;
  --accent:#f5c518;
  --bg:#fbfaf6;
  --fg:#1f2933;
  --muted:#6b7280;
  --card:#ffffff;
  --border:#e5e7eb;
  --shadow:0 14px 35px rgba(0,0,0,.16);
}

*{box-sizing:border-box;margin:0;padding:0}

html{scroll-behavior:smooth}

body{
  background:var(--bg);
  color:var(--fg);
  font-family:'Inter',system-ui,sans-serif;
  line-height:1.5;
}

h1,h2,h3{
  font-family:'Poppins',sans-serif;
  font-weight:800;
}

a{text-decoration:none;color:inherit}

.container{
  max-width:1200px;
  margin:auto;
  padding:0 1rem;
}

/* NAVBAR */
.nav{
  position:sticky;
  top:0;
  z-index:100;
  background:rgba(22,71,40,.96);
  backdrop-filter:blur(10px);
  color:white;
  box-shadow:0 8px 25px rgba(0,0,0,.18);
}

.nav-inner{
  max-width:1200px;
  margin:auto;
  padding:.85rem 1rem;
  display:flex;
  align-items:center;
  justify-content:space-between;
  gap:1rem;
}

.brand{
  display:flex;
  align-items:center;
  gap:.65rem;
  font-family:'Poppins';
  font-weight:800;
  font-size:1rem;
}

.logo-circle{
  background:var(--accent);
  color:#164728;
  width:38px;
  height:38px;
  border-radius:50%;
  display:flex;
  align-items:center;
  justify-content:center;
  font-weight:800;
}

.nav-links{
  display:flex;
  align-items:center;
  gap:.35rem;
}

.nav-links a{
  padding:.55rem .85rem;
  border-radius:999px;
  font-size:.92rem;
  font-weight:600;
}

.nav-links a:hover{
  background:rgba(255,255,255,.12);
}

.btn{
  display:inline-flex;
  align-items:center;
  justify-content:center;
  padding:.75rem 1.2rem;
  border-radius:999px;
  font-weight:800;
  border:none;
  cursor:pointer;
}

.btn-accent{
  background:var(--accent);
  color:#1a1a1a;
}

.btn-primary{
  background:var(--primary);
  color:white;
}

.btn-outline{
  color:white;
  border:1px solid rgba(255,255,255,.5);
}

#menu-toggle{display:none}
.menu-btn{display:none}
.login-mobile{display:none}

/* HERO */
.hero{
  min-height:88vh;
  position:relative;
  display:flex;
  align-items:center;
  overflow:hidden;
  isolation:isolate;
}

.hero img.bg{
  position:absolute;
  inset:0;
  width:100%;
  height:100%;
  object-fit:cover;
  z-index:-2;
}

.hero::after{
  content:"";
  position:absolute;
  inset:0;
  background:
    linear-gradient(90deg,rgba(0,0,0,.75),rgba(22,71,40,.72),rgba(22,71,40,.25)),
    linear-gradient(180deg,transparent 60%,var(--primary) 100%);
  z-index:-1;
}

.hero-content{
  width:100%;
  max-width:1200px;
  margin:auto;
  padding:5rem 1rem;
  color:white;
}

.chip{
  display:inline-flex;
  background:rgba(245,197,24,.95);
  color:#1a1a1a;
  padding:.5rem 1rem;
  border-radius:999px;
  font-weight:800;
  font-size:.9rem;
}

.hero h1{
  margin-top:1.3rem;
  font-size:clamp(2.3rem,6vw,4.8rem);
  line-height:1.02;
  max-width:760px;
}

.hero h1 span{
  color:var(--accent);
}

.hero p{
  margin-top:1.2rem;
  font-size:1.12rem;
  max-width:600px;
  color:rgba(255,255,255,.92);
}

.hero-ctas{
  margin-top:2rem;
  display:flex;
  flex-wrap:wrap;
  gap:.8rem;
}

/* CARDS */
.section{
  padding:4rem 0;
}

.grid-3{
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:1.3rem;
}

.card{
  background:white;
  padding:1.5rem;
  border-radius:1.2rem;
  border:1px solid var(--border);
  box-shadow:0 6px 20px rgba(0,0,0,.06);
}

.card .icon{
  width:48px;
  height:48px;
  border-radius:14px;
  background:#eaf5ee;
  color:var(--primary);
  display:flex;
  align-items:center;
  justify-content:center;
  font-size:1.4rem;
}

.card h3{
  margin-top:1rem;
  font-size:1.2rem;
}

.card p{
  color:var(--muted);
  margin-top:.4rem;
}

/* INSTALACIONES */
.section h2{
  color:var(--primary);
  font-size:clamp(1.9rem,4vw,2.6rem);
}

.lead{
  color:var(--muted);
  margin-top:.4rem;
}

.grid-2{
  margin-top:2rem;
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:1.5rem;
}

.tile{
  position:relative;
  border-radius:1.5rem;
  overflow:hidden;
  box-shadow:var(--shadow);
  min-height:330px;
}

.tile img{
  width:100%;
  height:100%;
  min-height:330px;
  object-fit:cover;
}

.tile::after{
  content:"";
  position:absolute;
  inset:0;
  background:linear-gradient(0deg,rgba(0,0,0,.78),rgba(0,0,0,.15));
}

.tile-text{
  position:absolute;
  z-index:2;
  left:0;
  right:0;
  bottom:0;
  padding:1.6rem;
  color:white;
}

.tile-text h3{
  font-size:1.6rem;
}

.tile-text p{
  margin-top:.35rem;
  color:rgba(255,255,255,.9);
}

/* CTA */
.cta{
  max-width:950px;
  margin:auto;
  padding:2rem 1rem 4rem;
}

.cta-box{
  background:linear-gradient(135deg,#f5c518,#f59e0b);
  border-radius:1.7rem;
  padding:3rem 2rem;
  text-align:center;
  box-shadow:var(--shadow);
}

.cta-box h2{
  color:#1a1a1a;
  font-size:clamp(1.8rem,4vw,2.4rem);
}

.cta-box p{
  margin-top:.5rem;
}

.cta-box .btn{
  margin-top:1.5rem;
}

/* FOOTER */
footer{
  background:var(--primary);
  color:white;
  padding:2.5rem 1rem;
  text-align:center;
}

footer .name{
  font-family:'Poppins';
  font-weight:800;
  font-size:1.2rem;
}

footer .tag{
  margin-top:.3rem;
  opacity:.8;
}

footer .legal{
  margin-top:1rem;
  font-size:.85rem;
  opacity:.6;
}

/* WHATSAPP */
.wa{
  position:fixed;
  right:1rem;
  bottom:1rem;
  width:58px;
  height:58px;
  border-radius:50%;
  background:#25D366;
  color:white;
  display:flex;
  align-items:center;
  justify-content:center;
  box-shadow:0 10px 24px rgba(37,211,102,.45);
  z-index:120;
}

.wa svg{
  width:30px;
  height:30px;
}

/* CELULAR */
@media(max-width:768px){
  .nav-inner{
    padding:.75rem 1rem;
  }

  .brand{
    font-size:.88rem;
    max-width:240px;
  }

  .logo-circle{
    width:34px;
    height:34px;
    font-size:.8rem;
    flex-shrink:0;
  }

  .menu-btn{
    display:flex;
    align-items:center;
    justify-content:center;
    width:42px;
    height:42px;
    border-radius:12px;
    background:rgba(255,255,255,.12);
    color:white;
    font-size:1.6rem;
    cursor:pointer;
  }

  .login-desktop{
    display:none;
  }

  .login-mobile{
    display:block;
    background:var(--accent);
    color:#1a1a1a;
    text-align:center;
    margin-top:.5rem;
  }

  .nav-links{
    position:absolute;
    top:100%;
    left:0;
    right:0;
    background:var(--primary);
    flex-direction:column;
    align-items:stretch;
    padding:1rem;
    display:none;
    box-shadow:0 12px 22px rgba(0,0,0,.2);
  }

  .nav-links a{
    padding:.9rem 1rem;
    border-radius:.8rem;
  }

  #menu-toggle:checked ~ .nav-links{
    display:flex;
  }

  .hero{
    min-height:82vh;
    text-align:left;
  }

  .hero::after{
    background:linear-gradient(180deg,rgba(0,0,0,.58),rgba(22,71,40,.95));
  }

  .hero-content{
    padding:4.5rem 1.2rem 3rem;
  }

  .hero h1{
    font-size:2.35rem;
    line-height:1.08;
  }

  .hero p{
    font-size:1rem;
  }

  .hero-ctas{
    flex-direction:column;
  }

  .hero-ctas .btn{
    width:100%;
  }

  .grid-3,
  .grid-2{
    grid-template-columns:1fr;
  }

  .section{
    padding:2.8rem 0;
  }

  .card{
    padding:1.25rem;
  }

  .tile{
    min-height:260px;
  }

  .tile img{
    min-height:260px;
  }

  .tile-text{
    padding:1.2rem;
  }

  .cta-box{
    padding:2.2rem 1.2rem;
  }
}

@media(max-width:420px){
  .brand span:last-child{
    font-size:.8rem;
  }

  .hero h1{
    font-size:2rem;
  }

  .chip{
    font-size:.78rem;
  }
}
</style>
