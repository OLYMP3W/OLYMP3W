<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
Olympe readme · HTML
<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>OLYMPE — Fondateur & Bâtisseur</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500;700;900&family=Space+Grotesk:wght@400;500;600;700&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  :root{
    --bg: #05070d;
    --bg2: #080c16;
    --panel: rgba(255,255,255,0.03);
    --border: rgba(120,160,220,0.14);
    --cyan: #29e0ff;
    --cyan-dim: rgba(41,224,255,0.35);
    --gold: #d9b24c;
    --gold-dim: rgba(217,178,76,0.35);
    --text: #e9edf6;
    --muted: #7c8aa8;
  }
  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0;
    background:
      radial-gradient(ellipse 120% 60% at 50% -10%, rgba(41,224,255,0.09), transparent 60%),
      radial-gradient(ellipse 100% 50% at 100% 100%, rgba(217,178,76,0.06), transparent 60%),
      var(--bg);
    color:var(--text);
    font-family:'Space Grotesk', sans-serif;
    overflow-x:hidden;
  }
  ::selection{ background: var(--cyan-dim); color:#fff; }
 
  #stars{ position:fixed; inset:0; z-index:0; }
 
  .wrap{ position:relative; z-index:2; max-width:1180px; margin:0 auto; padding:0 32px; }
  .eyebrow{
    font-family:'JetBrains Mono', monospace;
    letter-spacing:0.28em;
    text-transform:uppercase;
    font-size:11.5px;
    color:var(--cyan);
    display:flex; align-items:center; gap:10px;
  }
  .eyebrow::before{
    content:''; width:7px; height:7px; border-radius:50%;
    background:var(--cyan); box-shadow:0 0 12px 2px var(--cyan);
    animation: pulse 1.8s ease-in-out infinite;
  }
  @keyframes pulse{ 0%,100%{opacity:1;} 50%{opacity:.35;} }
 
  /* ---------- HERO ---------- */
  header.hero{
    position:relative; z-index:2;
    min-height:100vh;
    display:flex; flex-direction:column; justify-content:center;
    padding:120px 32px 80px;
    perspective:1400px;
  }
  .hero-inner{ max-width:1180px; margin:0 auto; width:100%; display:grid; grid-template-columns:1.05fr 0.95fr; gap:40px; align-items:center; }
  @media (max-width:920px){ .hero-inner{ grid-template-columns:1fr; } }
 
  h1.name{
    font-family:'Orbitron', sans-serif;
    font-weight:900;
    font-size:clamp(46px, 7.2vw, 92px);
    line-height:0.98;
    margin:18px 0 6px;
    letter-spacing:0.01em;
    background:linear-gradient(115deg, #ffffff 20%, var(--cyan) 55%, #ffffff 80%);
    background-size:220% 100%;
    -webkit-background-clip:text; background-clip:text; color:transparent;
    animation: sheen 6s linear infinite;
  }
  @keyframes sheen{ 0%{background-position:0% 0;} 100%{background-position:220% 0;} }
 
  .role-line{ font-family:'JetBrains Mono', monospace; font-size:14.5px; color:var(--muted); margin-bottom:26px; }
  .role-line b{ color:var(--text); font-weight:500; }
 
  .tagline{ font-size:18px; line-height:1.65; color:#c3cbdd; max-width:520px; margin-bottom:34px; }
  .tagline em{ color:var(--gold); font-style:normal; }
 
  .cta-row{ display:flex; gap:14px; flex-wrap:wrap; }
  .cta{
    font-family:'JetBrains Mono', monospace; font-size:13px; letter-spacing:.04em;
    padding:14px 22px; border-radius:3px; text-decoration:none;
    border:1px solid var(--border); color:var(--text);
    transition: all .25s ease; display:inline-flex; align-items:center; gap:10px;
  }
  .cta.primary{ background:linear-gradient(120deg, var(--cyan), #7ef4ff); color:#031017; border:none; font-weight:600; }
  .cta:hover{ transform:translateY(-2px); border-color:var(--cyan); box-shadow:0 8px 30px -8px var(--cyan-dim); }
  .cta.primary:hover{ box-shadow:0 10px 34px -6px rgba(41,224,255,0.55); }
 
  /* ---------- 3D ORBIT SYSTEM ---------- */
  .orbit-stage{
    position:relative; height:460px;
    display:flex; align-items:center; justify-content:center;
    transform-style:preserve-3d;
  }
  .core{
    position:absolute; width:118px; height:118px; border-radius:50%;
    background:radial-gradient(circle at 35% 30%, #1a2436, #060810 70%);
    border:1px solid var(--cyan-dim);
    box-shadow: 0 0 0 1px rgba(41,224,255,0.08), 0 0 60px -8px var(--cyan-dim), inset 0 0 30px rgba(41,224,255,0.15);
    display:flex; align-items:center; justify-content:center;
    font-family:'Orbitron', sans-serif; font-weight:700; font-size:13px; letter-spacing:.12em; color:var(--cyan);
    z-index:5; animation: corebeat 3.2s ease-in-out infinite;
  }
  @keyframes corebeat{ 0%,100%{ box-shadow:0 0 0 1px rgba(41,224,255,0.08), 0 0 60px -8px var(--cyan-dim), inset 0 0 30px rgba(41,224,255,0.15);} 50%{ box-shadow:0 0 0 1px rgba(41,224,255,0.16), 0 0 90px -6px var(--cyan-dim), inset 0 0 40px rgba(41,224,255,0.25);} }
 
  .ring{
    position:absolute; border-radius:50%;
    border:1px dashed rgba(140,170,220,0.22);
    transform-style:preserve-3d;
  }
  .ring.r1{ width:260px; height:260px; transform:rotateX(72deg); animation: spin 14s linear infinite; }
  .ring.r2{ width:360px; height:360px; transform:rotateX(72deg) rotateZ(35deg); animation: spin 22s linear infinite reverse; border-color:rgba(217,178,76,0.22); }
  .ring.r3{ width:440px; height:440px; transform:rotateX(72deg) rotateZ(-20deg); animation: spin 30s linear infinite; }
  @keyframes spin{ from{ transform:rotateX(72deg) rotateZ(0deg) rotateY(0deg);} to{ transform:rotateX(72deg) rotateZ(0deg) rotateY(360deg);} }
 
  .sat{
    position:absolute; top:50%; left:50%;
    width:auto; white-space:nowrap;
    transform-origin:0 0;
    font-family:'JetBrains Mono', monospace; font-size:11.5px; letter-spacing:.06em;
    padding:6px 12px; border-radius:20px;
    background:rgba(6,10,18,0.75); backdrop-filter:blur(6px);
    border:1px solid var(--border); color:var(--text);
  }
  .sat::before{ content:''; position:absolute; left:-5px; top:50%; transform:translateY(-50%); width:6px; height:6px; border-radius:50%; background:var(--cyan); box-shadow:0 0 10px 2px var(--cyan); }
  .ring.r1 .sat{ animation: counter1 14s linear infinite; margin:-13px 0 0 130px; }
  .ring.r2 .sat{ animation: counter2 22s linear infinite reverse; margin:-13px 0 0 180px; }
  .ring.r3 .sat{ animation: counter2 30s linear infinite; margin:-13px 0 0 220px; }
  @keyframes counter1{ from{ transform:rotateY(0deg) rotateX(-72deg);} to{ transform:rotateY(-360deg) rotateX(-72deg);} }
  @keyframes counter2{ from{ transform:rotateY(0deg) rotateX(-72deg);} to{ transform:rotateY(360deg) rotateX(-72deg);} }
 
  /* ---------- SECTIONS ---------- */
  section{ position:relative; z-index:2; padding:110px 0; }
  .section-head{ margin-bottom:56px; }
  h2.h{
    font-family:'Orbitron', sans-serif; font-weight:700; font-size:clamp(26px,3.4vw,38px);
    margin:10px 0 0; color:#fff;
  }
  .h span{ color:var(--cyan); }
 
  .reveal{ opacity:0; transform:translateY(28px); transition:opacity .8s ease, transform .8s ease; }
  .reveal.in{ opacity:1; transform:translateY(0); }
 
  /* Ventures */
  .ventures{ display:grid; grid-template-columns:repeat(3,1fr); gap:22px; perspective:1200px; }
  @media (max-width:900px){ .ventures{ grid-template-columns:1fr; } }
  .vcard{
    position:relative; border:1px solid var(--border); border-radius:8px;
    padding:30px 26px; background:linear-gradient(180deg, var(--panel), transparent);
    transform-style:preserve-3d; transition: transform .5s cubic-bezier(.2,.8,.2,1), border-color .4s ease, box-shadow .5s ease;
  }
  .vcard:hover{ transform: rotateY(-6deg) rotateX(4deg) translateZ(10px); border-color:var(--cyan-dim); box-shadow:0 30px 60px -30px rgba(41,224,255,0.35); }
  .vcard .tag{ font-family:'JetBrains Mono', monospace; font-size:11px; letter-spacing:.14em; color:var(--gold); text-transform:uppercase; }
  .vcard h3{ font-family:'Space Grotesk',sans-serif; font-size:22px; font-weight:700; margin:12px 0 10px; color:#fff; }
  .vcard p{ color:var(--muted); font-size:14.5px; line-height:1.6; margin:0 0 16px; }
  .vcard .stat{ font-family:'JetBrains Mono', monospace; font-size:12px; color:var(--cyan); border-top:1px solid var(--border); padding-top:14px; margin-top:auto; }
 
  /* Network map (pan-African footprint) */
  .netmap{
    position:relative; border:1px solid var(--border); border-radius:10px;
    padding:40px; background:radial-gradient(ellipse at center, rgba(41,224,255,0.05), transparent 70%);
    overflow:hidden;
  }
  .netmap svg{ width:100%; height:auto; display:block; }
  .node-label{ font-family:'JetBrains Mono', monospace; font-size:10.5px; fill:var(--muted); letter-spacing:.05em; }
  .node-dot{ fill:var(--cyan); filter:drop-shadow(0 0 6px var(--cyan)); }
  .link-line{ stroke:url(#lg); stroke-width:1.1; fill:none; stroke-dasharray:4 5; animation: dash 3.5s linear infinite; opacity:.55; }
  @keyframes dash{ to{ stroke-dashoffset:-90; } }
  .node-core{ fill:var(--gold); filter:drop-shadow(0 0 10px var(--gold)); }
 
  /* Timeline / trajectory */
  .traj{ display:flex; flex-direction:column; gap:0; border-left:1px solid var(--border); margin-left:8px; }
  .tstep{ position:relative; padding:0 0 46px 32px; }
  .tstep:last-child{ padding-bottom:0; }
  .tstep::before{ content:''; position:absolute; left:-5.5px; top:2px; width:10px; height:10px; border-radius:50%; background:var(--bg); border:2px solid var(--cyan); }
  .tstep .tt{ font-family:'JetBrains Mono', monospace; font-size:11px; color:var(--gold); letter-spacing:.1em; text-transform:uppercase; }
  .tstep h4{ margin:6px 0 6px; font-size:19px; font-weight:600; color:#fff; }
  .tstep p{ margin:0; color:var(--muted); font-size:14.5px; line-height:1.6; max-width:620px; }
 
  footer{ position:relative; z-index:2; padding:70px 0 60px; border-top:1px solid var(--border); margin-top:40px; }
  footer .foot-inner{ display:flex; justify-content:space-between; align-items:center; flex-wrap:wrap; gap:16px; }
  .signature{ font-family:'Orbitron',sans-serif; font-weight:700; letter-spacing:.08em; color:#fff; }
  .signature span{ color:var(--cyan); }
  .coord{ font-family:'JetBrains Mono', monospace; font-size:12px; color:var(--muted); }
 
  @media (prefers-reduced-motion: reduce){
    *{ animation-duration:0.001ms !important; animation-iteration-count:1 !important; transition-duration:0.001ms !important; }
  }
</style>
</head>
<body>
 
<canvas id="stars"></canvas>
 
<header class="hero">
  <div class="hero-inner">
    <div>
      <div class="eyebrow">Bâtisseur pan-africain — Port-Gentil, Gabon</div>
      <h1 class="name">OLYMPE</h1>
      <div class="role-line">Sous-Chef @ <b>ACA</b> · Fondateur &amp; CEO @ <b>DOMIA</b> · Créateur @ <b>DocFlow</b></div>
      <p class="tagline">Je construis l'infrastructure de la prochaine décennie africaine — <em>immobilier</em>, <em>documents</em>, <em>commerce</em> — pièce par pièce, marché par marché.</p>
      <div class="cta-row">
        <a href="#ventures" class="cta primary">Explorer les projets ↓</a>
        <a href="#network" class="cta">Voir l'empreinte pan-africaine</a>
      </div>
    </div>
 
    <div class="orbit-stage">
      <div class="ring r1"><div class="sat">ACA</div></div>
      <div class="ring r2"><div class="sat">DOMIA</div></div>
      <div class="ring r3"><div class="sat">DOCFLOW</div></div>
      <div class="core">OLYMPE</div>
    </div>
  </div>
</header>
 
<div class="wrap">
 
  <section id="ventures">
    <div class="section-head reveal">
      <div class="eyebrow">01 — Portefeuille</div>
      <h2 class="h">Trois fronts, <span>une seule vision</span></h2>
    </div>
    <div class="ventures">
      <div class="vcard reveal">
        <div class="tag">Agence</div>
        <h3>ACA</h3>
        <p>Sous-chef de projet au sein d'Acreative Agency Group, agence créative et digitale — production éditoriale, identités de marque et exécution client au quotidien.</p>
        <div class="stat">RÔLE — Sous-Chef / Chef de Projet Adjoint</div>
      </div>
      <div class="vcard reveal">
        <div class="tag">Fondateur</div>
        <h3>DOMIA</h3>
        <p>Plateforme pan-africaine d'annonces immobilières et automobiles, pensée pour les marchés francophones — de la maison à la voiture, un seul endroit de confiance.</p>
        <div class="stat">EMPREINTE — 6 pays · Gabon, RDC, Cameroun, Bénin, Guinée, Congo-Brazza</div>
      </div>
      <div class="vcard reveal">
        <div class="tag">Fondateur</div>
        <h3>DocFlow</h3>
        <p>Infrastructure SaaS de conformité administrative — le "Canva des documents" pour les PME africaines : factures, contrats, RH, générés en minutes.</p>
        <div class="stat">AMBITION — Devenir l'OS administratif francophone</div>
      </div>
    </div>
  </section>
 
  <section id="network">
    <div class="section-head reveal">
      <div class="eyebrow">02 — Empreinte</div>
      <h2 class="h">Un réseau à <span>l'échelle du continent</span></h2>
    </div>
    <div class="netmap reveal">
      <svg viewBox="0 0 900 380" xmlns="http://www.w3.org/2000/svg">
        <defs>
          <linearGradient id="lg" x1="0" y1="0" x2="1" y2="0">
            <stop offset="0%" stop-color="#29e0ff"/>
            <stop offset="100%" stop-color="#d9b24c"/>
          </linearGradient>
        </defs>
        <!-- links from core (Gabon) to each market -->
        <path class="link-line" d="M450,190 C400,140 340,110 260,95"/>
        <path class="link-line" d="M450,190 C480,120 520,90 560,70"/>
        <path class="link-line" d="M450,190 C500,220 560,235 620,250"/>
        <path class="link-line" d="M450,190 C400,240 340,270 280,300"/>
        <path class="link-line" d="M450,190 C420,260 400,300 380,335"/>
        <!-- core node: Gabon -->
        <circle class="node-core" cx="450" cy="190" r="8"/>
        <text class="node-label" x="450" y="215" text-anchor="middle">GABON · SIÈGE</text>
        <!-- market nodes -->
        <circle class="node-dot" cx="260" cy="95" r="5"/>
        <text class="node-label" x="260" y="82" text-anchor="middle">GUINÉE</text>
        <circle class="node-dot" cx="560" cy="70" r="5"/>
        <text class="node-label" x="560" y="57" text-anchor="middle">BÉNIN</text>
        <circle class="node-dot" cx="620" cy="250" r="5"/>
        <text class="node-label" x="640" y="255" text-anchor="middle">RDC</text>
        <circle class="node-dot" cx="280" cy="300" r="5"/>
        <text class="node-label" x="255" y="322" text-anchor="middle">CAMEROUN</text>
        <circle class="node-dot" cx="380" cy="335" r="5"/>
        <text class="node-label" x="380" y="358" text-anchor="middle">CONGO-BRAZZA</text>
      </svg>
    </div>
  </section>
 
  <section id="trajectory">
    <div class="section-head reveal">
      <div class="eyebrow">03 — Trajectoire</div>
      <h2 class="h">Construit en <span>public, livré vite</span></h2>
    </div>
    <div class="traj reveal">
      <div class="tstep">
        <div class="tt">Fondation</div>
        <h4>Pacte des Fondateurs — DOMIA</h4>
        <p>Gouvernance et vesting conformes OHADA, répartition 55/15/15/15, structure inspirée des standards Silicon Valley.</p>
      </div>
      <div class="tstep">
        <div class="tt">Construction</div>
        <h4>DocFlow prend forme</h4>
        <p>De la landing page à l'éditeur temps réel : facture, devis, contrats — repositionné en infrastructure de conformité pour les PME émergentes.</p>
      </div>
      <div class="tstep">
        <div class="tt">Expansion</div>
        <h4>Suivi terrain sur 6 pays</h4>
        <p>Tableau de bord de collecte sur 8 semaines pour armer le lancement commercial de DOMIA à l'échelle régionale.</p>
      </div>
    </div>
  </section>
 
</div>
 
<footer>
  <div class="wrap foot-inner">
    <div class="signature">OLYMPE<span>.</span> — LE FUTUR SE CONSTRUIT ICI</div>
    <div class="coord">PORT-GENTIL · GABON — 09.1°N 8.8°E</div>
  </div>
</footer>
 
<script>
  // Starfield canvas
  const canvas = document.getElementById('stars');
  const ctx = canvas.getContext('2d');
  let w, h, stars = [];
  function resize(){
    w = canvas.width = window.innerWidth;
    h = canvas.height = window.innerHeight * 2.4;
    const count = Math.floor((w*h)/9000);
    stars = Array.from({length:count}, ()=>({
      x:Math.random()*w, y:Math.random()*h,
      r:Math.random()*1.3+0.2,
      s:Math.random()*0.5+0.1,
      o:Math.random()*0.6+0.2
    }));
  }
  function draw(){
    ctx.clearRect(0,0,w,h);
    ctx.fillStyle = '#050710';
    ctx.fillRect(0,0,w,h);
    for(const st of stars){
      st.y += st.s;
      if(st.y > h) st.y = 0;
      ctx.beginPath();
      ctx.arc(st.x, st.y, st.r, 0, Math.PI*2);
      ctx.fillStyle = `rgba(150,200,255,${st.o})`;
      ctx.fill();
    }
    requestAnimationFrame(draw);
  }
  resize();
  window.addEventListener('resize', resize);
  draw();
 
  // Scroll reveal
  const io = new IntersectionObserver((entries)=>{
    entries.forEach(e=>{ if(e.isIntersecting){ e.target.classList.add('in'); } });
  }, {threshold:0.15});
  document.querySelectorAll('.reveal').forEach(el=>io.observe(el));
</script>
 
</body>
</html>
 
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>OLYMPE — Fondateur & Bâtisseur</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500;700;900&family=Space+Grotesk:wght@400;500;600;700&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  :root{
    --bg: #05070d;
    --bg2: #080c16;
    --panel: rgba(255,255,255,0.03);
    --border: rgba(120,160,220,0.14);
    --cyan: #29e0ff;
    --cyan-dim: rgba(41,224,255,0.35);
    --gold: #d9b24c;
    --gold-dim: rgba(217,178,76,0.35);
    --text: #e9edf6;
    --muted: #7c8aa8;
  }
  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0;
    background:
      radial-gradient(ellipse 120% 60% at 50% -10%, rgba(41,224,255,0.09), transparent 60%),
      radial-gradient(ellipse 100% 50% at 100% 100%, rgba(217,178,76,0.06), transparent 60%),
      var(--bg);
    color:var(--text);
    font-family:'Space Grotesk', sans-serif;
    overflow-x:hidden;
  }
  ::selection{ background: var(--cyan-dim); color:#fff; }

  #stars{ position:fixed; inset:0; z-index:0; }

  .wrap{ position:relative; z-index:2; max-width:1180px; margin:0 auto; padding:0 32px; }
  .eyebrow{
    font-family:'JetBrains Mono', monospace;
    letter-spacing:0.28em;
    text-transform:uppercase;
    font-size:11.5px;
    color:var(--cyan);
    display:flex; align-items:center; gap:10px;
  }
  .eyebrow::before{
    content:''; width:7px; height:7px; border-radius:50%;
    background:var(--cyan); box-shadow:0 0 12px 2px var(--cyan);
    animation: pulse 1.8s ease-in-out infinite;
  }
  @keyframes pulse{ 0%,100%{opacity:1;} 50%{opacity:.35;} }

  /* ---------- HERO ---------- */
  header.hero{
    position:relative; z-index:2;
    min-height:100vh;
    display:flex; flex-direction:column; justify-content:center;
    padding:120px 32px 80px;
    perspective:1400px;
  }
  .hero-inner{ max-width:1180px; margin:0 auto; width:100%; display:grid; grid-template-columns:1.05fr 0.95fr; gap:40px; align-items:center; }
  @media (max-width:920px){ .hero-inner{ grid-template-columns:1fr; } }

  h1.name{
    font-family:'Orbitron', sans-serif;
    font-weight:900;
    font-size:clamp(46px, 7.2vw, 92px);
    line-height:0.98;
    margin:18px 0 6px;
    letter-spacing:0.01em;
    background:linear-gradient(115deg, #ffffff 20%, var(--cyan) 55%, #ffffff 80%);
    background-size:220% 100%;
    -webkit-background-clip:text; background-clip:text; color:transparent;
    animation: sheen 6s linear infinite;
  }
  @keyframes sheen{ 0%{background-position:0% 0;} 100%{background-position:220% 0;} }

  .role-line{ font-family:'JetBrains Mono', monospace; font-size:14.5px; color:var(--muted); margin-bottom:26px; }
  .role-line b{ color:var(--text); font-weight:500; }

  .tagline{ font-size:18px; line-height:1.65; color:#c3cbdd; max-width:520px; margin-bottom:34px; }
  .tagline em{ color:var(--gold); font-style:normal; }

  .cta-row{ display:flex; gap:14px; flex-wrap:wrap; }
  .cta{
    font-family:'JetBrains Mono', monospace; font-size:13px; letter-spacing:.04em;
    padding:14px 22px; border-radius:3px; text-decoration:none;
    border:1px solid var(--border); color:var(--text);
    transition: all .25s ease; display:inline-flex; align-items:center; gap:10px;
  }
  .cta.primary{ background:linear-gradient(120deg, var(--cyan), #7ef4ff); color:#031017; border:none; font-weight:600; }
  .cta:hover{ transform:translateY(-2px); border-color:var(--cyan); box-shadow:0 8px 30px -8px var(--cyan-dim); }
  .cta.primary:hover{ box-shadow:0 10px 34px -6px rgba(41,224,255,0.55); }

  /* ---------- 3D ORBIT SYSTEM ---------- */
  .orbit-stage{
    position:relative; height:460px;
    display:flex; align-items:center; justify-content:center;
    transform-style:preserve-3d;
  }
  .core{
    position:absolute; width:118px; height:118px; border-radius:50%;
    background:radial-gradient(circle at 35% 30%, #1a2436, #060810 70%);
    border:1px solid var(--cyan-dim);
    box-shadow: 0 0 0 1px rgba(41,224,255,0.08), 0 0 60px -8px var(--cyan-dim), inset 0 0 30px rgba(41,224,255,0.15);
    display:flex; align-items:center; justify-content:center;
    font-family:'Orbitron', sans-serif; font-weight:700; font-size:13px; letter-spacing:.12em; color:var(--cyan);
    z-index:5; animation: corebeat 3.2s ease-in-out infinite;
  }
  @keyframes corebeat{ 0%,100%{ box-shadow:0 0 0 1px rgba(41,224,255,0.08), 0 0 60px -8px var(--cyan-dim), inset 0 0 30px rgba(41,224,255,0.15);} 50%{ box-shadow:0 0 0 1px rgba(41,224,255,0.16), 0 0 90px -6px var(--cyan-dim), inset 0 0 40px rgba(41,224,255,0.25);} }

  .ring{
    position:absolute; border-radius:50%;
    border:1px dashed rgba(140,170,220,0.22);
    transform-style:preserve-3d;
  }
  .ring.r1{ width:260px; height:260px; transform:rotateX(72deg); animation: spin 14s linear infinite; }
  .ring.r2{ width:360px; height:360px; transform:rotateX(72deg) rotateZ(35deg); animation: spin 22s linear infinite reverse; border-color:rgba(217,178,76,0.22); }
  .ring.r3{ width:440px; height:440px; transform:rotateX(72deg) rotateZ(-20deg); animation: spin 30s linear infinite; }
  @keyframes spin{ from{ transform:rotateX(72deg) rotateZ(0deg) rotateY(0deg);} to{ transform:rotateX(72deg) rotateZ(0deg) rotateY(360deg);} }

  .sat{
    position:absolute; top:50%; left:50%;
    width:auto; white-space:nowrap;
    transform-origin:0 0;
    font-family:'JetBrains Mono', monospace; font-size:11.5px; letter-spacing:.06em;
    padding:6px 12px; border-radius:20px;
    background:rgba(6,10,18,0.75); backdrop-filter:blur(6px);
    border:1px solid var(--border); color:var(--text);
  }
  .sat::before{ content:''; position:absolute; left:-5px; top:50%; transform:translateY(-50%); width:6px; height:6px; border-radius:50%; background:var(--cyan); box-shadow:0 0 10px 2px var(--cyan); }
  .ring.r1 .sat{ animation: counter1 14s linear infinite; margin:-13px 0 0 130px; }
  .ring.r2 .sat{ animation: counter2 22s linear infinite reverse; margin:-13px 0 0 180px; }
  .ring.r3 .sat{ animation: counter2 30s linear infinite; margin:-13px 0 0 220px; }
  @keyframes counter1{ from{ transform:rotateY(0deg) rotateX(-72deg);} to{ transform:rotateY(-360deg) rotateX(-72deg);} }
  @keyframes counter2{ from{ transform:rotateY(0deg) rotateX(-72deg);} to{ transform:rotateY(360deg) rotateX(-72deg);} }

  /* ---------- SECTIONS ---------- */
  section{ position:relative; z-index:2; padding:110px 0; }
  .section-head{ margin-bottom:56px; }
  h2.h{
    font-family:'Orbitron', sans-serif; font-weight:700; font-size:clamp(26px,3.4vw,38px);
    margin:10px 0 0; color:#fff;
  }
  .h span{ color:var(--cyan); }

  .reveal{ opacity:0; transform:translateY(28px); transition:opacity .8s ease, transform .8s ease; }
  .reveal.in{ opacity:1; transform:translateY(0); }

  /* Ventures */
  .ventures{ display:grid; grid-template-columns:repeat(3,1fr); gap:22px; perspective:1200px; }
  @media (max-width:900px){ .ventures{ grid-template-columns:1fr; } }
  .vcard{
    position:relative; border:1px solid var(--border); border-radius:8px;
    padding:30px 26px; background:linear-gradient(180deg, var(--panel), transparent);
    transform-style:preserve-3d; transition: transform .5s cubic-bezier(.2,.8,.2,1), border-color .4s ease, box-shadow .5s ease;
  }
  .vcard:hover{ transform: rotateY(-6deg) rotateX(4deg) translateZ(10px); border-color:var(--cyan-dim); box-shadow:0 30px 60px -30px rgba(41,224,255,0.35); }
  .vcard .tag{ font-family:'JetBrains Mono', monospace; font-size:11px; letter-spacing:.14em; color:var(--gold); text-transform:uppercase; }
  .vcard h3{ font-family:'Space Grotesk',sans-serif; font-size:22px; font-weight:700; margin:12px 0 10px; color:#fff; }
  .vcard p{ color:var(--muted); font-size:14.5px; line-height:1.6; margin:0 0 16px; }
  .vcard .stat{ font-family:'JetBrains Mono', monospace; font-size:12px; color:var(--cyan); border-top:1px solid var(--border); padding-top:14px; margin-top:auto; }

  /* Network map (pan-African footprint) */
  .netmap{
    position:relative; border:1px solid var(--border); border-radius:10px;
    padding:40px; background:radial-gradient(ellipse at center, rgba(41,224,255,0.05), transparent 70%);
    overflow:hidden;
  }
  .netmap svg{ width:100%; height:auto; display:block; }
  .node-label{ font-family:'JetBrains Mono', monospace; font-size:10.5px; fill:var(--muted); letter-spacing:.05em; }
  .node-dot{ fill:var(--cyan); filter:drop-shadow(0 0 6px var(--cyan)); }
  .link-line{ stroke:url(#lg); stroke-width:1.1; fill:none; stroke-dasharray:4 5; animation: dash 3.5s linear infinite; opacity:.55; }
  @keyframes dash{ to{ stroke-dashoffset:-90; } }
  .node-core{ fill:var(--gold); filter:drop-shadow(0 0 10px var(--gold)); }

  /* Timeline / trajectory */
  .traj{ display:flex; flex-direction:column; gap:0; border-left:1px solid var(--border); margin-left:8px; }
  .tstep{ position:relative; padding:0 0 46px 32px; }
  .tstep:last-child{ padding-bottom:0; }
  .tstep::before{ content:''; position:absolute; left:-5.5px; top:2px; width:10px; height:10px; border-radius:50%; background:var(--bg); border:2px solid var(--cyan); }
  .tstep .tt{ font-family:'JetBrains Mono', monospace; font-size:11px; color:var(--gold); letter-spacing:.1em; text-transform:uppercase; }
  .tstep h4{ margin:6px 0 6px; font-size:19px; font-weight:600; color:#fff; }
  .tstep p{ margin:0; color:var(--muted); font-size:14.5px; line-height:1.6; max-width:620px; }

  footer{ position:relative; z-index:2; padding:70px 0 60px; border-top:1px solid var(--border); margin-top:40px; }
  footer .foot-inner{ display:flex; justify-content:space-between; align-items:center; flex-wrap:wrap; gap:16px; }
  .signature{ font-family:'Orbitron',sans-serif; font-weight:700; letter-spacing:.08em; color:#fff; }
  .signature span{ color:var(--cyan); }
  .coord{ font-family:'JetBrains Mono', monospace; font-size:12px; color:var(--muted); }

  @media (prefers-reduced-motion: reduce){
    *{ animation-duration:0.001ms !important; animation-iteration-count:1 !important; transition-duration:0.001ms !important; }
  }
</style>
</head>
<body>

<canvas id="stars"></canvas>

<header class="hero">
  <div class="hero-inner">
    <div>
      <div class="eyebrow">Bâtisseur pan-africain — Port-Gentil, Gabon</div>
      <h1 class="name">OLYMPE</h1>
      <div class="role-line">Sous-Chef @ <b>ACA</b> · Fondateur &amp; CEO @ <b>DOMIA</b> · Créateur @ <b>DocFlow</b></div>
      <p class="tagline">Je construis l'infrastructure de la prochaine décennie africaine — <em>immobilier</em>, <em>documents</em>, <em>commerce</em> — pièce par pièce, marché par marché.</p>
      <div class="cta-row">
        <a href="#ventures" class="cta primary">Explorer les projets ↓</a>
        <a href="#network" class="cta">Voir l'empreinte pan-africaine</a>
      </div>
    </div>

    <div class="orbit-stage">
      <div class="ring r1"><div class="sat">ACA</div></div>
      <div class="ring r2"><div class="sat">DOMIA</div></div>
      <div class="ring r3"><div class="sat">DOCFLOW</div></div>
      <div class="core">OLYMPE</div>
    </div>
  </div>
</header>

<div class="wrap">

  <section id="ventures">
    <div class="section-head reveal">
      <div class="eyebrow">01 — Portefeuille</div>
      <h2 class="h">Trois fronts, <span>une seule vision</span></h2>
    </div>
    <div class="ventures">
      <div class="vcard reveal">
        <div class="tag">Agence</div>
        <h3>ACA</h3>
        <p>Sous-chef de projet au sein d'Acreative Agency Group, agence créative et digitale — production éditoriale, identités de marque et exécution client au quotidien.</p>
        <div class="stat">RÔLE — Sous-Chef / Chef de Projet Adjoint</div>
      </div>
      <div class="vcard reveal">
        <div class="tag">Fondateur</div>
        <h3>DOMIA</h3>
        <p>Plateforme pan-africaine d'annonces immobilières et automobiles, pensée pour les marchés francophones — de la maison à la voiture, un seul endroit de confiance.</p>
        <div class="stat">EMPREINTE — 6 pays · Gabon, RDC, Cameroun, Bénin, Guinée, Congo-Brazza</div>
      </div>
      <div class="vcard reveal">
        <div class="tag">Fondateur</div>
        <h3>DocFlow</h3>
        <p>Infrastructure SaaS de conformité administrative — le "Canva des documents" pour les PME africaines : factures, contrats, RH, générés en minutes.</p>
        <div class="stat">AMBITION — Devenir l'OS administratif francophone</div>
      </div>
    </div>
  </section>

  <section id="network">
    <div class="section-head reveal">
      <div class="eyebrow">02 — Empreinte</div>
      <h2 class="h">Un réseau à <span>l'échelle du continent</span></h2>
    </div>
    <div class="netmap reveal">
      <svg viewBox="0 0 900 380" xmlns="http://www.w3.org/2000/svg">
        <defs>
          <linearGradient id="lg" x1="0" y1="0" x2="1" y2="0">
            <stop offset="0%" stop-color="#29e0ff"/>
            <stop offset="100%" stop-color="#d9b24c"/>
          </linearGradient>
        </defs>
        <!-- links from core (Gabon) to each market -->
        <path class="link-line" d="M450,190 C400,140 340,110 260,95"/>
        <path class="link-line" d="M450,190 C480,120 520,90 560,70"/>
        <path class="link-line" d="M450,190 C500,220 560,235 620,250"/>
        <path class="link-line" d="M450,190 C400,240 340,270 280,300"/>
        <path class="link-line" d="M450,190 C420,260 400,300 380,335"/>
        <!-- core node: Gabon -->
        <circle class="node-core" cx="450" cy="190" r="8"/>
        <text class="node-label" x="450" y="215" text-anchor="middle">GABON · SIÈGE</text>
        <!-- market nodes -->
        <circle class="node-dot" cx="260" cy="95" r="5"/>
        <text class="node-label" x="260" y="82" text-anchor="middle">GUINÉE</text>
        <circle class="node-dot" cx="560" cy="70" r="5"/>
        <text class="node-label" x="560" y="57" text-anchor="middle">BÉNIN</text>
        <circle class="node-dot" cx="620" cy="250" r="5"/>
        <text class="node-label" x="640" y="255" text-anchor="middle">RDC</text>
        <circle class="node-dot" cx="280" cy="300" r="5"/>
        <text class="node-label" x="255" y="322" text-anchor="middle">CAMEROUN</text>
        <circle class="node-dot" cx="380" cy="335" r="5"/>
        <text class="node-label" x="380" y="358" text-anchor="middle">CONGO-BRAZZA</text>
      </svg>
    </div>
  </section>

  <section id="trajectory">
    <div class="section-head reveal">
      <div class="eyebrow">03 — Trajectoire</div>
      <h2 class="h">Construit en <span>public, livré vite</span></h2>
    </div>
    <div class="traj reveal">
      <div class="tstep">
        <div class="tt">Fondation</div>
        <h4>Pacte des Fondateurs — DOMIA</h4>
        <p>Gouvernance et vesting conformes OHADA, répartition 55/15/15/15, structure inspirée des standards Silicon Valley.</p>
      </div>
      <div class="tstep">
        <div class="tt">Construction</div>
        <h4>DocFlow prend forme</h4>
        <p>De la landing page à l'éditeur temps réel : facture, devis, contrats — repositionné en infrastructure de conformité pour les PME émergentes.</p>
      </div>
      <div class="tstep">
        <div class="tt">Expansion</div>
        <h4>Suivi terrain sur 6 pays</h4>
        <p>Tableau de bord de collecte sur 8 semaines pour armer le lancement commercial de DOMIA à l'échelle régionale.</p>
      </div>
    </div>
  </section>

</div>

<footer>
  <div class="wrap foot-inner">
    <div class="signature">OLYMPE<span>.</span> — LE FUTUR SE CONSTRUIT ICI</div>
    <div class="coord">PORT-GENTIL · GABON — 09.1°N 8.8°E</div>
  </div>
</footer>

<script>
  // Starfield canvas
  const canvas = document.getElementById('stars');
  const ctx = canvas.getContext('2d');
  let w, h, stars = [];
  function resize(){
    w = canvas.width = window.innerWidth;
    h = canvas.height = window.innerHeight * 2.4;
    const count = Math.floor((w*h)/9000);
    stars = Array.from({length:count}, ()=>({
      x:Math.random()*w, y:Math.random()*h,
      r:Math.random()*1.3+0.2,
      s:Math.random()*0.5+0.1,
      o:Math.random()*0.6+0.2
    }));
  }
  function draw(){
    ctx.clearRect(0,0,w,h);
    ctx.fillStyle = '#050710';
    ctx.fillRect(0,0,w,h);
    for(const st of stars){
      st.y += st.s;
      if(st.y > h) st.y = 0;
      ctx.beginPath();
      ctx.arc(st.x, st.y, st.r, 0, Math.PI*2);
      ctx.fillStyle = `rgba(150,200,255,${st.o})`;
      ctx.fill();
    }
    requestAnimationFrame(draw);
  }
  resize();
  window.addEventListener('resize', resize);
  draw();

  // Scroll reveal
  const io = new IntersectionObserver((entries)=>{
    entries.forEach(e=>{ if(e.isIntersecting){ e.target.classList.add('in'); } });
  }, {threshold:0.15});
  document.querySelectorAll('.reveal').forEach(el=>io.observe(el));
</script>

</body>
</html>
