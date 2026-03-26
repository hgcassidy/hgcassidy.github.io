<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Harvy Cassidy — Especialista en Sistemas</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
  <style>
    :root {
      --bg: #0f172a;        /* Azul Oxford muy sobrio */
      --bg-alt: #1e293b;    /* Slate 800 */
      --panel: #1e293b;
      --accent: #38bdf8;    /* Azul cielo suave para acentos técnicos */
      --accent-dim: rgba(56, 189, 248, 0.1);
      --text: #94a3b8;      /* Gris azulado para lectura descansada */
      --heading: #f8fafc;   /* Blanco casi puro para jerarquía */
      --border: rgba(148, 163, 184, 0.1);
      --font-main: 'Inter', sans-serif;
      --font-mono: 'JetBrains Mono', monospace;
    }

    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
    html { scroll-behavior: smooth; }
    body {
      background: var(--bg);
      color: var(--text);
      font-family: var(--font-main);
      line-height: 1.6;
    }

    /* HEADER / BANNER */
    .banner-container {
      width: 100%;
      max-width: 1100px;
      margin: 20px auto 0;
      padding: 0 20px;
    }
    .banner-container img {
      width: 100%;
      border-radius: 12px;
      border: 1px solid var(--border);
      display: block;
    }

    /* NAV */
    nav {
      position: sticky;
      top: 0;
      background: rgba(15, 23, 42, 0.9);
      backdrop-filter: blur(10px);
      border-bottom: 1px solid var(--border);
      z-index: 100;
      padding: 15px 0;
    }
    .nav-inner {
      max-width: 1100px;
      margin: 0 auto;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 0 20px;
    }
    .nav-links { display: flex; gap: 25px; list-style: none; }
    .nav-links a {
      color: var(--text);
      text-decoration: none;
      font-size: 14px;
      font-weight: 500;
      transition: color 0.2s;
    }
    .nav-links a:hover { color: var(--accent); }

    /* SECTIONS */
    section {
      max-width: 1100px;
      margin: 60px auto;
      padding: 0 20px;
    }
    h2 {
      font-size: 28px;
      color: var(--heading);
      margin-bottom: 30px;
      display: flex;
      align-items: center;
      gap: 15px;
    }
    h2::after {
      content: '';
      flex: 1;
      height: 1px;
      background: var(--border);
    }

    /* METRIC CARDS */
    .metrics-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 20px;
      margin-bottom: 40px;
    }
    .metric-card {
      background: var(--panel);
      padding: 25px;
      border-radius: 10px;
      border: 1px solid var(--border);
      text-align: center;
    }
    .metric-val {
      display: block;
      font-size: 32px;
      font-weight: 700;
      color: var(--accent);
      font-family: var(--font-mono);
    }
    .metric-label { font-size: 13px; text-transform: uppercase; letter-spacing: 1px; }

    /* SKILLS LISTS */
    .skills-container {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
    }
    .skill-box {
      background: rgba(30, 41, 59, 0.5);
      border: 1px solid var(--border);
      padding: 20px;
      border-radius: 8px;
    }
    .skill-box h3 { color: var(--heading); margin-bottom: 15px; font-size: 18px; }
    .skill-tags { display: flex; flex-wrap: wrap; gap: 8px; }
    .tag {
      background: var(--accent-dim);
      color: var(--accent);
      padding: 4px 12px;
      border-radius: 4px;
      font-size: 12px;
      font-family: var(--font-mono);
      border: 1px solid rgba(56, 189, 248, 0.2);
    }

    /* PROJECTS */
    .project-card {
      background: var(--panel);
      border: 1px solid var(--border);
      border-radius: 12px;
      padding: 30px;
      margin-bottom: 25px;
    }
    .project-card h3 { color: var(--accent); margin-bottom: 15px; }
    .project-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 30px; }
    @media (max-width: 768px) { .project-grid { grid-template-columns: 1fr; } }
    .project-col h4 { color: var(--heading); font-size: 14px; margin-bottom: 10px; text-transform: uppercase; }
    .project-col ul { list-style: none; }
    .project-col li { margin-bottom: 8px; font-size: 14px; position: relative; padding-left: 20px; }
    .project-col li::before { content: '▹'; position: absolute; left: 0; color: var(--accent); }

    /* FOOTER */
    footer {
      text-align: center;
      padding: 60px 20px;
      border-top: 1px solid var(--border);
      margin-top: 100px;
    }

    /* ANIMATIONS */
    .fade-in { opacity: 0; transform: translateY(20px); transition: all 0.6s ease-out; }
    .fade-in.visible { opacity: 1; transform: translateY(0); }
  </style>
</head>
<body>

  <div class="banner-container">
    <img src="header.png" alt="Harvy Cassidy Banner">
  </div>

  <nav>
    <div class="nav-inner">
      <div style="font-weight: 700; color: var(--heading)">HARVY CASSIDY</div>
      <ul class="nav-links">
        <li><a href="#propuesta">Propuesta</a></li>
        <li><a href="#stack">Stack</a></li>
        <li><a href="#proyectos">Proyectos</a></li>
        <li><a href="mailto:hgcassidy@gmail.com">Contacto</a></li>
      </ul>
    </div>
  </nav>

  <main>
    <section>
      <div class="metrics-grid">
        <div class="metric-card">
          <span class="metric-val">99.9%</span>
          <span class="metric-label">Uptime Sistemas</span>
        </div>
        <div class="metric-card">
          <span class="metric-val">70%</span>
          <span class="metric-label">Automatización</span>
        </div>
        <div class="metric-card">
          <span class="metric-val">60%</span>
          <span class="metric-label">↓ Tiempo Respuesta</span>
        </div>
        <div class="metric-card">
          <span class="metric-val">B2</span>
          <span class="metric-label">Nivel Inglés</span>
        </div>
      </div>
    </section>

    <section id="propuesta" class="fade-in">
      <h2>Propuesta de Valor</h2>
      <p style="font-size: 18px; max-width: 800px;">
        Administrador de Sistemas Informáticos en Red especializado en infraestructuras <strong>on-premise e híbridas</strong>. Experto en optimización operativa mediante automatización con PowerShell, Bash y Power Automate. Aporto una visión integral basada en metodologías <strong>PM2 e ITIL</strong>.
      </p>
    </section>

    <section id="stack" class="fade-in">
      <h2>Especialización Técnica</h2>
      <div class="skills-container">
        <div class="skill-box">
          <h3>Sistemas y Virtualización</h3>
          <div class="skill-tags">
            <span class="tag">Windows Server</span><span class="tag">Ubuntu</span>
            <span class="tag">VMware</span><span class="tag">Hyper-V</span>
            <span class="tag">Failover Clustering</span>
          </div>
        </div>
        <div class="skill-box">
          <h3>Redes y Seguridad</h3>
          <div class="skill-tags">
            <span class="tag">VLANs</span><span class="tag">VPNs</span>
            <span class="tag">Firewalls</span><span class="tag">Hardening</span>
            <span class="tag">Active Directory</span>
          </div>
        </div>
        <div class="skill-box">
          <h3>Automatización y Monitorización</h3>
          <div class="skill-tags">
            <span class="tag">PowerShell</span><span class="tag">Bash</span>
            <span class="tag">Grafana</span><span class="tag">Check_MK</span>
            <span class="tag">Power BI</span>
          </div>
        </div>
      </div>
    </section>

    <section id="proyectos" class="fade-in">
      <h2>Proyectos Estratégicos</h2>
      
      <div class="project-card">
        <h3>Migración y Modernización de Infraestructura Crítica</h3>
        <div class="project-grid">
          <div class="project-col">
            <h4>Acción</h4>
            <ul>
              <li>Virtualización del ERP SAP en entorno productivo.</li>
              <li>Migración de firewalls FortiGate sin interrupciones.</li>
            </ul>
          </div>
          <div class="project-col">
            <h4>Resultado</h4>
            <ul>
              <li>Continuidad operativa sin impacto en negocio.</li>
              <li>Mejora significativa en seguridad perimetral.</li>
            </ul>
          </div>
        </div>
      </div>

      <div class="project-card">
        <h3>Automatización Operativa</h3>
        <div class="project-grid">
          <div class="project-col">
            <h4>Acción</h4>
            <ul>
              <li>Desarrollo de automatizaciones con PowerShell y Bash.</li>
              <li>Implementación de soluciones basadas en IA.</li>
            </ul>
          </div>
          <div class="project-col">
            <h4>Resultado</h4>
            <ul>
              <li>Reducción de tareas manuales en más del 70%.</li>
              <li>Liberación del 20% de capacidad operativa.</li>
            </ul>
          </div>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <p>© 2026 Harvy Cassidy — "Transformo infraestructuras IT en sistemas eficientes y seguros"</p>
  </footer>

  <script>
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.classList.add('visible');
        }
      });
    }, { threshold: 0.1 });

    document.querySelectorAll('.fade-in').forEach(el => observer.observe(el));
  </script>
</body>
</html>
