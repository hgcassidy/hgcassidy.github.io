<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Harvy Cassidy — Especialista en Sistemas</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        /* Mantenemos tus colores originales tal cual */
        :root {
            --bg: #0a0f16;
            --bg2: #111827;
            --panel: #1f2937;
            --accent: #22d3ee; /* Tu cyan brillante */
            --accent2: #4f8fff;
            --text: #ffffff;
            --heading: #ffffff;
            --border: rgba(255,255,255,0.05);
        }

        *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
        body {
            background-color: var(--bg);
            color: var(--text);
            font-family: 'Poppins', sans-serif;
            margin: 0;
            display: flex;
        }

        /* SIDEBAR - Mantenemos la estructura de tu diseño */
        .sidebar {
            width: 300px;
            background-color: var(--bg2);
            padding: 40px;
            height: 100vh;
            position: fixed;
            display: flex;
            flex-direction: column;
            align-items: center;
            border-right: 1px solid var(--border);
        }

        .profile-pic {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            object-fit: cover;
            border: 4px solid var(--panel);
            margin-bottom: 20px;
        }

        .name { font-size: 24px; font-weight: 700; text-align: center; }
        .title { color: var(--accent); font-size: 14px; margin-bottom: 30px; text-align: center; }

        .nav-links { list-style: none; width: 100%; }
        .nav-links li { margin-bottom: 15px; }
        .nav-links a {
            text-decoration: none;
            color: var(--text);
            font-size: 16px;
            display: block;
            padding: 10px;
            border-radius: 8px;
            transition: 0.3s;
        }
        .nav-links a:hover { background-color: var(--panel); color: var(--accent); }

        /* MAIN CONTENT - Aquí integramos tu info real */
        .main-content {
            margin-left: 300px;
            padding: 60px;
            width: calc(100% - 300px);
        }

        section { margin-bottom: 60px; }
        h1 { font-size: 40px; margin-bottom: 10px; }
        h2 { font-size: 24px; color: var(--accent); margin-bottom: 30px; border-bottom: 2px solid var(--accent); display: inline-block; padding-bottom: 5px;}
        p { font-size: 16px; line-height: 1.8; margin-bottom: 20px; color: #d1d5db; }

        /* Integramos tu stack técnico como tarjetas */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
        }

        .skill-item {
            background-color: var(--panel);
            padding: 20px;
            border-radius: 12px;
            border: 1px solid var(--border);
        }

        .skill-item h3 { color: #ffffff; margin-bottom: 10px; font-size: 18px;}
        .skill-item p { font-size: 14px; margin-bottom: 0;}

        /* Integramos tus proyectos */
        .project-item {
            background-color: var(--panel);
            padding: 25px;
            border-radius: 12px;
            margin-bottom: 20px;
            border: 1px solid var(--border);
        }
        .project-item h3 { color: var(--accent); margin-bottom: 10px; }
        .project-item h4 { color: #ffffff; margin-bottom: 5px; font-size: 16px;}
        .project-item ul { list-style: none; margin-bottom: 15px;}
        .project-item li { font-size: 14px; color: #d1d5db; margin-bottom: 5px; position: relative; padding-left: 15px;}
        .project-item li::before { content: "›"; position: absolute; left: 0; color: var(--accent); }

        /* Botón de contacto */
        .btn {
            display: inline-block;
            padding: 10px 20px;
            background-color: var(--accent);
            color: var(--bg);
            text-decoration: none;
            border-radius: 8px;
            font-weight: 600;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div class="sidebar">
        <img src="profile.jpg" alt="Harvy Cassidy" class="profile-pic">
        <div class="name">Harvy Cassidy</div>
        <div class="title">Especialista en Sistemas</div>
        <ul class="nav-links">
            <li><a href="#about">Sobre Mí</a></li>
            <li><a href="#skills">Especialización</a></li>
            <li><a href="#projects">Proyectos</a></li>
            <li><a href="#contact">Contacto</a></li>
        </ul>
    </div>
    <div class="main-content">
        <section id="about">
            <h1>Hola, Soy Harvy Cassidy</h1>
            <p>Administrador de Sistemas Informáticos en Red especializado en infraestructuras on-premise e híbridas. Experto en la optimización operativa mediante la automatización de procesos con PowerShell, Bash y Power Automate.</p>
            <p>Gracias a mi formación en gestión de proyectos (PM2) y de servicios (ITIL), aporto una visión integral en la planificación, ejecución y seguridad de entornos TI.</p>
        </section>

        <section id="skills">
            <h2>Especialización Técnica</h2>
            <div class="skills-grid">
                <div class="skill-item">
                    <h3>Sistemas Operativos</h3>
                    <p>Windows Server, Linux (Ubuntu)</p>
                </div>
                <div class="skill-item">
                    <h3>Redes y Seguridad</h3>
                    <p>VLANs, VPNs, Firewalls, Hardening, Active Directory, GPOs.</p>
                </div>
                <div class="skill-item">
                    <h3>Virtualización</h3>
                    <p>VMware, Hyper-V, Entornos on-premise e híbridos.</p>
                </div>
                <div class="skill-item">
                    <h3>Automatización</h3>
                    <p>PowerShell, Bash, Power Automate.</p>
                </div>
            </div>
        </section>

        <section id="projects">
            <h2>Proyectos Estratégicos</h2>
            <div class="project-item">
                <h3>Migración y Modernización</h3>
                <h4>Acción</h4>
                <ul>
                    <li>Virtualización del ERP SAP en entorno productivo.</li>
                    <li>Migración de firewalls FortiGate sin interrupciones.</li>
                </ul>
                <h4>Resultado</h4>
                <ul>
                    <li>Continuidad operativa sin impacto en negocio.</li>
                    <li>Mejora significativa en seguridad perimetral.</li>
                </ul>
            </div>
        </section>
        
        <section id="contact">
            <h2>Contacto</h2>
            <p>Estoy abierto a nuevas oportunidades en Administración de Sistemas, Infraestructura IT y Automatización.</p>
            <a href="mailto:hgcassidy@gmail.com" class="btn">Enviar Correo</a>
        </section>
    </div>
</body>
</html>
