<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sharifakhon Ibrohimova — Marketing Strategist</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300;1,400&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/4.4.1/chart.umd.min.js"></script>
<style>
  :root {
    --cream: #F7F4EF;
    --ink: #1A1A1A;
    --ink-light: #4A4A4A;
    --terracotta: #C4614A;
    --terracotta-light: #E8957F;
    --gold: #B8976A;
    --border: #E0DAD0;
    --white: #FFFFFF;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--cream);
    color: var(--ink);
    font-size: 16px;
    line-height: 1.6;
  }

  /* NAV */
  nav {
    position: fixed; top: 0; left: 0; right: 0;
    z-index: 100;
    display: flex; justify-content: space-between; align-items: center;
    padding: 1.2rem 4rem;
    background: rgba(247,244,239,0.92);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--border);
  }

  .nav-logo {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.1rem;
    font-weight: 400;
    letter-spacing: 0.05em;
    color: var(--ink);
    text-decoration: none;
  }

  .nav-links { display: flex; gap: 2.5rem; list-style: none; }
  .nav-links a {
    font-size: 0.8rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--ink-light);
    text-decoration: none;
    transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--terracotta); }

  /* HERO */
  .hero {
    min-height: 100vh;
    display: grid;
    grid-template-columns: 1fr 1fr;
    padding-top: 80px;
  }

  .hero-left {
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 6rem 4rem 6rem 4rem;
  }

  .hero-tag {
    font-size: 0.75rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--terracotta);
    margin-bottom: 1.5rem;
    display: flex; align-items: center; gap: 0.8rem;
  }
  .hero-tag::before {
    content: '';
    display: block; width: 32px; height: 1px;
    background: var(--terracotta);
  }

  .hero-name {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(3rem, 5vw, 5rem);
    font-weight: 300;
    line-height: 1.05;
    letter-spacing: -0.01em;
    margin-bottom: 2rem;
  }

  .hero-name em {
    font-style: italic;
    color: var(--terracotta);
  }

  .hero-desc {
    font-size: 1rem;
    color: var(--ink-light);
    max-width: 420px;
    line-height: 1.8;
    margin-bottom: 3rem;
    font-weight: 300;
  }

  .hero-stats {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 2rem;
    padding: 2rem 0;
    border-top: 1px solid var(--border);
  }

  .stat-number {
    font-family: 'Cormorant Garamond', serif;
    font-size: 2.4rem;
    font-weight: 600;
    color: var(--terracotta);
    line-height: 1;
    margin-bottom: 0.3rem;
  }

  .stat-label {
    font-size: 0.72rem;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    color: var(--ink-light);
    line-height: 1.4;
  }

  .hero-right {
    position: relative;
    overflow: hidden;
    background: var(--ink);
  }

  .hero-right img {
    width: 100%; height: 100%;
    object-fit: cover;
    opacity: 0.85;
    mix-blend-mode: luminosity;
  }

  .hero-image-overlay {
    position: absolute; inset: 0;
    background: linear-gradient(135deg, rgba(196,97,74,0.3) 0%, transparent 60%);
  }

  .hero-image-text {
    position: absolute;
    bottom: 3rem; left: 3rem; right: 3rem;
    color: white;
  }

  .hero-image-text h3 {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.2rem;
    font-weight: 300;
    font-style: italic;
    margin-bottom: 0.3rem;
  }

  .hero-image-text p {
    font-size: 0.75rem;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    opacity: 0.7;
  }

  .hero-placeholder {
    width: 100%; height: 100%;
    background: linear-gradient(135deg, #2A2A2A 0%, #1A1A1A 100%);
    display: flex; flex-direction: column;
    align-items: center; justify-content: center;
    color: white; text-align: center; padding: 3rem;
  }

  .hero-placeholder .initials {
    font-family: 'Cormorant Garamond', serif;
    font-size: 8rem;
    font-weight: 300;
    color: var(--terracotta);
    line-height: 1;
    margin-bottom: 1rem;
  }

  /* SECTION COMMON */
  section { padding: 8rem 4rem; }

  .section-label {
    font-size: 0.72rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--terracotta);
    margin-bottom: 1rem;
    display: flex; align-items: center; gap: 0.8rem;
  }
  .section-label::before {
    content: '';
    display: block; width: 24px; height: 1px;
    background: var(--terracotta);
  }

  .section-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(2.2rem, 3.5vw, 3.5rem);
    font-weight: 300;
    line-height: 1.1;
    margin-bottom: 1rem;
  }

  /* ABOUT */
  .about {
    background: white;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 6rem;
    align-items: start;
  }

  .about-text p {
    font-size: 1.05rem;
    color: var(--ink-light);
    line-height: 1.9;
    font-weight: 300;
    margin-bottom: 1.5rem;
  }

  .about-text p strong {
    color: var(--ink);
    font-weight: 500;
  }

  .credentials {
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
    padding-top: 0.5rem;
  }

  .credential-item {
    padding: 1.5rem;
    border: 1px solid var(--border);
    position: relative;
    transition: border-color 0.3s;
  }
  .credential-item:hover { border-color: var(--terracotta); }

  .credential-item::before {
    content: '';
    position: absolute; left: 0; top: 0; bottom: 0;
    width: 3px; background: var(--terracotta);
    transform: scaleY(0);
    transition: transform 0.3s;
    transform-origin: bottom;
  }
  .credential-item:hover::before { transform: scaleY(1); }

  .credential-school {
    font-size: 0.72rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--terracotta);
    margin-bottom: 0.4rem;
  }

  .credential-degree {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.1rem;
    font-weight: 600;
    margin-bottom: 0.3rem;
  }

  .credential-detail {
    font-size: 0.82rem;
    color: var(--ink-light);
  }

  .credential-badge {
    display: inline-block;
    margin-top: 0.5rem;
    padding: 0.2rem 0.7rem;
    background: var(--terracotta);
    color: white;
    font-size: 0.68rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
  }

  /* EXPERTISE */
  .expertise {
    background: var(--cream);
  }

  .expertise-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 0;
    margin-top: 3rem;
    border: 1px solid var(--border);
  }

  .expertise-item {
    padding: 2.5rem;
    border-right: 1px solid var(--border);
    border-bottom: 1px solid var(--border);
    transition: background 0.3s;
    position: relative;
    overflow: hidden;
  }
  .expertise-item:hover { background: white; }
  .expertise-item:nth-child(3n) { border-right: none; }
  .expertise-item:nth-last-child(-n+3) { border-bottom: none; }

  .expertise-num {
    font-family: 'Cormorant Garamond', serif;
    font-size: 3rem;
    font-weight: 300;
    color: var(--border);
    line-height: 1;
    margin-bottom: 1rem;
    transition: color 0.3s;
  }
  .expertise-item:hover .expertise-num { color: var(--terracotta); opacity: 0.4; }

  .expertise-title {
    font-size: 0.85rem;
    font-weight: 500;
    letter-spacing: 0.05em;
    margin-bottom: 0.8rem;
    text-transform: uppercase;
    font-size: 0.78rem;
    letter-spacing: 0.1em;
  }

  .expertise-desc {
    font-size: 0.85rem;
    color: var(--ink-light);
    line-height: 1.7;
    font-weight: 300;
  }

  .tools-list {
    display: flex; flex-wrap: wrap; gap: 0.4rem;
    margin-top: 1rem;
  }

  .tool-tag {
    font-size: 0.68rem;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    padding: 0.2rem 0.6rem;
    border: 1px solid var(--border);
    color: var(--ink-light);
  }

  /* CASE STUDIES */
  .case-studies {
    background: white;
  }

  .case-study {
    margin-top: 5rem;
    padding-top: 5rem;
    border-top: 1px solid var(--border);
  }
  .case-study:first-of-type { margin-top: 3rem; padding-top: 0; border-top: none; }

  .case-header {
    display: grid;
    grid-template-columns: auto 1fr auto;
    align-items: start;
    gap: 2rem;
    margin-bottom: 3rem;
  }

  .case-num {
    font-family: 'Cormorant Garamond', serif;
    font-size: 5rem;
    font-weight: 300;
    color: var(--border);
    line-height: 1;
  }

  .case-meta {}

  .case-tag {
    font-size: 0.68rem;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--terracotta);
    margin-bottom: 0.5rem;
  }

  .case-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: 2.2rem;
    font-weight: 400;
    line-height: 1.2;
    margin-bottom: 0.5rem;
  }

  .case-subtitle {
    font-size: 0.82rem;
    color: var(--ink-light);
  }

  .case-kpis {
    display: flex; flex-direction: column; gap: 1rem;
    min-width: 200px;
  }

  .kpi-item {
    text-align: right;
  }

  .kpi-value {
    font-family: 'Cormorant Garamond', serif;
    font-size: 2.2rem;
    font-weight: 600;
    color: var(--terracotta);
    line-height: 1;
  }

  .kpi-label {
    font-size: 0.7rem;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    color: var(--ink-light);
  }

  .case-body {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4rem;
    align-items: start;
  }

  .case-narrative h4 {
    font-size: 0.72rem;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--terracotta);
    margin-bottom: 0.8rem;
    margin-top: 1.8rem;
  }
  .case-narrative h4:first-child { margin-top: 0; }

  .case-narrative p {
    font-size: 0.92rem;
    color: var(--ink-light);
    line-height: 1.9;
    font-weight: 300;
  }

  .chart-container {
    background: var(--cream);
    padding: 2rem;
    border: 1px solid var(--border);
  }

  .chart-title {
    font-size: 0.72rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--ink-light);
    margin-bottom: 1.5rem;
  }

  .chart-wrapper {
    position: relative;
    height: 220px;
  }

  .chart-insight {
    margin-top: 1rem;
    padding-top: 1rem;
    border-top: 1px solid var(--border);
    font-size: 0.78rem;
    color: var(--ink-light);
    font-style: italic;
  }

  .multi-chart {
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
  }

  /* CAMPAIGN VISUAL */
  .campaign-image {
    width: 100%;
    border: 1px solid var(--border);
    display: block;
  }

  .campaign-images {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1rem;
    margin-top: 1.5rem;
  }

  /* BRANDS */
  .brands {
    background: var(--ink);
    color: white;
    text-align: center;
  }

  .brands .section-label { justify-content: center; color: var(--terracotta-light); }
  .brands .section-label::before { background: var(--terracotta-light); }
  .brands .section-title { color: white; }

  .brand-logos {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 5rem;
    margin-top: 4rem;
    flex-wrap: wrap;
  }

  .brand-logo-item {
    display: flex; flex-direction: column; align-items: center; gap: 0.8rem;
  }

  .brand-icon {
    width: 64px; height: 64px;
    border: 1px solid rgba(255,255,255,0.15);
    border-radius: 12px;
    display: flex; align-items: center; justify-content: center;
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.4rem;
    font-weight: 600;
    color: var(--terracotta-light);
  }

  .brand-name {
    font-size: 0.75rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: rgba(255,255,255,0.5);
  }

  /* CONTACT */
  .contact {
    background: var(--cream);
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 6rem;
    align-items: center;
  }

  .contact-left .section-title {
    margin-bottom: 1.5rem;
  }

  .contact-left p {
    font-size: 1rem;
    color: var(--ink-light);
    line-height: 1.9;
    font-weight: 300;
    margin-bottom: 2rem;
  }

  .contact-links {
    display: flex;
    flex-direction: column;
    gap: 1.2rem;
  }

  .contact-link {
    display: flex; align-items: center; gap: 1.2rem;
    text-decoration: none; color: var(--ink);
    padding: 1.2rem 1.5rem;
    border: 1px solid var(--border);
    transition: all 0.2s;
  }
  .contact-link:hover {
    background: white;
    border-color: var(--terracotta);
    color: var(--terracotta);
  }

  .contact-link-icon {
    width: 36px; height: 36px;
    border-radius: 50%;
    background: var(--terracotta);
    color: white;
    display: flex; align-items: center; justify-content: center;
    font-size: 0.85rem;
    flex-shrink: 0;
  }

  .contact-link-text { flex: 1; }
  .contact-link-label {
    font-size: 0.68rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--ink-light);
    margin-bottom: 0.2rem;
  }
  .contact-link-value {
    font-size: 0.9rem;
    font-weight: 400;
  }

  .skills-visual {
    display: flex;
    flex-direction: column;
    gap: 1rem;
  }

  .skill-bar-item {
    display: flex; flex-direction: column; gap: 0.4rem;
  }

  .skill-bar-header {
    display: flex; justify-content: space-between; align-items: center;
  }

  .skill-bar-name {
    font-size: 0.78rem;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    font-weight: 500;
  }

  .skill-bar-level {
    font-size: 0.72rem;
    color: var(--ink-light);
  }

  .skill-bar-track {
    height: 3px;
    background: var(--border);
    position: relative;
    overflow: hidden;
  }

  .skill-bar-fill {
    position: absolute; left: 0; top: 0; bottom: 0;
    background: var(--terracotta);
    transform: scaleX(0);
    transform-origin: left;
    transition: transform 1.2s cubic-bezier(0.4, 0, 0.2, 1);
  }
  .skill-bar-fill.animate { transform: scaleX(1); }

  /* FOOTER */
  footer {
    background: var(--ink);
    color: rgba(255,255,255,0.4);
    text-align: center;
    padding: 2rem;
    font-size: 0.75rem;
    letter-spacing: 0.08em;
  }

  /* ANIMATIONS */
  .fade-in {
    opacity: 0;
    transform: translateY(24px);
    transition: opacity 0.8s ease, transform 0.8s ease;
  }
  .fade-in.visible {
    opacity: 1;
    transform: translateY(0);
  }

  @media (max-width: 900px) {
    nav { padding: 1rem 1.5rem; }
    .nav-links { display: none; }
    .hero { grid-template-columns: 1fr; }
    .hero-right { display: none; }
    section { padding: 5rem 1.5rem; }
    .about, .contact { grid-template-columns: 1fr; gap: 3rem; }
    .expertise-grid { grid-template-columns: 1fr 1fr; }
    .case-body { grid-template-columns: 1fr; }
    .case-header { grid-template-columns: 1fr; }
    .case-num { font-size: 3rem; }
    .brand-logos { gap: 2.5rem; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <a href="#" class="nav-logo">Sharifakhon Ibrohimova</a>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#expertise">Expertise</a></li>
    <li><a href="#work">Work</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<!-- HERO -->
<section class="hero" style="padding: 0;">
  <div class="hero-left fade-in">
    <div class="hero-tag">Marketing Strategist · Amsterdam</div>
    <h1 class="hero-name">
      Sharifa<em>khon</em><br>Ibrohimova
    </h1>
    <p class="hero-desc">
      Marketing professional with hands-on experience turning commercial objectives into measurable results — from global FIFA activations to B2B marketing automation across international consumer electronics markets.
    </p>
    <div class="hero-stats">
      <div>
        <div class="stat-number">3×</div>
        <div class="stat-label">Campaign participation growth</div>
      </div>
      <div>
        <div class="stat-number">30%</div>
        <div class="stat-label">Brand recognition increase</div>
      </div>
      <div>
        <div class="stat-number">37%</div>
        <div class="stat-label">Process improvement rate</div>
      </div>
    </div>
  </div>

  <div class="hero-right">
    <div class="hero-placeholder">
      <div class="initials">SI</div>
      <p style="font-size:0.75rem; letter-spacing:0.15em; text-transform:uppercase; opacity:0.4;">
        Add your photo here
      </p>
    </div>
    <div class="hero-image-overlay"></div>
    <div class="hero-image-text">
      <h3>MSc Digital Marketing</h3>
      <p>Wittenborg University · Graduated with Distinction</p>
    </div>
  </div>
</section>

<!-- ABOUT -->
<section class="about" id="about">
  <div class="about-text fade-in">
    <div class="section-label">About</div>
    <h2 class="section-title">From Tashkent to Amsterdam, I build campaigns that convert.</h2>
    <p>
      I'm a marketing strategist with a background in consumer electronics — having led promotional operations for <strong>vivo (BBK Electronics)</strong> in Uzbekistan and supported B2B marketing at <strong>Avery Dennison</strong> in the Netherlands. I work across the full campaign lifecycle: strategy and planning, cross-functional execution, budget management, and post-campaign analysis.
    </p>
    <p>
      What sets my work apart is the combination of <strong>ground-level operational experience</strong> with formal analytical training. I've planned and controlled budgets, coordinated with regional retail partners, built email automation workflows, and reported performance to senior management — all within structured corporate environments.
    </p>
    <p>
      I bring a multilingual perspective (Uzbek, Russian, English) and a track record of executing in complex, fast-moving markets.
    </p>
  </div>

  <div class="credentials fade-in">
    <div class="section-label">Education</div>
    <div class="credential-item">
      <div class="credential-school">Wittenborg University · Amsterdam</div>
      <div class="credential-degree">MSc Digital Marketing & Communications</div>
      <div class="credential-detail">GPA 7.8/10 · Thesis: 9/10 · Sep 2023 – Dec 2025</div>
      <span class="credential-badge">Graduated with Distinction</span>
    </div>
    <div class="credential-item">
      <div class="credential-school">Wittenborg University</div>
      <div class="credential-degree">Pre-Master's Program — Business & Management</div>
      <div class="credential-detail">Feb 2023 – Aug 2023</div>
    </div>
    <div class="credential-item">
      <div class="credential-school">Uzbek State World Languages University · Tashkent</div>
      <div class="credential-degree">BA English Philology & Teaching Languages</div>
      <div class="credential-detail">GPA 4.3/5 · Sep 2017 – Jun 2021</div>
    </div>

    <div style="margin-top:1rem; padding:1.5rem; background:var(--cream); border:1px solid var(--border);">
      <div class="credential-school" style="margin-bottom:0.8rem;">Languages</div>
      <div style="display:flex; flex-direction:column; gap:0.5rem;">
        <div style="display:flex; justify-content:space-between; font-size:0.82rem;">
          <span>Uzbek</span><span style="color:var(--terracotta);">Native</span>
        </div>
        <div style="display:flex; justify-content:space-between; font-size:0.82rem;">
          <span>Russian</span><span style="color:var(--terracotta);">Fluent</span>
        </div>
        <div style="display:flex; justify-content:space-between; font-size:0.82rem;">
          <span>English</span><span style="color:var(--terracotta);">Professional</span>
        </div>
        <div style="display:flex; justify-content:space-between; font-size:0.82rem;">
          <span>Dutch</span><span style="color:var(--ink-light);">Beginner</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- EXPERTISE -->
<section class="expertise" id="expertise">
  <div class="section-label">Expertise</div>
  <h2 class="section-title">What I bring to the table</h2>
  <div class="expertise-grid fade-in">
    <div class="expertise-item">
      <div class="expertise-num">01</div>
      <div class="expertise-title">Campaign Strategy & Planning</div>
      <div class="expertise-desc">End-to-end campaign development: audience segmentation, mechanic design, channel selection, and budget allocation across open market and key account channels.</div>
    </div>
    <div class="expertise-item">
      <div class="expertise-num">02</div>
      <div class="expertise-title">GTM & Product Launch</div>
      <div class="expertise-desc">Coordinating multi-SKU product launches with cross-functional teams including sales, retail, product, and regional management.</div>
    </div>
    <div class="expertise-item">
      <div class="expertise-num">03</div>
      <div class="expertise-title">Marketing Automation</div>
      <div class="expertise-desc">Building and managing email automation workflows. Experienced with ACT ON, Klaviyo, HubSpot, and Salesforce CRM data management.</div>
      <div class="tools-list">
        <span class="tool-tag">ACT ON</span>
        <span class="tool-tag">Klaviyo</span>
        <span class="tool-tag">HubSpot</span>
        <span class="tool-tag">Salesforce</span>
      </div>
    </div>
    <div class="expertise-item">
      <div class="expertise-num">04</div>
      <div class="expertise-title">Data Analysis & Reporting</div>
      <div class="expertise-desc">Post-campaign performance analysis, promo ROI modelling, and structured reporting to senior stakeholders. Proficient in SQL, Python, and Tableau.</div>
      <div class="tools-list">
        <span class="tool-tag">SQL</span>
        <span class="tool-tag">Python</span>
        <span class="tool-tag">Tableau</span>
        <span class="tool-tag">Excel</span>
      </div>
    </div>
    <div class="expertise-item">
      <div class="expertise-num">05</div>
      <div class="expertise-title">Retail & Channel Marketing</div>
      <div class="expertise-desc">Co-marketing programme management with key account partners, in-store activation, partner relationship management, and regional market visits.</div>
    </div>
    <div class="expertise-item">
      <div class="expertise-num">06</div>
      <div class="expertise-title">Budget Management</div>
      <div class="expertise-desc">Planning and controlling promotional budgets across multiple simultaneous activations. Experience tracking planned vs. actual spend and reporting variance.</div>
    </div>
  </div>
</section>

<!-- CASE STUDIES -->
<section class="case-studies" id="work">
  <div class="section-label">Selected Work</div>
  <h2 class="section-title">Three campaigns, three different disciplines.</h2>

  <!-- CASE STUDY 1 - FIFA -->
  <div class="case-study fade-in">
    <div class="case-header">
      <div class="case-num">01</div>
      <div class="case-meta">
        <div class="case-tag">vivo · BBK Electronics · Uzbekistan · Aug–Dec 2022</div>
        <h3 class="case-title">FIFA World Cup Qatar 2022 — Integrated Campaign Activation</h3>
        <p class="case-subtitle">Translating a global sponsorship into a 5-month national sales promotion strategy</p>
      </div>
      <div class="case-kpis">
        <div class="kpi-item">
          <div class="kpi-value">3×</div>
          <div class="kpi-label">Participation YoY</div>
        </div>
        <div class="kpi-item">
          <div class="kpi-value">7.4K</div>
          <div class="kpi-label">Launch post reach</div>
        </div>
        <div class="kpi-item">
          <div class="kpi-value">3</div>
          <div class="kpi-label">KA partners activated</div>
        </div>
      </div>
    </div>

    <div class="case-body">
      <div class="case-narrative">
        <h4>The Challenge</h4>
        <p>vivo was the Official Smartphone of FIFA World Cup Qatar 2022 — a global sponsorship that created a rare opportunity for the Uzbekistan market. The challenge was translating a premium global IP into a locally resonant, multi-month campaign that drove measurable sell-out across a portfolio of 6 smartphone models, through both open market and key account retail channels simultaneously.</p>

        <h4>The Approach</h4>
        <p>Rather than a single burst campaign, I planned a phased 5-month promotional arc. The campaign opened with a high-stakes grand prize mechanic (flights + hotel + FIFA Final tickets in Doha) to generate registrations and awareness in Q3, then transitioned to gifting-based promotions (branded backpacks, FIFA merchandise from China) to maintain momentum through the tournament. Each phase was differentiated by channel — open market received in-store activations while key accounts (Texnomart, Elmakon, MediaPark) ran co-marketing executions with dedicated budgets.</p>

        <h4>The Execution</h4>
        <p>Campaign creative ran bilingual (Uzbek and Russian). Customers registered through a dedicated digital platform, providing traceable participation data. Winners were announced via Instagram Live — extending campaign reach beyond the promotion window. Budget was managed across $29K in H2 promotional and event spend, delivered on time across all partner activations.</p>
      </div>

      <div style="display:flex; flex-direction:column; gap:1.5rem;">
        <div class="chart-container">
          <div class="chart-title">Campaign Participation — Indexed Year on Year</div>
          <div class="chart-wrapper">
            <canvas id="fifaChart"></canvas>
          </div>
          <div class="chart-insight">Campaign participation grew 3× versus the prior year's comparable promotion, driven by the premium grand prize mechanic and phased rollout across channels.</div>
        </div>

        <div class="chart-container">
          <div class="chart-title">H2 Promotional Timeline — Channel Coverage</div>
          <div class="chart-wrapper" style="height:160px;">
            <canvas id="timelineChart"></canvas>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- CASE STUDY 2 - VIVO BRAND -->
  <div class="case-study fade-in">
    <div class="case-header">
      <div class="case-num">02</div>
      <div class="case-meta">
        <div class="case-tag">vivo · BBK Electronics · Uzbekistan · 2021–2022</div>
        <h3 class="case-title">Brand Expansion & Retail Growth Strategy</h3>
        <p class="case-subtitle">Full-year promotional programme driving recognition and partner network expansion</p>
      </div>
      <div class="case-kpis">
        <div class="kpi-item">
          <div class="kpi-value">30%</div>
          <div class="kpi-label">Brand recognition ↑</div>
        </div>
        <div class="kpi-item">
          <div class="kpi-value">23%</div>
          <div class="kpi-label">Sales increase</div>
        </div>
        <div class="kpi-item">
          <div class="kpi-value">11%</div>
          <div class="kpi-label">Partner store growth</div>
        </div>
      </div>
    </div>

    <div class="case-body">
      <div class="case-narrative">
        <h4>The Context</h4>
        <p>As Promotion Manager at vivo Uzbekistan, I oversaw end-to-end promotional strategy for the full product portfolio across a highly competitive smartphone market. The department's mandate was to increase brand visibility, drive retail sell-out, and build stronger relationships with key account partners — while operating within defined budgets and maintaining efficiency.</p>

        <h4>The Strategy</h4>
        <p>I developed a tiered promotional model — separating mass-market open channel activations from individually tailored key account programmes. For high-priority A/A+ category stores, I implemented individual shop focus plans with customised support. Budget allocation was driven by promo ROI analysis tracking investment percentage per unit sold, allowing us to identify which mechanics and models delivered the strongest return and reallocate spend accordingly.</p>

        <h4>Budget Efficiency</h4>
        <p>By applying data-driven decision-making to gift allocation and timing, H1 actual spend came in 49% under plan while still delivering 8+ sales promotions and 3 co-marketing projects — demonstrating that disciplined planning, not just spend, drives results.</p>
      </div>

      <div style="display:flex; flex-direction:column; gap:1.5rem;">
        <div class="chart-container">
          <div class="chart-title">Key Business Outcomes — Full Tenure</div>
          <div class="chart-wrapper">
            <canvas id="brandChart"></canvas>
          </div>
          <div class="chart-insight">All three core KPIs exceeded targets, with brand recognition showing the strongest absolute growth at +30 percentage points.</div>
        </div>

        <div class="chart-container">
          <div class="chart-title">H1 Budget Efficiency — Planned vs. Actual ($USD)</div>
          <div class="chart-wrapper" style="height:160px;">
            <canvas id="budgetChart"></canvas>
          </div>
          <div class="chart-insight">Full H1 programme delivered 49% under budget across all promotion categories.</div>
        </div>
      </div>
    </div>
  </div>

  <!-- CASE STUDY 3 - AVERY DENNISON -->
  <div class="case-study fade-in">
    <div class="case-header">
      <div class="case-num">03</div>
      <div class="case-meta">
        <div class="case-tag">Avery Dennison · B2B · Netherlands · 2024–2025</div>
        <h3 class="case-title">B2B Marketing Automation — Product Communication Workflow</h3>
        <p class="case-subtitle">Streamlining multi-SKU product updates across departments using ACT ON and Salesforce</p>
      </div>
      <div class="case-kpis">
        <div class="kpi-item">
          <div class="kpi-value">37%</div>
          <div class="kpi-label">Process improvement</div>
        </div>
        <div class="kpi-item">
          <div class="kpi-value">36</div>
          <div class="kpi-label">SKUs managed</div>
        </div>
        <div class="kpi-item">
          <div class="kpi-value">25%</div>
          <div class="kpi-label">Foot traffic ↑</div>
        </div>
      </div>
    </div>

    <div class="case-body">
      <div class="case-narrative">
        <h4>The Problem</h4>
        <p>At Avery Dennison's Netherlands office, product update communications for a 36-SKU portfolio were handled manually and inconsistently across departments. This created delays, data discrepancies in Salesforce, and a fragmented experience for downstream stakeholders who relied on accurate, timely product information.</p>

        <h4>The Solution</h4>
        <p>I implemented an automated email communication workflow using ACT ON, designed to systematically distribute product update notifications to the right stakeholders at the right time. The automation replaced an ad hoc process with a structured, trackable pipeline — with all data feeding consistently into Salesforce CRM.</p>

        <h4>The Impact</h4>
        <p>The workflow delivered a 37% improvement in process efficiency, reduced manual effort across departments, and improved data consistency in Salesforce. This project also required navigating a complex cross-functional environment — coordinating with sales, product, and IT teams — which developed my ability to manage stakeholder expectations and drive adoption of new processes in a structured corporate setting.</p>
      </div>

      <div style="display:flex; flex-direction:column; gap:1.5rem;">
        <div class="chart-container">
          <div class="chart-title">Process Efficiency — Before vs. After Automation</div>
          <div class="chart-wrapper">
            <canvas id="automationChart"></canvas>
          </div>
          <div class="chart-insight">Automation reduced manual process overhead by 37%, with consistent data quality improvement across all 36 product SKUs.</div>
        </div>

        <div class="chart-container">
          <div class="chart-title">Tool Stack Used</div>
          <div style="display:flex; flex-wrap:wrap; gap:0.6rem; margin-top:0.5rem;">
            <span class="tool-tag" style="padding:0.5rem 1rem; font-size:0.78rem;">ACT ON Automation</span>
            <span class="tool-tag" style="padding:0.5rem 1rem; font-size:0.78rem;">Salesforce CRM</span>
            <span class="tool-tag" style="padding:0.5rem 1rem; font-size:0.78rem;">Email Workflows</span>
            <span class="tool-tag" style="padding:0.5rem 1rem; font-size:0.78rem;">Data QA</span>
            <span class="tool-tag" style="padding:0.5rem 1rem; font-size:0.78rem;">Cross-dept Coordination</span>
            <span class="tool-tag" style="padding:0.5rem 1rem; font-size:0.78rem;">Stakeholder Reporting</span>
          </div>
          <div style="margin-top:1.5rem;">
            <div class="chart-title">Additional Outcomes</div>
            <div style="display:flex; flex-direction:column; gap:0.8rem; margin-top:0.8rem;">
              <div style="display:flex; align-items:center; gap:1rem;">
                <div style="width:4px; height:4px; border-radius:50%; background:var(--terracotta); flex-shrink:0;"></div>
                <span style="font-size:0.85rem; color:var(--ink-light);">25% increase in foot traffic through integrated campaign support</span>
              </div>
              <div style="display:flex; align-items:center; gap:1rem;">
                <div style="width:4px; height:4px; border-radius:50%; background:var(--terracotta); flex-shrink:0;"></div>
                <span style="font-size:0.85rem; color:var(--ink-light);">Improved data consistency across Salesforce records</span>
              </div>
              <div style="display:flex; align-items:center; gap:1rem;">
                <div style="width:4px; height:4px; border-radius:50%; background:var(--terracotta); flex-shrink:0;"></div>
                <span style="font-size:0.85rem; color:var(--ink-light);">Cross-functional stakeholder coordination across 3 departments</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- BRANDS -->
<section class="brands">
  <div class="section-label">Experience</div>
  <h2 class="section-title" style="color:white;">Brands I've worked with</h2>
  <div class="brand-logos">
    <div class="brand-logo-item">
      <div class="brand-icon">AD</div>
      <div class="brand-name">Avery Dennison</div>
    </div>
    <div class="brand-logo-item">
      <div class="brand-icon">V</div>
      <div class="brand-name">vivo · BBK Electronics</div>
    </div>
    <div class="brand-logo-item">
      <div class="brand-icon" style="font-size:0.9rem; letter-spacing:0.05em;">FIFA</div>
      <div class="brand-name">FIFA World Cup 2022</div>
    </div>
    <div class="brand-logo-item">
      <div class="brand-icon" style="font-size:0.75rem; text-align:center; line-height:1.2;">WU</div>
      <div class="brand-name">Wittenborg University</div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section class="contact" id="contact">
  <div class="contact-left fade-in">
    <div class="section-label">Contact</div>
    <h2 class="section-title">Let's work together.</h2>
    <p>I'm open to Marketing Specialist, Product Marketing, and CRM/Marketing Automation roles in the Netherlands. Based in the Amsterdam area.</p>
    <div class="contact-links">
      <a href="mailto:ibrohimovasharifa@gmail.com" class="contact-link">
        <div class="contact-link-icon">@</div>
        <div class="contact-link-text">
          <div class="contact-link-label">Email</div>
          <div class="contact-link-value">ibrohimovasharifa@gmail.com</div>
        </div>
      </a>
      <a href="https://linkedin.com/in/sharifakhon-ibrohimova" class="contact-link" target="_blank">
        <div class="contact-link-icon">in</div>
        <div class="contact-link-text">
          <div class="contact-link-label">LinkedIn</div>
          <div class="contact-link-value">Sharifakhon Ibrohimova</div>
        </div>
      </a>
      <a href="tel:0687829867" class="contact-link">
        <div class="contact-link-icon">↗</div>
        <div class="contact-link-text">
          <div class="contact-link-label">Phone</div>
          <div class="contact-link-value">+31 687 829 867</div>
        </div>
      </a>
    </div>
  </div>

  <div class="skills-visual fade-in">
    <div class="section-label">Core Skills</div>
    <div class="skill-bar-item">
      <div class="skill-bar-header">
        <span class="skill-bar-name">Campaign Strategy</span>
        <span class="skill-bar-level">Advanced</span>
      </div>
      <div class="skill-bar-track">
        <div class="skill-bar-fill" style="width:90%"></div>
      </div>
    </div>
    <div class="skill-bar-item">
      <div class="skill-bar-header">
        <span class="skill-bar-name">Marketing Automation</span>
        <span class="skill-bar-level">Advanced</span>
      </div>
      <div class="skill-bar-track">
        <div class="skill-bar-fill" style="width:85%"></div>
      </div>
    </div>
    <div class="skill-bar-item">
      <div class="skill-bar-header">
        <span class="skill-bar-name">Data Analysis / SQL / Python</span>
        <span class="skill-bar-level">Proficient</span>
      </div>
      <div class="skill-bar-track">
        <div class="skill-bar-fill" style="width:75%"></div>
      </div>
    </div>
    <div class="skill-bar-item">
      <div class="skill-bar-header">
        <span class="skill-bar-name">Budget Management</span>
        <span class="skill-bar-level">Advanced</span>
      </div>
      <div class="skill-bar-track">
        <div class="skill-bar-fill" style="width:88%"></div>
      </div>
    </div>
    <div class="skill-bar-item">
      <div class="skill-bar-header">
        <span class="skill-bar-name">GTM & Product Launch</span>
        <span class="skill-bar-level">Proficient</span>
      </div>
      <div class="skill-bar-track">
        <div class="skill-bar-fill" style="width:80%"></div>
      </div>
    </div>
    <div class="skill-bar-item">
      <div class="skill-bar-header">
        <span class="skill-bar-name">CRM / Salesforce</span>
        <span class="skill-bar-level">Proficient</span>
      </div>
      <div class="skill-bar-track">
        <div class="skill-bar-fill" style="width:72%"></div>
      </div>
    </div>
    <div class="skill-bar-item">
      <div class="skill-bar-header">
        <span class="skill-bar-name">Stakeholder Management</span>
        <span class="skill-bar-level">Advanced</span>
      </div>
      <div class="skill-bar-track">
        <div class="skill-bar-fill" style="width:85%"></div>
      </div>
    </div>
  </div>
</section>

<footer>
  © 2025 Sharifakhon Ibrohimova — Marketing Strategist — Amsterdam, Netherlands
</footer>

<script>
// Chart defaults
Chart.defaults.font.family = "'DM Sans', sans-serif";
Chart.defaults.color = '#4A4A4A';

const terracotta = '#C4614A';
const terracottaLight = '#E8957F';
const border = '#E0DAD0';
const ink = '#1A1A1A';
const gold = '#B8976A';

// FIFA participation chart
new Chart(document.getElementById('fifaChart'), {
  type: 'bar',
  data: {
    labels: ['Prior Year Campaign', 'FIFA 2022 Campaign'],
    datasets: [{
      label: 'Participation Index',
      data: [100, 300],
      backgroundColor: [border, terracotta],
      borderWidth: 0,
      borderRadius: 2,
    }]
  },
  options: {
    responsive: true, maintainAspectRatio: false,
    plugins: {
      legend: { display: false },
      tooltip: {
        callbacks: {
          label: ctx => `Index: ${ctx.raw} (base = 100)`
        }
      }
    },
    scales: {
      y: {
        beginAtZero: true,
        max: 350,
        ticks: { stepSize: 100, callback: v => v + 'x' === '100x' ? 'Baseline' : v/100 + '×' },
        grid: { color: border }
      },
      x: { grid: { display: false } }
    }
  }
});

// Timeline / channel coverage
new Chart(document.getElementById('timelineChart'), {
  type: 'bar',
  data: {
    labels: ['Aug', 'Sep', 'Oct', 'Nov', 'Dec'],
    datasets: [
      {
        label: 'Open Market',
        data: [1, 1, 1, 1, 1],
        backgroundColor: terracotta,
        borderRadius: 3,
      },
      {
        label: 'Key Accounts',
        data: [1, 1, 1, 1, 1],
        backgroundColor: gold,
        borderRadius: 3,
      }
    ]
  },
  options: {
    responsive: true, maintainAspectRatio: false,
    plugins: {
      legend: { position: 'bottom', labels: { boxWidth: 10, font: { size: 11 } } },
      tooltip: {
        callbacks: { label: ctx => ctx.dataset.label + ': Active' }
      }
    },
    scales: {
      y: { display: false, stacked: true },
      x: { stacked: true, grid: { display: false } }
    }
  }
});

// Brand outcomes chart
new Chart(document.getElementById('brandChart'), {
  type: 'bar',
  data: {
    labels: ['Brand Recognition', 'Sales Growth', 'Partner Store Growth'],
    datasets: [{
      label: '% Increase',
      data: [30, 23, 11],
      backgroundColor: [terracotta, gold, '#8B9E8A'],
      borderWidth: 0,
      borderRadius: 2,
    }]
  },
  options: {
    indexAxis: 'y',
    responsive: true, maintainAspectRatio: false,
    plugins: {
      legend: { display: false },
      tooltip: { callbacks: { label: ctx => '+' + ctx.raw + '%' } }
    },
    scales: {
      x: {
        beginAtZero: true, max: 40,
        ticks: { callback: v => '+' + v + '%' },
        grid: { color: border }
      },
      y: { grid: { display: false } }
    }
  }
});

// Budget chart
new Chart(document.getElementById('budgetChart'), {
  type: 'bar',
  data: {
    labels: ['Sales Promotion', 'Co-marketing', 'Other'],
    datasets: [
      {
        label: 'Planned ($)',
        data: [53000, 23000, 4000],
        backgroundColor: border,
        borderWidth: 0,
        borderRadius: 2,
      },
      {
        label: 'Actual Spent ($)',
        data: [33900, 5900, 1120],
        backgroundColor: terracotta,
        borderWidth: 0,
        borderRadius: 2,
      }
    ]
  },
  options: {
    responsive: true, maintainAspectRatio: false,
    plugins: {
      legend: { position: 'bottom', labels: { boxWidth: 10, font: { size: 11 } } },
      tooltip: {
        callbacks: { label: ctx => ctx.dataset.label + ': $' + ctx.raw.toLocaleString() }
      }
    },
    scales: {
      y: {
        beginAtZero: true,
        ticks: { callback: v => '$' + (v/1000) + 'K' },
        grid: { color: border }
      },
      x: { grid: { display: false } }
    }
  }
});

// Automation chart
new Chart(document.getElementById('automationChart'), {
  type: 'doughnut',
  data: {
    labels: ['Process Improvement', 'Remaining Baseline'],
    datasets: [{
      data: [37, 63],
      backgroundColor: [terracotta, border],
      borderWidth: 0,
      hoverOffset: 4,
    }]
  },
  options: {
    responsive: true, maintainAspectRatio: false,
    cutout: '72%',
    plugins: {
      legend: { display: false },
      tooltip: { callbacks: { label: ctx => ctx.label + ': ' + ctx.raw + '%' } }
    }
  },
  plugins: [{
    id: 'centerText',
    beforeDraw(chart) {
      const { width, height, ctx } = chart;
      ctx.save();
      ctx.font = "600 2rem 'Cormorant Garamond', serif";
      ctx.fillStyle = terracotta;
      ctx.textAlign = 'center';
      ctx.textBaseline = 'middle';
      ctx.fillText('37%', width/2, height/2 - 10);
      ctx.font = "300 0.7rem 'DM Sans', sans-serif";
      ctx.fillStyle = '#4A4A4A';
      ctx.letterSpacing = '0.1em';
      ctx.fillText('IMPROVEMENT', width/2, height/2 + 20);
      ctx.restore();
    }
  }]
});

// Intersection Observer for animations
const observer = new IntersectionObserver(entries => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      entry.target.classList.add('visible');
      // Animate skill bars
      entry.target.querySelectorAll('.skill-bar-fill').forEach(bar => {
        bar.classList.add('animate');
      });
    }
  });
}, { threshold: 0.1 });

document.querySelectorAll('.fade-in').forEach(el => observer.observe(el));
// Trigger hero immediately
document.querySelector('.hero-left').classList.add('visible');
</script>
</body>
</html>
