# portefolio
<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Kiki Lucandro — Portfolio</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;700&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  :root{
    --bg: #10131a;
    --bg-panel: #161a23;
    --border: #262c38;
    --text: #e7e9ee;
    --text-dim: #8b93a3;
    --accent: #5eead4;
    --accent-2: #f4b860;
  }
  *{ box-sizing: border-box; margin:0; padding:0; }
  html{ scroll-behavior: smooth; }
  body{
    background: var(--bg);
    color: var(--text);
    font-family: 'Space Grotesk', sans-serif;
    line-height: 1.6;
  }
  .mono{ font-family: 'JetBrains Mono', monospace; }

  /* Layout */
  .layout{ display:flex; min-height:100vh; }
  nav.gutter{
    width: 220px;
    flex-shrink:0;
    border-right: 1px solid var(--border);
    padding: 40px 0;
    position: sticky;
    top:0;
    height: 100vh;
  }
  nav.gutter .brand{
    font-family:'JetBrains Mono', monospace;
    font-size: 0.85rem;
    color: var(--text-dim);
    padding: 0 28px 32px;
  }
  nav.gutter .brand strong{ color: var(--text); }
  nav.gutter ul{ list-style:none; }
  nav.gutter li a{
    display:flex;
    gap: 14px;
    padding: 10px 28px;
    color: var(--text-dim);
    text-decoration:none;
    font-size: 0.95rem;
    border-left: 2px solid transparent;
    transition: color .15s, border-color .15s;
  }
  nav.gutter li a .ln{
    font-family:'JetBrains Mono', monospace;
    font-size: 0.8rem;
    color: #3d4454;
    width: 18px;
  }
  nav.gutter li a:hover, nav.gutter li a:focus-visible{
    color: var(--text);
    border-left-color: var(--accent);
  }

  main{ flex:1; min-width:0; }
  section{
    padding: 90px 60px;
    border-bottom: 1px solid var(--border);
    max-width: 780px;
  }
  section:last-of-type{ border-bottom:none; }

  /* Hero */
  #accueil{ padding-top: 110px; }
  #accueil .kicker{
    font-family:'JetBrains Mono', monospace;
    color: var(--accent);
    font-size: 0.9rem;
    margin-bottom: 18px;
  }
  h1{
    font-size: clamp(2.4rem, 5vw, 3.6rem);
    font-weight: 700;
    letter-spacing: -0.01em;
    margin-bottom: 18px;
  }
  #accueil p.lede{
    font-size: 1.15rem;
    color: var(--text-dim);
    max-width: 560px;
    margin-bottom: 34px;
  }
  .cta-row{ display:flex; gap: 16px; flex-wrap: wrap; }
  .btn{
    font-family:'JetBrains Mono', monospace;
    font-size: 0.9rem;
    padding: 12px 22px;
    border-radius: 4px;
    text-decoration:none;
    border: 1px solid var(--border);
    color: var(--text);
    transition: border-color .15s, background .15s;
  }
  .btn.primary{ background: var(--accent); color: #0a0e14; border-color: var(--accent); font-weight: 500; }
  .btn.primary:hover{ opacity: .88; }
  .btn:not(.primary):hover{ border-color: var(--accent); }

  h2{
    font-size: 1.5rem;
    margin-bottom: 28px;
    display:flex;
    align-items:baseline;
    gap: 12px;
  }
  h2 .tag{
    font-family:'JetBrains Mono', monospace;
    font-size: 0.85rem;
    color: var(--text-dim);
    font-weight: 400;
  }

  #apropos p{ color: var(--text-dim); max-width: 620px; }
  #apropos .fill{
    color: var(--accent-2);
    font-family:'JetBrains Mono', monospace;
    font-style: normal;
  }

  /* Skills */
  .skills{ display:flex; flex-wrap:wrap; gap: 10px; }
  .skill{
    font-family:'JetBrains Mono', monospace;
    font-size: 0.85rem;
    padding: 8px 14px;
    border: 1px solid var(--border);
    border-radius: 4px;
    color: var(--text-dim);
    background: var(--bg-panel);
  }
  .skill.fill{ color: var(--accent-2); border-color: #3a3020; }

  /* Projects */
  .project{
    border: 1px solid var(--border);
    background: var(--bg-panel);
    border-radius: 6px;
    padding: 26px 28px;
    margin-bottom: 20px;
  }
  .project h3{
    font-size: 1.1rem;
    margin-bottom: 8px;
  }
  .project h3 .fill{ color: var(--accent-2); font-family:'JetBrains Mono', monospace; font-size: 0.95rem; }
  .project p{ color: var(--text-dim); font-size: 0.95rem; margin-bottom: 12px; }
  .project .stack{
    font-family:'JetBrains Mono', monospace;
    font-size: 0.78rem;
    color: var(--accent);
  }
  .project a.link{
    display:inline-block;
    margin-top: 10px;
    font-family:'JetBrains Mono', monospace;
    font-size: 0.82rem;
    color: var(--text-dim);
    text-decoration: none;
    border-bottom: 1px dashed var(--border);
  }
  .project a.link:hover{ color: var(--accent); border-color: var(--accent); }

  /* Contact */
  #contact ul{ list-style:none; }
  #contact li{ margin-bottom: 12px; }
  #contact a{
    color: var(--text);
    text-decoration:none;
    font-family:'JetBrains Mono', monospace;
    font-size: 0.95rem;
    border-bottom: 1px solid var(--border);
    padding-bottom: 2px;
  }
  #contact a:hover{ color: var(--accent); border-color: var(--accent); }
  #contact .fill{ color: var(--accent-2); }

  footer{
    padding: 30px 60px;
    color: var(--text-dim);
    font-family:'JetBrains Mono', monospace;
    font-size: 0.8rem;
  }

  @media (max-width: 780px){
    .layout{ flex-direction:column; }
    nav.gutter{
      width:100%; height:auto; position:relative;
      display:flex; align-items:center; overflow-x:auto;
      padding: 18px 0;
      border-right:none; border-bottom:1px solid var(--border);
    }
    nav.gutter .brand{ display:none; }
    nav.gutter ul{ display:flex; }
    nav.gutter li a{ padding: 8px 16px; border-left:none; border-bottom:2px solid transparent; white-space:nowrap; }
    nav.gutter li a:hover{ border-left-color:transparent; border-bottom-color: var(--accent); }
    section{ padding: 60px 24px; }
    footer{ padding: 24px; }
  }

  @media (prefers-reduced-motion: reduce){
    html{ scroll-behavior:auto; }
  }
</style>
</head>
<body>
<div class="layout">

  <nav class="gutter">
    <div class="brand"><strong>kiki_lucandro</strong><br>portfolio.html</div>
    <ul>
      <li><a href="#accueil"><span class="ln mono">01</span>Accueil</a></li>
      <li><a href="#apropos"><span class="ln mono">02</span>À propos</a></li>
      <li><a href="#competences"><span class="ln mono">03</span>Compétences</a></li>
      <li><a href="#projets"><span class="ln mono">04</span>Projets</a></li>
      <li><a href="#contact"><span class="ln mono">05</span>Contact</a></li>
    </ul>
  </nav>

  <main>

    <section id="accueil">
      <div class="kicker mono">// développeur en formation</div>
      <h1>Kiki Lucandro</h1>
      <p class="lede">
        Étudiant en BTS SIO option SLAM à Vannes, à la recherche d'un stage.
        <!-- À COMPLÉTER : remplace/ajuste cette phrase avec ta propre accroche -->
      </p>
      <div class="cta-row">
        <a href="#projets" class="btn primary">Voir mes projets</a>
        <a href="#contact" class="btn">Me contacter</a>
      </div>
    </section>

    <section id="apropos">
      <h2>À propos <span class="tag mono">who_am_i</span></h2>
      <p>
        <!-- À COMPLÉTER : 3-4 phrases de présentation (parcours, ce que tu aimes coder, ce que tu cherches) -->
        <span class="fill">[À compléter : ta présentation ici]</span>
      </p>
    </section>

    <section id="competences">
      <h2>Compétences <span class="tag mono">stack</span></h2>
      <div class="skills">
        <span class="skill">SQL</span>
        <span class="skill">HTML / CSS</span>
        <span class="skill fill">[À compléter]</span>
        <span class="skill fill">[À compléter]</span>
        <span class="skill fill">[À compléter]</span>
      </div>
    </section>

    <section id="projets">
      <h2>Projets <span class="tag mono">./projets</span></h2>

      <div class="project">
        <h3>Fiche de révision SQL interactive</h3>
        <p>Support HTML interactif créé pour réviser les bases du SQL (requêtes, jointures, etc.).</p>
        <div class="stack mono">HTML · CSS · JavaScript</div>
        <a class="link" href="#">Voir le projet →</a>
        <!-- À COMPLÉTER : remplace le href par le lien réel du dépôt ou de la démo -->
      </div>

      <div class="project">
        <h3><span class="fill">[À compléter : nom du projet]</span></h3>
        <p><span class="fill">[À compléter : description courte du projet]</span></p>
        <div class="stack mono">[techs]</div>
        <a class="link" href="#">Voir le projet →</a>
      </div>

      <div class="project">
        <h3><span class="fill">[À compléter : nom du projet]</span></h3>
        <p><span class="fill">[À compléter : description courte du projet]</span></p>
        <div class="stack mono">[techs]</div>
        <a class="link" href="#">Voir le projet →</a>
      </div>
    </section>

    <section id="contact">
      <h2>Contact <span class="tag mono">get_in_touch()</span></h2>
      <ul>
        <li>Email : <a href="mailto:contact@exemple.fr" class="fill">[À compléter : ton email]</a></li>
        <li>GitHub : <a href="#" class="fill">[À compléter : lien GitHub]</a></li>
        <li>LinkedIn : <a href="#" class="fill">[À compléter : lien LinkedIn]</a></li>
      </ul>
    </section>

    <footer>
      Vannes, Bretagne — BTS SIO SLAM
    </footer>

  </main>
</div>
</body>
</html>
