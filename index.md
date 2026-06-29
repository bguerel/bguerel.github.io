<style>
  /* ── Global Theme Overrides ── */
  body { background: #000 !important; color: #c8d6e8 !important; }
  #header_wrap { background: #000 !important; background-image: none !important; border-bottom: 1px solid #1e2a3a !important; }
  #main_content_wrap { background: #080d12 !important; border-top: none !important; border-bottom: none !important; overflow: visible !important; }
  #main_content_wrap.outer { overflow: visible !important; }
  .inner { max-width: 800px !important; overflow: visible !important; }
  #main_content { overflow: visible !important; padding-left: 10px !important; padding-right: 10px !important; box-sizing: border-box !important; }
  #footer_wrap { background: #000 !important; }

  /* ── Terminal Card ── */
  .bio-section { margin-bottom: 2.5rem; }

  .container {
    width: 100%;
    background: #000;
    border-radius: 10px;
    border: 1px solid #1e2a3a;
    box-shadow: 0 10px 30px rgba(0,0,0,0.5);
    overflow: hidden;
  }
  .terminal_toolbar {
    display: flex; height: 35px; align-items: center;
    padding: 0 15px; background: #0a0a0a;
    border-bottom: 1px solid #1e2a3a; justify-content: space-between;
  }
  .butt { display: flex; align-items: center; }
  .btn {
    height: 13px; width: 13px; border-radius: 50%;
    margin-right: 8px; border: none; cursor: pointer;
    transition: transform 0.2s ease;
  }
  .btn:hover { transform: scale(1.1); }
  .btn-color:nth-child(1) { background: #ff5f56; }
  .btn-color:nth-child(2) { background: #ffbd2e; }
  .btn-color:nth-child(3) { background: #27c93f; }
  .user { color: #fff; font-size: 12px; font-weight: bold; font-family: 'Consolas', monospace; }
  .terminal_body {
    background: #000; padding: 15px 18px 20px;
    font-family: 'Consolas', 'SF Mono', monospace;
    font-size: 13px; line-height: 1.6; min-height: 180px;
  }
  .terminal_promt {
    display: flex; align-items: center;
    margin-bottom: 12px; flex-wrap: wrap; gap: 0;
  }
  .terminal_user     { color: #fff; }
  .terminal_location { color: #fff; }
  .terminal_bling    { color: #fff; }
  .terminal_sep      { color: #a0b4c8; margin: 0 2px; }
  .terminal_cmd      { color: #fff; margin-left: 4px; }
  .terminal_output   { color: #a0b4c8; line-height: 1.8; text-align: left; }
  .terminal_cursor {
    display: inline-block; width: 8px; height: 14px;
    background: #fff; margin-left: 3px; vertical-align: middle;
    animation: blink 1s step-end infinite;
  }
  @keyframes blink { 0%,100%{opacity:1} 50%{opacity:0} }

  /* ── Section Headers ── */
  .skills-section h3 {
    font-size: 0.72rem !important; letter-spacing: 0.2em !important;
    text-transform: uppercase !important; color: #6c8ebf !important;
    margin-bottom: 1rem !important; margin-top: 2rem !important;
    border: none !important; background: none !important;
    -webkit-text-fill-color: #6c8ebf !important; padding: 0 !important;
  }

  /* ── Grids ── */
  .skills-section { overflow: visible !important; }
  .skills-grid {
    display: grid !important;
    grid-template-columns: repeat(3, 1fr) !important;
    gap: 20px !important;
    padding: 30px 0 8px !important;
    overflow: visible !important;
    margin-bottom: 0.5rem !important;
  }
  .cert-grid {
    display: grid !important;
    grid-template-columns: repeat(2, 1fr) !important;
    gap: 20px !important;
    padding: 30px 0 8px !important;
    overflow: visible !important;
    max-width: none !important;
    margin-left: 0 !important;
    margin-right: 0 !important;
  }

  /* ── Card Wrap — 1:1 index2.html, Farben cyan→grün ── */
  .skill-card-wrap, .cert-card-wrap {
    position: relative !important;
    display: flex !important;
    border-radius: 17px !important;
    padding: 3px !important;
    background: rgba(255,255,255,0.2) !important;
    transition: transform 0.4s ease !important;
  }
  .skill-card-wrap::before, .cert-card-wrap::before {
    content: "" !important;
    position: absolute !important;
    inset: 0 !important;
    margin: auto !important;
    border-radius: 17px !important;
    z-index: -1 !important;
    background: linear-gradient(90deg, #00e5ff, #00e676) !important;
    filter: blur(0) !important;
    opacity: 0 !important;
    transition: filter 0.4s ease, opacity 0.4s ease !important;
    pointer-events: none !important;
    -webkit-transform: translateZ(0) !important;
    transform: translateZ(0) !important;
  }
  .skill-card-wrap:hover::before, .cert-card-wrap:hover::before {
    filter: blur(1.2em) !important;
    opacity: 1 !important;
  }
  .skill-card-wrap::after, .cert-card-wrap::after {
    content: "" !important;
    position: absolute !important;
    inset: 0 !important;
    border-radius: 17px !important;
    background: linear-gradient(90deg, #00e5ff, #00e676) !important;
    opacity: 0 !important;
    transition: opacity 0.4s ease !important;
    pointer-events: none !important;
    z-index: 0 !important;
  }
  .skill-card-wrap:hover::after, .cert-card-wrap:hover::after { opacity: 1 !important; }
  .skill-card-wrap:hover, .cert-card-wrap:hover { transform: translateY(-8px) !important; }
  .skill-card-wrap:hover .skill-card, .cert-card-wrap:hover .cert-card { transform: none !important; }

  /* ── Inner Cards ── */
  .skill-card, .cert-card {
    width: 100% !important; background: #000 !important; border: none !important;
    border-radius: 14px !important; padding: 1.6rem 1.4rem !important;
    position: relative !important; overflow: hidden !important;
    z-index: 1 !important; color: #c8d6e8 !important;
    transition: all 0.4s ease !important;
  }
  .skill-icon { font-size: 1.6rem !important; display: block !important; margin-bottom: 0.9rem !important; }
  .skill-name {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif !important;
    font-size: 0.95rem !important; font-weight: 600 !important;
    color: #e0eaf5 !important; margin-bottom: 0.5rem !important;
  }
  .skill-desc {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif !important;
    font-size: 0.8rem !important; line-height: 1.6 !important; color: #5a6a80 !important;
  }
  .skill-icon, .skill-name, .skill-desc,
  .cert-title, .cert-desc, .cert-link, .cert-info {
    transform: translateZ(0) !important;
    -webkit-font-smoothing: antialiased !important;
    -moz-osx-font-smoothing: grayscale !important;
  }

  /* ── Cert Card ── */
  .cert-card { display: flex !important; align-items: center !important; gap: 1rem !important; }
  .cert-badge-img {
    width: 146px !important; height: 146px !important;
    object-fit: contain !important; flex-shrink: 0 !important;
    margin: 0 !important; padding: 0 !important;
    border: none !important; box-shadow: none !important;
    position: static !important; display: block !important;
  }
  .cert-info { display: flex !important; flex-direction: column !important; text-align: left !important; }
  .cert-title {
    font-family: 'SF Mono', 'Fira Code', Consolas, monospace !important;
    font-size: 0.85rem !important; color: #c8d6e8 !important;
  }
  .cert-desc {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif !important;
    font-size: 0.78rem !important; color: #5a6a80 !important;
    line-height: 1.5 !important; margin-top: 0.5rem !important;
  }
  .cert-link {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif !important;
    font-size: 0.75rem !important; color: #00e5ff !important;
    text-decoration: none !important; margin-top: 0.5rem !important;
    display: inline-block !important; transition: color 0.2s !important;
  }
  .cert-link:hover { color: #00e676 !important; }

  /* ── Responsive: Tablet (≤768px) ── */
  @media (max-width: 768px) {
    .inner { max-width: 100% !important; }
    .skills-grid {
      grid-template-columns: repeat(2, 1fr) !important;
      gap: 14px !important;
    }
    .cert-grid {
      grid-template-columns: 1fr !important;
      gap: 14px !important;
    }
    .cert-card {
      flex-direction: column !important;
      align-items: flex-start !important;
    }
    .cert-badge-img { width: 100px !important; height: 100px !important; }
    #main_content_wrap { background: #000 !important; }
  }

  /* ── Responsive: Mobile (≤480px) ── */
  @media (max-width: 480px) {
    .skills-grid {
      grid-template-columns: 1fr !important;
      gap: 12px !important;
    }
    .skill-card, .cert-card { padding: 1.2rem 1rem !important; }
    .terminal_body { font-size: 11px !important; min-height: 140px !important; }
    #main_content { padding-left: 6px !important; padding-right: 6px !important; }
  }
</style>

<div class="bio-section">
  <div class="container">
    <div class="terminal_toolbar">
      <div class="butt">
        <button class="btn btn-color"></button>
        <button class="btn btn-color"></button>
        <button class="btn btn-color"></button>
      </div>
      <div class="user">about.txt</div>
      <div></div>
    </div>
    <div class="terminal_body">
      <div class="terminal_promt">
        <span class="terminal_user">bguerel</span><span class="terminal_bling">@</span><span class="terminal_location">rockylinux</span><span class="terminal_sep">:~$</span><span class="terminal_cmd" id="typed-cmd"></span>
      </div>
      <div class="terminal_output" id="typed-output" style="display:none;"></div>
    </div>
  </div>
</div>

<div class="skills-section">

  <h3>// Skills</h3>

  <div class="skills-grid">
    <div class="skill-card-wrap"><div class="skill-card">
      <span class="skill-icon">🐧</span>
      <div class="skill-name">Linux</div>
      <div class="skill-desc">Administration and operation across server and cloud environments.</div>
    </div></div>
    <div class="skill-card-wrap"><div class="skill-card">
      <span class="skill-icon">🌐</span>
      <div class="skill-name">Networking</div>
      <div class="skill-desc">Configuration and administration of bridging, VLANs, routing, firewalling and VPNs.</div>
    </div></div>
    <div class="skill-card-wrap"><div class="skill-card">
      <span class="skill-icon">⚙️</span>
      <div class="skill-name">Configuration Management</div>
      <div class="skill-desc">Infrastructure as Code with Ansible for reproducible and maintainable system states.</div>
    </div></div>
    <div class="skill-card-wrap"><div class="skill-card">
      <span class="skill-icon">🐳</span>
      <div class="skill-name">Containerization</div>
      <div class="skill-desc">Container builds and runtime management with Podman and Buildah.</div>
    </div></div>
    <div class="skill-card-wrap"><div class="skill-card">
      <span class="skill-icon">☸️</span>
      <div class="skill-name">Kubernetes</div>
      <div class="skill-desc">Orchestration and management of container workloads in clusters.</div>
    </div></div>
    <div class="skill-card-wrap"><div class="skill-card">
      <span class="skill-icon">🔁</span>
      <div class="skill-name">CI/CD Pipelines</div>
      <div class="skill-desc">Automated build, test and deployment processes for fast and reliable releases.</div>
    </div></div>
    <div class="skill-card-wrap"><div class="skill-card">
      <span class="skill-icon">💻</span>
      <div class="skill-name">Shell Scripting</div>
      <div class="skill-desc">Automating system tasks and operational workflows with Bash and POSIX.</div>
    </div></div>
    <div class="skill-card-wrap"><div class="skill-card">
      <span class="skill-icon">📊</span>
      <div class="skill-name">Monitoring & Logging</div>
      <div class="skill-desc">System monitoring, alerting and centralized log analysis for stable environments.</div>
    </div></div>
    <div class="skill-card-wrap"><div class="skill-card">
      <span class="skill-icon">🖥️</span>
      <div class="skill-name">Virtualization</div>
      <div class="skill-desc">Management of hypervisors and virtual machines with Xen, VMware, and Proxmox.</div>
    </div></div>
  </div>

  <h3>// Certifications</h3>

  <div class="cert-grid">
    <div class="cert-card-wrap">
      <div class="cert-card">
        <img class="cert-badge-img" src="https://www.lpi.org/wp-content/uploads/2024/12/LPIC-2-1-300x300.png" alt="LPIC-2 Badge" />
        <div class="cert-info">
          <div class="cert-title">Linux Professional Institute — LPIC-2</div>
          <p class="cert-desc">Advanced Linux system administration, network services and security.</p>
          <a class="cert-link" href="https://www.credly.com/users/bguerel/badges/credly" target="_blank">Verify on Credly</a>
        </div>
      </div>
    </div>
    <div class="cert-card-wrap">
      <div class="cert-card">
        <img class="cert-badge-img" src="https://www.lpi.org/wp-content/uploads/2024/12/LPIC-1-1-300x300.png" alt="LPIC-1 Badge" />
        <div class="cert-info">
          <div class="cert-title">Linux Professional Institute — LPIC-1</div>
          <p class="cert-desc">Fundamentals of Linux system administration and the command line.</p>
          <a class="cert-link" href="https://www.credly.com/users/bguerel/badges/credly" target="_blank">Verify on Credly</a>
        </div>
      </div>
    </div>
  </div>

</div>

<script>
  const cmdEl    = document.getElementById('typed-cmd');
  const outputEl = document.getElementById('typed-output');
  const cursor   = document.createElement('span');
  cursor.className = 'terminal_cursor';

  const command = ' cat about.txt';

  const segments = [
    ['I\'m a Linux System Engineer.\n', null],
    ['My focus is on reducing complexity and minimizing operational overhead, with systems that are declaratively defined, versioned and reproducibly deployable.\n\n', null],
    ['I build resilient platforms, automated operational processes and sustainable infrastructure concepts.\n\n', null],
    ['The goal: infrastructure that is documented, transparent and reproducible at any time, so that deployments become routine, not a risk factor.', null],
  ];

  function typeText(el, text, speed, done) {
    let i = 0;
    const span = document.createElement('span');
    el.appendChild(span);
    const iv = setInterval(() => {
      if (i >= text.length) { clearInterval(iv); if (done) done(); return; }
      const ch = text[i++];
      span.innerHTML += ch === '\n' ? '<br>' : ch;
    }, speed);
  }

  function typeSegments(segs, idx, done) {
    if (idx >= segs.length) { if (done) done(); return; }
    const [text, cls] = segs[idx];
    const wrapper = document.createElement('span');
    if (cls) wrapper.className = cls;
    outputEl.appendChild(wrapper);
    let i = 0;
    const iv = setInterval(() => {
      if (i >= text.length) {
        clearInterval(iv);
        typeSegments(segs, idx + 1, done);
        return;
      }
      const ch = text[i++];
      wrapper.innerHTML += ch === '\n' ? '<br>' : ch;
    }, 18);
  }

  setTimeout(() => {
    typeText(cmdEl, command, 60, () => {
      setTimeout(() => {
        outputEl.style.display = 'block';
        typeSegments(segments, 0, () => {
          outputEl.appendChild(document.createTextNode(' '));
          outputEl.appendChild(cursor);
        });
      }, 400);
    });
  }, 600);
</script>
