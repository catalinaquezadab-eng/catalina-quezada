<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <meta name="description" content="Perfil profesional de Catalina Quezada Bodaleo — Ingeniera Industrial, especialista en gestión de procesos y experiencia cliente, Chile."/>
  <title>Catalina Quezada Bodaleo — Perfil Profesional</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300;1,400&family=DM+Sans:opsz,wght@9..40,300;9..40,400;9..40,500&display=swap" rel="stylesheet"/>
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --cream: #f5f0e8;
      --warm-white: #faf8f4;
      --dark: #1a1612;
      --charcoal: #2e2a26;
      --brown: #6b4f3a;
      --gold: #b8895a;
      --gold-light: #d4a96a;
      --muted: #8a7f76;
      --border: #e0d8ce;
    }

    html { scroll-behavior: smooth; }

    body {
      font-family: 'DM Sans', 'Segoe UI', system-ui, sans-serif;
      background-color: var(--warm-white);
      color: var(--charcoal);
      min-height: 100vh;
      overflow-x: hidden;
    }

    /* HERO */
    .hero {
      background-color: var(--dark);
      color: var(--cream);
      min-height: 100vh;
      display: grid;
      grid-template-columns: 1fr 1fr;
      position: relative;
      overflow: hidden;
    }

    .hero::before {
      content: '';
      position: absolute;
      inset: 0;
      background:
        radial-gradient(ellipse 60% 80% at 70% 50%, rgba(184,137,90,0.12) 0%, transparent 70%),
        radial-gradient(ellipse 40% 60% at 20% 80%, rgba(107,79,58,0.2) 0%, transparent 60%);
      pointer-events: none;
    }

    .hero-left {
      display: flex;
      flex-direction: column;
      justify-content: center;
      padding: 80px 60px 80px 80px;
      position: relative;
      z-index: 1;
    }

    .eyebrow {
      font-size: 11px;
      font-weight: 500;
      letter-spacing: 0.25em;
      text-transform: uppercase;
      color: var(--gold);
      margin-bottom: 28px;
      opacity: 0;
      will-change: opacity, transform;
      animation: fadeUp 0.8s ease 0.2s forwards;
    }

    .hero-name {
      font-family: 'Cormorant Garamond', Georgia, serif;
      font-size: clamp(44px, 5.5vw, 78px);
      font-weight: 300;
      line-height: 1.05;
      color: var(--cream);
      margin-bottom: 10px;
      opacity: 0;
      will-change: opacity, transform;
      animation: fadeUp 0.8s ease 0.4s forwards;
    }

    .hero-name em {
      font-style: italic;
      color: var(--gold-light);
    }

    .hero-title {
      font-family: 'Cormorant Garamond', Georgia, serif;
      font-size: clamp(15px, 1.8vw, 21px);
      font-weight: 300;
      font-style: italic;
      color: var(--muted);
      margin-bottom: 36px;
      opacity: 0;
      will-change: opacity, transform;
      animation: fadeUp 0.8s ease 0.6s forwards;
    }

    .hero-summary {
      font-size: 15px;
      font-weight: 300;
      line-height: 1.85;
      color: rgba(245,240,232,0.75);
      max-width: 480px;
      margin-bottom: 48px;
      opacity: 0;
      will-change: opacity, transform;
      animation: fadeUp 0.8s ease 0.8s forwards;
    }

    .hero-contacts {
      display: flex;
      flex-direction: column;
      gap: 14px;
      opacity: 0;
      will-change: opacity, transform;
      animation: fadeUp 0.8s ease 1s forwards;
    }

    .contact-item {
      display: flex;
      align-items: center;
      gap: 14px;
      font-size: 13.5px;
      color: rgba(245,240,232,0.65);
      text-decoration: none;
      transition: color 0.2s;
    }

    .contact-item:hover { color: var(--gold-light); }

    .contact-icon {
      width: 34px;
      height: 34px;
      border: 1px solid rgba(184,137,90,0.4);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      flex-shrink: 0;
      font-size: 14px;
      line-height: 1;
    }

    /* Hero derecho decorativo */
    .hero-right {
      position: relative;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .hero-deco {
      position: absolute;
      inset: 0;
      display: flex;
      align-items: center;
      justify-content: center;
      opacity: 0;
      will-change: opacity;
      animation: fadeIn 1.2s ease 1.2s forwards;
    }

    .deco-circle {
      width: 420px;
      height: 420px;
      border-radius: 50%;
      border: 1px solid rgba(184,137,90,0.12);
      position: absolute;
    }
    .deco-circle:nth-child(2) { width: 300px; height: 300px; border-color: rgba(184,137,90,0.22); }
    .deco-circle:nth-child(3) { width: 190px; height: 190px; border-color: rgba(184,137,90,0.38); }

    .initials {
      font-family: 'Cormorant Garamond', Georgia, serif;
      font-size: 110px;
      font-weight: 300;
      color: rgba(184,137,90,0.13);
      letter-spacing: -0.05em;
      z-index: 1;
      user-select: none;
    }

    .skills-tags {
      position: absolute;
      bottom: 80px;
      right: 60px;
      display: flex;
      flex-direction: column;
      gap: 10px;
      align-items: flex-end;
      opacity: 0;
      will-change: opacity, transform;
      animation: fadeUp 0.8s ease 1.4s forwards;
    }

    .tag {
      background: rgba(184,137,90,0.1);
      border: 1px solid rgba(184,137,90,0.3);
      color: var(--gold-light);
      padding: 7px 18px;
      border-radius: 20px;
      font-size: 11px;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      font-weight: 500;
    }

    /* DIVIDER */
    .section-divider {
      height: 1px;
      background: linear-gradient(to right, transparent, var(--gold), transparent);
      opacity: 0.35;
    }

    /* MAIN */
    main {
      max-width: 1100px;
      margin: 0 auto;
      padding: 90px 48px;
    }

    .section {
      margin-bottom: 90px;
    }

    .section-label {
      font-size: 10px;
      font-weight: 500;
      letter-spacing: 0.3em;
      text-transform: uppercase;
      color: var(--gold);
      margin-bottom: 10px;
    }

    .section-title {
      font-family: 'Cormorant Garamond', Georgia, serif;
      font-size: clamp(30px, 3.5vw, 46px);
      font-weight: 300;
      color: var(--dark);
      margin-bottom: 52px;
      line-height: 1.1;
    }

    /* TIMELINE */
    .timeline {
      position: relative;
      padding-left: 36px;
    }

    .timeline::before {
      content: '';
      position: absolute;
      left: 0;
      top: 10px;
      bottom: 0;
      width: 1px;
      background: linear-gradient(to bottom, var(--gold) 0%, transparent 100%);
      opacity: 0.45;
    }

    .timeline-item {
      position: relative;
      margin-bottom: 52px;
      opacity: 0;
      transform: translateX(-18px);
      will-change: opacity, transform;
      transition: opacity 0.65s ease, transform 0.65s ease;
    }

    .timeline-item.visible {
      opacity: 1;
      transform: translateX(0);
    }

    .timeline-item::before {
      content: '';
      position: absolute;
      left: -41px;
      top: 9px;
      width: 10px;
      height: 10px;
      border-radius: 50%;
      background: var(--gold);
      border: 2px solid var(--warm-white);
      box-shadow: 0 0 0 1px var(--gold);
    }

    .job-header {
      display: flex;
      align-items: flex-start;
      justify-content: space-between;
      gap: 20px;
      margin-bottom: 5px;
      flex-wrap: wrap;
    }

    .job-title {
      font-family: 'Cormorant Garamond', Georgia, serif;
      font-size: 23px;
      font-weight: 600;
      color: var(--dark);
      line-height: 1.2;
    }

    .job-period {
      font-size: 12px;
      color: var(--muted);
      letter-spacing: 0.04em;
      white-space: nowrap;
      padding-top: 5px;
      flex-shrink: 0;
    }

    .job-company {
      font-size: 13px;
      font-weight: 500;
      color: var(--gold);
      letter-spacing: 0.05em;
      margin-bottom: 16px;
    }

    .job-tasks {
      list-style: none;
      display: flex;
      flex-direction: column;
      gap: 9px;
    }

    .job-tasks li {
      font-size: 14px;
      font-weight: 300;
      line-height: 1.75;
      color: var(--charcoal);
      padding-left: 18px;
      position: relative;
    }

    .job-tasks li::before {
      content: '\2013';
      position: absolute;
      left: 0;
      color: var(--gold);
    }

    /* DOS COLUMNAS */
    .two-col {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 64px;
    }

    /* Skills */
    .skills-list {
      display: flex;
      flex-direction: column;
      gap: 22px;
    }

    .skill-item {
      opacity: 0;
      transform: translateY(14px);
      will-change: opacity, transform;
      transition: opacity 0.55s ease, transform 0.55s ease;
    }

    .skill-item.visible {
      opacity: 1;
      transform: translateY(0);
    }

    .skill-name {
      font-size: 13px;
      font-weight: 400;
      color: var(--dark);
      margin-bottom: 9px;
    }

    .skill-bar {
      height: 2px;
      background: var(--border);
      border-radius: 2px;
      overflow: hidden;
    }

    .skill-fill {
      height: 100%;
      background: linear-gradient(to right, var(--brown), var(--gold-light));
      border-radius: 2px;
      width: 0;
      transition: width 1.3s cubic-bezier(0.4,0,0.2,1);
    }

    /* Educacion */
    .edu-list {
      display: flex;
      flex-direction: column;
      gap: 30px;
    }

    .edu-item {
      border-left: 2px solid var(--border);
      padding-left: 22px;
      opacity: 0;
      transform: translateY(14px);
      will-change: opacity, transform;
      transition: opacity 0.55s ease, transform 0.55s ease;
    }

    .edu-item.visible {
      opacity: 1;
      transform: translateY(0);
    }

    .edu-degree {
      font-family: 'Cormorant Garamond', Georgia, serif;
      font-size: 21px;
      font-weight: 600;
      color: var(--dark);
      margin-bottom: 5px;
    }

    .edu-school {
      font-size: 13px;
      font-weight: 500;
      color: var(--gold);
      margin-bottom: 4px;
    }

    .edu-period {
      font-size: 12px;
      color: var(--muted);
    }

    /* Idiomas */
    .lang-section-label {
      font-size: 10px;
      font-weight: 500;
      letter-spacing: 0.3em;
      text-transform: uppercase;
      color: var(--gold);
      margin-bottom: 18px;
      margin-top: 44px;
    }

    .lang-grid {
      display: flex;
      gap: 14px;
      flex-wrap: wrap;
    }

    .lang-card {
      background: var(--dark);
      color: var(--cream);
      padding: 22px 32px;
      border-radius: 6px;
      text-align: center;
      opacity: 0;
      transform: translateY(14px);
      will-change: opacity, transform;
      transition: opacity 0.5s ease, transform 0.5s ease;
      min-width: 120px;
    }

    .lang-card.visible {
      opacity: 1;
      transform: translateY(0);
    }

    .lang-name {
      font-family: 'Cormorant Garamond', Georgia, serif;
      font-size: 22px;
      font-weight: 400;
      margin-bottom: 5px;
    }

    .lang-level {
      font-size: 10.5px;
      letter-spacing: 0.14em;
      text-transform: uppercase;
      color: var(--gold);
    }

    /* FOOTER */
    footer {
      background: var(--dark);
      color: rgba(245,240,232,0.38);
      text-align: center;
      padding: 36px 24px;
      font-size: 12px;
      letter-spacing: 0.1em;
    }

    footer span { color: var(--gold); }

    /* ANIMACIONES */
    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(22px); }
      to   { opacity: 1; transform: translateY(0); }
    }

    @keyframes fadeIn {
      from { opacity: 0; }
      to   { opacity: 1; }
    }

    /* RESPONSIVE */
    @media (max-width: 900px) {
      .hero { grid-template-columns: 1fr; min-height: auto; }
      .hero-left { padding: 64px 36px 56px; }
      .hero-right { display: none; }
      .two-col { grid-template-columns: 1fr; gap: 48px; }
      main { padding: 64px 28px; }
      .timeline { padding-left: 28px; }
      .timeline-item::before { left: -33px; }
    }

    @media (max-width: 480px) {
      .hero-left { padding: 52px 20px 48px; }
      main { padding: 52px 16px; }
      .job-header { flex-direction: column; gap: 4px; }
      .job-period { padding-top: 0; }
    }
  </style>
</head>
<body>

<!-- HERO -->
<section class="hero">
  <div class="hero-left">
    <p class="eyebrow">Perfil Profesional &middot; Chile</p>
    <h1 class="hero-name">Catalina<br><em>Quezada</em> Bodaleo</h1>
    <p class="hero-title">Ingeniera Industrial &middot; Gestión de Procesos &amp; Experiencia Cliente</p>
    <p class="hero-summary">
      Profesional con sólida formación en el sector de servicios y más de cinco años de experiencia
      en atención al cliente, análisis de incidencias y mejora continua. Comprometida con la eficiencia,
      la innovación y la satisfacción del cliente mediante metodología Lean.
    </p>
    <div class="hero-contacts">
      <a class="contact-item" href="tel:+56932538858">
        <span class="contact-icon" aria-hidden="true">&#9990;</span>
        +56 9 3253 8858
      </a>
      <a class="contact-item" href="mailto:catalina.quezada.b@gmail.com">
        <span class="contact-icon" aria-hidden="true">&#9993;</span>
        catalina.quezada.b@gmail.com
      </a>
      <a class="contact-item" href="https://www.linkedin.com/in/catalina-quezada-bodaleo-883071b9" target="_blank" rel="noopener">
        <span class="contact-icon" style="font-size:11px; font-weight:600;" aria-hidden="true">in</span>
        linkedin.com/in/catalina-quezada-bodaleo
      </a>
    </div>
  </div>

  <div class="hero-right" aria-hidden="true">
    <div class="hero-deco">
      <div class="deco-circle"></div>
      <div class="deco-circle"></div>
      <div class="deco-circle"></div>
      <span class="initials">CQ</span>
    </div>
    <div class="skills-tags">
      <span class="tag">Lean &amp; Mejora Continua</span>
      <span class="tag">Gestión de Proyectos</span>
      <span class="tag">Experiencia Cliente</span>
    </div>
  </div>
</section>

<div class="section-divider" role="separator"></div>

<!-- MAIN -->
<main>

  <section class="section" aria-label="Experiencia profesional">
    <p class="section-label">Trayectoria</p>
    <h2 class="section-title">Experiencia Profesional</h2>

    <div class="timeline">

      <article class="timeline-item">
        <div class="job-header">
          <h3 class="job-title">Ejecutiva de Atención al Cliente</h3>
          <span class="job-period">Sep 2021 &ndash; Presente &middot; 4 años</span>
        </div>
        <p class="job-company">Fundación Chile</p>
        <ul class="job-tasks">
          <li>Gestión de solicitudes de usuarios de plataformas digitales a través de llamadas, correos y sistema de tickets, garantizando tiempos de respuesta eficientes.</li>
          <li>Resolución de incidencias y preguntas frecuentes, mejorando la experiencia cliente y asegurando la continuidad en el uso de plataformas de gestión de personas.</li>
          <li>Seguimiento de procesos y envío de notificaciones automatizadas, optimizando la comunicación interna.</li>
          <li>Configuración y validación de datos en Excel para carga en plataforma, asegurando precisión y calidad de la información.</li>
          <li>Elaboración de reportes de resultados y métricas de uso para la toma de decisiones de clientes.</li>
        </ul>
      </article>

      <article class="timeline-item">
        <div class="job-header">
          <h3 class="job-title">Asistente de Clientes</h3>
          <span class="job-period">Jul 2018 &ndash; Ago 2021 &middot; 3 años</span>
        </div>
        <p class="job-company">Mallplaza &middot; Santiago, RM</p>
        <ul class="job-tasks">
          <li>Gestión de reclamos de visitantes mediante CRM, asegurando seguimiento y soluciones oportunas.</li>
          <li>Participación en iniciativas de mejora continua de instalaciones mediante levantamientos periódicos.</li>
          <li>Revisión y actualización de plataformas digitales, optimizando la comunicación con usuarios.</li>
          <li>Elaboración de reportes diarios de encuestas NPS, identificando oportunidades de mejora en la satisfacción del cliente.</li>
        </ul>
      </article>

      <article class="timeline-item">
        <div class="job-header">
          <h3 class="job-title">Asistente Administrativa</h3>
          <span class="job-period">Mar 2017 &ndash; Jun 2018 &middot; 1 año 4 meses</span>
        </div>
        <p class="job-company">MVSGROUP &ndash; Banco BCI &middot; Santiago, RM</p>
        <ul class="job-tasks">
          <li>Atención presencial y telefónica a clientes internos y externos, asegurando servicio eficiente y de calidad.</li>
          <li>Actualización y seguimiento de la cartera de clientes, garantizando precisión en la información.</li>
          <li>Elaboración de informes diarios y reportes de gestión para la toma de decisiones del departamento.</li>
          <li>Coordinación de procesos internos, contribuyendo a la mejora continua y optimización de tiempos.</li>
        </ul>
      </article>

      <article class="timeline-item">
        <div class="job-header">
          <h3 class="job-title">Agente Control de Pasajeros</h3>
          <span class="job-period">Ene 2016 &ndash; Nov 2016 &middot; 11 meses</span>
        </div>
        <p class="job-company">Grupo de Empresas Turbus S.A. &middot; Estación Central, RM</p>
        <ul class="job-tasks">
          <li>Operación en el Centro de Control de Pasajeros (CCP), gestionando sistemas de contingencia y ajustes de servicios.</li>
          <li>Elaboración de itinerarios y coordinación de servicios diarios.</li>
          <li>Revisión de demanda de servicios diarios aportando información para decisiones operativas y comerciales.</li>
        </ul>
      </article>

      <article class="timeline-item">
        <div class="job-header">
          <h3 class="job-title">Estudiante en Práctica &mdash; Depto. Ingeniería</h3>
          <span class="job-period">Ene 2015 &ndash; Mar 2015</span>
        </div>
        <p class="job-company">Hotel Sheraton Santiago</p>
        <ul class="job-tasks">
          <li>Labores administrativas incluyendo registros de consumos, facturas, cotizaciones y órdenes de compra.</li>
          <li>Gestión de pagos a proveedores y tramitación de documentos.</li>
          <li>Apoyo a la operación diaria del hotel, resolviendo incidencias de distintos departamentos.</li>
        </ul>
      </article>

    </div>
  </section>

  <section class="section" aria-label="Aptitudes y formacion">
    <div class="two-col">

      <div>
        <p class="section-label">Competencias</p>
        <h2 class="section-title">Aptitudes Clave</h2>
        <div class="skills-list">
          <div class="skill-item">
            <div class="skill-name">Gestión Administrativa y Control de Recursos</div>
            <div class="skill-bar"><div class="skill-fill" data-width="92%"></div></div>
          </div>
          <div class="skill-item">
            <div class="skill-name">Resolución de Incidencias</div>
            <div class="skill-bar"><div class="skill-fill" data-width="95%"></div></div>
          </div>
          <div class="skill-item">
            <div class="skill-name">Gestión Operativa y Coordinación</div>
            <div class="skill-bar"><div class="skill-fill" data-width="90%"></div></div>
          </div>
          <div class="skill-item">
            <div class="skill-name">Mejora Continua (Metodología Lean)</div>
            <div class="skill-bar"><div class="skill-fill" data-width="85%"></div></div>
          </div>
          <div class="skill-item">
            <div class="skill-name">Análisis de Datos y Reportería (Excel)</div>
            <div class="skill-bar"><div class="skill-fill" data-width="88%"></div></div>
          </div>
          <div class="skill-item">
            <div class="skill-name">Gestión de CRM y Plataformas Digitales</div>
            <div class="skill-bar"><div class="skill-fill" data-width="87%"></div></div>
          </div>
        </div>
      </div>

      <div>
        <p class="section-label">Formación</p>
        <h2 class="section-title">Educación</h2>
        <div class="edu-list">
          <div class="edu-item">
            <p class="edu-degree">Ingeniería Industrial</p>
            <p class="edu-school">Universidad Mayor</p>
            <p class="edu-period">Mar 2021 &ndash; Ago 2025 &middot; En proceso de titulación</p>
          </div>
          <div class="edu-item">
            <p class="edu-degree">Técnico en Empresas Turísticas</p>
            <p class="edu-school">Duoc UC</p>
            <p class="edu-period">Mar 2013 &ndash; Sep 2015</p>
          </div>
        </div>

        <p class="lang-section-label">Idiomas</p>
        <div class="lang-grid">
          <div class="lang-card">
            <p class="lang-name">Español</p>
            <p class="lang-level">Nativo / Bilingüe</p>
          </div>
          <div class="lang-card">
            <p class="lang-name">Inglés</p>
            <p class="lang-level">Nivel Profesional</p>
          </div>
        </div>
      </div>

    </div>
  </section>

</main>

<footer>
  <p>&#169; 2025 <span>Catalina Quezada Bodaleo</span> &middot; Ingeniera Industrial &middot; Chile</p>
</footer>

<script>
  const observer = new IntersectionObserver((entries) => {
    entries.forEach((entry, i) => {
      if (entry.isIntersecting) {
        setTimeout(() => {
          entry.target.classList.add('visible');
          const fill = entry.target.querySelector('.skill-fill');
          if (fill) fill.style.width = fill.dataset.width;
        }, i * 80);
        observer.unobserve(entry.target);
      }
    });
  }, { threshold: 0.12 });

  document.querySelectorAll('.timeline-item, .skill-item, .edu-item, .lang-card').forEach(el => {
    observer.observe(el);
  });
</script>
</body>
</html>
