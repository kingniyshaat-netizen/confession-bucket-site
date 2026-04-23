# confession-bucket-site<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Confession Bucket | Public Launch Version 2</title>
  <meta name="description" content="Confession Bucket is a healing-centered digital sanctuary for truth, ritual, empathy, and legacy." />
  <style>
    :root{
      --bg:#090807;--bg2:#110e0d;--panel:#171210;--panel2:#201915;--line:rgba(255,255,255,.10);
      --text:#f7f0e8;--muted:#c9bbab;--soft:#9f8f7d;--ember:#ffb15c;--ember2:#ff7a18;--gold:#e3b163;--gold2:#f1cf9a;
      --radius:24px;--shadow:0 18px 44px rgba(0,0,0,.35);--max:1240px;
    }
    *{box-sizing:border-box} html{scroll-behavior:smooth}
    body{
      margin:0;font-family:Inter,ui-sans-serif,system-ui,-apple-system,Segoe UI,Roboto,Arial,sans-serif;color:var(--text);
      background:
        radial-gradient(900px 460px at 10% 0%, rgba(255,122,24,.18), transparent 45%),
        radial-gradient(900px 460px at 100% 12%, rgba(227,177,99,.12), transparent 48%),
        linear-gradient(180deg,#0a0807 0%,#0c0a09 32%,#090807 100%);
      line-height:1.55;
    }
    a{text-decoration:none;color:inherit}.wrap{max-width:var(--max);margin:0 auto;padding:0 20px}
    .topbar{position:sticky;top:0;z-index:50;backdrop-filter:blur(18px);background:rgba(9,8,7,.84);border-bottom:1px solid var(--line)}
    .nav{min-height:76px;display:flex;align-items:center;justify-content:space-between;gap:16px}
    .brand{display:flex;align-items:center;gap:14px}
    .mark{width:50px;height:50px;border-radius:17px;display:grid;place-items:center;background:linear-gradient(145deg,var(--gold),var(--ember2));color:#2c1708;font-size:24px;font-weight:900;box-shadow:0 10px 26px rgba(255,122,24,.24)}
    .brand p{margin:0;color:var(--soft);font-size:.82rem;letter-spacing:.14em;text-transform:uppercase}.brand h1{margin:3px 0 0;font-size:1rem;line-height:1.1}
    .navlinks{display:flex;gap:18px;flex-wrap:wrap}.navlinks a{color:var(--muted);font-size:.95rem}.navlinks a:hover{color:#fff}
    .cta-row{display:flex;gap:10px;flex-wrap:wrap}
    .btn{display:inline-flex;align-items:center;justify-content:center;gap:10px;min-height:46px;padding:0 18px;border-radius:999px;border:1px solid var(--line);background:rgba(255,255,255,.03);color:var(--text);font-weight:800;cursor:pointer;transition:.2s ease}
    .btn:hover{transform:translateY(-1px);background:rgba(255,255,255,.07)}
    .btn.primary{background:linear-gradient(135deg,var(--gold),var(--ember));color:#2d1707;border:none;box-shadow:0 12px 28px rgba(255,122,24,.20)}
    .hero{padding:84px 0 50px;border-bottom:1px solid var(--line)} .hero-grid{display:grid;grid-template-columns:1.15fr .85fr;gap:28px;align-items:center}
    .eyebrow{display:inline-flex;align-items:center;gap:10px;padding:10px 14px;border-radius:999px;border:1px solid rgba(227,177,99,.25);background:rgba(227,177,99,.08);color:var(--gold2);font-size:.88rem;font-weight:800;margin-bottom:18px}
    .hero-title{margin:0;font-size:clamp(2.8rem,5vw,5.3rem);line-height:.96;letter-spacing:-.05em}.accent{color:#ffd8ac}
    .hero-copy{font-size:1.08rem;color:var(--muted);max-width:760px;margin:18px 0 24px}
    .quote-band{margin-top:18px;padding:16px 18px;border-radius:18px;border:1px solid rgba(227,177,99,.16);background:rgba(227,177,99,.06);color:#ecd6b2;font-size:.98rem}
    .panel{background:linear-gradient(180deg, rgba(255,255,255,.035), rgba(255,255,255,.02));border:1px solid var(--line);border-radius:var(--radius);box-shadow:var(--shadow)}
    .hero-card{padding:20px}.windowbar{display:flex;justify-content:space-between;align-items:center;color:var(--soft);font-size:.82rem;margin-bottom:16px}
    .dots{display:flex;gap:8px}.dot{width:11px;height:11px;border-radius:999px}.red{background:#f87171}.yellow{background:#fbbf24}.green{background:#4ade80}
    .hero-list{display:grid;gap:12px}.hero-item{padding:14px 16px;border-radius:18px;background:rgba(255,255,255,.03);border:1px solid var(--line)} .hero-item strong{display:block;margin-bottom:4px}
    .hero-stats{display:grid;grid-template-columns:repeat(2,1fr);gap:12px;margin-top:14px}.mini-stat{padding:15px;border-radius:18px;background:rgba(255,255,255,.03);border:1px solid var(--line)}
    .mini-stat .l{font-size:.78rem;color:var(--soft);letter-spacing:.14em;text-transform:uppercase}.mini-stat .v{font-size:1.45rem;font-weight:900;margin-top:5px}
    .section{padding:78px 0}.section-head{max-width:880px;margin-bottom:30px}
    .kicker{display:inline-block;padding:7px 12px;border-radius:999px;background:rgba(255,255,255,.04);border:1px solid var(--line);color:#ebcc9f;font-size:.8rem;letter-spacing:.15em;text-transform:uppercase;font-weight:900;margin-bottom:16px}
    .section h2{margin:0 0 12px;font-size:clamp(2rem,4vw,3.5rem);line-height:1.04;letter-spacing:-.03em}.lead{margin:0;color:var(--muted);font-size:1.04rem;max-width:860px}
    .grid-2{display:grid;grid-template-columns:repeat(2,1fr);gap:18px}.grid-3{display:grid;grid-template-columns:repeat(3,1fr);gap:18px}
    .card{padding:22px}.icon{width:48px;height:48px;border-radius:16px;display:grid;place-items:center;background:rgba(255,177,92,.12);border:1px solid rgba(255,177,92,.15);color:#ffd29f;font-size:1.2rem;margin-bottom:14px}
    h3{margin:0 0 8px;font-size:1.12rem} p{margin:0}.muted{color:var(--muted)}.subtle{color:var(--soft)}
    .pillars{display:grid;grid-template-columns:repeat(4,1fr);gap:14px}.pillar{padding:18px;border-radius:18px;background:rgba(255,255,255,.03);border:1px solid var(--line)}
    .journey{display:grid;grid-template-columns:repeat(5,1fr);gap:12px;margin-top:18px}.step{padding:18px;border-radius:18px;background:rgba(255,255,255,.03);border:1px solid var(--line)}
    .step .n{font-size:.78rem;letter-spacing:.18em;text-transform:uppercase;color:#f0c78d;margin-bottom:8px}
    .score-box{padding:18px;border-radius:22px;background:linear-gradient(135deg, rgba(255,177,92,.12), rgba(255,122,24,.10));border:1px solid rgba(255,177,92,.14)}
    .score-row{margin:13px 0}.bar{height:10px;border-radius:999px;background:rgba(255,255,255,.08);overflow:hidden}.fill{height:100%;background:linear-gradient(90deg,var(--gold),var(--ember2));border-radius:999px}
    .badge-row{display:grid;grid-template-columns:repeat(5,1fr);gap:12px}.badge{padding:16px;border-radius:18px;background:rgba(255,255,255,.03);border:1px solid var(--line);text-align:center}
    .chip{display:inline-flex;padding:6px 12px;border-radius:999px;margin-top:10px;font-size:.74rem;font-weight:900;background:rgba(227,177,99,.12);color:#ffd29f;border:1px solid rgba(227,177,99,.18)}
    .feature-band{display:grid;grid-template-columns:1.1fr .9fr;gap:18px}.founder{padding:22px;border-radius:24px;background:linear-gradient(180deg, rgba(255,255,255,.05), rgba(255,255,255,.025));border:1px solid var(--line)}
    .tabs{display:flex;gap:10px;flex-wrap:wrap;margin:18px 0 24px}.tabbtn{border:none;border-radius:999px;padding:11px 15px;font-weight:900;cursor:pointer;background:rgba(255,255,255,.05);color:var(--muted);border:1px solid var(--line)}
    .tabbtn.active{background:linear-gradient(135deg,var(--gold),var(--ember));color:#2a1608}.tabpane{display:none}.tabpane.active{display:block}
    .table-wrap{overflow:auto;border-radius:22px;border:1px solid var(--line)} table{width:100%;border-collapse:collapse;min-width:720px;background:rgba(255,255,255,.02)}
    th,td{padding:16px 14px;border-bottom:1px solid var(--line);text-align:left;vertical-align:top} th{font-size:.82rem;letter-spacing:.14em;text-transform:uppercase;color:var(--soft);background:rgba(255,255,255,.03)} td{color:var(--muted)} tr:last-child td{border-bottom:none}
    .faq-item{border:1px solid var(--line);border-radius:18px;background:rgba(255,255,255,.03);overflow:hidden}.faq-q{width:100%;text-align:left;border:none;background:transparent;color:var(--text);padding:18px;font-size:1rem;font-weight:900;cursor:pointer}.faq-a{display:none;padding:0 18px 18px;color:var(--muted)} .faq-item.open .faq-a{display:block}
    .note{padding:16px 18px;border-radius:18px;border:1px solid rgba(255,177,92,.16);background:rgba(255,177,92,.06);color:#ecd6b2}
    .footer{padding:36px 0 56px;border-top:1px solid var(--line);color:var(--soft)} .footer-grid{display:flex;justify-content:space-between;gap:22px;align-items:flex-start;flex-wrap:wrap} .small{font-size:.92rem}
    @media (max-width:1080px){.hero-grid,.grid-3,.pillars,.badge-row,.feature-band{grid-template-columns:1fr 1fr}.journey{grid-template-columns:repeat(3,1fr)}}
    @media (max-width:760px){.navlinks{display:none}.hero{padding-top:54px}.hero-grid,.grid-2,.grid-3,.pillars,.badge-row,.feature-band{grid-template-columns:1fr}.journey{grid-template-columns:1fr 1fr}.cta-row{width:100%}.cta-row .btn{width:100%}}
    @media (max-width:520px){.journey{grid-template-columns:1fr}}
  </style>
</head>
<body>
  <header class="topbar">
    <div class="wrap nav">
      <div class="brand"><div class="mark">🔥</div><div><p>Confession Bucket</p><h1>Where Truth Ignites Legacy</h1></div></div>
      <nav class="navlinks"><a href="#platform">Platform</a><a href="#experience">Experience</a><a href="#partners">Partners</a><a href="#launch">Launch</a><a href="#faq">FAQ</a></nav>
      <div class="cta-row"><a class="btn" href="#partners">Partner</a><a class="btn primary" href="#experience">Enter the Experience</a></div>
    </div>
  </header>  <main>
    <section class="hero">
      <div class="wrap hero-grid">
        <div>
          <div class="eyebrow">Public Launch Version 2 • Healing-centered digital sanctuary</div>
          <h2 class="hero-title">Truth deserves more than a comment section.<br><span class="accent">It deserves a place to be witnessed, held, and transformed.</span></h2>
          <p class="hero-copy">Confession Bucket is a ritual-based platform for healing, connection, empathy, and ancestral empowerment. It is built for people who need more than a feed, more than performance, and more than noise. It is built for truth, for reflection, for community resonance, and for legacy.</p>
          <div class="cta-row"><a class="btn primary" href="#platform">See the Platform</a><a class="btn" href="#launch">View Launch Path</a></div>
          <div class="quote-band">“A transformative platform for healing, connection, and ancestral empowerment.”</div>
        </div><div class="panel hero-card">
      <div class="windowbar"><div class="dots"><span class="dot red"></span><span class="dot yellow"></span><span class="dot green"></span></div><div>Public Launch Snapshot</div></div>
      <div class="hero-list">
        <div class="hero-item"><strong>Onboarding Ritual</strong><span class="subtle">Consent, reflection, privacy, and identity before participation.</span></div>
        <div class="hero-item"><strong>Confession Flow</strong><span class="subtle">Truth-sharing with emotional tone, visibility control, and structured care.</span></div>
        <div class="hero-item"><strong>Community Resonance</strong><span class="subtle">Empathy reactions and witnessing designed to support healing, not spectacle.</span></div>
        <div class="hero-item"><strong>Maze Journal</strong><span class="subtle">A modular daily reflection system for depth, continuity, and ritual memory.</span></div>
      </div>
      <div class="hero-stats">
        <div class="mini-stat"><div class="l">Guiding Value</div><div class="v">Truth</div></div>
        <div class="mini-stat"><div class="l">Guiding Value</div><div class="v">Empathy</div></div>
        <div class="mini-stat"><div class="l">Guiding Value</div><div class="v">Ritual</div></div>
        <div class="mini-stat"><div class="l">Guiding Value</div><div class="v">Legacy</div></div>
      </div>
    </div>
  </div>
</section>

<section class="section" id="platform">
  <div class="wrap">
    <div class="section-head">
      <div class="kicker">Platform Story</div>
      <h2>Not another app for attention. A platform for restoration.</h2>
      <p class="lead">Confession Bucket answers a real gap: too many people are visible online and still feel emotionally homeless. The platform replaces performance-driven interaction with guided ritual, confession, resonance, journaling, and legacy-centered progression.</p>
    </div>

    <div class="pillars">
      <div class="pillar"><strong>Truth</strong><br><span class="subtle">Honesty is invited with structure, not exploited for content.</span></div>
      <div class="pillar"><strong>Safety</strong><br><span class="subtle">Privacy, moderation, and consent are built into the experience.</span></div>
      <div class="pillar"><strong>Ritual</strong><br><span class="subtle">Users move through intentional reflection, not random endless scrolling.</span></div>
      <div class="pillar"><strong>Legacy</strong><br><span class="subtle">Growth is measured through meaningful actions, not vanity metrics.</span></div>
    </div>

    <div class="panel card" style="margin-top:18px">
      <div class="kicker">Core Journey</div>
      <div class="journey">
        <div class="step"><div class="n">01</div><strong>Onboarding Ritual</strong><br><span class="subtle">Build trust through consent and reflection.</span></div>
        <div class="step"><div class="n">02</div><strong>Confession</strong><br><span class="subtle">Share truth with emotional and visibility framing.</span></div>
        <div class="step"><div class="n">03</div><strong>Resonance</strong><br><span class="subtle">Receive empathy, witnessing, and support.</span></div>
        <div class="step"><div class="n">04</div><strong>Maze Journal</strong><br><span class="subtle">Deepen meaning through ongoing reflection.</span></div>
        <div class="step"><div class="n">05</div><strong>Legacy Growth</strong><br><span class="subtle">Unlock badges, mentorship, and ritual continuity.</span></div>
      </div>
    </div>
  </div>
</section>

<section class="section" id="experience">
  <div class="wrap">
    <div class="section-head">
      <div class="kicker">Experience Design</div>
      <h2>The platform experience is designed to feel sacred, human, and usable.</h2>
      <p class="lead">Version 2 pushes the public site closer to a real launch face by tightening the narrative, clarifying what the product does, and making the experience sound like a living platform instead of a PDF in church clothes.</p>
    </div>

    <div class="feature-band">
      <div class="panel card">
        <h3>Legacy Score & Badge Logic</h3>
        <p class="muted" style="margin-bottom:14px">Legacy Score rewards vulnerability, empathy reactions, journaling, mentorship, and consistency. The point is not to gamify ego. The point is to reinforce healing behavior with visible meaning.</p>
        <div class="score-box">
          <div class="score-row"><div style="display:flex;justify-content:space-between;margin-bottom:6px"><span>Vulnerability</span><span>Weighted</span></div><div class="bar"><div class="fill" style="width:90%"></div></div></div>
          <div class="score-row"><div style="display:flex;justify-content:space-between;margin-bottom:6px"><span>Empathy Reactions</span><span>Weighted</span></div><div class="bar"><div class="fill" style="width:81%"></div></div></div>
          <div class="score-row"><div style="display:flex;justify-content:space-between;margin-bottom:6px"><span>Maze Journal</span><span>Weighted</span></div><div class="bar"><div class="fill" style="width:73%"></div></div></div>
          <div class="score-row"><div style="display:flex;justify-content:space-between;margin-bottom:6px"><span>Mentorship</span><span>Weighted</span></div><div class="bar"><div class="fill" style="width:66%"></div></div></div>
          <div class="score-row"><div style="display:flex;justify-content:space-between;margin-bottom:6px"><span>Consistency</span><span>Weighted</span></div><div class="bar"><div class="fill" style="width:70%"></div></div></div>
        </div>
      </div>

      <div class="panel card">
        <h3>Badge Framework</h3>
        <div class="badge-row">
          <div class="badge"><strong>Spark</strong><div class="chip">Courage</div></div>
          <div class="badge"><strong>Flamekeeper</strong><div class="chip">Trust</div></div>
          <div class="badge"><strong>Resonant</strong><div class="chip">Empathy</div></div>
          <div class="badge"><strong>Guide</strong><div class="chip">Mentorship</div></div>
          <div class="badge"><strong>Legacy Builder</strong><div class="chip">Impact</div></div>
        </div>
        <p class="subtle" style="margin-top:16px">These badges symbolize movement through healing, service, and sustained transformation. They belong to the culture of the platform, not just the interface.</p>
      </div>
    </div>

    <div class="grid-3" style="margin-top:18px">
      <div class="panel card"><div class="icon">📝</div><h3>Maze Journal</h3><p class="muted">A thematic daily prompt system for deep reflection, ritual continuity, and emotional memory.</p></div>
      <div class="panel card"><div class="icon">🤝</div><h3>Community Resonance</h3><p class="muted">Empathy reactions and supportive witnessing reshape interaction around care, not performance.</p></div>
      <div class="panel card"><div class="icon">🛡️</div><h3>Safety Stewardship</h3><p class="muted">Moderation, privacy control, and support workflows frame the platform with responsibility.</p></div>
    </div>
  </div>
</section>

<section class="section" id="partners">
  <div class="wrap">
    <div class="section-head">
      <div class="kicker">Partnership Path</div>
      <h2>Designed for schools, justice work, healing collectives, and faith-centered youth support.</h2>
      <p class="lead">Confession Bucket is positioned as both a platform and an ecosystem. It is meant to work with organizations committed to healing, reflection, restoration, and generational change.</p>
    </div>

    <div class="tabs">
      <button class="tabbtn active" data-tab="targets">Target Partners</button>
      <button class="tabbtn" data-tab="tactics">Outreach Tactics</button>
      <button class="tabbtn" data-tab="success">Success Metrics</button>
    </div>

    <div id="targets" class="tabpane active">
      <div class="grid-3">
        <div class="panel card"><h3>Urban Schools</h3><p class="muted">Especially those using restorative justice models and seeking culturally grounded student support.</p></div>
        <div class="panel card"><h3>Justice Diversion Programs</h3><p class="muted">Organizations needing alternatives rooted in reflection, healing, and emotional reorientation.</p></div>
        <div class="panel card"><h3>Cultural + Faith Institutions</h3><p class="muted">Black cultural organizations, healing arts spaces, and faith-based youth communities aligned with restoration.</p></div>
      </div>
    </div>

    <div id="tactics" class="tabpane">
      <div class="grid-2">
        <div class="panel card"><h3>Personalized Outreach</h3><p class="muted">One-page overview, case-study framing, pilot invitation, and follow-up cadence at 7 and 14 days.</p></div>
        <div class="panel card"><h3>Warm Introductions</h3><p class="muted">Use advisory council networks, trusted referrals, coffee chats, and site visits to deepen trust.</p></div>
        <div class="panel card"><h3>Webinars</h3><p class="muted">“Healing in the Digital Age” sessions supported by founder voice and cultural-tech positioning.</p></div>
        <div class="panel card"><h3>Pilot Legacy Circles</h3><p class="muted">Co-host healing circles to generate early stories, testimonials, and partnership validation.</p></div>
      </div>
    </div>

    <div id="success" class="tabpane">
      <div class="grid-2">
        <div class="panel card"><h3>Objectives</h3><p class="muted">10 school and justice MOUs, 5 cultural or health centers, and 3 co-hosted healing circles in pilot phase.</p></div>
        <div class="panel card"><h3>Success Measures</h3><p class="muted">Signed MOUs, partner-referred youth engagement, partner satisfaction above 90%, and publishable case studies.</p></div>
      </div>
    </div>
  </div>
</section>

<section class="section" id="launch">
  <div class="wrap">
    <div class="section-head">
      <div class="kicker">Launch Architecture</div>
      <h2>A staged public launch with operational backbone.</h2>
      <p class="lead">The launch model organizes the work from preparation and beta through public release, summit activation, and long-term optimization.</p>
    </div>

    <div class="table-wrap">
      <table>
        <thead><tr><th>Phase</th><th>Timing</th><th>Key Tasks</th><th>Ownership</th></tr></thead>
        <tbody>
          <tr><td><strong>Preparation & Setup</strong></td><td>Weeks 1–3</td><td>Finalize branding, complete API development, configure CRM, recruit and train volunteers, load content, test quality.</td><td>Marketing, Design, Engineering, Ops, Volunteer Lead, QA</td></tr>
          <tr><td><strong>Soft Beta Launch</strong></td><td>Weeks 4–6</td><td>Invite beta users, host kickoff, gather feedback, monitor signals, iterate experience, warm the public audience.</td><td>Community, Partnerships, UX, Analytics, Product</td></tr>
          <tr><td><strong>Public Beta + Teaser</strong></td><td>Weeks 7–9</td><td>Public signups, teaser campaign, second Legacy Circle, publish case studies, finalize summit logistics, stress test.</td><td>Marketing, Growth, Events, Content, Engineering</td></tr>
          <tr><td><strong>Official Launch + Legacy Summit</strong></td><td>Weeks 10–12</td><td>Press outreach, activate paid memberships, launch referral program, support center, and flagship summit.</td><td>Leadership, PR, Finance, Growth, Support, Community</td></tr>
        </tbody>
      </table>
    </div>

    <div class="note" style="margin-top:18px">Public truth: this is a polished launch website, not the full backend application. Real accounts, payments, database logic, moderation systems, and analytics pipelines still require implementation in the live platform layer.</div>
  </div>
</section>

<section class="section" id="faq">
  <div class="wrap">
    <div class="section-head">
      <div class="kicker">FAQ</div>
      <h2>Clear answers for early visitors and future members.</h2>
      <p class="lead">These are public-site answers shaped from your blueprint and kept honest about what is conceptual versus fully live.</p>
    </div>

    <div class="grid-2">
      <div>
        <div class="faq-item open"><button class="faq-q">What is Confession Bucket?</button><div class="faq-a">Confession Bucket is a healing-centered digital sanctuary built around truth, ritual, empathy, and legacy. It is designed to move people from confession into reflection, resonance, and sustained growth.</div></div>
        <div class="faq-item"><button class="faq-q">How does the platform begin?</button><div class="faq-a">The journey begins with an onboarding ritual that introduces privacy, consent, reflection, and the emotional frame of the platform before deeper features open up.</div></div>
        <div class="faq-item"><button class="faq-q">What is the Maze Journal?</button><div class="faq-a">The Maze Journal is a structured prompt system for multi-day reflection tracks, helping users return to their healing process with continuity.</div></div>
        <div class="faq-item"><button class="faq-q">What does Legacy Score represent?</button><div class="faq-a">Legacy Score reflects how users show up through vulnerability, empathy, journaling, mentorship, and consistency. It is meant to reinforce healing behavior, not popularity.</div></div>
      </div>
      <div>
        <div class="faq-item"><button class="faq-q">Is this a live full application yet?</button><div class="faq-a">No. This website is a polished public launch layer. Full authentication, account saving, payment systems, and database features require backend deployment.</div></div>
        <div class="faq-item"><button class="faq-q">Who is this for?</button><div class="faq-a">Confession Bucket is designed for individuals, communities, schools, justice-centered programs, cultural institutions, and healing partners seeking a deeper digital model.</div></div>
        <div class="faq-item"><button class="faq-q">How can organizations get involved?</button><div class="faq-a">Organizations can partner through pilot circles, restorative programming, cultural collaboration, and early outreach relationships aligned with the platform mission.</div></div>
        <div class="faq-item"><button class="faq-q">Can this grow into a bigger platform later?</button><div class="faq-a">Yes. Your blueprint already points toward summits, curriculum, a broader media platform, deeper analytics, and eventually a full mobile and web product ecosystem.</div></div>
      </div>
    </div>
  </div>
</section>

  </main>  <footer class="footer">
    <div class="wrap footer-grid">
      <div><div style="font-weight:900;color:var(--text);margin-bottom:6px">Confession Bucket • Public Launch Version 2</div><div class="small">Single-file HTML launch site for Chrome, Chromebook, direct sharing, and GitHub Pages publishing.</div></div>
      <div class="small"><div>Upload this file as <strong>index.html</strong> to your Confession Bucket repo.</div><div>Commit, refresh GitHub Pages, and the live URL updates.</div></div>
    </div>
  </footer>  <script>
    document.querySelectorAll('.tabbtn').forEach(btn => {
      btn.addEventListener('click', () => {
        const parent = btn.parentElement;
        const section = parent.parentElement;
        const target = btn.dataset.tab;
        parent.querySelectorAll('.tabbtn').forEach(b => b.classList.remove('active'));
        btn.classList.add('active');
        section.querySelectorAll('.tabpane').forEach(p => p.classList.remove('active'));
        const pane = section.querySelector('#' + target);
        if (pane) pane.classList.add('active');
      });
    });
    document.querySelectorAll('.faq-q').forEach(q => {
      q.addEventListener('click', () => q.parentElement.classList.toggle('open'));
    });
  </script></body>
</html>
