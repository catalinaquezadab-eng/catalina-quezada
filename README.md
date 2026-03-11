<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Catalina Quezada Bodaleo — Perfil Profesional</title>
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300;1,400&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet"/>
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
      font-family: 'DM Sans', sans-serif;
      background-color: var(--warm-white);
      color: var(--charcoal);
      min-height: 100vh;
      overflow-x: hidden;
    }

    /* ── HERO ── */
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
      font-family: 'DM Sans', sans-serif;
      font-size: 11px;
      font-weight: 500;
      letter-spacing: 0.25em;
      text-transform: uppercase;
      color: var(--gold);
      margin-bottom: 28px;
      opacity: 0;
      animation: fadeUp 0.8s ease 0.2s forwards;
    }

    .hero-name {
      font-family: 'Cormorant Garamond', serif;
      font-size: clamp(48px, 6vw, 82px);
      font-weight: 300;
      line-height: 1.05;
      letter-spacing: -0.01em;
      color: var(--cream);
      margin-bottom: 8px;
      opacity: 0;
      animation: fadeUp 0.8s ease 0.4s forwards;
    }

    .hero-name em {
      font-style: italic;
      color: var(--gold-light);
    }

    .hero-title {
      font-family: 'Cormorant Garamond', serif;
      font-size: clamp(16px, 2vw, 22px);
      font-weight: 300;
      font-style: italic;
      color: var(--muted);
      margin-bottom: 40px;
      opacity: 0;
      animation: fadeUp 0.8s ease 0.6s forwards;
    }

    .hero-summary {
      font-size: 15px;
      font-weight: 300;
      line-height: 1.8;
      color: rgba(245,240,232,0.75);
      max-width: 480px;
      margin-bottom: 48px;
      opacity: 0;
      animation: fadeUp 0.8s ease 0.8s forwards;
    }

    .hero-contacts {
      display: flex;
      flex-direction: column;
      gap: 12px;
      opacity: 0;
      animation: fadeUp 0.8s ease 1s forwards;
    }

    .contact-item {
      display: flex;
      align-items: center;
      gap: 12px;
      font-size: 13px;
      color: rgba(245,240,232,0.65);
      text-decoration: none;
      transition: color 0.2s;
    }

    .contact-item:hover { color: var(--gold-light); }

    .contact-icon {
      width: 32px;
      height: 32px;
      border: 1px solid rgba(184,137,90,0.4);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      flex-shrink: 0;
      font-size: 13px;
    }

    /* Hero right — decorative */
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
      animation: fadeIn 1.2s ease 1.2s forwards;
    }

    .deco-circle {
      width: 420px;
      height: 420px;
      border-radius: 50%;
      border: 1px solid rgba(184,137,90,0.15);
      position: absolute;
    }
    .deco-circle:nth-child(2) { width: 320px; height: 320px; border-color: rgba(184,137,90,0.25); }
    .deco-circle:nth-child(3) { width: 220px; height: 220px; border-color: rgba(184,137,90,0.4); }

    .initials {
      font-family: 'Cormorant Garamond', serif;
      font-size: 120px;
      font-weight: 300;
      color: rgba(184,137,90,0.15);
      letter-spacing: -0.05em;
      z-index: 1;
    }

    .skills-tags {
      position: absolute;
      bottom: 80px;
      right: 60px;
      display: flex;
      flex-direction: column;
      gap: 8px;
      align-items: flex-end;
      opacity: 0;
      animation: fadeUp 0.8s ease 1.4s forwards;
    }

    .tag {
      background: rgba(184,137,90,0.12);
      border: 1px solid rgba(184,137,90,0.3);
      color: var(--gold-light);
      padding: 6px 16px;
      border-radius: 20px;
      font-size: 11px;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      font-weight: 500;
    }

    /* ── DIVIDER ── */
    .section-divider {
      height: 1px;
      background: linear-gradient(to right, transparent, var(--gold), transparent);
      opacity: 0.4;
    }

    /* ── MAIN CONTENT ── */
    main {
      max-width: 1100px;
      margin: 0 auto;
      padding: 80px 40px;
    }

    .section {
      margin-bottom: 80px;
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
      font-family: 'Cormorant Garamond', serif;
      font-size: clamp(32px, 4vw, 48px);
      font-weight: 300;
      color: var(--dark);
      margin-bottom: 48px;
      line-height: 1.1;
    }

    /* ── EXPERIENCE ── */
    .timeline {
      position: relative;
      padding-left: 32px;
    }

    .timeline::before {
      content: '';
      position: absolute;
      left: 0;
      top: 8px;
      bottom: 0;
      width: 1px;
      background: linear-gradient(to bottom, var(--gold), transparent);
      opacity: 0.5;
    }

    .timeline-item {
      position: relative;
      margin-bottom: 48px;
      opacity: 0;
      transform: translateX(-20px);
      transition: opacity 0.6s ease, transform 0.6s ease;
    }

    .timeline-item.visible {
      opacity: 1;
      transform: translateX(0);
    }

    .timeline-item::before {
      content: '';
      position: absolute;
      left: -37px;
      top: 8px;
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
      margin-bottom: 6px;
      flex-wrap: wrap;
    }

    .job-title {
      font-family: 'Cormorant Garamond', serif;
      font-size: 22px;
      font-weight: 600;
      color: var(--dark);
    }

    .job-period {
      font-size: 12px;
      color: var(--muted);
      letter-spacing: 0.05em;
      white-space: nowrap;
      padding-top: 4px;
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
      gap: 8px;
    }

    .job-tasks li {
      font-size: 14px;
      font-weight: 300;
      line-height: 1.7;
      color: var(--charcoal);
      padding-left: 16px;
      position: relative;
    }

    .job-tasks li::before {
      content: '—';
      position: absolute;
      left: 0;
      color: var(--gold);
      font-size: 12px;
    }

    /* ── SKILLS + EDUCATION GRID ── */
    .two-col {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 60px;
    }

    /* Skills */
    .skills-list {
      display: flex;
      flex-direction: column;
      gap: 20px;
    }

    .skill-item {
      opacity: 0;
      transform: translateY(16px);
      transition: opacity 0.5s ease, transform 0.5s ease;
    }

    .skill-item.visible {
      opacity: 1;
      transform: translateY(0);
    }

    .skill-name {
      font-size: 13px;
      font-weight: 500;
      color: var(--dark);
      margin-bottom: 8px;
      display: flex;
      justify-content: space-between;
    }

    .skill-bar {
      height: 2px;
      background: var(--border);
      border-radius: 2px;
      overflow: hidden;
    }

    .skill-fill {
      height: 100%;
      background: linear-gradient(to right, var(--brown), var(--gold));
      border-radius: 2px;
      width: 0;
      transition: width 1.2s cubic-bezier(0.4,0,0.2,1);
    }

    /* Education */
    .edu-list {
      display: flex;
      flex-direction: column;
      gap: 28px;
    }

    .edu-item {
      border-left: 2px solid var(--border);
      padding-left: 20px;
      opacity: 0;
      transform: translateY(16px);
      transition: opacity 0.5s ease, transform 0.5s ease;
    }

    .edu-item.visible {
      opacity: 1;
      transform: translateY(0);
    }

    .edu-degree {
      font-family: 'Cormorant Garamond', serif;
      font-size: 20px;
      font-weight: 600;
      color: var(--dark);
      margin-bottom: 4px;
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

    /* Languages */
    .lang-grid {
      display: flex;
      gap: 16px;
      flex-wrap: wrap;
    }

    .lang-card {
      background: var(--dark);
      color: var(--cream);
      padding: 20px 28px;
      border-radius: 4px;
      text-align: center;
      opacity: 0;
      transform: translateY(16px);
      transition: opacity 0.5s ease, transform 0.5s ease;
    }

    .lang-card.visible {
      opacity: 1;
      transform: translateY(0);
    }

    .lang-name {
      font-family: 'Cormorant Garamond', serif;
      font-size: 22px;
      font-weight: 400;
      margin-bottom: 4px;
    }

    .lang-level {
      font-size: 11px;
      letter-spacing: 0.15em;
      text-transform: uppercase;
      color: var(--gold);
    }

    /* ── FOOTER ── */
    footer {
      background: var(--dark);
      color: rgba(245,240,232,0.4);
      text-align: center;
      padding: 32px;
      font-size: 12px;
      letter-spacing: 0.1em;
    }

    footer span { color: var(--gold); }

    /* ── ANIMATIONS ── */
    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(24px); }
      to   { opacity: 1; transform: translateY(0); }
    }

    @keyframes fadeIn {
      from { opacity: 0; }
      to   { opacity: 1; }
    }

    /* ── RESPONSIVE ── */
    @media (max-width: 768px) {
      .hero {
        grid-template-columns: 1fr;
        min-height: auto;
      }
      .hero-left { padding: 60px 32px; }
      .hero-right { display: none; }
      .two-col { grid-template-columns: 1fr; gap: 40px; }
      main { padding: 60px 24px; }
    }
  </style>
</head>
<body>

<!-- ══ HERO ══ -->
<section class="hero">
  <div class="hero-left">
    <p class="eyebrow">Perfil Profesional</p>
    <h1 class="hero-name">Catalina<br><em>Quezada</em> Bodaleo</h1>
    <p class="hero-title">Ingeniero Industrial · Gestión de Procesos &amp; Experiencia Cliente</p>
    <p class="hero-summary">
      Profesional con sólida formación en el sector de servicios y más de cinco años de experiencia
      en atención al cliente, análisis de incidencias y mejora continua. Comprometida con la eficiencia,
      la innovación y la satisfacción del cliente mediante metodología Lean.
    </p>
    <div class="hero-contacts">
      <a class="contact-item" href="tel:+56932538858">
        <span class="contact-icon">📞</span> +56 9 3253 8858
      </a>
      <a class="contact-item" href="mailto:catalina.quezada.b@gmail.com">
        <span class="contact-icon">✉</span> catalina.quezada.b@gmail.com
      </a>
      <a class="contact-item" href="https://www.linkedin.com/in/catalina-quezada-bodaleo-883071b9" target="_blank">
        <span class="contact-icon">in</span> linkedin.com/in/catalina-quezada-bodaleo
      </a>
    </div>
  </div>

  <div class="hero-right">
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

<div class="section-divider"></div>

<!-- ══ MAIN ══ -->
<main>

  <!-- EXPERIENCIA -->
  <section class="section">
    <p class="section-label">Trayectoria</p>
    <h2 class="section-title">Experiencia Profesional</h2>

    <div class="timeline">

      <div class="timeline-item">
        <div class="job-header">
          <h3 class="job-title">Ejecutiva de Atención al Cliente</h3>
          <span class="job-period">Sep 2021 — Presente · 4 años</span>
        </div>
        <p class="job-company">Fundación Chile</p>
        <ul class="job-tasks">
          <li>Gestión de solicitudes de usuarios de plataformas digitales a través de llamadas, correos y sistema de tickets, garantizando tiempos de respuesta eficientes.</li>
          <li>Resolución de incidencias y preguntas frecuentes, mejorando la experiencia cliente y asegurando la continuidad en el uso de plataformas de gestión de personas.</li>
          <li>Seguimiento de procesos y envío de notificaciones automatizadas a usuarios, optimizando la comunicación interna.</li>
          <li>Configuración y validación de datos en Excel para carga en plataforma, asegurando precisión y calidad de la información.</li>
          <li>Elaboración de reportes de resultados y métricas de uso para la toma de decisiones de clientes.</li>
        </ul>
      </div>

      <div class="timeline-item">
        <div class="job-header">
          <h3 class="job-title">Asistente de Clientes</h3>
          <span class="job-period">Jul 2018 — Ago 2021 · 3 años</span>
        </div>
        <p class="job-company">Mallplaza · Santiago, RM</p>
        <ul class="job-tasks">
          <li>Gestión de reclamos de visitantes mediante CRM, asegurando seguimiento y soluciones oportunas.</li>
          <li>Participación en iniciativas de mejora continua de instalaciones mediante levantamientos periódicos.</li>
          <li>Revisión y actualización de plataformas digitales, optimizando la comunicación con usuarios.</li>
          <li>Elaboración de reportes diarios de encuestas NPS, identificando oportunidades de mejora en la satisfacción del cliente.</li>
        </ul>
      </div>

      <div class="timeline-item">
        <div class="job-header">
          <h3 class="job-title">Asistente Administrativo</h3>
          <span class="job-period">Mar 2017 — Jun 2018 · 1 año 4 meses</span>
        </div>
        <p class="job-company">MVSGROUP – Banco BCI · Santiago, RM</p>
        <ul class="job-tasks">
          <li>Atención presencial y telefónica a clientes internos y externos, asegurando servicio eficiente y de calidad.</li>
          <li>Actualización y seguimiento de la cartera de clientes, garantizando precisión en la información.</li>
          <li>Elaboración de informes diarios y reportes de gestión para la toma de decisiones del departamento.</li>
          <li>Coordinación de procesos internos, contribuyendo a la mejora continua y optimización de tiempos.</li>
        </ul>
      </div>

      <div class="timeline-item">
        <div class="job-header">
          <h3 class="job-title">Agente Control de Pasajeros</h3>
          <span class="job-period">Ene 2016 — Nov 2016 · 11 meses</span>
        </div>
        <p class="job-company">Grupo de Empresas Turbus S.A. · Estación Central, RM</p>
        <ul class="job-tasks">
          <li>Operación en el Centro de Control de Pasajeros (CCP), gestionando sistemas de contingencia y ajustes de servicios.</li>
          <li>Elaboración de itinerarios y coordinación de servicios diarios.</li>
          <li>Revisión de demanda de servicios diarios aportando información para decisiones operativas y comerciales.</li>
        </ul>
      </div>

      <div class="timeline-item">
        <div class="job-header">
          <h3 class="job-title">Estudiante en Práctica — Depto. Ingeniería</h3>
          <span class="job-period">Ene 2015 — Mar 2015</span>
        </div>
        <p class="job-company">Hotel Sheraton Santiago</p>
        <ul class="job-tasks">
          <li>Labores administrativas incluyendo registros de consumos, facturas, cotizaciones y órdenes de compra.</li>
          <li>Gestión de pagos a proveedores y tramitación de documentos.</li>
          <li>Apoyo a la operación diaria del hotel, resolviendo incidencias de distintos departamentos.</li>
        </ul>
      </div>

    </div>
  </section>

  <!-- SKILLS + EDUCACIÓN -->
  <section class="section">
    <div class="two-col">

      <!-- Aptitudes -->
      <div>
        <p class="section-label">Competencias</p>
        <h2 class="section-title" style="font-size: clamp(28px, 3vw, 38px);">Aptitudes Clave</h2>
        <div class="skills-list">
          <div class="skill-item">
            <div class="skill-name"><span>Gestión Administrativa y Control de Recursos</span></div>
            <div class="skill-bar"><div class="skill-fill" data-width="92%"></div></div>
          </div>
          <div class="skill-item">
            <div class="skill-name"><span>Resolución de Incidencias</span></div>
            <div class="skill-bar"><div class="skill-fill" data-width="95%"></div></div>
          </div>
          <div class="skill-item">
            <div class="skill-name"><span>Gestión Operativa y Coordinación</span></div>
            <div class="skill-bar"><div class="skill-fill" data-width="90%"></div></div>
          </div>
          <div class="skill-item">
            <div class="skill-name"><span>Mejora Continua (Metodología Lean)</span></div>
            <div class="skill-bar"><div class="skill-fill" data-width="85%"></div></div>
          </div>
          <div class="skill-item">
            <div class="skill-name"><span>Análisis de Datos y Reportería (Excel)</span></div>
            <div class="skill-bar"><div class="skill-fill" data-width="88%"></div></div>
          </div>
          <div class="skill-item">
            <div class="skill-name"><span>Gestión de CRM y Plataformas Digitales</span></div>
            <div class="skill-bar"><div class="skill-fill" data-width="87%"></div></div>
          </div>
        </div>
      </div>

      <!-- Educación -->
      <div>
        <p class="section-label">Formación</p>
        <h2 class="section-title" style="font-size: clamp(28px, 3vw, 38px);">Educación</h2>
        <div class="edu-list">
          <div class="edu-item">
            <p class="edu-degree">Ingeniería Industrial</p>
            <p class="edu-school">Universidad Mayor</p>
            <p class="edu-period">Mar 2021 — Ago 2025 · En proceso de titulación</p>
          </div>
          <div class="edu-item">
            <p class="edu-degree">Técnico en Empresas Turísticas</p>
            <p class="edu-school">Duoc UC</p>
            <p class="edu-period">Mar 2013 — Sep 2015</p>
          </div>
        </div>

        <br/><br/>
        <p class="section-label">Idiomas</p>
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
  <p>© 2025 <span>Catalina Quezada Bodaleo</span> · Ingeniero Industrial · Chile</p>
</footer>

<script>
  // Intersection Observer for scroll animations
  const observer = new IntersectionObserver((entries) => {
    entries.forEach((entry, i) => {
      if (entry.isIntersecting) {
        setTimeout(() => {
          entry.target.classList.add('visible');
          // Animate skill bars
          const fill = entry.target.querySelector('.skill-fill');
          if (fill) fill.style.width = fill.dataset.width;
        }, i * 100);
      }
    });
  }, { threshold: 0.15 });

  document.querySelectorAll('.timeline-item, .skill-item, .edu-item, .lang-card').forEach(el => {
    observer.observe(el);
  });
</script>
</body>
</html>
