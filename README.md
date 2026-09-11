[index.html](https://github.com/user-attachments/files/32088117/index.html)
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Renuevo — Reto Postparto con Jessica</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,400;0,9..144,500;0,9..144,600;1,9..144,500&family=Karla:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
  :root{
    --bg: #F3EEE7;
    --bg-panel: #EAE2D6;
    --ink: #2A2130;
    --ink-soft: #5B5460;
    --rose: #A63B54;
    --rose-deep: #7E2B40;
    --sage: #5B6E4F;
    --gold: #E3A857;
    --line: #D9CFC1;
    --paper: #FBF8F3;
    --max: 1120px;
  }
  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0;
    background:var(--bg);
    color:var(--ink);
    font-family:'Karla', sans-serif;
    font-size:17px;
    line-height:1.6;
    -webkit-font-smoothing:antialiased;
  }
  h1,h2,h3,.serif{
    font-family:'Fraunces', serif;
    font-weight:500;
    line-height:1.15;
    margin:0;
    color:var(--ink);
  }
  p{margin:0 0 1em;}
  a{color:inherit;}
  .wrap{max-width:var(--max); margin:0 auto; padding:0 28px;}
  img{max-width:100%; display:block;}

  /* NAV */
  header{
    position:sticky; top:0; z-index:50;
    background:rgba(243,238,231,0.92);
    backdrop-filter:blur(6px);
    border-bottom:1px solid var(--line);
  }
  nav.wrap{
    display:flex; align-items:center; justify-content:space-between;
    padding:18px 28px;
  }
  .logo{font-family:'Fraunces', serif; font-size:1.4rem; letter-spacing:0.01em;}
  .logo span{color:var(--rose);}
  .navlinks{display:flex; gap:32px; font-size:0.95rem; list-style:none; margin:0; padding:0;}
  .navlinks a{text-decoration:none; color:var(--ink-soft); transition:color .2s;}
  .navlinks a:hover{color:var(--rose);}
  .nav-cta{
    background:var(--rose); color:var(--paper); text-decoration:none;
    padding:10px 22px; border-radius:2px; font-size:0.92rem; font-weight:600;
    white-space:nowrap;
  }
  .menu-btn{display:none; background:none; border:none; font-size:1.6rem; cursor:pointer; color:var(--ink);}

  /* HERO */
  .hero{
    display:grid; grid-template-columns:1.1fr 0.9fr; gap:0;
    align-items:stretch; min-height:640px;
  }
  .hero-text{
    display:flex; flex-direction:column; justify-content:center;
    padding:80px 60px 80px 0; margin-left:28px; max-width:560px;
  }
  .hero-text h1{font-size:2.9rem; margin-bottom:26px;}
  .hero-text h1 em{font-style:italic; color:var(--rose-deep);}
  .hero-sub{font-size:1.15rem; color:var(--ink-soft); max-width:480px; margin-bottom:34px;}
  .cta-row{display:flex; align-items:center; gap:18px; flex-wrap:wrap;}
  .btn-primary{
    background:var(--rose); color:var(--paper); text-decoration:none;
    padding:16px 34px; font-weight:600; font-size:1rem; border-radius:2px;
    border:none; cursor:pointer; display:inline-block;
  }
  .btn-primary:hover{background:var(--rose-deep);}
  .microcopy{font-size:0.88rem; color:var(--ink-soft);}
  .hero-visual{
    position:relative;
    background:linear-gradient(155deg, var(--gold) 0%, var(--rose) 55%, var(--rose-deep) 100%);
    display:flex; align-items:flex-end; justify-content:center;
    min-height:400px;
  }
  .photo-slot{
    width:100%; height:100%; min-height:400px;
    display:flex; align-items:center; justify-content:center;
    color:rgba(255,255,255,0.85); font-family:'Fraunces', serif; font-style:italic;
    font-size:1rem; text-align:center; padding:20px;
  }

  /* SECTIONS */
  section{padding:96px 0;}
  .section-line{border-top:1px solid var(--line);}
  .eyebrow-label{font-size:0.85rem; color:var(--rose-deep); font-weight:600; margin-bottom:10px; display:block;}
  h2.head{font-size:2.1rem; max-width:640px; margin-bottom:22px;}
  .lede{font-size:1.1rem; color:var(--ink-soft); max-width:600px;}

  /* STORY */
  .story{display:grid; grid-template-columns:0.85fr 1.15fr; gap:64px; align-items:center;}
  .story .photo-slot{
    background:var(--bg-panel); color:var(--ink-soft); min-height:460px;
    border:1px solid var(--line);
  }
  .story blockquote{
    font-family:'Fraunces', serif; font-style:italic; font-size:1.5rem;
    color:var(--rose-deep); border-left:3px solid var(--rose); padding-left:24px;
    margin:28px 0;
  }

  /* FOR WHOM */
  .for-grid{display:grid; grid-template-columns:1fr 1fr; gap:56px; margin-top:48px;}
  .for-col h3{font-size:1.2rem; margin-bottom:20px;}
  .for-col ul{list-style:none; margin:0; padding:0;}
  .for-col li{
    padding:14px 0 14px 30px; position:relative; border-bottom:1px solid var(--line);
    color:var(--ink-soft); font-size:0.98rem;
  }
  .yes li:before{content:"✓"; position:absolute; left:0; color:var(--sage); font-weight:700;}
  .no li:before{content:"✕"; position:absolute; left:0; color:var(--rose); font-weight:700;}

  /* PHASES */
  .phases{margin-top:56px;}
  .phase{
    display:grid; grid-template-columns:90px 1fr; gap:28px;
    padding:34px 0; border-top:1px solid var(--line);
  }
  .phase:last-child{border-bottom:1px solid var(--line);}
  .phase-num{font-family:'Fraunces', serif; font-size:2.2rem; color:var(--rose); font-style:italic;}
  .phase h3{font-size:1.25rem; margin-bottom:10px;}
  .phase p{color:var(--ink-soft); max-width:620px;}

  /* FAITH SECTION */
  .faith{background:var(--rose-deep); color:var(--paper);}
  .faith h2.head{color:var(--paper);}
  .faith .lede{color:rgba(251,248,243,0.82);}
  .faith blockquote{
    font-family:'Fraunces', serif; font-style:italic; font-size:1.6rem;
    max-width:720px; margin:36px 0; color:var(--paper); line-height:1.4;
  }
  .faith .microcopy{color:rgba(251,248,243,0.7);}

  /* PRICING */
  .pricing-grid{display:grid; grid-template-columns:1fr 1fr; gap:40px; margin-top:48px;}
  .price-card{
    border:1px solid var(--line); padding:44px 36px; background:var(--paper);
  }
  .price-card.featured{border:1px solid var(--rose); position:relative;}
  .price-tag{font-size:0.85rem; color:var(--rose-deep); font-weight:600; margin-bottom:6px; display:block;}
  .price-amount{font-family:'Fraunces', serif; font-size:2.4rem; margin:10px 0 22px;}
  .price-card ul{list-style:none; padding:0; margin:0 0 28px;}
  .price-card li{padding:8px 0; border-bottom:1px solid var(--line); font-size:0.95rem; color:var(--ink-soft);}
  .btn-outline{
    display:inline-block; text-align:center; width:100%;
    border:1px solid var(--ink); color:var(--ink); text-decoration:none;
    padding:14px; font-weight:600; font-size:0.95rem;
  }
  .price-card.featured .btn-outline{background:var(--rose); color:var(--paper); border-color:var(--rose);}

  /* FAQ */
  .faq-item{border-top:1px solid var(--line); padding:24px 0;}
  .faq-item:last-child{border-bottom:1px solid var(--line);}
  .faq-q{
    display:flex; justify-content:space-between; align-items:center;
    cursor:pointer; font-family:'Fraunces', serif; font-size:1.15rem;
  }
  .faq-q .plus{font-size:1.4rem; color:var(--rose); transition:transform .2s;}
  .faq-item.open .plus{transform:rotate(45deg);}
  .faq-a{max-height:0; overflow:hidden; transition:max-height .3s ease; color:var(--ink-soft);}
  .faq-item.open .faq-a{max-height:300px; margin-top:14px;}

  /* DISCLAIMER */
  .disclaimer{background:var(--bg-panel); font-size:0.85rem; color:var(--ink-soft); padding:40px 0;}
  .disclaimer .wrap{border-top:1px solid var(--line); padding-top:28px;}

  /* FOOTER */
  footer{padding:48px 0; text-align:center; font-size:0.85rem; color:var(--ink-soft);}

  /* PLACEHOLDER FLAG */
  .flag{color:var(--rose-deep); font-weight:600;}

  @media(max-width:860px){
    .navlinks, .menu-btn{display:none;}
    .hero{grid-template-columns:1fr;}
    .hero-text{padding:56px 24px; margin-left:0;}
    .hero-text h1{font-size:2.2rem;}
    .story, .for-grid, .pricing-grid{grid-template-columns:1fr; gap:36px;}
    .phase{grid-template-columns:60px 1fr;}
    section{padding:64px 0;}
  }
</style>
</head>
<body>

<header>
  <nav class="wrap">
    <div class="logo">Renuevo<span>.</span></div>
    <ul class="navlinks">
      <li><a href="#historia">Su historia</a></li>
      <li><a href="#reto">El reto</a></li>
      <li><a href="#fe">Fe</a></li>
      <li><a href="#precio">Inversión</a></li>
      <li><a href="#faq">Preguntas</a></li>
    </ul>
    <a class="nav-cta" href="#precio">Únete al reto</a>
  </nav>
</header>

<section class="hero">
  <div class="hero-text">
    <h1>Subí de peso en la lactancia. <em>Así fue como empecé de nuevo.</em></h1>
    <p class="hero-sub">Un reto de alimentación y sanidad emocional para mamás en posparto — sin rutinas de gym, sin dietas genéricas, con Dios en el centro de cada paso. Termina justo a tiempo para que te sientas bien en Navidad.</p>
    <div class="cta-row">
      <a class="btn-primary" href="#precio">Quiero unirme al reto</a>
      <span class="microcopy">Cupo limitado · Del 13 de noviembre al 17 de diciembre</span>
    </div>
  </div>
  <div class="hero-visual">
    <div class="photo-slot">
      <svg viewBox="0 0 300 300" width="70%" style="opacity:0.9;" xmlns="http://www.w3.org/2000/svg">
        <circle cx="150" cy="190" r="70" fill="none" stroke="rgba(255,255,255,0.55)" stroke-width="2"/>
        <path d="M150 120 V60 M150 60 L130 85 M150 60 L170 85" stroke="rgba(255,255,255,0.7)" stroke-width="2" fill="none" stroke-linecap="round"/>
        <path d="M40 230 Q150 190 260 230" stroke="rgba(255,255,255,0.5)" stroke-width="2" fill="none"/>
        <path d="M40 250 Q150 215 260 250" stroke="rgba(255,255,255,0.35)" stroke-width="2" fill="none"/>
      </svg>
    </div>
  </div>
</section>

<section id="historia" class="section-line">
  <div class="wrap story">
    <div class="photo-slot">
      <svg viewBox="0 0 300 300" width="60%" xmlns="http://www.w3.org/2000/svg">
        <path d="M150 260 V140" stroke="#5B6E4F" stroke-width="3" fill="none" stroke-linecap="round"/>
        <path d="M150 180 Q120 160 110 120" stroke="#5B6E4F" stroke-width="3" fill="none" stroke-linecap="round"/>
        <path d="M150 150 Q180 130 190 90" stroke="#5B6E4F" stroke-width="3" fill="none" stroke-linecap="round"/>
        <circle cx="150" cy="260" r="6" fill="#A63B54"/>
      </svg>
    </div>
    <div>
      <span class="eyebrow-label">Su historia</span>
      <h2 class="head">La mayoría de mamás baja de peso lactando. A mí me pasó lo contrario.</h2>
      <p class="lede">Durante mi lactancia subí de peso, no lo bajé. Nadie me había preparado para eso, y por un tiempo sentí que mi cuerpo ya no me pertenecía. Lo que cambió mi camino no fue una dieta de moda ni horas de gimnasio — fue un cambio de alimentación sostenible, y aprender a sanar lo que cargaba por dentro con la ayuda de mi fe.</p>
      <blockquote>«No quiero enseñarte a verte diferente. Quiero acompañarte a sentirte tú otra vez.»</blockquote>
      <p class="microcopy">— Jessica · instagram.com/jessicalopezh</p>
    </div>
  </div>
</section>

<section id="reto" class="section-line">
  <div class="wrap">
    <span class="eyebrow-label">¿Para quién es Renuevo?</span>
    <h2 class="head">Esto no es para todas. Y está bien.</h2>
    <p class="lede">Renuevo fue diseñado para una etapa muy específica del posparto — léelo con calma antes de unirte.</p>
    <div class="for-grid">
      <div class="for-col yes">
        <h3>Es para ti si...</h3>
        <ul>
          <li>Ya pasaste tu mes 6, 8 o 10 de posparto</li>
          <li>Ya no estás lactando (o, bajo tu propio criterio y el de tu médico, decides comenzar aun lactando)</li>
          <li>Estás cansada de rutinas de gym que no aplican a tu etapa de vida actual</li>
          <li>Quieres un espacio que hable de fe y sanidad emocional, no solo de números en la báscula</li>
          <li>Buscas algo sostenible, no una solución de un fin de semana</li>
        </ul>
      </div>
      <div class="for-col no">
        <h3>No es para ti si...</h3>
        <ul>
          <li>Estás actualmente en lactancia y tu médico no ha aprobado un cambio de alimentación</li>
          <li>Buscas un plan clínico de nutrición personalizado (no somos nutricionistas)</li>
          <li>Esperas incluir rutinas de ejercicio o gym — este reto no las incluye</li>
          <li>Buscas resultados inmediatos sin cambiar hábitos a largo plazo</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<section class="section-line">
  <div class="wrap">
    <span class="eyebrow-label">Cómo funciona</span>
    <h2 class="head">Tres momentos, un solo camino</h2>
    <p class="lede">5 semanas en total: 1 de preparación, 3 de método activo y 1 de cierre. Avanzas a tu ritmo dentro de estas tres fases, terminando justo antes de Nochebuena.</p>
    <div class="phases">
      <div class="phase">
        <div class="phase-num">1</div>
        <div>
          <h3>Preparación <span class="microcopy">· semana 1</span></h3>
          <p>Antes de tocar la comida, trabajamos la mentalidad: por qué has intentado bajar de peso antes y no ha funcionado, cómo preparar tu cocina y tu casa, y qué esperar de las próximas semanas.</p>
        </div>
      </div>
      <div class="phase">
        <div class="phase-num">2</div>
        <div>
          <h3>Primeros pasos con el Método Renuevo <span class="microcopy">· semanas 2 a 4</span></h3>
          <p>La transición y las primeras libras. Guías prácticas de alimentación pensadas para tu etapa postparto, acompañamiento cercano y una comunidad que va contigo al mismo paso.</p>
        </div>
      </div>
      <div class="phase">
        <div class="phase-num">3</div>
        <div>
          <h3>Sostenimiento y fe <span class="microcopy">· semana 5</span></h3>
          <p>Aquí el hábito se vuelve parte de tu vida. Pláticas de sanidad emocional y fe corren en paralelo a todo el reto, no solo al final.</p>
        </div>
      </div>
    </div>
  </div>
</section>

<section id="fe" class="faith">
  <div class="wrap">
    <span class="eyebrow-label" style="color:rgba(251,248,243,0.8);">Más que alimentación</span>
    <h2 class="head">El posparto también se sana con fe</h2>
    <p class="lede">Renuevo incluye pláticas dedicadas a la depresión posparto, los miedos y las dificultades emocionales que casi nadie te explica antes de tenerlas — desde una mirada centrada en Jesús.</p>
    <blockquote>«Lo físico fue solo una parte de mi proceso. Lo que de verdad me sostuvo en los días difíciles fue mi fe — y quiero compartir eso contigo también.»</blockquote>
    <p class="microcopy">Estas pláticas son un espacio de acompañamiento espiritual, no una terapia clínica. Si atraviesas depresión posparto, te animamos también a buscar apoyo profesional.</p>
  </div>
</section>

<section id="precio" class="section-line">
  <div class="wrap">
    <span class="eyebrow-label">Inversión</span>
    <h2 class="head">Elige tu lugar en esta edición</h2>
    <div class="pricing-grid">
      <div class="price-card">
        <span class="price-tag">Autoguiado</span>
        <div class="price-amount">$67</div>
        <ul>
          <li>Acceso al contenido completo del reto</li>
          <li>Guías de las 3 fases</li>
          <li>Pláticas de fe grabadas</li>
        </ul>
        <a class="btn-outline" href="#">Reservar mi lugar</a>
      </div>
      <div class="price-card featured">
        <span class="price-tag">Fundadoras · cupo limitado</span>
        <div class="price-amount">$97</div>
        <ul>
          <li>Todo lo anterior</li>
          <li>Comunidad privada con Jessica</li>
          <li>Check-ins en vivo durante el reto</li>
          <li>Precio especial de primera edición</li>
        </ul>
        <a class="btn-outline" href="#">Quiero mi lugar de fundadora</a>
      </div>
    </div>
  </div>
</section>

<section id="faq" class="section-line">
  <div class="wrap">
    <span class="eyebrow-label">Preguntas frecuentes</span>
    <h2 class="head">Antes de que te unas</h2>
    <div id="faq-list">
      <div class="faq-item">
        <div class="faq-q"><span>¿Es seguro este método de alimentación en el posparto?</span><span class="plus">+</span></div>
        <div class="faq-a"><p>Renuevo no sustituye una valoración médica. Recomendamos consultar a tu médico antes de comenzar cualquier cambio de alimentación, especialmente si estás en los primeros meses del posparto.</p></div>
      </div>
      <div class="faq-item">
        <div class="faq-q"><span>Estoy lactando, ¿puedo unirme?</span><span class="plus">+</span></div>
        <div class="faq-a"><p>No lo recomendamos mientras estás en lactancia. Dicho esto, respetamos tu decisión y la de tu médico — si decides comenzar de todas formas, hazlo con supervisión profesional.</p></div>
      </div>
      <div class="faq-item">
        <div class="faq-q"><span>¿Necesito ir al gym o hacer ejercicio?</span><span class="plus">+</span></div>
        <div class="faq-a"><p>No. Renuevo se enfoca solo en alimentación y acompañamiento emocional/espiritual — cero rutinas de ejercicio.</p></div>
      </div>
      <div class="faq-item">
        <div class="faq-q"><span>¿Jessica es nutricionista?</span><span class="plus">+</span></div>
        <div class="faq-a"><p>No. Este es un acompañamiento basado en su experiencia personal, no una consulta de nutrición clínica. Para condiciones médicas específicas, consulta a un profesional de la salud.</p></div>
      </div>
      <div class="faq-item">
        <div class="faq-q"><span>¿Cuánto dura el reto?</span><span class="plus">+</span></div>
        <div class="faq-a"><p>5 semanas: la primera de preparación, tres de método activo donde verás tus primeros resultados, y una de cierre para consolidar el hábito — terminas justo antes de Nochebuena.</p></div>
      </div>
    </div>
  </div>
</section>

<div class="disclaimer">
  <div class="wrap">
    <p><strong>Aviso importante:</strong> Renuevo es un programa de acompañamiento en alimentación y bienestar emocional/espiritual, no un servicio médico ni de nutrición clínica. Jessica y el equipo de Renuevo no son nutricionistas ni profesionales de la salud. La información compartida no sustituye el diagnóstico, tratamiento o seguimiento de un médico o nutricionista certificado. Consulta a tu médico antes de iniciar cualquier cambio de alimentación en el posparto, y especialmente si estás en periodo de lactancia. Si atraviesas síntomas de depresión posparto, busca también apoyo profesional de salud mental.</p>
  </div>
</div>

<footer>
  <div class="wrap">
    <p>Renuevo — un programa de Jessica López, producido por MrMediaCompany</p>
  </div>
</footer>

<script>
  document.querySelectorAll('.faq-q').forEach(function(q){
    q.addEventListener('click', function(){
      var item = q.parentElement;
      var wasOpen = item.classList.contains('open');
      document.querySelectorAll('.faq-item').forEach(function(i){ i.classList.remove('open'); });
      if(!wasOpen){ item.classList.add('open'); }
    });
  });
</script>

</body>
</html>
