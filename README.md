# Skilsecc.io
<!doctype html>
<html lang="id">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Hacker Etis — Learning Hub</title>
  <meta name="description" content="Hacker Etis — Roadmap & modul belajar keamanan siber yang legal dan defensif." />
  <style>
    /* ===== Base & Theme ===== */
    :root{
      --bg:#0b0f13;
      --card:#0f1720;
      --muted:#98a0ad;
      --accent:#7c5cff;
      --accent-2:#00d4ff;
      --glass: rgba(255,255,255,0.03);
      --success:#32d583;
      --danger:#ff5c7c;
      --radius:14px;
      --mono: ui-monospace, SFMono-Regular, Menlo, Monaco, "Roboto Mono", "Courier New", monospace;
      --sans: Inter, ui-sans-serif, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family:var(--sans);
      background:linear-gradient(180deg,var(--bg),#061018 140%);
      color:#e6eef8;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.45;
    }
    a{color:inherit}
    img{max-width:100%;display:block}
    .container{max-width:1100px;margin:0 auto;padding:24px}
    header{position:sticky;top:0;z-index:40;background:linear-gradient(180deg, rgba(10,12,15,0.6), rgba(10,12,15,0.25));backdrop-filter: blur(6px);border-bottom:1px solid rgba(255,255,255,0.03)}
    .header-inner{display:flex;gap:12px;align-items:center;padding:14px 24px}
    .brand{display:flex;align-items:center;gap:12px}
    .logo{
      width:44px;height:44px;border-radius:10px;background:linear-gradient(145deg,var(--accent),#4b8bff);display:flex;align-items:center;justify-content:center;font-weight:800;color:white;font-family:var(--mono);
      box-shadow:0 6px 24px rgba(10,12,20,0.6), inset 0 -8px 24px rgba(255,255,255,0.03);
    }
    .title{font-size:1.05rem;font-weight:700}
    .subtitle{font-size:0.78rem;color:var(--muted)}
    /* Hero */
    .hero{display:grid;grid-template-columns:1fr;gap:18px;align-items:center;padding:28px 0}
    @media(min-width:880px){.hero{grid-template-columns:1fr 420px}}
    .hero-card{background:linear-gradient(180deg, rgba(255,255,255,0.02), transparent);border:1px solid rgba(255,255,255,0.04);padding:22px;border-radius:20px}
    .h1{font-size:1.8rem;font-weight:800;margin:0;line-height:1.05}
    .h1 .accent{background:linear-gradient(90deg,var(--accent),var(--accent-2));-webkit-background-clip:text;background-clip:text;color:transparent}
    .lead{color:var(--muted);margin-top:10px}
    .cta-row{margin-top:16px;display:flex;gap:10px;flex-wrap:wrap}
    .btn{
      display:inline-flex;align-items:center;gap:8px;padding:10px 14px;border-radius:999px;border:1px solid rgba(255,255,255,0.04);
      background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));cursor:pointer;font-weight:700;
    }
    .btn.primary{background:linear-gradient(90deg,var(--accent),var(--accent-2));color:#061018;border:none;box-shadow:0 10px 30px rgba(124,92,255,0.14)}
    /* Progress */
    .progress-wrap{padding:14px;border-radius:12px;background:linear-gradient(180deg, rgba(0,0,0,0.15), rgba(255,255,255,0.01));border:1px solid rgba(255,255,255,0.03)}
    .prog-bar{height:12px;background:rgba(255,255,255,0.04);border-radius:999px;overflow:hidden}
    .prog-bar > i{height:100%;display:block;background:linear-gradient(90deg,var(--accent),var(--accent-2));width:0%}
    .small{font-size:0.85rem;color:var(--muted)}
    /* Filters */
    .controls{display:flex;gap:10px;flex-wrap:wrap;margin-top:18px}
    .search{
      flex:1;min-width:200px;padding:10px 12px;border-radius:12px;border:1px solid rgba(255,255,255,0.04);background:var(--glass);color:inherit;
    }
    .select{padding:10px 12px;border-radius:12px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:inherit}
    /* Grid */
    .grid{display:grid;grid-template-columns:1fr;gap:14px;margin-top:14px}
    @media(min-width:720px){.grid{grid-template-columns:repeat(2,1fr)}}
    @media(min-width:1024px){.grid{grid-template-columns:repeat(3,1fr)}}
    .card{background:linear-gradient(180deg, rgba(255,255,255,0.02), transparent);border-radius:14px;padding:16px;border:1px solid rgba(255,255,255,0.03)}
    .card h4{margin:0;font-size:1.02rem}
    .meta{font-size:0.78rem;color:var(--muted);margin-top:6px}
    .objectives{margin-top:10px;font-size:0.92rem;color:var(--muted);padding-left:14px}
    .labs{margin-top:10px;display:flex;gap:8px;flex-wrap:wrap}
    .lab{padding:6px 8px;border-radius:999px;border:1px solid rgba(255,255,255,0.03);font-size:0.82rem;background:rgba(255,255,255,0.01)}
    .check{display:flex;align-items:center;gap:10px}
    .checkbox{width:18px;height:18px;border-radius:6px;border:1px solid rgba(255,255,255,0.06);display:inline-grid;place-items:center;cursor:pointer}
    .checkbox.active{background:linear-gradient(90deg,var(--accent),var(--accent-2));border:none;color:#06202a}
    .empty{color:var(--muted);padding:22px;border-radius:12px;border:1px dashed rgba(255,255,255,0.03);text-align:center}
    /* Roadmap & Ethics */
    .roadmap{display:grid;gap:12px}
    .step{display:flex;gap:12px;align-items:flex-start}
    .step .n{width:38px;height:38px;border-radius:10px;background:linear-gradient(90deg,var(--accent),var(--accent-2));display:flex;align-items:center;justify-content:center;font-weight:800;color:#041018}
    .step .content{background:rgba(255,255,255,0.02);padding:12px;border-radius:10px;border:1px solid rgba(255,255,255,0.03)}
    /* footer / resources */
    footer{margin-top:30px;padding:26px 0;color:var(--muted);border-top:1px solid rgba(255,255,255,0.03)}
    .resources{display:grid;grid-template-columns:repeat(2,1fr);gap:8px}
    @media(max-width:600px){.resources{grid-template-columns:1fr}}
    .resource{padding:10px;border-radius:10px;border:1px solid rgba(255,255,255,0.03);background:rgba(255,255,255,0.01)}
    /* small helpers */
    .tag{padding:6px 8px;border-radius:999px;font-size:0.78rem;background:rgba(255,255,255,0.02);border:1px solid rgba(255,255,255,0.03)}
    .muted{color:var(--muted)}
    .right{margin-left:auto}
    .kbd{background:rgba(255,255,255,0.02);padding:6px 8px;border-radius:8px;border:1px solid rgba(255,255,255,0.03);font-family:var(--mono);font-size:0.82rem}
    /* tiny responsiveness */
    @media(max-width:480px){.h1{font-size:1.5rem}.hero{gap:10px}.header-inner{padding:10px}}
  </style>
</head>
<body>
  <header>
    <div class="container header-inner">
      <div class="brand">
        <div class="logo">HE</div>
        <div>
          <div class="title">Hacker Etis</div>
          <div class="subtitle">Belajar keamanan siber — legal & defensif</div>
        </div>
      </div>
      <div class="right small muted">Built for learning • Do it responsibly</div>
    </div>
  </header>

  <main class="container">
    <!-- Hero -->
    <section class="hero">
      <div class="hero-card">
        <h1 class="h1">Kuasai keamanan siber — <span class="accent">secara etis</span></h1>
        <p class="lead">Roadmap, modul, lab legal, dan tracker progress yang ringan. Uji hanya di lab sendiri atau lingkungan yang kamu punya izin.</p>

        <div class="controls" style="margin-top:18px;">
          <input id="search" class="search" placeholder="Cari skill, mis. OSINT, Wireshark, OWASP..." />
          <select id="filter-domain" class="select">
            <option value="all">Semua domain</option>
          </select>
          <select id="filter-level" class="select">
            <option value="all">Semua level</option>
            <option value="Beginner">Beginner</option>
            <option value="Intermediate">Intermediate</option>
            <option value="Advanced">Advanced</option>
          </select>
        </div>

        <div style="display:flex;gap:12px;margin-top:14px;flex-wrap:wrap;">
          <button class="btn primary" id="btn-start">Mulai Modul</button>
          <button class="btn" id="btn-reset">Reset Progress</button>
          <div style="margin-left:auto" class="small muted">Saved in browser • lokal</div>
        </div>
      </div>

      <aside class="hero-card progress-wrap">
        <div class="small muted">Progress kamu</div>
        <div style="margin-top:10px" class="prog-bar"><i id="prog-fill" style="width:0%"></i></div>
        <div style="display:flex;align-items:center;gap:8px;margin-top:10px">
          <div style="font-weight:800;font-size:1.15rem" id="prog-number">0%</div>
          <div class="muted small">modul selesai</div>
          <div class="right small muted">Total modul: <span id="total-mod">0</span></div>
        </div>

        <div style="margin-top:14px">
          <div style="font-weight:700">Etika & Legal</div>
          <p class="muted small" style="margin-top:6px">Selalu minta izin tertulis sebelum uji keamanan ke pihak lain. Latihan di lab sendiri atau platform legal (TryHackMe, HTB, OverTheWire).</p>
        </div>
      </aside>
    </section>

    <!-- Skills -->
    <section style="margin-top:18px">
      <div style="display:flex;align-items:center;gap:12px">
        <h3 style="margin:0">Modul Skill</h3>
        <div class="muted small">Filter, tandai saat selesai</div>
      </div>

      <div id="skills-grid" class="grid" style="margin-top:12px"></div>
      <div id="no-result" class="empty" style="display:none;margin-top:12px">Tidak ada hasil. Coba ubah filter atau kata kunci.</div>
    </section>

    <!-- Roadmap -->
    <section style="margin-top:24px">
      <div style="display:flex;align-items:center;gap:10px">
        <h3 style="margin:0">Roadmap Pembelajaran</h3>
        <div class="muted small">Langkah demi langkah</div>
      </div>
      <div class="roadmap" style="margin-top:12px" id="roadmap"></div>
    </section>

    <!-- Resources -->
    <section style="margin-top:24px">
      <div style="display:flex;align-items:center;gap:8px">
        <h3 style="margin:0">Sumber & Lab Legal</h3>
        <div class="muted small">Link ke lab & dokumentasi yang aman</div>
      </div>
      <div style="margin-top:12px" class="resources" id="resources"></div>
    </section>

    <footer>
      <div style="display:flex;gap:12px;align-items:center;">
        <div style="font-weight:800">Hacker Etis</div>
        <div class="muted small">• Buat portofolio — catat write-up & izin saat praktek</div>
        <div class="right muted small">— Upload ke GitHub Pages untuk live</div>
      </div>
    </footer>
  </main>

  <script>
    /* ===== Data ===== */
    const SKILLS = [
      { id: 'linux-basics', title: 'Linux & CLI Basics', level:'Beginner', domain:'Fundamentals',
        summary:'Filesystem, permissions, process, bash scripting.',
        objectives:['ls/cd/grep/sed/awk','Manage users & permissions','Bash scripting basics'],
        labs:[
          {name:'OverTheWire: Bandit', url:'https://overthewire.org/wargames/bandit/'}
        ]
      },
      { id:'networking', title:'Networking Essentials', level:'Beginner', domain:'Network',
        summary:'OSI/TCP-IP, subnets, DNS, packet flow.',
        objectives:['OSI vs TCP/IP','tcpdump & Wireshark basics','nmap safe scans in lab'],
        labs:[{name:'Wireshark sample captures', url:'https://wiki.wireshark.org/SampleCaptures'}]
      },
      { id:'web-owasp', title:'OWASP Top 10 (defensive)', level:'Intermediate', domain:'Web',
        summary:'Injection, XSS, auth flaws — prevention & testing in legal lab.',
        objectives:['Threat modeling','Input validation & encoding','Harden auth & sessions'],
        labs:[{name:'OWASP Juice Shop', url:'https://owasp.org/www-project-juice-shop/'},{name:'WebGoat',url:'https://owasp.org/www-project-webgoat/'}]
      },
      { id:'osint-core', title:'OSINT Core (ethical)', level:'Intermediate', domain:'OSINT',
        summary:'Search operators, metadata, mapping, correlation.',
        objectives:['Advanced search queries','Metadata extraction','Correlate public profiles ethically'],
        labs:[{name:'Maltego CE', url:'https://www.maltego.com/downloads/'},{name:'theHarvester',url:'https://github.com/laramies/theHarvester'}]
      },
      { id:'forensics', title:'Forensics Basics', level:'Intermediate', domain:'Forensics',
        summary:'File systems, memory acquisition, timelines.',
        objectives:['Evidence collection basics','Log analysis & timelines','Volatility & Autopsy in lab'],
        labs:[{name:'Volatility',url:'https://www.volatilityfoundation.org/releases'},{name:'Autopsy',url:'https://www.autopsy.com/download/'}]
      },
      { id:'reverse', title:'Intro to Reverse Engineering', level:'Advanced', domain:'Reverse',
        summary:'Disassembly & debugging in CTFs/VMs you own.',
        objectives:['Assembly primer','Ghidra/radare2 static analysis','Debug with gdb/x64dbg'],
        labs:[{name:'Ghidra',url:'https://ghidra-sre.org/'},{name:'radare2',url:'https://rada.re/n/'}]
      },
      { id:'crypto', title:'Applied Crypto Primer', level:'Beginner', domain:'Crypto',
        summary:'Hashes, symmetric/asymmetric, TLS basics.',
        objectives:['Correct primitives','Avoid home-rolled crypto','Use libsodium/openssl'],
        labs:[{name:'CryptoPals',url:'https://cryptopals.com/'}]
      },
      { id:'cloud', title:'Cloud Security Fundamentals', level:'Intermediate', domain:'Cloud',
        summary:'IAM least privilege, logging, IaC scanning.',
        objectives:['Design least-privilege IAM','Enable logging & alerts','Scan IaC (tfsec/Checkov)'],
        labs:[{name:'tfsec',url:'https://aquasecurity.github.io/tfsec/'},{name:'Checkov',url:'https://www.checkov.io/'}]
      },
      { id:'blueteam', title:'Blue Team & SOC', level:'Intermediate', domain:'Blue Team',
        summary:'Detection engineering, SIEM, IR playbooks.',
        objectives:['Detection rules','Threat hunting basics','IR playbook practice'],
        labs:[{name:'Sigma Rules',url:'https://sigmahq.io/'},{name:'Security Onion',url:'https://securityonion.net/'}]
      }
    ];

    const ROADMAP = [
      { step:1, title:'Etika & Legal', detail:'Pahami batas hukum. Dapatkan izin tertulis sebelum melakukan pengujian pada sistem orang lain.' },
      { step:2, title:'Computing Basics', detail:'Linux, networking, Git, dan pemrograman (Python/JS).' },
      { step:3, title:'Web & Network', detail:'Pelajari HTTP, DNS, TLS, nmap, Wireshark, dan coding aman.' },
      { step:4, title:'Pilih Spesialisasi', detail:'WebSec, OSINT, Forensics, Cloud, Blue Team, atau Reverse Engineering.' },
      { step:5, title:'Homelab & CTFs', detail:'Bangun lab, ikuti CTF, dokumentasikan write-up & izin.' },
      { step:6, title:'Portofolio & Sertifikasi', detail:'Buat blog, GitHub, dan pertimbangkan sertifikasi bila perlu.' }
    ];

    const RESOURCES = [
      { title:'OWASP', url:'https://owasp.org/' },
      { title:'TryHackMe', url:'https://tryhackme.com/' },
      { title:'Hack The Box Academy', url:'https://academy.hackthebox.com/' },
      { title:'OverTheWire', url:'https://overthewire.org/' },
      { title:'MITRE ATT&CK', url:'https://attack.mitre.org/' },
      { title:'NIST Cybersecurity Framework', url:'https://www.nist.gov/cyberframework' }
    ];

    /* ===== State & Storage ===== */
    const STORAGE_KEY = 'hacker-etis-progress-v1';
    let progress = {};
    function loadProgress(){
      try{
        const raw = localStorage.getItem(STORAGE_KEY);
        progress = raw ? JSON.parse(raw) : {};
      }catch(e){ progress = {}; }
    }
    function saveProgress(){
      try{ localStorage.setItem(STORAGE_KEY, JSON.stringify(progress)); }catch(e){}
    }

    /* ===== UI Renders ===== */
    const skillsGrid = document.getElementById('skills-grid');
    const filterDomain = document.getElementById('filter-domain');
    const filterLevel = document.getElementById('filter-level');
    const searchInput = document.getElementById('search');
    const progFill = document.getElementById('prog-fill');
    const progNumber = document.getElementById('prog-number');
    const totalMod = document.getElementById('total-mod');
    const noResult = document.getElementById('no-result');

    function uniqueDomains(){
      const d = [...new Set(SKILLS.map(s=>s.domain))];
      return d.sort();
    }

    function renderDomainOptions(){
      const domains = uniqueDomains();
      domains.forEach(dom=>{
        const opt = document.createElement('option');
        opt.value = dom; opt.textContent = dom;
        filterDomain.appendChild(opt);
      });
    }

    function renderSkills(){
      const q = searchInput.value.trim().toLowerCase();
      const d = filterDomain.value;
      const lvl = filterLevel.value;

      const filtered = SKILLS.filter(s=>{
        if(d !== 'all' && s.domain !== d) return false;
        if(lvl !== 'all' && s.level !== lvl) return false;
        if(q !== ''){
          const hay = (s.title + ' ' + s.summary + ' ' + s.objectives.join(' ')).toLowerCase();
          if(!hay.includes(q)) return false;
        }
        return true;
      });

      skillsGrid.innerHTML = '';
      if(filtered.length === 0){
        noResult.style.display = 'block';
      } else {
        noResult.style.display = 'none';
        filtered.forEach(s => skillsGrid.appendChild(cardForSkill(s)));
      }

      totalMod.textContent = SKILLS.length;
      updateProgressUI();
    }

    function cardForSkill(s){
      const el = document.createElement('article');
      el.className = 'card';
      el.innerHTML = `
        <div style="display:flex;justify-content:space-between;gap:10px">
          <div>
            <h4>${s.title}</h4>
            <div class="meta">${s.level} • ${s.domain}</div>
          </div>
          <div class="check">
            <div class="checkbox ${progress[s.id] ? 'active' : ''}" data-id="${s.id}" title="Tandai selesai">
              ${progress[s.id] ? '✓' : ''}
            </div>
          </div>
        </div>
        <p class="muted" style="margin-top:10px">${s.summary}</p>
        <ul class="objectives">
          ${s.objectives.map(o => `<li>${o}</li>`).join('')}
        </ul>
        <div class="labs">
          ${s.labs.map(l => `<a class="lab" href="${l.url}" target="_blank" rel="noreferrer">${escapeHtml(l.name)}</a>`).join('')}
        </div>
      `;
      // toggle handler
      el.querySelector('.checkbox').addEventListener('click', (ev)=>{
        const id = ev.currentTarget.getAttribute('data-id');
        progress[id] = !progress[id];
        saveProgress();
        renderSkills();
      });
      return el;
    }

    function renderRoadmap(){
      const node = document.getElementById('roadmap');
      node.innerHTML = '';
      ROADMAP.forEach(r=>{
        const div = document.createElement('div');
        div.className = 'step';
        div.innerHTML = `
          <div class="n">${r.step}</div>
          <div class="content">
            <div style="font-weight:700">${escapeHtml(r.title)}</div>
            <div class="muted small" style="margin-top:6px">${escapeHtml(r.detail)}</div>
          </div>
        `;
        node.appendChild(div);
      });
    }

    function renderResources(){
      const node = document.getElementById('resources');
      node.innerHTML = '';
      RESOURCES.forEach(r=>{
        const a = document.createElement('a');
        a.className = 'resource';
        a.href = r.url; a.target = '_blank'; a.rel = 'noreferrer';
        a.innerHTML = `<div style="display:flex;justify-content:space-between;align-items:center"><div>${escapeHtml(r.title)}</div><div class="tag">Open</div></div>`;
        node.appendChild(a);
      });
    }

    /* ===== Progress UI ===== */
    function updateProgressUI(){
      const done = Object.values(progress).filter(Boolean).length;
      const total = SKILLS.length;
      const pct = total === 0 ? 0 : Math.round((done/total)*100);
      progFill.style.width = pct + '%';
      progNumber.textContent = pct + '%';
    }

    /* ===== Helpers ===== */
    function escapeHtml(s){ return String(s).replace(/[&<>"']/g, function(m){ return ({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'})[m]; }); }

    /* ===== Init ===== */
    document.getElementById('btn-reset').addEventListener('click', ()=>{
      if(confirm('Reset semua progress?')){ progress = {}; saveProgress(); renderSkills(); }
    });
    document.getElementById('btn-start').addEventListener('click', ()=>{
      window.scrollTo({top: document.querySelector('#skills-grid').offsetTop - 20, behavior:'smooth'});
    });

    searchInput.addEventListener('input', debounce(()=>renderSkills(), 220));
    filterDomain.addEventListener('change', ()=>renderSkills());
    filterLevel.addEventListener('change', ()=>renderSkills());

    // fill domain options
    (function boot(){
      renderDomainOptions();
      loadProgress();
      renderSkills();
      renderRoadmap();
      renderResources();
    })();

    /* ===== Utility: debounce ===== */
    function debounce(fn, wait){
      let t; return function(){ clearTimeout(t); t = setTimeout(()=>fn.apply(this, arguments), wait); };
    }

    /* Optional: expose progress to console for debugging (dev only) */
    // window.__HE_progress = () => progress;

  </script>
</body>
</html>
