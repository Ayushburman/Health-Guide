<!DOCTYPE html0
>
<html 
    lang=
    "en">
    jnaj
<meta 
    
    charset="UTF-8meta name="viewport" content="widle>Post-SCT DayRoadmap</tithref="https://fonts.googleapis.family=splay:italrel="stylesheent: #c444952 --sage: #4a7c5 --sky: #2e6b8a--la--warm: #b85c2 --card: #faf7f2 --border: #d4c9b8--muted: #7a6e6 --green-light: #e8f4ec --amber-light: #fdf3 --blue-light: #e8f0f7-red-light: #fdeee9;
    --purple-light: #f0ec
  * { margin:
  * 0; padding: 0; box-sizing: border-box; }body {
    font-family: 'Instrument Sans', sans-serif;
    background: var(--bg);
    color: var(--ink);
    line-height: 1.6;
    overflow-x: hidden;
  }m* ── HERO ── */
  .hero {
    position: relative;
    background: var(--ink);
    color: var(--bg);
    padding: 80px 40px 60px;
    overflow: hidden;
    text-align: center;
  }

  .hero-bg-circles {
    position: absolute;
    inset: 0;
    pointer-events: none;
  }

  .hero-bg-circles circle {
    fill: none;
    stroke: rgba(212,195,184,0.12);
    stroke-width: 1;
  }

  .hero-badge {
    display: inline-block;
    font-family: 'DM Mono', monospace;
    font-size: 11px;
    font-weight: 500;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    border: 1px solid rgba(212,149,42,0.6);
    color: var(--gold);
    padding: 5px 14px;
    border-radius: 2px;
    margin-bottom: 24px;
    animation: fadeUp 0.7s ease both;
  }

  .hero h1 {
    font-family: 'DM Serif Display', serif;
    font-size: clamp(2.4rem, 5vw, 4.2rem);
    line-height: 1.15;
    max-width: 820px;
    margin: 0 auto 16px;
    animation: fadeUp 0.7s 0.1s ease both;
  }

  .hero h1 em {
    font-style: italic;
    color: var(--gold);
  }

  .hero-sub {
    font-family: 'Instrument Sans', sans-serif;
    font-size: 1.05rem;
    color: rgba(244,240,232,0.65);
    max-width: 600px;
    margin: 0 auto 40px;
    animation: fadeUp 0.7s 0.2s ease both;
  }

  .day-counter {
    display: inline-flex;
    align-items: center;
    gap: 20px;
    background: rgba(255,255,255,0.06);
    border: 1px solid rgba(255,255,255,0.12);
    border-radius: 4px;
    padding: 16px 32px;
    animation: fadeUp 0.7s 0.3s ease both;
  }

  .day-num {
    font-family: 'DM Serif Display', serif;
    font-size: 3.2rem;
    color: var(--gold);
    line-height: 1;
  }

  .day-label {
    font-family: 'DM Mono', monospace;
    font-size: 11px;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: rgba(244,240,232,0.5);
    line-height: 1.4;
    text-align: left;
  }

  /* ── PROGRESS TIMELINE ── */
  .timeline-strip {
    background: var(--ink);
    padding: 0 40px 50px;
    overflow-x: auto;
  }

  .timeline-inner {
    display: flex;
    gap: 0;
    max-width: 1000px;
    margin: 0 auto;
    position: relative;
  }

  .timeline-inner::before {
    content: '';
    position: absolute;
    top: 22px;
    left: 20px;
    right: 20px;
    height: 2px;
    background: rgba(255,255,255,0.1);
  }

  .t-phase {
    flex: 1;
    min-width: 120px;
    text-align: center;
    position: relative;
  }

  .t-dot {
    width: 44px;
    height: 44px;
    border-radius: 50%;
    margin: 0 auto 10px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 18px;
    border: 2px solid transparent;
    position: relative;
    z-index: 1;
  }

  .t-dot.done { background: var(--sage); border-color: var(--sage); }
  .t-dot.active { background: var(--gold); border-color: var(--gold); animation: pulse 2s infinite; }
  .t-dot.future { background: rgba(255,255,255,0.08); border-color: rgba(255,255,255,0.2); }

  .t-label {
    font-family: 'DM Mono', monospace;
    font-size: 10px;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: rgba(244,240,232,0.5);
    line-height: 1.4;
  }

  .t-label.done { color: var(--sage); }
  .t-label.active { color: var(--gold); }

  /* ── MAIN GRID ── */
  .container {
    max-width: 1100px;
    margin: 0 auto;
    padding: 60px 24px;
  }

  .section-head {
    display: flex;
    align-items: center;
    gap: 12px;
    margin-bottom: 28px;
    padding-bottom: 14px;
    border-bottom: 1.5px solid var(--border);
  }

  .section-icon {
    width: 42px;
    height: 42px;
    border-radius: 8px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 20px;
    flex-shrink: 0;
  }

  .section-head h2 {
    font-family: 'DM Serif Display', serif;
    font-size: 1.7rem;
  }

  .section-head .mono-tag {
    font-family: 'DM Mono', monospace;
    font-size: 10px;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    color: var(--muted);
    margin-left: auto;
  }

  /* ── CARDS ── */
  .cards-3 { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 16px; margin-bottom: 56px; }
  .cards-2 { display: grid; grid-template-columns: repeat(auto-fit, minmax(340px, 1fr)); gap: 16px; margin-bottom: 56px; }
  .cards-4 { display: grid; grid-template-columns: repeat(auto-fit, minmax(230px, 1fr)); gap: 14px; margin-bottom: 56px; }

  .card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 22px;
    position: relative;
    transition: transform 0.2s, box-shadow 0.2s;
  }

  .card:hover {
    transform: translateY(-2px);
    box-shadow: 0 8px 24px rgba(0,0,0,0.08);
  }

  .card-accent {
    position: absolute;
    top: 0; left: 0;
    width: 4px;
    height: 100%;
    border-radius: 10px 0 0 10px;
  }

  .card h3 {
    font-family: 'DM Serif Display', serif;
    font-size: 1.15rem;
    margin-bottom: 10px;
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .card p, .card li {
    font-size: 0.88rem;
    color: var(--muted);
    line-height: 1.65;
  }

  .card ul { list-style: none; padding: 0; }
  .card ul li { padding: 3px 0 3px 18px; position: relative; }
  .card ul li::before {
    content: '→';
    position: absolute;
    left: 0;
    color: var(--accent);
    font-size: 10px;
    top: 5px;
  }

  .tag {
    display: inline-block;
    font-family: 'DM Mono', monospace;
    font-size: 9.5px;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    padding: 2px 8px;
    border-radius: 3px;
    margin-bottom: 8px;
  }

  .tag.green { background: var(--green-light); color: var(--sage); }
  .tag.amber { background: var(--amber-light); color: #a07010; }
  .tag.blue  { background: var(--blue-light);  color: var(--sky); }
  .tag.red   { background: var(--red-light);   color: var(--accent); }
  .tag.purple{ background: var(--purple-light); color: var(--lavender); }

  /* ── FOOD PLATE SVG ── */
  .visual-plate {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 28px;
    margin-bottom: 56px;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 32px;
    align-items: center;
  }

  .plate-labels h3 {
    font-family: 'DM Serif Display', serif;
    font-size: 1.3rem;
    margin-bottom: 14px;
  }

  .plate-legend { list-style: none; padding: 0; }
  .plate-legend li {
    display: flex;
    align-items: center;
    gap: 10px;
    font-size: 0.86rem;
    color: var(--muted);
    padding: 5px 0;
    border-bottom: 1px solid var(--border);
  }

  .plate-legend li:last-child { border-bottom: none; }

  .legend-dot {
    width: 14px;
    height: 14px;
    border-radius: 50%;
    flex-shrink: 0;
  }

  .legend-pct {
    margin-left: auto;
    font-family: 'DM Mono', monospace;
    font-size: 11px;
    color: var(--ink);
    font-weight: 500;
  }

  /* ── MINERALS TABLE ── */
  .mineral-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 12px;
    margin-bottom: 56px;
  }

  .mineral-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 16px;
    display: flex;
    gap: 14px;
    align-items: flex-start;
    transition: transform 0.2s;
  }

  .mineral-card:hover { transform: translateY(-2px); box-shadow: 0 6px 18px rgba(0,0,0,0.07); }

  .mineral-icon {
    width: 38px;
    height: 38px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 17px;
    flex-shrink: 0;
  }

  .mineral-name {
    font-family: 'DM Serif Display', serif;
    font-size: 1rem;
    margin-bottom: 3px;
  }

  .mineral-dose {
    font-family: 'DM Mono', monospace;
    font-size: 10px;
    color: var(--muted);
    margin-bottom: 5px;
  }

  .mineral-note {
    font-size: 0.78rem;
    color: var(--muted);
    line-height: 1.5;
  }

  /* ── DAILY SCHEDULE ── */
  .schedule {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 28px;
    margin-bottom: 56px;
  }

  .schedule-row {
    display: flex;
    gap: 20px;
    padding: 14px 0;
    border-bottom: 1px solid var(--border);
    align-items: flex-start;
  }

  .schedule-row:last-child { border-bottom: none; }

  .sched-time {
    font-family: 'DM Mono', monospace;
    font-size: 11px;
    color: var(--muted);
    min-width: 70px;
    padding-top: 2px;
    letter-spacing: 0.05em;
  }

  .sched-dot {
    width: 10px;
    height: 10px;
    border-radius: 50%;
    margin-top: 5px;
    flex-shrink: 0;
  }

  .sched-content { flex: 1; }

  .sched-title {
    font-weight: 600;
    font-size: 0.9rem;
    margin-bottom: 4px;
  }

  .sched-detail {
    font-size: 0.82rem;
    color: var(--muted);
    line-height: 1.55;
  }

  /* ── WARNING BOX ── */
  .warning-box {
    background: #fff8f4;
    border: 1.5px solid #e8b49a;
    border-left: 5px solid var(--accent);
    border-radius: 8px;
    padding: 20px 24px;
    margin-bottom: 56px;
    display: flex;
    gap: 16px;
    align-items: flex-start;
  }

  .warning-icon { font-size: 24px; flex-shrink: 0; padding-top: 2px; }

  .warning-box h3 {
    font-family: 'DM Serif Display', serif;
    font-size: 1.1rem;
    color: var(--accent);
    margin-bottom: 8px;
  }

  .warning-box p, .warning-box li {
    font-size: 0.85rem;
    color: #7a4030;
    line-height: 1.65;
  }

  .warning-box ul { list-style: none; padding: 0; }
  .warning-box ul li { padding: 2px 0 2px 16px; position: relative; }
  .warning-box ul li::before {
    content: '✗';
    position: absolute;
    left: 0;
    color: var(--accent);
    font-size: 11px;
  }

  /* ── EXERCISE TIMELINE ── */
  .ex-phases {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 0;
    margin-bottom: 56px;
    border: 1px solid var(--border);
    border-radius: 10px;
    overflow: hidden;
  }

  .ex-phase {
    padding: 22px;
    border-right: 1px solid var(--border);
    background: var(--card);
    position: relative;
  }

  .ex-phase:last-child { border-right: none; }

  .ex-phase-num {
    font-family: 'DM Serif Display', serif;
    font-size: 2.5rem;
    color: var(--border);
    line-height: 1;
    margin-bottom: 8px;
  }

  .ex-phase-range {
    font-family: 'DM Mono', monospace;
    font-size: 10px;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 6px;
  }

  .ex-phase h3 {
    font-size: 0.95rem;
    font-weight: 600;
    margin-bottom: 8px;
  }

  .ex-phase ul { list-style: none; padding: 0; }
  .ex-phase ul li {
    font-size: 0.8rem;
    color: var(--muted);
    padding: 3px 0 3px 14px;
    position: relative;
  }

  .ex-phase ul li::before {
    content: '•';
    position: absolute;
    left: 0;
  }

  .ex-phase.active-phase {
    background: #fffcf5;
    border-top: 3px solid var(--gold);
  }

  /* ── HYDRATION ── */
  .hydration-bar {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 28px;
    margin-bottom: 56px;
  }

  .water-glasses {
    display: flex;
    gap: 10px;
    flex-wrap: wrap;
    margin: 18px 0;
  }

  .glass {
    width: 44px;
    height: 58px;
  }

  .glass-filled rect.fill { opacity: 1; }
  .glass-empty rect.fill { opacity: 0.15; }

  .hydration-rules {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 12px;
    margin-top: 18px;
  }

  .hyd-rule {
    font-size: 0.84rem;
    color: var(--muted);
    padding: 10px 14px;
    background: var(--blue-light);
    border-radius: 6px;
    display: flex;
    gap: 8px;
    align-items: flex-start;
  }

  .hyd-rule span:first-child { font-size: 16px; flex-shrink: 0; }

  /* ── CLOTHING ── */
  .clothing-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 14px;
    margin-bottom: 56px;
  }

  .cloth-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 18px;
    text-align: center;
  }

  .cloth-icon { font-size: 2rem; margin-bottom: 8px; }

  .cloth-card h3 {
    font-size: 0.9rem;
    font-weight: 600;
    margin-bottom: 6px;
  }

  .cloth-card p {
    font-size: 0.78rem;
    color: var(--muted);
    line-height: 1.55;
  }

  .cloth-status {
    display: inline-block;
    font-family: 'DM Mono', monospace;
    font-size: 9px;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    padding: 2px 8px;
    border-radius: 3px;
    margin-top: 8px;
  }

  .status-ok { background: var(--green-light); color: var(--sage); }
  .status-warn { background: var(--red-light); color: var(--accent); }
  .status-caution { background: var(--amber-light); color: #a07010; }

  /* ── MENTAL HEALTH ── */
  .mental-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 16px;
    margin-bottom: 56px;
  }

  /* ── FOOTER ── */
  .footer {
    background: var(--ink);
    color: rgba(244,240,232,0.5);
    text-align: center;
    padding: 40px 24px;
    font-size: 0.82rem;
    font-family: 'DM Mono', monospace;
    letter-spacing: 0.05em;
  }

  .footer strong { color: var(--gold); }

  /* ── ANIMATIONS ── */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(18px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  @keyframes pulse {
    0%, 100% { box-shadow: 0 0 0 0 rgba(212,149,42,0.4); }
    50%       { box-shadow: 0 0 0 8px rgba(212,149,42,0); }
  }

  /* ── SECTION SEPARATOR ── */
  .section-sep {
    height: 1px;
    background: linear-gradient(to right, transparent, var(--border), transparent);
    margin: 10px 0 50px;
  }

  /* responsive */
  @media(max-width: 600px) {
    .hero { padding: 50px 20px 40px; }
    .visual-plate { grid-template-columns: 1fr; }
    .ex-phases { grid-template-columns: 1fr 1fr; }
    .container { padding: 40px 16px; }
  }
</style>
</head>
<body>

<!-- ═══════════════ HERO ═══════════════ -->
<section class="hero">
  <svg class="hero-bg-circles" viewBox="0 0 1200 320" preserveAspectRatio="xMidYMid slice">
    <circle cx="600" cy="160" r="250"/>
    <circle cx="600" cy="160" r="180"/>
    <circle cx="600" cy="160" r="110"/>
    <circle cx="600" cy="160" r="50"/>
    <circle cx="100" cy="80"  r="120"/>
    <circle cx="1100" cy="240" r="140"/>
  </svg>

  <div class="hero-badge">Post-Transplant Recovery Guide · SCT Day +100</div>
  <h1>Your <em>New Life</em> Roadmap —<br>After Stem Cell Transplant</h1>
  <p class="hero-sub">A comprehensive guide covering nutrition, hydration, exercise, clothing, sleep, minerals, and mental wellness for life beyond Day +100</p>

  <div class="day-counter">
    <div class="day-num">+100</div>
    <div class="day-label">Days Post<br>Transplant<br><strong style="color:rgba(212,149,42,0.8)">Your journey starts now</strong></div>
  </div>
</section>

<!-- ═══════════════ TIMELINE STRIP ═══════════════ -->
<section class="timeline-strip">
  <div class="timeline-inner">
    <div class="t-phase">
      <div class="t-dot done">✓</div>
      <div class="t-label done">Day 0<br>Transplant</div>
    </div>
    <div class="t-phase">
      <div class="t-dot done">✓</div>
      <div class="t-label done">Day +30<br>Engraftment</div>
    </div>
    <div class="t-phase">
      <div class="t-dot done">✓</div>
      <div class="t-label done">Day +60<br>Early Recovery</div>
    </div>
    <div class="t-phase">
      <div class="t-dot active">★</div>
      <div class="t-label active">Day +100<br>YOU ARE HERE</div>
    </div>
    <div class="t-phase">
      <div class="t-dot future">◯</div>
      <div class="t-label">Day +180<br>6-Month Check</div>
    </div>
    <div class="t-phase">
      <div class="t-dot future">◯</div>
      <div class="t-label">Year 1<br>Milestone</div>
    </div>
    <div class="t-phase">
      <div class="t-dot future">◯</div>
      <div class="t-label">Year 2+<br>Full Life</div>
    </div>
  </div>
</section>

<!-- ═══════════════ MAIN CONTENT ═══════════════ -->
<main class="container">

  <!-- ── WARNING ── -->
  <div class="warning-box">
    <div class="warning-icon">⚕️</div>
    <div>
      <h3>Always Consult Your Transplant Team First</h3>
      <p>This guide is educational and general in nature. Every SCT patient's recovery is unique. All decisions about diet, exercise, medications, and activities must be approved by your hematologist and transplant coordinator. Do not make major changes without medical supervision.</p>
    </div>
  </div>

  <!-- ════════════ 1. NUTRITION ════════════ -->
  <div class="section-head">
    <div class="section-icon" style="background:#e8f4ec">🥗</div>
    <div>
      <h2>Nutrition & Food</h2>
      <div style="font-size:0.8rem; color:var(--muted); font-family:'DM Mono',monospace;">Building your immune army through food</div>
    </div>
    <span class="mono-tag">Section 01</span>
  </div>

  <!-- Plate visual -->
  <div class="visual-plate">
    <div>
      <svg viewBox="0 0 320 320" width="100%" max-width="300">
        <!-- Plate outer ring -->
        <circle cx="160" cy="160" r="148" fill="#e8e2d8" stroke="#c8bfb0" stroke-width="2"/>
        <circle cx="160" cy="160" r="138" fill="white"/>

        <!-- Segments -->
        <!-- Protein 30% -->
        <path d="M160,160 L160,22 A138,138,0,0,1,289,231 Z" fill="#4a7c59" opacity="0.85"/>
        <!-- Vegetables 35% -->
        <path d="M160,160 L289,231 A138,138,0,0,1,72,285 Z" fill="#6aab80" opacity="0.85"/>
        <!-- Complex Carbs 25% -->
        <path d="M160,160 L72,285 A138,138,0,0,1,38,78 Z" fill="#d4952a" opacity="0.85"/>
        <!-- Healthy Fats 10% -->
        <path d="M160,160 L38,78 A138,138,0,0,1,160,22 Z" fill="#2e6b8a" opacity="0.85"/>

        <!-- Inner white circle -->
        <circle cx="160" cy="160" r="52" fill="white" stroke="#e8e2d8" stroke-width="2"/>
        <text x="160" y="154" text-anchor="middle" font-family="DM Serif Display,serif" font-size="15" fill="#1a1410">Post-SCT</text>
        <text x="160" y="172" text-anchor="middle" font-family="DM Serif Display,serif" font-size="15" fill="#1a1410">Plate</text>

        <!-- Labels -->
        <text x="220" y="100" text-anchor="middle" font-family="Instrument Sans,sans-serif" font-size="11" fill="white" font-weight="600">Protein</text>
        <text x="220" y="112" text-anchor="middle" font-family="Instrument Sans,sans-serif" font-size="10" fill="rgba(255,255,255,0.8)">30%</text>

        <text x="200" y="248" text-anchor="middle" font-family="Instrument Sans,sans-serif" font-size="11" fill="white" font-weight="600">Vegetables</text>
        <text x="200" y="260" text-anchor="middle" font-family="Instrument Sans,sans-serif" font-size="10" fill="rgba(255,255,255,0.8)">35%</text>

        <text x="72" y="200" text-anchor="middle" font-family="Instrument Sans,sans-serif" font-size="11" fill="white" font-weight="600">Carbs</text>
        <text x="72" y="212" text-anchor="middle" font-family="Instrument Sans,sans-serif" font-size="10" fill="rgba(255,255,255,0.8)">25%</text>

        <text x="82" y="108" text-anchor="middle" font-family="Instrument Sans,sans-serif" font-size="11" fill="white" font-weight="600">Fats</text>
        <text x="82" y="120" text-anchor="middle" font-family="Instrument Sans,sans-serif" font-size="10" fill="rgba(255,255,255,0.8)">10%</text>
      </svg>
    </div>

    <div class="plate-labels">
      <h3>The Post-SCT Plate Method</h3>
      <p style="font-size:0.84rem; color:var(--muted); margin-bottom:16px">Designed to rebuild immunity, prevent infection, maintain muscle, and support gut health after your immune system reset.</p>

      <ul class="plate-legend">
        <li>
          <div class="legend-dot" style="background:#4a7c59"></div>
          <div>
            <strong style="font-size:0.86rem">Lean Protein</strong><br>
            <span style="font-size:0.78rem; color:var(--muted)">Cooked chicken, eggs, fish, tofu (well-cooked)</span>
          </div>
          <span class="legend-pct">30%</span>
        </li>
        <li>
          <div class="legend-dot" style="background:#6aab80"></div>
          <div>
            <strong style="font-size:0.86rem">Cooked Vegetables</strong><br>
            <span style="font-size:0.78rem; color:var(--muted)">Steamed/boiled; no raw salads initially</span>
          </div>
          <span class="legend-pct">35%</span>
        </li>
        <li>
          <div class="legend-dot" style="background:#d4952a"></div>
          <div>
            <strong style="font-size:0.86rem">Complex Carbohydrates</strong><br>
            <span style="font-size:0.78rem; color:var(--muted)">Brown rice, cooked oats, sweet potato</span>
          </div>
          <span class="legend-pct">25%</span>
        </li>
        <li>
          <div class="legend-dot" style="background:#2e6b8a"></div>
          <div>
            <strong style="font-size:0.86rem">Healthy Fats</strong><br>
            <span style="font-size:0.78rem; color:var(--muted)">Olive oil, avocado, nuts (if approved)</span>
          </div>
          <span class="legend-pct">10%</span>
        </li>
      </ul>
    </div>
  </div>

  <!-- Food DO/DON'T -->
  <div class="cards-2">
    <div class="card">
      <div class="card-accent" style="background:var(--sage)"></div>
      <div class="tag green">✓ EAT Freely</div>
      <h3>✅ Safe Foods (Day +100)</h3>
      <ul>
        <li>Well-cooked meats, poultry, fish (no raw/rare)</li>
        <li>Pasteurized dairy — yogurt with live cultures (ask team)</li>
        <li>Steamed/boiled vegetables — carrots, broccoli, zucchini</li>
        <li>Cooked eggs — well-done, not runny</li>
        <li>Brown rice, cooked oatmeal, bread, pasta</li>
        <li>Peeled fruit — bananas, cooked/canned fruits</li>
        <li>Olive oil, coconut oil for cooking</li>
        <li>Herbal teas (no licorice root, grapefruit)</li>
        <li>Soups — homemade, well-heated</li>
        <li>Legumes — lentils, well-cooked beans</li>
      </ul>
    </div>
    <div class="card">
      <div class="card-accent" style="background:var(--accent)"></div>
      <div class="tag red">✗ AVOID</div>
      <h3>🚫 Foods to Avoid</h3>
      <ul>
        <li>Raw fish, sushi, sashimi, ceviche</li>
        <li>Raw sprouts — alfalfa, bean, radish</li>
        <li>Unpasteurized milk, cheese, juices</li>
        <li>Deli meats / cold cuts (unless heated to steaming)</li>
        <li>Raw eggs, soft-boiled eggs, runny yolks</li>
        <li>Buffet/restaurant food left out > 2 hours</li>
        <li>Raw honey (risk of Clostridium)</li>
        <li>Grapefruit (interacts with many meds)</li>
        <li>Unwashed raw produce / raw salads</li>
        <li>Moldy cheeses — blue cheese, brie, camembert</li>
      </ul>
    </div>
  </div>

  <!-- ════════════ 2. MINERALS & VITAMINS ════════════ -->
  <div class="section-sep"></div>
  <div class="section-head">
    <div class="section-icon" style="background:#fdf3e3">💊</div>
    <div>
      <h2>Minerals, Vitamins & Supplements</h2>
      <div style="font-size:0.8rem; color:var(--muted); font-family:'DM Mono',monospace;">What your new immune system needs to rebuild</div>
    </div>
    <span class="mono-tag">Section 02</span>
  </div>

  <div class="mineral-grid">
    <div class="mineral-card">
      <div class="mineral-icon" style="background:#e8f4ec; color:var(--sage)">🦴</div>
      <div>
        <div class="mineral-name">Calcium</div>
        <div class="mineral-dose">1000–1200 mg/day</div>
        <div class="mineral-note">Critical — steroids deplete bone density. Dairy, fortified plant milk, broccoli, almonds.</div>
      </div>
    </div>

    <div class="mineral-card">
      <div class="mineral-icon" style="background:#fdf3e3; color:#a07010">☀️</div>
      <div>
        <div class="mineral-name">Vitamin D3</div>
        <div class="mineral-dose">1000–2000 IU/day</div>
        <div class="mineral-note">Pairs with calcium, immune modulator. Often deficient post-transplant. Supplement with doctor approval.</div>
      </div>
    </div>

    <div class="mineral-card">
      <div class="mineral-icon" style="background:#fdeee9; color:var(--accent)">🩸</div>
      <div>
        <div class="mineral-name">Iron</div>
        <div class="mineral-dose">Monitor via labs</div>
        <div class="mineral-note">Can be too high post-transfusions. Do NOT supplement without bloodwork. Red meat, lentils if low.</div>
      </div>
    </div>

    <div class="mineral-card">
      <div class="mineral-icon" style="background:#e8f0f7; color:var(--sky)">⚡</div>
      <div>
        <div class="mineral-name">Magnesium</div>
        <div class="mineral-dose">200–400 mg/day</div>
        <div class="mineral-note">Often low post-SCT (cyclosporine depletes it). Helps fatigue, muscle cramps, sleep. Nuts, seeds, leafy greens.</div>
      </div>
    </div>

    <div class="mineral-card">
      <div class="mineral-icon" style="background:#f0ecf7; color:var(--lavender)">🧬</div>
      <div>
        <div class="mineral-name">Zinc</div>
        <div class="mineral-dose">8–11 mg/day</div>
        <div class="mineral-note">Immune cell development, wound healing. Meat, shellfish (cooked), pumpkin seeds, chickpeas.</div>
      </div>
    </div>

    <div class="mineral-card">
      <div class="mineral-icon" style="background:#e8f4ec; color:var(--sage)">🍋</div>
      <div>
        <div class="mineral-name">Vitamin C</div>
        <div class="mineral-dose">75–200 mg/day</div>
        <div class="mineral-note">Antioxidant, iron absorption, immune support. Cooked bell peppers, potatoes, citrus (check interactions).</div>
      </div>
    </div>

    <div class="mineral-card">
      <div class="mineral-icon" style="background:#fdf3e3; color:#a07010">🥩</div>
      <div>
        <div class="mineral-name">Vitamin B12</div>
        <div class="mineral-dose">2.4 mcg/day+</div>
        <div class="mineral-note">Nerve health, red blood cell production. Meat, fish, dairy, eggs. Supplement if on methotrexate.</div>
      </div>
    </div>

    <div class="mineral-card">
      <div class="mineral-icon" style="background:#e8f0f7; color:var(--sky)">🧂</div>
      <div>
        <div class="mineral-name">Potassium</div>
        <div class="mineral-dose">Per lab values</div>
        <div class="mineral-note">Monitor closely — can be high or low. Bananas, cooked potato, avocado. Follow transplant team labs.</div>
      </div>
    </div>

    <div class="mineral-card">
      <div class="mineral-icon" style="background:#fdeee9; color:var(--accent)">🫀</div>
      <div>
        <div class="mineral-name">Folate (B9)</div>
        <div class="mineral-dose">400 mcg/day</div>
        <div class="mineral-note">Cell renewal, DNA repair. Lentils, cooked spinach, asparagus, fortified grains.</div>
      </div>
    </div>

    <div class="mineral-card">
      <div class="mineral-icon" style="background:#f0ecf7; color:var(--lavender)">🐟</div>
      <div>
        <div class="mineral-name">Omega-3 (EPA/DHA)</div>
        <div class="mineral-dose">1–2 g/day (ask team)</div>
        <div class="mineral-note">Anti-inflammatory, heart health, brain function. Cooked salmon, sardines, flaxseed. Ask about supplements.</div>
      </div>
    </div>

    <div class="mineral-card">
      <div class="mineral-icon" style="background:#e8f4ec; color:var(--sage)">🦠</div>
      <div>
        <div class="mineral-name">Probiotics</div>
        <div class="mineral-dose">Consult doctor</div>
        <div class="mineral-note">Gut microbiome rebuilding. Some centers approve pasteurized yogurt. Live culture supplements require team sign-off.</div>
      </div>
    </div>

    <div class="mineral-card">
      <div class="mineral-icon" style="background:#fdf3e3; color:#a07010">🧠</div>
      <div>
        <div class="mineral-name">Selenium</div>
        <div class="mineral-dose">55 mcg/day</div>
        <div class="mineral-note">Thyroid function, antioxidant defense. Brazil nuts (1–2/day), tuna, eggs, sunflower seeds.</div>
      </div>
    </div>
  </div>

  <div class="warning-box">
    <div class="warning-icon">⚠️</div>
    <div>
      <h3>Supplement Safety Post-SCT</h3>
      <ul>
        <li>Never take herbal supplements without medical clearance — many interact with immunosuppressants</li>
        <li>Avoid high-dose antioxidants (Vit E &gt;400 IU, Vit C &gt;500 mg) unless prescribed</li>
        <li>St John's Wort, echinacea, and turmeric supplements are generally contraindicated</li>
        <li>Always take supplements at least 2 hours away from cyclosporine/tacrolimus</li>
      </ul>
    </div>
  </div>

  <!-- ════════════ 3. HYDRATION ════════════ -->
  <div class="section-sep"></div>
  <div class="section-head">
    <div class="section-icon" style="background:#e8f0f7">💧</div>
    <div>
      <h2>Hydration</h2>
      <div style="font-size:0.8rem; color:var(--muted); font-family:'DM Mono',monospace;">Your kidneys are working extra hard right now</div>
    </div>
    <span class="mono-tag">Section 03</span>
  </div>

  <div class="hydration-bar">
    <h3 style="font-family:'DM Serif Display',serif; font-size:1.2rem; margin-bottom:6px">Daily Water Target: 8–10 Glasses</h3>
    <p style="font-size:0.84rem; color:var(--muted); margin-bottom:14px">Approximately 2–2.5 litres per day to flush medications, protect kidneys, and support circulation.</p>

    <div class="water-glasses">
      <!-- 8 filled + 2 lighter (target) -->
      <svg class="glass glass-filled" viewBox="0 0 44 58"><rect x="6" y="2" width="32" height="54" rx="4" fill="#dbeeff" stroke="#2e6b8a" stroke-width="1.5"/><rect class="fill" x="8" y="14" width="28" height="40" rx="3" fill="#2e6b8a" opacity="0.7"/><text x="22" y="44" text-anchor="middle" font-size="14" fill="white">💧</text></svg>
      <svg class="glass glass-filled" viewBox="0 0 44 58"><rect x="6" y="2" width="32" height="54" rx="4" fill="#dbeeff" stroke="#2e6b8a" stroke-width="1.5"/><rect class="fill" x="8" y="14" width="28" height="40" rx="3" fill="#2e6b8a" opacity="0.7"/><text x="22" y="44" text-anchor="middle" font-size="14" fill="white">💧</text></svg>
      <svg class="glass glass-filled" viewBox="0 0 44 58"><rect x="6" y="2" width="32" height="54" rx="4" fill="#dbeeff" stroke="#2e6b8a" stroke-width="1.5"/><rect class="fill" x="8" y="14" width="28" height="40" rx="3" fill="#2e6b8a" opacity="0.7"/><text x="22" y="44" text-anchor="middle" font-size="14" fill="white">💧</text></svg>
      <svg class="glass glass-filled" viewBox="0 0 44 58"><rect x="6" y="2" width="32" height="54" rx="4" fill="#dbeeff" stroke="#2e6b8a" stroke-width="1.5"/><rect class="fill" x="8" y="14" width="28" height="40" rx="3" fill="#2e6b8a" opacity="0.7"/><text x="22" y="44" text-anchor="middle" font-size="14" fill="white">💧</text></svg>
      <svg class="glass glass-filled" viewBox="0 0 44 58"><rect x="6" y="2" width="32" height="54" rx="4" fill="#dbeeff" stroke="#2e6b8a" stroke-width="1.5"/><rect class="fill" x="8" y="14" width="28" height="40" rx="3" fill="#2e6b8a" opacity="0.7"/><text x="22" y="44" text-anchor="middle" font-size="14" fill="white">💧</text></svg>
      <svg class="glass glass-filled" viewBox="0 0 44 58"><rect x="6" y="2" width="32" height="54" rx="4" fill="#dbeeff" stroke="#2e6b8a" stroke-width="1.5"/><rect class="fill" x="8" y="14" width="28" height="40" rx="3" fill="#2e6b8a" opacity="0.7"/><text x="22" y="44" text-anchor="middle" font-size="14" fill="white">💧</text></svg>
      <svg class="glass glass-filled" viewBox="0 0 44 58"><rect x="6" y="2" width="32" height="54" rx="4" fill="#dbeeff" stroke="#2e6b8a" stroke-width="1.5"/><rect class="fill" x="8" y="14" width="28" height="40" rx="3" fill="#2e6b8a" opacity="0.7"/><text x="22" y="44" text-anchor="middle" font-size="14" fill="white">💧</text></svg>
      <svg class="glass glass-filled" viewBox="0 0 44 58"><rect x="6" y="2" width="32" height="54" rx="4" fill="#dbeeff" stroke="#2e6b8a" stroke-width="1.5"/><rect class="fill" x="8" y="14" width="28" height="40" rx="3" fill="#2e6b8a" opacity="0.7"/><text x="22" y="44" text-anchor="middle" font-size="14" fill="white">💧</text></svg>
      <svg class="glass glass-empty" viewBox="0 0 44 58"><rect x="6" y="2" width="32" height="54" rx="4" fill="#dbeeff" stroke="#2e6b8a" stroke-width="1.5" stroke-dasharray="4 2"/><rect class="fill" x="8" y="14" width="28" height="40" rx="3" fill="#2e6b8a"/><text x="22" y="44" text-anchor="middle" font-size="14" fill="white" opacity="0.4">+</text></svg>
      <svg class="glass glass-empty" viewBox="0 0 44 58"><rect x="6" y="2" width="32" height="54" rx="4" fill="#dbeeff" stroke="#2e6b8a" stroke-width="1.5" stroke-dasharray="4 2"/><rect class="fill" x="8" y="14" width="28" height="40" rx="3" fill="#2e6b8a"/><text x="22" y="44" text-anchor="middle" font-size="14" fill="white" opacity="0.4">+</text></svg>
    </div>

    <div class="hydration-rules">
      <div class="hyd-rule"><span>🟢</span><span><strong>Drink:</strong> Filtered water, boiled water, herbal teas (chamomile, ginger), diluted 100% juice (pasteurized)</span></div>
      <div class="hyd-rule"><span>🟡</span><span><strong>Limit:</strong> Caffeinated drinks (1 cup max), sports drinks (high sugar), carbonated beverages if GI issues persist</span></div>
      <div class="hyd-rule"><span>🔴</span><span><strong>Avoid:</strong> Alcohol (absolute), unpasteurized fresh juices, well water (unless tested), raw herbal tonics</span></div>
      <div class="hyd-rule"><span>💊</span><span><strong>Medication tip:</strong> Take cyclosporine/tacrolimus with water — NEVER grapefruit juice</span></div>
      <div class="hyd-rule"><span>🌡️</span><span><strong>If sweating/fever:</strong> Increase intake. Electrolyte drinks (Pedialyte-type) may be needed — check with team</span></div>
      <div class="hyd-rule"><span>🔍</span><span><strong>Urine check:</strong> Pale yellow = good. Dark = drink more. Red/brown = call your team immediately</span></div>
    </div>
  </div>

  <!-- ════════════ 4. EXERCISE ════════════ -->
  <div class="section-sep"></div>
  <div class="section-head">
    <div class="section-icon" style="background:#e8f4ec">🏃</div>
    <div>
      <h2>Exercise & Physical Activity</h2>
      <div style="font-size:0.8rem; color:var(--muted); font-family:'DM Mono',monospace;">Rebuild strength — slowly, safely, deliberately</div>
    </div>
    <span class="mono-tag">Section 04</span>
  </div>

  <div class="ex-phases">
    <div class="ex-phase">
      <div class="ex-phase-num">01</div>
      <div class="ex-phase-range">Day +100 to +120</div>
      <h3>Gentle Mobilization</h3>
      <ul>
        <li>5–10 min walks indoors</li>
        <li>Gentle stretching in bed/chair</li>
        <li>Deep breathing exercises</li>
        <li>Seated leg raises</li>
        <li>1–2 sessions per day</li>
      </ul>
    </div>

    <div class="ex-phase active-phase">
      <div class="ex-phase-num" style="color:rgba(212,149,42,0.3)">02</div>
      <div class="ex-phase-range">Day +120 to +180</div>
      <h3>Light Aerobic <span style="font-family:'DM Mono',monospace; font-size:9px; color:var(--gold); letter-spacing:0.1em">YOU ARE HERE</span></h3>
      <ul>
        <li>15–20 min walks outdoors (low crowd)</li>
        <li>Stationary cycling (low resistance)</li>
        <li>Yoga (gentle, no hot yoga)</li>
        <li>Light resistance bands</li>
        <li>3–4 days per week</li>
      </ul>
    </div>

    <div class="ex-phase">
      <div class="ex-phase-num">03</div>
      <div class="ex-phase-range">Month 6–9</div>
      <h3>Building Endurance</h3>
      <ul>
        <li>30–45 min walks or cycling</li>
        <li>Swimming (when cleared)</li>
        <li>Light weight training</li>
        <li>Pilates, tai chi</li>
        <li>4–5 days per week</li>
      </ul>
    </div>

    <div class="ex-phase">
      <div class="ex-phase-num">04</div>
      <div class="ex-phase-range">Month 9–12</div>
      <h3>Progressive Fitness</h3>
      <ul>
        <li>Jogging intervals</li>
        <li>Moderate weight training</li>
        <li>Group fitness (if immune OK)</li>
        <li>Sport activities (low-contact)</li>
        <li>5 days per week</li>
      </ul>
    </div>

    <div class="ex-phase">
      <div class="ex-phase-num">05</div>
      <div class="ex-phase-range">Year 2+</div>
      <h3>Full Activity</h3>
      <ul>
        <li>All activities (team-cleared)</li>
        <li>Running, cycling, hiking</li>
        <li>Team sports</li>
        <li>Gym programs</li>
        <li>Standard fitness goals</li>
      </ul>
    </div>
  </div>

  <div class="cards-3">
    <div class="card">
      <div class="card-accent" style="background:var(--accent)"></div>
      <div class="tag red">Stop Immediately If:</div>
      <h3>⛔ Exercise Warning Signs</h3>
      <ul>
        <li>Chest pain or palpitations</li>
        <li>Sudden shortness of breath</li>
        <li>Dizziness or near-fainting</li>
        <li>Temperature above 38°C / 100.4°F</li>
        <li>Platelet count below 50,000/μL</li>
        <li>Severe fatigue / muscle weakness</li>
      </ul>
    </div>
    <div class="card">
      <div class="card-accent" style="background:var(--gold)"></div>
      <div class="tag amber">Avoid Until Cleared:</div>
      <h3>🚫 Sports Restrictions</h3>
      <ul>
        <li>Contact sports (basketball, football)</li>
        <li>Water activities until approved (infection)</li>
        <li>Heavy weightlifting (platelet risk)</li>
        <li>Crowded gyms (infection risk)</li>
        <li>High-altitude or extreme heat</li>
        <li>Competitive, high-intensity sport</li>
      </ul>
    </div>
    <div class="card">
      <div class="card-accent" style="background:var(--sage)"></div>
      <div class="tag green">Always Safe:</div>
      <h3>✅ Best Early Activities</h3>
      <ul>
        <li>Walking in quiet parks</li>
        <li>Gentle yoga & stretching</li>
        <li>Breathing exercises (diaphragmatic)</li>
        <li>Chair-based exercises</li>
        <li>Light gardening (wear gloves)</li>
        <li>Balance training</li>
      </ul>
    </div>
  </div>

  <!-- ════════════ 5. CLOTHING ════════════ -->
  <div class="section-sep"></div>
  <div class="section-head">
    <div class="section-icon" style="background:#f0ecf7">👔</div>
    <div>
      <h2>What to Wear</h2>
      <div style="font-size:0.8rem; color:var(--muted); font-family:'DM Mono',monospace;">Protecting your skin and reducing infection risk</div>
    </div>
    <span class="mono-tag">Section 05</span>
  </div>

  <div class="clothing-grid">
    <div class="cloth-card">
      <div class="cloth-icon">👕</div>
      <h3>Fabric Choice</h3>
      <p>100% cotton or bamboo — breathable, hypoallergenic, gentle on sensitive post-transplant skin.</p>
      <div class="cloth-status status-ok">Recommended</div>
    </div>

    <div class="cloth-card">
      <div class="cloth-icon">🧤</div>
      <h3>Garden / Outdoor Gloves</h3>
      <p>Wear gloves when gardening, cleaning, or handling soil. Soil harbors Aspergillus fungus — dangerous to you.</p>
      <div class="cloth-status status-warn">Essential</div>
    </div>

    <div class="cloth-card">
      <div class="cloth-icon">😷</div>
      <h3>Mask (N95/KN95)</h3>
      <p>Wear in crowded indoor spaces, hospitals, public transport. Continue until immune system is fully rebuilt.</p>
      <div class="cloth-status status-warn">Required in crowds</div>
    </div>

    <div class="cloth-card">
      <div class="cloth-icon">🕶️</div>
      <h3>UV Sunglasses</h3>
      <p>Protect eyes from UV — GVHD can affect eyes and immunosuppressants increase sun sensitivity.</p>
      <div class="cloth-status status-ok">Highly Recommended</div>
    </div>

    <div class="cloth-card">
      <div class="cloth-icon">🧴</div>
      <h3>SPF 50+ Sunscreen</h3>
      <p>Immunosuppressants sharply increase skin cancer risk. Apply daily, even on cloudy days. Reapply every 2 hours outdoors.</p>
      <div class="cloth-status status-warn">Daily Essential</div>
    </div>

    <div class="cloth-card">
      <div class="cloth-icon">👟</div>
      <h3>Footwear</h3>
      <p>Wear closed-toe shoes, always. No barefoot outdoors — risk of cuts, soil contact, fungal infection.</p>
      <div class="cloth-status status-caution">Always Wear</div>
    </div>

    <div class="cloth-card">
      <div class="cloth-icon">🧦</div>
      <h3>Compression Socks</h3>
      <p>If swelling (edema) in legs — common on steroids. Discuss appropriate compression level with your care team.</p>
      <div class="cloth-status status-caution">If Swelling Present</div>
    </div>

    <div class="cloth-card">
      <div class="cloth-icon">🧥</div>
      <h3>Layering / Warmth</h3>
      <p>Temperature regulation is harder post-SCT. Dress in layers. Avoid extreme cold or heat — both stress your immune system.</p>
      <div class="cloth-status status-ok">Smart Strategy</div>
    </div>

    <div class="cloth-card">
      <div class="cloth-icon">🚫</div>
      <h3>Avoid: Synthetic & Tight</h3>
      <p>Avoid polyester and nylon — trap sweat, irritate skin. Avoid tight waistbands — blood flow and clot risk on some medications.</p>
      <div class="cloth-status status-warn">Avoid</div>
    </div>
  </div>

  <!-- ════════════ 6. DAILY SCHEDULE ════════════ -->
  <div class="section-sep"></div>
  <div class="section-head">
    <div class="section-icon" style="background:#fdf3e3">🕐</div>
    <div>
      <h2>Model Daily Schedule</h2>
      <div style="font-size:0.8rem; color:var(--muted); font-family:'DM Mono',monospace;">A biology-aligned structure for healing</div>
    </div>
    <span class="mono-tag">Section 06</span>
  </div>

  <div class="schedule">
    <div class="schedule-row">
      <div class="sched-time">06:30</div>
      <div class="sched-dot" style="background:var(--gold)"></div>
      <div class="sched-content">
        <div class="sched-title">Wake & Hydrate</div>
        <div class="sched-detail">500ml warm water. Check temperature. Take morning medications (cyclosporine/tacrolimus) with water only — exact same time daily.</div>
      </div>
    </div>
    <div class="schedule-row">
      <div class="sched-time">07:00</div>
      <div class="sched-dot" style="background:var(--sage)"></div>
      <div class="sched-content">
        <div class="sched-title">Breakfast</div>
        <div class="sched-detail">Cooked oatmeal with pasteurized milk or banana, boiled egg, herbal tea. High-protein, moderate carb. Take supplements if prescribed.</div>
      </div>
    </div>
    <div class="schedule-row">
      <div class="sched-time">08:00</div>
      <div class="sched-dot" style="background:var(--sky)"></div>
      <div class="sched-content">
        <div class="sched-title">Morning Walk / Light Exercise</div>
        <div class="sched-detail">10–20 min outdoor walk (quiet area, wear mask if needed). Low-intensity. Gloves if gardening. SPF sunscreen applied.</div>
      </div>
    </div>
    <div class="schedule-row">
      <div class="sched-time">10:30</div>
      <div class="sched-dot" style="background:var(--sage)"></div>
      <div class="sched-content">
        <div class="sched-title">Mid-Morning Snack</div>
        <div class="sched-detail">Peeled apple or banana, small handful of cooked/roasted nuts, or pasteurized yogurt. Drink water.</div>
      </div>
    </div>
    <div class="schedule-row">
      <div class="sched-time">13:00</div>
      <div class="sched-dot" style="background:var(--sage)"></div>
      <div class="sched-content">
        <div class="sched-title">Lunch</div>
        <div class="sched-detail">Cooked rice or pasta + steamed vegetables + lean protein (chicken breast, fish, tofu). Olive oil dressing. Herbal tea or water.</div>
      </div>
    </div>
    <div class="schedule-row">
      <div class="sched-time">14:00</div>
      <div class="sched-dot" style="background:var(--lavender)"></div>
      <div class="sched-content">
        <div class="sched-title">Rest / Low-Stimulation Recovery</div>
        <div class="sched-detail">Short nap (20–30 min) if fatigued — common at this stage. Meditation, reading, light music. Avoid screens for 30 min.</div>
      </div>
    </div>
    <div class="schedule-row">
      <div class="sched-time">15:30</div>
      <div class="sched-dot" style="background:var(--sky)"></div>
      <div class="sched-content">
        <div class="sched-title">Afternoon Activity</div>
        <div class="sched-detail">Gentle stretching, yoga, breathing exercises, or light resistance bands. 15–20 minutes. Avoid vigorous exercise later in day.</div>
      </div>
    </div>
    <div class="schedule-row">
      <div class="sched-time">16:30</div>
      <div class="sched-dot" style="background:var(--sage)"></div>
      <div class="sched-content">
        <div class="sched-title">Afternoon Snack</div>
        <div class="sched-detail">Whole grain crackers + hummus (commercial, pasteurized), or cooked egg + toast. Continue hydrating.</div>
      </div>
    </div>
    <div class="schedule-row">
      <div class="sched-time">19:00</div>
      <div class="sched-dot" style="background:var(--sage)"></div>
      <div class="sched-content">
        <div class="sched-title">Dinner</div>
        <div class="sched-detail">Warm soup or stew + protein + cooked veg. Easy to digest. Avoid heavy, spicy, or greasy food — GVHD of gut can be triggered.</div>
      </div>
    </div>
    <div class="schedule-row">
      <div class="sched-time">20:00</div>
      <div class="sched-dot" style="background:var(--gold)"></div>
      <div class="sched-content">
        <div class="sched-title">Evening Medications</div>
        <div class="sched-detail">Second cyclosporine/tacrolimus dose (12 hours after morning dose, exact timing). Note any symptoms. Temperature check.</div>
      </div>
    </div>
    <div class="schedule-row">
      <div class="sched-time">21:00</div>
      <div class="sched-dot" style="background:var(--lavender)"></div>
      <div class="sched-content">
        <div class="sched-title">Wind-Down Routine</div>
        <div class="sched-detail">Dim lights. No screens after 21:30. Chamomile tea. Gentle breathing. Journal 3 things you're grateful for — proven to improve sleep quality.</div>
      </div>
    </div>
    <div class="schedule-row">
      <div class="sched-time">22:00</div>
      <div class="sched-dot" style="background:#8b7fa0"></div>
      <div class="sched-content">
        <div class="sched-title">Sleep — Target 8–9 Hours</div>
        <div class="sched-detail">Sleep is when your new immune system does its most critical repair work. Room temperature 18–20°C. Blackout curtains recommended.</div>
      </div>
    </div>
  </div>

  <!-- ════════════ 7. SLEEP ════════════ -->
  <div class="section-sep"></div>
  <div class="section-head">
    <div class="section-icon" style="background:#f0ecf7">🌙</div>
    <div>
      <h2>Sleep Optimization</h2>
      <div style="font-size:0.8rem; color:var(--muted); font-family:'DM Mono',monospace;">Your immune system rebuilds during deep sleep</div>
    </div>
    <span class="mono-tag">Section 07</span>
  </div>

  <div class="cards-3">
    <div class="card">
      <div class="card-accent" style="background:var(--lavender)"></div>
      <div class="tag purple">Target</div>
      <h3>🌙 Sleep Duration</h3>
      <p style="margin-bottom:10px">8–9 hours minimum. Fatigue is normal and expected at Day +100. Naps up to 30 minutes are helpful — do not fight fatigue.</p>
      <ul>
        <li>Same bedtime and wake time every day</li>
        <li>Track sleep with a simple journal</li>
        <li>If insomnia — discuss with team (common)</li>
      </ul>
    </div>
    <div class="card">
      <div class="card-accent" style="background:var(--sky)"></div>
      <div class="tag blue">Environment</div>
      <h3>🛏️ Sleep Environment</h3>
      <ul>
        <li>Clean, dust-free bedroom — HEPA filter if possible</li>
        <li>Cool room: 18–20°C optimal</li>
        <li>Blackout curtains for melatonin production</li>
        <li>No pets in bedroom (infection/allergen risk)</li>
        <li>Fresh laundered sheets weekly</li>
        <li>Humidifier if dry air irritates mucous membranes</li>
      </ul>
    </div>
    <div class="card">
      <div class="card-accent" style="background:var(--sage)"></div>
      <div class="tag green">Habits</div>
      <h3>✅ Sleep Hygiene</h3>
      <ul>
        <li>No screens 1 hour before bed</li>
        <li>No caffeine after 14:00</li>
        <li>Chamomile or lemon balm tea</li>
        <li>Avoid large meals within 2 hrs of sleep</li>
        <li>Evening stretching / breathing</li>
        <li>Keep room quiet or use white noise</li>
      </ul>
    </div>
  </div>

  <!-- ════════════ 8. MENTAL HEALTH ════════════ -->
  <div class="section-sep"></div>
  <div class="section-head">
    <div class="section-icon" style="background:#f0ecf7">🧠</div>
    <div>
      <h2>Mental Health & Emotional Wellbeing</h2>
      <div style="font-size:0.8rem; color:var(--muted); font-family:'DM Mono',monospace;">Your mind is recovering too — give it the same care</div>
    </div>
    <span class="mono-tag">Section 08</span>
  </div>

  <div class="mental-grid">
    <div class="card">
      <div class="card-accent" style="background:var(--lavender)"></div>
      <div class="tag purple">Common Experience</div>
      <h3>🌀 What You May Feel</h3>
      <ul>
        <li>Anxiety about relapse / infections</li>
        <li>Depression or emotional numbness</li>
        <li>"Chemo brain" — cognitive fog</li>
        <li>Grief over lost normalcy</li>
        <li>Steroid-induced mood swings</li>
        <li>Social isolation / loneliness</li>
        <li>Identity shift — "Who am I now?"</li>
      </ul>
      <p style="margin-top:10px; font-size:0.8rem">All of these are <strong>normal and valid</strong>. You are not weak. You survived one of medicine's most intense treatments.</p>
    </div>

    <div class="card">
      <div class="card-accent" style="background:var(--sage)"></div>
      <div class="tag green">Evidence-Based</div>
      <h3>✅ What Helps</h3>
      <ul>
        <li>Professional therapy — oncology psychologist</li>
        <li>Support groups (in-person or online SCT survivors)</li>
        <li>Mindfulness meditation (apps: Insight Timer, Calm)</li>
        <li>Journaling — process emotions safely</li>
        <li>Creative outlets — music, art, writing</li>
        <li>Gentle social connection — small gatherings</li>
        <li>Celebrate small milestones weekly</li>
      </ul>
    </div>

    <div class="card">
      <div class="card-accent" style="background:var(--sky)"></div>
      <div class="tag blue">Daily Practice</div>
      <h3>🧘 Mind-Body Protocol</h3>
      <ul>
        <li>5 min morning breathing (4-7-8 technique)</li>
        <li>Gratitude journaling — 3 entries/day</li>
        <li>1 enjoyable activity per day (non-negotiable)</li>
        <li>Connect with one person you trust daily</li>
        <li>Nature exposure — even 10 min outdoors helps</li>
        <li>Limit news and medical doom-scrolling</li>
      </ul>
    </div>

    <div class="card">
      <div class="card-accent" style="background:var(--accent)"></div>
      <div class="tag red">Seek Help If:</div>
      <h3>⚠️ When to Escalate</h3>
      <ul>
        <li>Persistent hopelessness > 2 weeks</li>
        <li>Inability to perform daily activities</li>
        <li>Appetite gone for more than 3 days</li>
        <li>Thoughts of self-harm</li>
        <li>Severe anxiety / panic attacks</li>
        <li>Complete social withdrawal</li>
      </ul>
      <p style="margin-top:10px; font-size:0.8rem">Tell your transplant team. Mental health is part of your medical care — there is no shame in needing support.</p>
    </div>
  </div>

  <!-- ════════════ 9. INFECTION PREVENTION ════════════ -->
  <div class="section-sep"></div>
  <div class="section-head">
    <div class="section-icon" style="background:#fdeee9">🛡️</div>
    <div>
      <h2>Infection Prevention</h2>
      <div style="font-size:0.8rem; color:var(--muted); font-family:'DM Mono',monospace;">Your immune system is still in infancy — protect it aggressively</div>
    </div>
    <span class="mono-tag">Section 09</span>
  </div>

  <div class="cards-3">
    <div class="card">
      <div class="card-accent" style="background:var(--sage)"></div>
      <div class="tag green">Hand Hygiene</div>
      <h3>🤲 Handwashing Protocol</h3>
      <ul>
        <li>Wash hands 20 seconds with soap — after every toilet use, before every meal, after contact with animals</li>
        <li>Alcohol hand sanitizer (60%+) when soap unavailable</li>
        <li>Avoid touching face, eyes, mouth in public</li>
        <li>Ask visitors to wash hands before contact</li>
      </ul>
    </div>
    <div class="card">
      <div class="card-accent" style="background:var(--gold)"></div>
      <div class="tag amber">Environment</div>
      <h3>🏠 Home Safety</h3>
      <ul>
        <li>No live plants in bedroom (mold risk)</li>
        <li>Change HVAC filters monthly</li>
        <li>No construction dust — stay away from building sites</li>
        <li>No pets sleeping in your bed</li>
        <li>Avoid crowds, sick people, children with colds</li>
        <li>Clean surfaces daily — especially kitchen</li>
      </ul>
    </div>
    <div class="card">
      <div class="card-accent" style="background:var(--accent)"></div>
      <div class="tag red">Emergency Signs</div>
      <h3>🚨 Call Team Immediately</h3>
      <ul>
        <li>Fever ≥ 38°C / 100.4°F</li>
        <li>Chills, rigors, shaking</li>
        <li>New skin rash</li>
        <li>Difficulty breathing</li>
        <li>Severe diarrhea / vomiting</li>
        <li>Bleeding that won't stop</li>
        <li>Severe pain anywhere</li>
      </ul>
    </div>
  </div>

  <!-- ════════════ CHECKLIST ════════════ -->
  <div class="section-sep"></div>
  <div class="section-head">
    <div class="section-icon" style="background:#e8f0f7">📋</div>
    <div>
      <h2>Weekly Health Checklist</h2>
      <div style="font-size:0.8rem; color:var(--muted); font-family:'DM Mono',monospace;">Track your recovery with these weekly markers</div>
    </div>
    <span class="mono-tag">Section 10</span>
  </div>

  <div class="cards-2" style="margin-bottom:20px">
    <div class="card" style="background:var(--green-light); border-color:#b4d9c4">
      <h3 style="margin-bottom:14px">📅 Weekly Essentials</h3>
      <ul>
        <li>Attended all scheduled clinic appointments</li>
        <li>Medications taken at exact same time daily</li>
        <li>Blood pressure and temperature logged daily</li>
        <li>Maintained 8–10 glasses of water per day</li>
        <li>Ate 3 balanced cooked meals daily</li>
        <li>Completed 3+ days of gentle exercise</li>
        <li>8+ hours sleep achieved on 5+ nights</li>
        <li>Wore SPF 50 on all outdoor outings</li>
        <li>No fever episodes this week</li>
        <li>Connected socially with a loved one</li>
      </ul>
    </div>
    <div class="card" style="background:var(--amber-light); border-color:#e8c88a">
      <h3 style="margin-bottom:14px">🔬 Monthly Lab Goals</h3>
      <ul>
        <li>CBC — neutrophils, platelets, hemoglobin stable</li>
        <li>Tacrolimus/cyclosporine levels in therapeutic range</li>
        <li>Kidney function (creatinine) normal</li>
        <li>Liver enzymes (AST/ALT) stable</li>
        <li>Magnesium, potassium, calcium in range</li>
        <li>Vitamin D level above 30 ng/mL</li>
        <li>No evidence of CMV reactivation</li>
        <li>Chimerism study — donor engraftment confirmed</li>
        <li>Skin and mouth GVHD assessment</li>
        <li>Weight stable (within 2–3 kg)</li>
      </ul>
    </div>
  </div>

</main>

<!-- ═══════════════ FOOTER ═══════════════ -->
<footer class="footer">
  <p style="margin-bottom:8px; font-size:1rem; color:rgba(244,240,232,0.9)">You have already done the hardest part.</p>
  <p><strong>Post-SCT Recovery Roadmap · Day +100 and Beyond</strong></p>
  <p style="margin-top:8px">This guide is for educational reference only · Always follow your transplant team's specific instructions · Every recovery is unique</p>
  <p style="margin-top:16px; font-size:10px; letter-spacing:0.08em">PRODUCED WITH CARE · NOT A SUBSTITUTE FOR MEDICAL ADVICE · CONSULT YOUR HEMATOLOGIST</p>
</footer>

</body>
</html>
