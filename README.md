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
<link rel="stylesheet" href="Acueil.css">
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
