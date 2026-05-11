
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Asef Amin Araf — Product Manager</title>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,wght@0,300;0,400;0,700;1,300&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet"/>
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg: #0d0d0d;
    --surface: #161616;
    --card: #1c1c1c;
    --border: rgba(255,255,255,0.08);
    --accent: #c8f04a;
    --accent2: #4af0c8;
    --text: #f0ede6;
    --muted: #7a7a72;
    --font-display: 'Fraunces', Georgia, serif;
    --font-body: 'DM Sans', sans-serif;
  }

  html { scroll-behavior: smooth; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: var(--font-body);
    font-size: 16px;
    line-height: 1.6;
    overflow-x: hidden;
  }

  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='1'/%3E%3C/svg%3E");
    opacity: 0.035;
    pointer-events: none;
    z-index: 999;
  }

  /* NAV */
  nav {
    position: fixed;
    top: 0; left: 0; right: 0;
    z-index: 100;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1.25rem 2.5rem;
    background: rgba(13,13,13,0.85);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--border);
  }
  .nav-logo { font-family: var(--font-display); font-size: 1.1rem; color: var(--accent); }
  .nav-links { display: flex; gap: 2rem; list-style: none; }
  .nav-links a { color: var(--muted); text-decoration: none; font-size: 0.875rem; letter-spacing: 0.04em; text-transform: uppercase; transition: color 0.2s; }
  .nav-links a:hover { color: var(--text); }

  /* HERO */
  .hero {
    min-height: 100vh;
    display: grid;
    grid-template-columns: 1fr 1fr;
    align-items: center;
    padding: 7rem 2.5rem 4rem;
    max-width: 1200px;
    margin: 0 auto;
    gap: 4rem;
  }
  .hero-text { animation: fadeUp 0.9s ease both; }
  .hero-tag {
    display: inline-flex; align-items: center; gap: 0.5rem;
    font-size: 0.75rem; font-weight: 500; letter-spacing: 0.12em; text-transform: uppercase;
    color: var(--accent); border: 1px solid rgba(200,240,74,0.25);
    padding: 0.35rem 0.85rem; border-radius: 100px; margin-bottom: 1.75rem;
    animation: fadeUp 0.7s ease both;
  }
  .hero-tag::before { content: ''; width: 6px; height: 6px; border-radius: 50%; background: var(--accent); animation: pulse 2s ease-in-out infinite; }
  @keyframes pulse { 0%,100%{opacity:1;transform:scale(1)} 50%{opacity:.5;transform:scale(.8)} }
  .hero h1 {
    font-family: var(--font-display);
    font-size: clamp(2.6rem, 5.5vw, 5rem);
    font-weight: 300; line-height: 1.08; letter-spacing: -0.02em;
    margin-bottom: 1.5rem; animation: fadeUp 0.8s 0.1s ease both;
  }
  .hero h1 em { font-style: italic; color: var(--accent); }
  .hero-desc { font-size: 1.05rem; color: var(--muted); max-width: 440px; line-height: 1.75; margin-bottom: 2.5rem; animation: fadeUp 0.8s 0.2s ease both; }
  .hero-cta { display: flex; gap: 1rem; flex-wrap: wrap; animation: fadeUp 0.8s 0.3s ease both; }
  .btn { display: inline-block; padding: 0.8rem 1.75rem; border-radius: 6px; font-size: 0.9rem; font-weight: 500; text-decoration: none; transition: all 0.2s; cursor: pointer; border: none; font-family: var(--font-body); }
  .btn-primary { background: var(--accent); color: #0d0d0d; }
  .btn-primary:hover { background: #d9ff55; transform: translateY(-2px); }
  .btn-ghost { background: transparent; color: var(--text); border: 1px solid var(--border); }
  .btn-ghost:hover { border-color: rgba(255,255,255,0.25); transform: translateY(-2px); }

  .hero-visual { display: flex; justify-content: center; animation: fadeUp 1s 0.2s ease both; }
  .avatar-ring { position: relative; width: 320px; height: 320px; }
  .avatar-ring::before { content:''; position:absolute; inset:-3px; border-radius:38% 62% 44% 56%/44% 38% 62% 56%; background:linear-gradient(135deg,var(--accent),var(--accent2)); animation:morph 8s ease-in-out infinite; z-index:0; }
  @keyframes morph { 0%,100%{border-radius:38% 62% 44% 56%/44% 38% 62% 56%} 33%{border-radius:60% 40% 55% 45%/50% 60% 40% 50%} 66%{border-radius:44% 56% 66% 34%/60% 44% 56% 40%} }
  .avatar-inner { position:absolute; inset:3px; background:var(--surface); z-index:1; display:flex; align-items:center; justify-content:center; flex-direction:column; gap:.5rem; border-radius:38% 62% 44% 56%/44% 38% 62% 56%; animation:morph 8s ease-in-out infinite; }
  .avatar-initials { font-family:var(--font-display); font-size:3.5rem; font-weight:300; color:var(--text); line-height:1; text-align:center; }
  .avatar-role { font-size:.72rem; letter-spacing:.15em; text-transform:uppercase; color:var(--accent); font-weight:500; }
  .badge { position:absolute; background:var(--card); border:1px solid var(--border); border-radius:10px; padding:.6rem 1rem; font-size:.78rem; font-weight:500; z-index:2; white-space:nowrap; animation:float 3s ease-in-out infinite; }
  .badge-1 { top:10px; right:-30px; animation-delay:0s; }
  .badge-2 { bottom:30px; left:-40px; animation-delay:1.5s; }
  .badge span { color:var(--accent); }
  @keyframes float { 0%,100%{transform:translateY(0)} 50%{transform:translateY(-8px)} }

  /* SECTIONS */
  section { padding: 6rem 2.5rem; max-width: 1200px; margin: 0 auto; }
  .section-label { font-size:.72rem; font-weight:500; letter-spacing:.15em; text-transform:uppercase; color:var(--accent); margin-bottom:.75rem; }
  .section-title { font-family:var(--font-display); font-size:clamp(2rem,4vw,3rem); font-weight:300; line-height:1.15; margin-bottom:1rem; }
  .section-title em { font-style:italic; color:var(--accent); }
  .section-sub { color:var(--muted); max-width:540px; line-height:1.75; }
  hr.divider { border:none; border-top:1px solid var(--border); margin:0 2.5rem; }

  /* ABOUT */
  .about-grid { display:grid; grid-template-columns:1fr 1fr; gap:4rem; margin-top:3rem; align-items:start; }
  .about-text p { color:var(--muted); line-height:1.8; margin-bottom:1rem; }
  .about-text p strong { color:var(--text); }
  .about-stats { display:grid; grid-template-columns:1fr 1fr; gap:1px; background:var(--border); border:1px solid var(--border); border-radius:12px; overflow:hidden; }
  .stat { background:var(--card); padding:1.75rem; transition:background .2s; }
  .stat:hover { background:#222; }
  .stat-number { font-family:var(--font-display); font-size:2.2rem; font-weight:300; color:var(--accent); line-height:1; margin-bottom:.4rem; }
  .stat-label { font-size:.82rem; color:var(--muted); }

  /* ACHIEVEMENTS */
  .ach-grid { display:grid; grid-template-columns:repeat(auto-fit,minmax(220px,1fr)); gap:1rem; margin-top:2.5rem; }
  .ach-card { background:var(--card); border:1px solid var(--border); border-radius:12px; padding:1.5rem; transition:all .25s; }
  .ach-card:hover { border-color:rgba(200,240,74,.3); transform:translateY(-4px); }
  .ach-number { font-family:var(--font-display); font-size:2.8rem; font-weight:300; color:var(--accent); line-height:1; margin-bottom:.5rem; }
  .ach-card p { font-size:.88rem; color:var(--muted); line-height:1.65; }

  /* SKILLS */
  .skills-section { background:var(--surface); border-top:1px solid var(--border); border-bottom:1px solid var(--border); }
  .skills-section section { padding:5rem 2.5rem; }
  .skills-cols { display:grid; grid-template-columns:1fr 1fr; gap:3rem; margin-top:3rem; }
  .skills-group h3 { font-size:.75rem; font-weight:500; letter-spacing:.12em; text-transform:uppercase; color:var(--accent); margin-bottom:1.25rem; }
  .skill-list { display:flex; flex-direction:column; gap:.75rem; }
  .skill-item { display:flex; align-items:center; gap:1rem; }
  .skill-item span { font-size:.88rem; color:var(--text); min-width:190px; }
  .skill-bar { flex:1; height:3px; background:var(--border); border-radius:2px; overflow:hidden; }
  .skill-bar-fill { height:100%; background:var(--accent); border-radius:2px; width:0; transition:width 1.2s ease; }
  .software-grid { display:flex; flex-wrap:wrap; gap:.6rem; margin-top:1.5rem; }
  .sw-pill { display:flex; align-items:center; gap:.5rem; background:var(--card); border:1px solid var(--border); border-radius:8px; padding:.5rem 1rem; font-size:.85rem; color:var(--text); transition:all .2s; }
  .sw-pill:hover { border-color:rgba(200,240,74,.3); color:var(--accent); }

  /* EXPERIENCE */
  .exp-list { margin-top:3rem; }
  .exp-item { display:grid; grid-template-columns:200px 1fr; gap:2rem; padding:2rem 0; border-bottom:1px solid var(--border); }
  .exp-item:last-child { border-bottom:none; }
  .exp-date { font-size:.82rem; color:var(--muted); padding-top:.2rem; line-height:1.6; }
  .exp-current { display:inline-block; font-size:.68rem; font-weight:500; letter-spacing:.08em; text-transform:uppercase; background:rgba(200,240,74,.1); color:var(--accent); border:1px solid rgba(200,240,74,.2); padding:.2rem .6rem; border-radius:100px; margin-top:.4rem; }
  .exp-role { font-weight:500; font-size:1.05rem; margin-bottom:.25rem; }
  .exp-company { font-family:var(--font-display); font-style:italic; color:var(--accent); font-size:.95rem; margin-bottom:.4rem; }
  .exp-location { font-size:.78rem; color:var(--muted); margin-bottom:.75rem; }
  .exp-bullets { margin-bottom:.75rem; }
  .exp-bullets li { font-size:.88rem; color:var(--muted); line-height:1.75; margin-bottom:.3rem; list-style:none; position:relative; padding-left:1.2rem; }
  .exp-bullets li::before { content:'→'; position:absolute; left:0; color:var(--accent); font-size:.75rem; top:.15rem; }
  .exp-tags { display:flex; flex-wrap:wrap; gap:.5rem; }
  .tag { font-size:.72rem; font-weight:500; letter-spacing:.06em; padding:.25rem .7rem; border-radius:100px; background:rgba(200,240,74,.08); color:var(--accent); border:1px solid rgba(200,240,74,.15); }

  /* EDUCATION */
  .edu-list { margin-top:3rem; }
  .edu-item { display:grid; grid-template-columns:200px 1fr; gap:2rem; padding:1.5rem 0; border-bottom:1px solid var(--border); }
  .edu-item:last-child { border-bottom:none; }
  .edu-year { font-size:.82rem; color:var(--muted); }
  .edu-degree { font-weight:500; font-size:.95rem; margin-bottom:.3rem; }
  .edu-school { font-family:var(--font-display); font-style:italic; color:var(--accent); font-size:.9rem; margin-bottom:.2rem; }
  .edu-location { font-size:.78rem; color:var(--muted); }

  /* CONTACT */
  .contact-section { text-align:center; padding:7rem 2.5rem; max-width:700px; margin:0 auto; }
  .contact-section .section-title { font-size:clamp(2.5rem,5vw,4rem); }
  .contact-links { display:flex; gap:1rem; justify-content:center; flex-wrap:wrap; margin-top:2.5rem; }
  .contact-link { display:flex; align-items:center; gap:.5rem; padding:.8rem 1.5rem; border:1px solid var(--border); border-radius:8px; text-decoration:none; color:var(--muted); font-size:.9rem; transition:all .2s; }
  .contact-link:hover { border-color:var(--accent); color:var(--accent); transform:translateY(-2px); }

  /* FOOTER */
  footer { border-top:1px solid var(--border); padding:2rem 2.5rem; display:flex; justify-content:space-between; align-items:center; font-size:.82rem; color:var(--muted); }

  /* ANIMATIONS */
  @keyframes fadeUp { from{opacity:0;transform:translateY(24px)} to{opacity:1;transform:translateY(0)} }
  .reveal { opacity:0; transform:translateY(30px); transition:opacity .7s ease,transform .7s ease; }
  .reveal.visible { opacity:1; transform:translateY(0); }

  /* MOBILE */
  @media (max-width:768px) {
    nav { padding:1rem 1.25rem; }
    .nav-links { gap:1rem; }
    .nav-links a { font-size:.75rem; }
    .hero { grid-template-columns:1fr; padding:6rem 1.25rem 3rem; gap:3rem; text-align:center; }
    .hero-desc { max-width:100%; }
    .hero-cta { justify-content:center; }
    .hero-visual { order:-1; }
    .avatar-ring { width:240px; height:240px; }
    .about-grid,.skills-cols { grid-template-columns:1fr; gap:2rem; }
    .exp-item,.edu-item { grid-template-columns:1fr; gap:.5rem; }
    section { padding:4rem 1.25rem; }
    footer { flex-direction:column; gap:.5rem; text-align:center; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-logo">Asef.</div>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#skills">Skills</a></li>
    <li><a href="#experience">Experience</a></li>
    <li><a href="#education">Education</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<!-- HERO -->
<div style="border-bottom:1px solid var(--border)">
<div class="hero">
  <div class="hero-text">
    <div class="hero-tag">Open to opportunities</div>
    <h1>Hi, I'm <em>Asef Amin Araf</em> —<br>Product Manager</h1>
    <p class="hero-desc">3+ years leading SaaS products across the full lifecycle. I bridge engineering, design, and business to ship scalable, user-loved solutions.</p>
    <div class="hero-cta">
      <a href="#contact" class="btn btn-primary">Get in touch</a>
      <a href="#experience" class="btn btn-ghost">See my work →</a>
    </div>
  </div>
  <div class="hero-visual">
    <div class="avatar-ring">
      <div class="avatar-inner">
        <div class="avatar-initials">AAA</div>
        <div class="avatar-role">Product Manager</div>
      </div>
      <div class="badge badge-1">🚀 <span>Priyoshop Ltd</span></div>
      <div class="badge badge-2">⚡ <span>3+ Years PM</span></div>
    </div>
  </div>
</div>
</div>

<!-- ABOUT -->
<section id="about">
  <div class="section-label">About me</div>
  <h2 class="section-title">Engineering mind,<br><em>product heart</em></h2>
  <div class="about-grid reveal">
    <div class="about-text">
      <p>I'm <strong>Asef Amin Araf</strong>, a Product Manager with <strong>3+ years of experience</strong> leading SaaS products across the full lifecycle — from strategy to shipping to post-launch optimization.</p>
      <p>Currently at <strong>Priyoshop Ltd</strong>, I shape product strategy for POS, OMS, and operational apps — working with engineering, design, and operations to deliver impactful, scalable updates.</p>
      <p>My <strong>BSc in Electrical &amp; Electronic Engineering</strong> from AUST gives me a technical edge: strong analytical skills and a hands-on approach to turning complex problems into practical, user-centered products.</p>
      <p>Native <strong>Bangla</strong> speaker, proficient in <strong>English</strong>, based in <strong>Dhaka, Bangladesh</strong>.</p>
    </div>
    <div class="about-stats">
      <div class="stat">
        <div class="stat-number">3+</div>
        <div class="stat-label">Years in Product</div>
      </div>
      <div class="stat">
        <div class="stat-number">40%</div>
        <div class="stat-label">Faster release cycles</div>
      </div>
      <div class="stat">
        <div class="stat-number">30%</div>
        <div class="stat-label">Market engagement boost</div>
      </div>
      <div class="stat">
        <div class="stat-number">25%</div>
        <div class="stat-label">User adoption improved</div>
      </div>
    </div>
  </div>

  <div style="margin-top:4rem">
    <div class="section-label">Key achievements</div>
    <div class="ach-grid reveal">
      <div class="ach-card">
        <div class="ach-number">40%</div>
        <p>Reduced development time by optimizing release cycles and accelerating time-to-market.</p>
      </div>
      <div class="ach-card">
        <div class="ach-number">30%</div>
        <p>Boosted market engagement through successful management of multiple product launches.</p>
      </div>
      <div class="ach-card">
        <div class="ach-number">25%</div>
        <p>Improved user adoption through targeted feature enhancements and UX improvements.</p>
      </div>
      <div class="ach-card">
        <div class="ach-number">20%</div>
        <p>Increased team efficiency by streamlining cross-functional workflows and ensuring on-time delivery.</p>
      </div>
    </div>
  </div>
</section>

<hr class="divider"/>

<!-- SKILLS -->
<div class="skills-section">
<section id="skills">
  <div class="section-label">What I do</div>
  <h2 class="section-title">Skills &amp; <em>expertise</em></h2>
  <p class="section-sub">A full PM toolkit — from strategy and research to execution and analytics.</p>
  <div class="skills-cols reveal">
    <div class="skills-group">
      <h3>Product Skills</h3>
      <div class="skill-list">
        <div class="skill-item"><span>Product Strategy &amp; Growth</span><div class="skill-bar"><div class="skill-bar-fill" data-width="92"></div></div></div>
        <div class="skill-item"><span>Roadmapping &amp; Backlog</span><div class="skill-bar"><div class="skill-bar-fill" data-width="90"></div></div></div>
        <div class="skill-item"><span>Stakeholder Management</span><div class="skill-bar"><div class="skill-bar-fill" data-width="88"></div></div></div>
        <div class="skill-item"><span>Product Analytics</span><div class="skill-bar"><div class="skill-bar-fill" data-width="85"></div></div></div>
        <div class="skill-item"><span>Agile &amp; Scrum</span><div class="skill-bar"><div class="skill-bar-fill" data-width="90"></div></div></div>
        <div class="skill-item"><span>Growth Experimentation</span><div class="skill-bar"><div class="skill-bar-fill" data-width="80"></div></div></div>
        <div class="skill-item"><span>Data-Driven Strategy</span><div class="skill-bar"><div class="skill-bar-fill" data-width="87"></div></div></div>
      </div>
    </div>
    <div class="skills-group">
      <h3>Strengths</h3>
      <div class="skill-list">
        <div class="skill-item"><span>Teamwork &amp; Leadership</span><div class="skill-bar"><div class="skill-bar-fill" data-width="95"></div></div></div>
        <div class="skill-item"><span>Analytical Thinking</span><div class="skill-bar"><div class="skill-bar-fill" data-width="92"></div></div></div>
        <div class="skill-item"><span>Problem Solving</span><div class="skill-bar"><div class="skill-bar-fill" data-width="93"></div></div></div>
        <div class="skill-item"><span>User-Centric Thinking</span><div class="skill-bar"><div class="skill-bar-fill" data-width="94"></div></div></div>
      </div>
      <h3 style="margin-top:2rem">Languages</h3>
      <div class="skill-list">
        <div class="skill-item"><span>Bangla (Native)</span><div class="skill-bar"><div class="skill-bar-fill" data-width="100"></div></div></div>
        <div class="skill-item"><span>English (Proficient)</span><div class="skill-bar"><div class="skill-bar-fill" data-width="82"></div></div></div>
      </div>
    </div>
  </div>

  <div style="margin-top:3rem">
    <div class="section-label" style="margin-bottom:1rem">Software &amp; Tools</div>
    <div class="software-grid reveal">
      <div class="sw-pill">📋 Confluence</div>
      <div class="sw-pill">🎯 Jira</div>
      <div class="sw-pill">✅ ClickUp</div>
      <div class="sw-pill">🎨 Figma</div>
      <div class="sw-pill">📊 Microsoft Office</div>
      <div class="sw-pill">🗃️ SQL</div>
    </div>
  </div>
</section>
</div>

<hr class="divider"/>

<!-- EXPERIENCE -->
<section id="experience">
  <div class="section-label">Experience</div>
  <h2 class="section-title">Where I've <em>worked</em></h2>
  <div class="exp-list reveal">

    <div class="exp-item">
      <div class="exp-date">
        Jul 2025 – Present
        <div><span class="exp-current">Current</span></div>
      </div>
      <div>
        <div class="exp-role">Product Manager</div>
        <div class="exp-company">Priyoshop Ltd</div>
        <div class="exp-location">📍 Dhaka, Bangladesh</div>
        <ul class="exp-bullets">
          <li>Assist the lead in defining product strategy for POS, OMS, and operational apps, enhancing process efficiency.</li>
          <li>Convert user and stakeholder insights into clear requirements and deliver roadmap items on schedule.</li>
          <li>Work with engineering, design and operations to launch scalable updates with smooth UAT cycles.</li>
          <li>Improve user experience through targeted feature enhancements and performance gains.</li>
          <li>Track product KPIs to drive continuous optimization and support rollout, training and adoption across teams.</li>
        </ul>
        <div class="exp-tags">
          <span class="tag">POS</span><span class="tag">OMS</span><span class="tag">SaaS</span>
          <span class="tag">KPI Tracking</span><span class="tag">UAT</span><span class="tag">E-commerce</span>
        </div>
      </div>
    </div>

    <div class="exp-item">
      <div class="exp-date">Jun 2023 – Jun 2025</div>
      <div>
        <div class="exp-role">Junior Product Manager</div>
        <div class="exp-company">ME SOLshare Ltd</div>
        <div class="exp-location">📍 Dhaka, Bangladesh</div>
        <ul class="exp-bullets">
          <li>Helped gather and refine product requirements with stakeholders, improving clarity by 25%.</li>
          <li>Worked with cross-functional teams to deliver features on time, increasing development efficiency by 20%.</li>
          <li>Supported product launches and used KPI tracking and post-launch insights to drive measurable improvements.</li>
          <li>Assisted in conducting market and competitive research to identify growth opportunities and roadmap decisions.</li>
        </ul>
        <div class="exp-tags">
          <span class="tag">Requirements</span><span class="tag">Stakeholders</span>
          <span class="tag">Product Launches</span><span class="tag">Market Research</span>
        </div>
      </div>
    </div>

    <div class="exp-item">
      <div class="exp-date">Jul 2022 – Jul 2023</div>
      <div>
        <div class="exp-role">Junior Product Coordinator</div>
        <div class="exp-company">ME SOLshare Ltd</div>
        <div class="exp-location">📍 Dhaka, Bangladesh</div>
        <ul class="exp-bullets">
          <li>Supported product lifecycle management for renewable energy solutions, including distribution, launches, and cross-team coordination.</li>
          <li>Trained internal teams and external stakeholders on new features to ensure smooth adoption and usage.</li>
          <li>Assisted in market research to identify customer needs and competitive trends, informing product strategy.</li>
        </ul>
        <div class="exp-tags">
          <span class="tag">Renewable Energy</span><span class="tag">Product Lifecycle</span>
          <span class="tag">Training</span><span class="tag">Market Research</span>
        </div>
      </div>
    </div>

  </div>
</section>

<hr class="divider"/>

<!-- EDUCATION -->
<section id="education">
  <div class="section-label">Education</div>
  <h2 class="section-title">Academic <em>background</em></h2>
  <div class="edu-list reveal">
    <div class="edu-item">
      <div class="edu-year">2018 – 2022</div>
      <div>
        <div class="edu-degree">BSc — Electrical &amp; Electronic Engineering (EEE)</div>
        <div class="edu-school">Ahsanullah University of Science &amp; Technology</div>
        <div class="edu-location">📍 Dhaka, Bangladesh</div>
      </div>
    </div>
    <div class="edu-item">
      <div class="edu-year">2015 – 2017</div>
      <div>
        <div class="edu-degree">Higher Secondary Certificate (HSC)</div>
        <div class="edu-school">Dhaka Residential Model College</div>
        <div class="edu-location">📍 Dhaka, Bangladesh</div>
      </div>
    </div>
    <div class="edu-item">
      <div class="edu-year">2007 – 2015</div>
      <div>
        <div class="edu-degree">Secondary School Certificate (SSC)</div>
        <div class="edu-school">Dhaka Residential Model College</div>
        <div class="edu-location">📍 Dhaka, Bangladesh</div>
      </div>
    </div>
  </div>
</section>

<hr class="divider"/>

<!-- CONTACT -->
<div id="contact">
<div class="contact-section reveal">
  <div class="section-label">Get in touch</div>
  <h2 class="section-title">Let's <em>connect</em></h2>
  <p style="color:var(--muted);margin-top:1rem;line-height:1.75">Whether it's a job opportunity, a product to build, or just a chat about PM — I'd love to hear from you.</p>
  <div class="contact-links">
    <a href="mailto:asefaminaraf@gmail.com" class="contact-link">✉️ asefaminaraf@gmail.com</a>
    <a href="tel:+8801971817271" class="contact-link">📞 +880 1971 817271</a>
    <a href="https://linkedin.com/in/asef-amin-araf" target="_blank" class="contact-link">💼 LinkedIn</a>
  </div>
</div>
</div>

<!-- FOOTER -->
<footer>
  <span>© 2026 Asef Amin Araf. All rights reserved.</span>
  <span>Product Manager · Dhaka, Bangladesh</span>
</footer>

<script>
  const revealObserver = new IntersectionObserver((entries) => {
    entries.forEach(e => { if (e.isIntersecting) { e.target.classList.add('visible'); revealObserver.unobserve(e.target); } });
  }, { threshold: 0.08 });
  document.querySelectorAll('.reveal').forEach(el => revealObserver.observe(el));

  const barObserver = new IntersectionObserver((entries) => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        e.target.querySelectorAll('.skill-bar-fill').forEach(bar => { bar.style.width = bar.dataset.width + '%'; });
        barObserver.unobserve(e.target);
      }
    });
  }, { threshold: 0.2 });
  document.querySelectorAll('.skills-cols').forEach(el => barObserver.observe(el));
</script>
</body>
</html>
