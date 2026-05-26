<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Vitor Batista</title>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@tabler/icons-webfont@latest/tabler-icons.min.css"/>
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    body {
      font-family: system-ui, -apple-system, sans-serif;
      background: #f9f9f8;
      color: #1a1a18;
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 2rem;
    }

    @media (prefers-color-scheme: dark) {
      body { background: #1a1a18; color: #f1efe8; }
      .card { background: #2c2c2a; border-color: #444441; }
      .terminal { background: #222220; border-color: #444441; }
      .btn { border-color: #444441; color: #f1efe8; }
      .btn:hover { background: #2c2c2a; }
      .divider { border-color: #444441; }
    }

    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(16px); }
      to   { opacity: 1; transform: translateY(0); }
    }
    @keyframes blink  { 0%,100% { opacity:1; } 50% { opacity:0; } }
    @keyframes pulse  { 0%,100% { transform:scale(1); } 50% { transform:scale(1.08); } }
    @keyframes float  { 0%,100% { transform:translateY(0); } 50% { transform:translateY(-4px); } }

    .fade1 { animation: fadeUp .5s      ease both; }
    .fade2 { animation: fadeUp .5s .10s ease both; }
    .fade3 { animation: fadeUp .5s .20s ease both; }
    .fade4 { animation: fadeUp .5s .30s ease both; }
    .fade5 { animation: fadeUp .5s .40s ease both; }

    .card {
      background: #fff;
      border: 0.5px solid #d3d1c7;
      border-radius: 16px;
      padding: 2rem 1.75rem;
      max-width: 560px;
      width: 100%;
    }

    /* Header */
    .header { display: flex; align-items: center; gap: 16px; margin-bottom: 2rem; }
    .avatar {
      width: 56px; height: 56px; border-radius: 50%;
      background: #f1efe8; border: 0.5px solid #d3d1c7;
      display: flex; align-items: center; justify-content: center;
      font-size: 18px; font-weight: 500; flex-shrink: 0;
    }
    .name-row { display: flex; align-items: center; gap: 8px; }
    .name-row h1 { font-size: 20px; font-weight: 500; }
    .status-dot {
      width: 8px; height: 8px; border-radius: 50%;
      background: #1D9E75;
      animation: pulse 2s ease-in-out infinite;
      display: inline-block;
    }
    .subtitle { margin-top: 3px; font-size: 14px; color: #888780; }

    /* Terminal */
    .terminal {
      font-family: ui-monospace, monospace;
      font-size: 13px;
      background: #f1efe8;
      border: 0.5px solid #d3d1c7;
      border-radius: 8px;
      padding: 1rem 1.25rem;
      margin-bottom: 1.75rem;
      line-height: 2;
    }
    .terminal .prompt { color: #b4b2a9; }
    .terminal .cmd    { color: #1a1a18; }
    .terminal .out    { color: #888780; }
    .terminal a       { color: #185fa5; text-decoration: none; }
    .terminal a:hover { text-decoration: underline; }
    .cursor { animation: blink 1s step-end infinite; }

    /* Stack */
    .section-label {
      font-size: 11px; font-weight: 500;
      text-transform: uppercase; letter-spacing: .08em;
      color: #b4b2a9; margin-bottom: .75rem;
    }
    .stack { display: flex; flex-wrap: wrap; gap: 18px; align-items: center; margin-bottom: 1.75rem; }
    .tech-icon {
      width: 32px; height: 32px; opacity: .85;
      animation: float 3s ease-in-out infinite;
      transition: transform .2s, opacity .2s;
    }
    .tech-icon:hover { transform: scale(1.25) translateY(-4px) !important; animation: none; opacity: 1; }

    /* Social buttons */
    .socials { display: flex; flex-wrap: wrap; gap: 8px; margin-bottom: 1.75rem; }
    .btn {
      display: flex; align-items: center; gap: 6px;
      padding: 7px 14px;
      border-radius: 8px;
      border: 0.5px solid #d3d1c7;
      font-size: 13px; font-weight: 400;
      color: #1a1a18; text-decoration: none;
      background: transparent;
      transition: background .15s, transform .15s;
    }
    .btn:hover { background: #f1efe8; transform: translateY(-2px); }
    .btn i { font-size: 16px; }

    /* Footer */
    .divider { border: none; border-top: 0.5px solid #d3d1c7; margin-bottom: 1rem; }
    .footer { display: flex; align-items: center; gap: 6px; font-size: 12px; color: #b4b2a9; }
    .footer i { font-size: 14px; }
  </style>
</head>
<body>
  <div class="card">

    <div class="header fade1">
      <div class="avatar">VB</div>
      <div>
        <div class="name-row">
          <h1>Vitor Batista</h1>
          <span class="status-dot"></span>
        </div>
        <p class="subtitle">Backend developer · Brazil 🇧🇷</p>
      </div>
    </div>

    <div class="terminal fade2">
      <span class="prompt">$ </span><span class="cmd">whoami</span><br>
      <span class="out">→ passionate backend developer</span><br>
      <span class="prompt">$ </span><span class="cmd">git status</span><br>
      <span class="out">→ working on <a href="https://github.com/vitorbatista1/dev_tracker" target="_blank">dev_tracker</a></span><br>
      <span class="prompt">$ </span><span class="cmd">npm learn</span><br>
      <span class="out">→ Java, Spring Boot, C#<span class="cursor">▌</span></span>
    </div>

    <div class="fade3">
      <p class="section-label">Stack</p>
      <div class="stack">
        <img class="tech-icon" style="animation-delay:0s"    src="https://raw.githubusercontent.com/devicons/devicon/master/icons/java/java-original.svg"                  title="Java"       alt="Java" />
        <img class="tech-icon" style="animation-delay:.2s"   src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-original-wordmark.svg"       title="Node.js"    alt="Node.js" />
        <img class="tech-icon" style="animation-delay:.4s"   src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg"        title="JavaScript" alt="JavaScript" />
        <img class="tech-icon" style="animation-delay:.6s"   src="https://raw.githubusercontent.com/devicons/devicon/master/icons/postgresql/postgresql-original-wordmark.svg" title="PostgreSQL" alt="PostgreSQL" />
        <img class="tech-icon" style="animation-delay:.8s"   src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original-wordmark.svg"          title="MySQL"      alt="MySQL" />
        <img class="tech-icon" style="animation-delay:1s"    src="https://raw.githubusercontent.com/devicons/devicon/master/icons/docker/docker-original-wordmark.svg"        title="Docker"     alt="Docker" />
        <img class="tech-icon" style="animation-delay:1.2s"  src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg"                                                title="Git"        alt="Git" />
        <img class="tech-icon" style="animation-delay:1.4s"  src="https://raw.githubusercontent.com/devicons/devicon/master/icons/oracle/oracle-original.svg"                title="Oracle"     alt="Oracle" />
      </div>
    </div>

    <div class="socials fade4">
      <a class="btn" href="https://linkedin.com/in/vitor-batista-80a4a11b0/" target="_blank">
        <i class="ti ti-brand-linkedin"></i> LinkedIn
      </a>
      <a class="btn" href="https://instagram.com/vitorbatista.1" target="_blank">
        <i class="ti ti-brand-instagram"></i> Instagram
      </a>
      <a class="btn" href="mailto:vitorbatista177@outlook.com">
        <i class="ti ti-mail"></i> Email
      </a>
      <a class="btn" href="https://github.com/vitorbatista1" target="_blank">
        <i class="ti ti-brand-github"></i> GitHub
      </a>
    </div>

    <hr class="divider fade5"/>
    <div class="footer fade5">
      <i class="ti ti-code"></i>
      <span>vitorbatista177@outlook.com</span>
    </div>

  </div>
</body>
</html>
