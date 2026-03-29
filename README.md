<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Siddareddy Rajesh Reddy — Profile</title>
<link href="https://fonts.googleapis.com/css2?family=DM+Mono:wght@400;500&family=Syne:wght@700;800&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet"/>
<style>
  :root {
    --bg: #0d0f14;
    --surface: #13161e;
    --border: #1e2230;
    --accent: #5b8dee;
    --accent2: #e8c468;
    --text: #d4d8e8;
    --muted: #636880;
    --green: #4ade80;
    --red: #f87171;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'DM Sans', sans-serif;
    min-height: 100vh;
    padding: 2rem 1rem 4rem;
  }

  .wrapper {
    max-width: 860px;
    margin: 0 auto;
  }

  /* ── Header ── */
  .header {
    border: 1px solid var(--border);
    background: var(--surface);
    border-radius: 16px;
    padding: 2.5rem 2rem 2rem;
    margin-bottom: 1.5rem;
    position: relative;
    overflow: hidden;
  }
  .header::before {
    content: '';
    position: absolute;
    top: -60px; right: -60px;
    width: 220px; height: 220px;
    background: radial-gradient(circle, rgba(91,141,238,0.15) 0%, transparent 70%);
    pointer-events: none;
  }

  .name {
    font-family: 'Syne', sans-serif;
    font-size: clamp(1.8rem, 5vw, 2.8rem);
    font-weight: 800;
    letter-spacing: -0.5px;
    color: #fff;
    line-height: 1.1;
  }
  .subtitle {
    font-family: 'DM Mono', monospace;
    font-size: 0.78rem;
    color: var(--muted);
    margin-top: 0.5rem;
    letter-spacing: 0.04em;
  }
  .cgpa-badge {
    display: inline-flex;
    align-items: center;
    gap: 0.4rem;
    background: rgba(78,220,120,0.1);
    border: 1px solid rgba(78,220,120,0.25);
    color: var(--green);
    font-family: 'DM Mono', monospace;
    font-size: 0.75rem;
    padding: 0.3rem 0.8rem;
    border-radius: 999px;
    margin-top: 0.75rem;
  }

  .links {
    display: flex;
    flex-wrap: wrap;
    gap: 0.6rem;
    margin-top: 1.5rem;
  }
  .link-pill {
    display: inline-flex;
    align-items: center;
    gap: 0.4rem;
    padding: 0.45rem 1rem;
    border-radius: 8px;
    font-size: 0.8rem;
    font-weight: 500;
    text-decoration: none;
    border: 1px solid var(--border);
    transition: border-color 0.2s, background 0.2s;
    color: var(--text);
  }
  .link-pill:hover { border-color: var(--accent); background: rgba(91,141,238,0.08); }
  .link-pill svg { width: 15px; height: 15px; }

  /* ── Section ── */
  .section {
    border: 1px solid var(--border);
    background: var(--surface);
    border-radius: 16px;
    padding: 1.75rem 2rem;
    margin-bottom: 1.5rem;
  }
  .section-title {
    font-family: 'Syne', sans-serif;
    font-size: 0.7rem;
    font-weight: 700;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 1.25rem;
  }

  /* ── About ── */
  .about-text {
    font-size: 0.92rem;
    line-height: 1.75;
    color: var(--text);
    font-weight: 300;
  }
  .about-meta {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem 2rem;
    margin-top: 1.2rem;
  }
  .meta-item {
    font-family: 'DM Mono', monospace;
    font-size: 0.74rem;
    color: var(--muted);
  }
  .meta-item span { color: var(--text); }

  /* ── LeetCode ── */
  .lc-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1rem;
  }
  @media (max-width: 540px) { .lc-grid { grid-template-columns: 1fr; } }

  .lc-card {
    background: var(--bg);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 1.2rem 1.4rem;
  }
  .lc-card-label {
    font-family: 'DM Mono', monospace;
    font-size: 0.68rem;
    color: var(--muted);
    letter-spacing: 0.08em;
    text-transform: uppercase;
    margin-bottom: 0.5rem;
  }
  .lc-card-value {
    font-family: 'Syne', sans-serif;
    font-size: 2rem;
    font-weight: 800;
    color: #fff;
    line-height: 1;
  }
  .lc-card-sub {
    font-size: 0.75rem;
    color: var(--muted);
    margin-top: 0.3rem;
  }
  .lc-card-value.accent { color: var(--accent2); }

  .lc-username-link {
    display: inline-flex;
    align-items: center;
    gap: 0.4rem;
    margin-top: 1.2rem;
    font-family: 'DM Mono', monospace;
    font-size: 0.78rem;
    color: var(--accent);
    text-decoration: none;
    border-bottom: 1px solid transparent;
    transition: border-color 0.2s;
  }
  .lc-username-link:hover { border-color: var(--accent); }

  .lc-full-stats {
    margin-top: 1.2rem;
  }
  .lc-imgs {
    display: flex;
    flex-direction: column;
    gap: 0.75rem;
    margin-top: 1rem;
  }
  .lc-imgs img {
    width: 100%;
    border-radius: 10px;
    border: 1px solid var(--border);
  }

  /* ── Tech Stack ── */
  .stack-group { margin-bottom: 1.2rem; }
  .stack-group-label {
    font-size: 0.72rem;
    color: var(--muted);
    font-family: 'DM Mono', monospace;
    letter-spacing: 0.06em;
    margin-bottom: 0.6rem;
  }
  .chips {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
  }
  .chip {
    display: inline-flex;
    align-items: center;
    gap: 0.4rem;
    padding: 0.35rem 0.85rem;
    border-radius: 8px;
    border: 1px solid var(--border);
    font-size: 0.78rem;
    font-weight: 500;
    color: var(--text);
    background: var(--bg);
  }
  .chip-dot {
    width: 7px; height: 7px;
    border-radius: 50%;
    flex-shrink: 0;
  }

  /* ── GitHub ── */
  .gh-imgs {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 0.75rem;
  }
  @media (max-width: 540px) { .gh-imgs { grid-template-columns: 1fr; } }
  .gh-imgs img {
    width: 100%;
    border-radius: 10px;
    border: 1px solid var(--border);
  }

  /* ── Footer ── */
  .footer {
    text-align: center;
    font-family: 'DM Mono', monospace;
    font-size: 0.7rem;
    color: var(--muted);
    margin-top: 2rem;
  }
  .visitor-badge {
    margin-top: 0.5rem;
  }
  .visitor-badge img { border-radius: 6px; }

  hr { border: none; border-top: 1px solid var(--border); margin: 1.5rem 0; }
</style>
</head>
<body>
<div class="wrapper">

  <!-- ── Header ── -->
  <div class="header">
    <div class="name">Siddareddy Rajesh Reddy</div>
    <div class="subtitle">Department of Computer Science and Engineering &nbsp;·&nbsp; National Institute of Technology, Sikkim</div>
    <div class="cgpa-badge">
      <svg viewBox="0 0 16 16" fill="currentColor" width="12"><path d="M8 1l1.9 3.85L14 5.72l-3 2.92.71 4.14L8 10.77l-3.71 1.01.71-4.14L2 5.72l4.1-.87z"/></svg>
      CGPA 9.01 / 10.0
    </div>
    <div class="links">
      <a class="link-pill" href="https://linkedin.com/in/s-rajesh-reddy" target="_blank">
        <svg viewBox="0 0 24 24" fill="currentColor"><path d="M19 0h-14c-2.76 0-5 2.24-5 5v14c0 2.76 2.24 5 5 5h14c2.76 0 5-2.24 5-5v-14c0-2.76-2.24-5-5-5zm-11 19h-3v-10h3v10zm-1.5-11.27c-.97 0-1.75-.79-1.75-1.76s.78-1.76 1.75-1.76 1.75.79 1.75 1.76-.78 1.76-1.75 1.76zm13.5 11.27h-3v-5.6c0-1.34-.03-3.07-1.87-3.07-1.87 0-2.16 1.46-2.16 2.97v5.7h-3v-10h2.88v1.36h.04c.4-.76 1.38-1.56 2.84-1.56 3.04 0 3.6 2 3.6 4.59v5.61z"/></svg>
        LinkedIn
      </a>
      <a class="link-pill" href="https://github.com/SiddareddyRajeshReddy" target="_blank">
        <svg viewBox="0 0 24 24" fill="currentColor"><path d="M12 0C5.37 0 0 5.37 0 12c0 5.3 3.44 9.8 8.2 11.38.6.11.82-.26.82-.58v-2.17c-3.34.73-4.04-1.61-4.04-1.61-.54-1.38-1.33-1.74-1.33-1.74-1.09-.74.08-.73.08-.73 1.2.09 1.84 1.24 1.84 1.24 1.07 1.83 2.8 1.3 3.48.99.11-.78.42-1.3.76-1.6-2.67-.3-5.47-1.33-5.47-5.93 0-1.31.47-2.38 1.24-3.22-.13-.3-.54-1.52.12-3.18 0 0 1.01-.32 3.3 1.23a11.5 11.5 0 0 1 3-.4c1.02 0 2.04.14 3 .4 2.28-1.55 3.29-1.23 3.29-1.23.66 1.66.25 2.88.12 3.18.77.84 1.24 1.91 1.24 3.22 0 4.61-2.81 5.63-5.48 5.92.43.37.81 1.1.81 2.22v3.29c0 .32.22.7.82.58C20.56 21.8 24 17.3 24 12c0-6.63-5.37-12-12-12z"/></svg>
        GitHub
      </a>
      <a class="link-pill" href="mailto:b230065@nitsikkim.ac.in">
        <svg viewBox="0 0 24 24" fill="currentColor"><path d="M20 4H4c-1.1 0-2 .9-2 2v12c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 4l-8 5-8-5V6l8 5 8-5v2z"/></svg>
        b230065@nitsikkim.ac.in
      </a>
      <a class="link-pill" href="https://leetcode.com/Siddareddy_Rajesh_Reddy/" target="_blank">
        <svg viewBox="0 0 24 24" fill="currentColor"><path d="M13.483 0a1.374 1.374 0 0 0-.961.438L7.116 6.226l-3.854 4.126a5.266 5.266 0 0 0-1.209 2.104 5.35 5.35 0 0 0-.125.513 5.527 5.527 0 0 0 .062 2.362 5.83 5.83 0 0 0 .349 1.017 5.938 5.938 0 0 0 1.271 1.818l4.277 4.193.039.038c2.248 2.165 5.852 2.133 8.063-.074l2.396-2.392c.54-.54.54-1.414.003-1.955a1.378 1.378 0 0 0-1.951-.003l-2.396 2.392a3.021 3.021 0 0 1-4.205.038l-.02-.019-4.276-4.193c-.652-.64-.972-1.469-.948-2.263a2.68 2.68 0 0 1 .066-.523 2.545 2.545 0 0 1 .619-1.164L9.13 8.114c1.058-1.134 3.204-1.27 4.43-.278l3.501 2.831c.593.48 1.461.387 1.94-.207a1.384 1.384 0 0 0-.207-1.943l-3.5-2.831c-.8-.647-1.766-1.045-2.774-1.202l2.015-2.158A1.384 1.384 0 0 0 13.483 0zm-2.866 12.815a1.38 1.38 0 0 0-1.38 1.382 1.38 1.38 0 0 0 1.38 1.382H20.79a1.38 1.38 0 0 0 1.38-1.382 1.38 1.38 0 0 0-1.38-1.382z"/></svg>
        LeetCode
      </a>
    </div>
  </div>

  <!-- ── About ── -->
  <div class="section">
    <div class="section-title">About</div>
    <p class="about-text">
      Software Engineering student focused on Full-Stack Development, Machine Learning, and Algorithmic Problem Solving.
      Currently expanding expertise in System Design and Scalable Architectures while maintaining a consistent presence in competitive programming.
    </p>
    <div class="about-meta">
      <div class="meta-item">Degree &nbsp;<span>B.Tech, CSE</span></div>
      <div class="meta-item">Institute &nbsp;<span>NIT Sikkim</span></div>
      <div class="meta-item">Batch &nbsp;<span>2023 – 2027</span></div>
      <div class="meta-item">Focus &nbsp;<span>DSA · MERN · DBMS</span></div>
    </div>
  </div>

  <!-- ── LeetCode ── -->
  <div class="section">
    <div class="section-title">Competitive Programming · LeetCode</div>

    <!-- 
      NOTE ON CONTEST RATING BADGE:
      The dynamic badge approach using third-party APIs (leetcode-stats-api-seven.vercel.app) 
      is unreliable. The correct fix for your README.md is to use the shield with a hardcoded 
      value (update manually after contests), OR use the alfadb API shown below.
      
      Working API endpoint: https://alfa-leetcode-api.onrender.com/userContestRankingInfo/Siddareddy_Rajesh_Reddy
      Query field: data.userContestRanking.rating (rounded)
    -->

    <!-- Stat cards — pulled from LeetCode stats API images (most reliable) -->
    <div class="lc-imgs">
      <img 
        src="https://leetcard.jacoblin.cool/Siddareddy_Rajesh_Reddy?theme=dark&font=Baloo+2&ext=heatmap"
        alt="LeetCode Stats + Heatmap"
        loading="lazy"
      />
    </div>

    <!-- Contest Rating — fixed badge using shields.io with alfa-leetcode-api -->
    <div style="margin-top:1.2rem; display:flex; align-items:center; gap:0.75rem; flex-wrap:wrap;">
      <img
        src="https://img.shields.io/badge/dynamic/json?style=for-the-badge&label=Contest%20Rating&query=%24.data.userContestRanking.rating&url=https%3A%2F%2Falfa-leetcode-api.onrender.com%2FuserContestRankingInfo%2FSiddareddy_Rajesh_Reddy&color=1A1A1A&logo=leetcode&logoColor=FFA116"
        alt="LeetCode Contest Rating"
        style="border-radius:6px;"
      />
      <a class="lc-username-link" href="https://leetcode.com/Siddareddy_Rajesh_Reddy/" target="_blank">
        @Siddareddy_Rajesh_Reddy ↗
      </a>
    </div>

    <div style="margin-top:1rem; padding: 0.75rem 1rem; background: var(--bg); border: 1px solid rgba(91,141,238,0.2); border-radius:10px; font-family:'DM Mono',monospace; font-size:0.72rem; color:var(--muted); line-height:1.7;">
      <strong style="color:var(--accent);">README fix note:</strong> Replace the old badge URL with:<br/>
      <span style="color:var(--text); word-break:break-all;">
        https://img.shields.io/badge/dynamic/json?style=for-the-badge&amp;label=Contest%20Rating&amp;query=%24.data.userContestRanking.rating&amp;url=https%3A%2F%2Falfa-leetcode-api.onrender.com%2FuserContestRankingInfo%2F&lt;username&gt;&amp;color=1A1A1A&amp;logo=leetcode&amp;logoColor=FFA116
      </span>
    </div>
  </div>

  <!-- ── Tech Stack ── -->
  <div class="section">
    <div class="section-title">Technical Stack</div>

    <div class="stack-group">
      <div class="stack-group-label">Languages</div>
      <div class="chips">
        <div class="chip"><div class="chip-dot" style="background:#00599C"></div>C</div>
        <div class="chip"><div class="chip-dot" style="background:#ED8B00"></div>Java</div>
        <div class="chip"><div class="chip-dot" style="background:#F7DF1E"></div>JavaScript</div>
        <div class="chip"><div class="chip-dot" style="background:#777BB4"></div>PHP</div>
      </div>
    </div>

    <div class="stack-group">
      <div class="stack-group-label">Databases</div>
      <div class="chips">
        <div class="chip"><div class="chip-dot" style="background:#4EA94B"></div>MongoDB</div>
        <div class="chip"><div class="chip-dot" style="background:#00758F"></div>MySQL</div>
      </div>
    </div>

    <div class="stack-group">
      <div class="stack-group-label">Frameworks & Tools</div>
      <div class="chips">
        <div class="chip"><div class="chip-dot" style="background:#61DAFB"></div>React</div>
        <div class="chip"><div class="chip-dot" style="background:#38B2AC"></div>Tailwind CSS</div>
        <div class="chip"><div class="chip-dot" style="background:#43853D"></div>Node.js</div>
        <div class="chip"><div class="chip-dot" style="background:#404D59"></div>Express.js</div>
        <div class="chip"><div class="chip-dot" style="background:#F05032"></div>Git</div>
      </div>
    </div>
  </div>

  <!-- ── GitHub Analytics ── -->
  <div class="section">
    <div class="section-title">GitHub Analytics</div>
    <div class="gh-imgs">
      <img
        src="https://github-readme-stats.vercel.app/api?username=SiddareddyRajeshReddy&show_icons=true&theme=tokyonight&hide_border=true&count_private=true"
        alt="GitHub Stats"
        loading="lazy"
      />
      <img
        src="https://github-readme-stats.vercel.app/api/top-langs/?username=SiddareddyRajeshReddy&layout=compact&theme=tokyonight&hide_border=true"
        alt="Top Languages"
        loading="lazy"
      />
    </div>
  </div>

  <!-- ── Footer ── -->
  <div class="footer">
    <div class="visitor-badge">
      <img
        src="https://komarev.com/ghpvc/?username=SiddareddyRajeshReddy&color=5b8dee&style=for-the-badge&label=PROFILE+VIEWS"
        alt="Visitor Count"
      />
    </div>
    <div style="margin-top:0.75rem;">Siddareddy Rajesh Reddy · NIT Sikkim · CSE 2023–2027</div>
  </div>

</div>
</body>
</html>
