<!DOCTYPE html>
<style>
@import url('https://fonts.googleapis.com/css2?family=Syne:wght@400;500;600;700;800&family=DM+Mono:wght@400;500&display=swap');

*{margin:0;padding:0;box-sizing:border-box}

.wrap{
  font-family:'Syne',sans-serif;
  color:var(--color-text-primary);
  padding:0;
  max-width:680px;
}

.hero{
  position:relative;
  padding:48px 40px 40px;
  border-bottom:0.5px solid var(--color-border-tertiary);
  overflow:hidden;
}

.hero-bg{
  position:absolute;inset:0;
  background: conic-gradient(from 200deg at 80% 20%, #0a0a1a 0deg, #1a1040 40deg, #0d1a2e 80deg, #0a0a1a 120deg);
  z-index:0;
}

.hero-dots{
  position:absolute;inset:0;z-index:1;
  background-image: radial-gradient(circle, rgba(120,100,255,0.12) 1px, transparent 1px);
  background-size: 28px 28px;
}

.hero-content{position:relative;z-index:2}

.status-pill{
  display:inline-flex;align-items:center;gap:6px;
  background:rgba(255,255,255,0.06);
  border:0.5px solid rgba(255,255,255,0.15);
  border-radius:100px;
  padding:5px 14px;
  font-size:11px;letter-spacing:0.08em;text-transform:uppercase;
  color:rgba(255,255,255,0.6);
  margin-bottom:20px;
  font-family:'DM Mono',monospace;
}

.dot-live{
  width:6px;height:6px;border-radius:50%;
  background:#4ade80;
  box-shadow:0 0 6px #4ade80;
  animation:pulse 2s infinite;
}

@keyframes pulse{0%,100%{opacity:1}50%{opacity:0.4}}

.hero h1{
  font-size:42px;font-weight:800;line-height:1.05;
  color:#fff;
  margin-bottom:6px;
  letter-spacing:-0.02em;
}

.hero h1 span{
  background: linear-gradient(135deg, #a78bfa 0%, #60a5fa 50%, #34d399 100%);
  -webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;
}

.hero-sub{
  font-size:14px;
  color:rgba(255,255,255,0.45);
  font-family:'DM Mono',monospace;
  margin-bottom:28px;
  letter-spacing:0.03em;
}

.hero-tags{display:flex;flex-wrap:wrap;gap:8px;margin-bottom:32px}

.tag{
  font-size:12px;padding:5px 12px;border-radius:4px;
  font-family:'DM Mono',monospace;letter-spacing:0.04em;
  background:rgba(255,255,255,0.06);
  border:0.5px solid rgba(255,255,255,0.12);
  color:rgba(255,255,255,0.55);
}

.tag.accent{
  background:rgba(167,139,250,0.12);
  border-color:rgba(167,139,250,0.3);
  color:#c4b5fd;
}

.hero-links{display:flex;flex-wrap:wrap;gap:10px}

.hero-link{
  display:inline-flex;align-items:center;gap:6px;
  padding:8px 16px;border-radius:6px;
  font-size:12px;font-weight:500;text-decoration:none;
  border:0.5px solid rgba(255,255,255,0.15);
  color:rgba(255,255,255,0.7);
  background:rgba(255,255,255,0.04);
  transition:all 0.2s;
  font-family:'DM Mono',monospace;
}
.hero-link:hover{background:rgba(255,255,255,0.1);color:#fff}
.hero-link i{font-size:15px}

.body{padding:32px 40px}

.section{margin-bottom:36px}

.section-label{
  font-size:10px;letter-spacing:0.14em;text-transform:uppercase;
  color:var(--color-text-tertiary);
  font-family:'DM Mono',monospace;
  margin-bottom:16px;
  display:flex;align-items:center;gap:10px;
}
.section-label::after{content:'';flex:1;height:0.5px;background:var(--color-border-tertiary)}

.stack-grid{
  display:grid;grid-template-columns:repeat(auto-fill,minmax(130px,1fr));gap:8px;
}

.stack-card{
  border:0.5px solid var(--color-border-tertiary);
  border-radius:var(--border-radius-md);
  padding:12px 14px;
  background:var(--color-background-primary);
  transition:border-color 0.2s,transform 0.15s;
  cursor:default;
}
.stack-card:hover{border-color:var(--color-border-primary);transform:translateY(-2px)}

.stack-icon{font-size:22px;margin-bottom:6px;display:block}
.stack-name{font-size:12px;font-weight:500;margin-bottom:2px}
.stack-type{font-size:11px;color:var(--color-text-tertiary);font-family:'DM Mono',monospace}

.focus-list{display:flex;flex-direction:column;gap:8px}

.focus-item{
  display:flex;align-items:center;gap:12px;
  padding:12px 16px;
  border:0.5px solid var(--color-border-tertiary);
  border-radius:var(--border-radius-md);
  background:var(--color-background-primary);
  font-size:13px;
}

.focus-num{
  font-family:'DM Mono',monospace;font-size:11px;
  color:var(--color-text-tertiary);min-width:20px;
}

.connect-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:8px}

.connect-btn{
  display:flex;align-items:center;justify-content:center;gap:8px;
  padding:12px;border-radius:var(--border-radius-md);
  font-size:12px;font-weight:500;text-decoration:none;
  border:0.5px solid var(--color-border-tertiary);
  color:var(--color-text-secondary);
  background:var(--color-background-primary);
  transition:all 0.18s;
  font-family:'DM Mono',monospace;
}
.connect-btn:hover{border-color:var(--color-border-secondary);color:var(--color-text-primary);transform:translateY(-1px)}
.connect-btn i{font-size:16px}

.quote{
  border-left:2px solid rgba(167,139,250,0.5);
  padding:12px 16px;
  margin-top:36px;
  font-size:13px;font-style:italic;
  color:var(--color-text-secondary);
  background:var(--color-background-secondary);
  border-radius:0 var(--border-radius-md) var(--border-radius-md) 0;
}
</style>

<div class="wrap">

<div class="hero">
  <div class="hero-bg"></div>
  <div class="hero-dots"></div>
  <div class="hero-content">
    <div class="status-pill"><span class="dot-live"></span>Available for freelance</div>
    <h1>Muhammad<br><span>Imran</span></h1>
    <div class="hero-sub">full-stack developer · freelance · 2023 →</div>
    <div class="hero-tags">
      <span class="tag accent">React</span>
      <span class="tag accent">PHP</span>
      <span class="tag accent">MySQL</span>
      <span class="tag accent">Python</span>
      <span class="tag">Bootstrap</span>
      <span class="tag">Tailwind</span>
      <span class="tag">REST APIs</span>
      <span class="tag">Git</span>
    </div>
    <div class="hero-links">
      <a class="hero-link" href="https://www.linkedin.com/in/muhammad-imran-5a9083250" target="_blank"><i class="ti ti-brand-linkedin"></i>LinkedIn</a>
      <a class="hero-link" href="https://www.instagram.com/codebyimran" target="_blank"><i class="ti ti-brand-instagram"></i>Instagram</a>
      <a class="hero-link" href="https://www.tiktok.com/@codebyimran" target="_blank"><i class="ti ti-brand-tiktok"></i>TikTok</a>
      <a class="hero-link" href="mailto:muhammadimran27584@gmail.com"><i class="ti ti-mail"></i>Email</a>
      <a class="hero-link" href="https://wa.me/923703027584" target="_blank"><i class="ti ti-brand-whatsapp"></i>WhatsApp</a>
    </div>
  </div>
</div>

<div class="body">

  <div class="section">
    <div class="section-label">About</div>
    <p style="font-size:14px;line-height:1.75;color:var(--color-text-secondary)">
      Full Stack Developer specializing in modern, responsive web applications with a focus on user experience and technical excellence. Since 2023, delivering freelance e-commerce platforms and interactive web solutions — from engaging React frontends to robust PHP/MySQL backends, complemented by Python data analysis.
    </p>
  </div>

  <div class="section">
    <div class="section-label">Tech stack</div>
    <div class="stack-grid">
      <div class="stack-card"><span class="stack-icon">⚛️</span><div class="stack-name">React.js</div><div class="stack-type">frontend</div></div>
      <div class="stack-card"><span class="stack-icon">🐘</span><div class="stack-name">PHP</div><div class="stack-type">backend</div></div>
      <div class="stack-card"><span class="stack-icon">🐬</span><div class="stack-name">MySQL</div><div class="stack-type">database</div></div>
      <div class="stack-card"><span class="stack-icon">🐍</span><div class="stack-name">Python</div><div class="stack-type">analytics</div></div>
      <div class="stack-card"><span class="stack-icon">🌊</span><div class="stack-name">Tailwind</div><div class="stack-type">styling</div></div>
      <div class="stack-card"><span class="stack-icon">🔗</span><div class="stack-name">REST APIs</div><div class="stack-type">integration</div></div>
      <div class="stack-card"><span class="stack-icon">📊</span><div class="stack-name">Pandas/NumPy</div><div class="stack-type">data</div></div>
      <div class="stack-card"><span class="stack-icon">🎨</span><div class="stack-name">Figma</div><div class="stack-type">design</div></div>
    </div>
  </div>

  <div class="section">
    <div class="section-label">Current focus</div>
    <div class="focus-list">
      <div class="focus-item"><span class="focus-num">01</span>Scalable full-stack apps with React and PHP</div>
      <div class="focus-item"><span class="focus-num">02</span>Expanding backend with Node.js and API development</div>
      <div class="focus-item"><span class="focus-num">03</span>Deep-diving Python data analysis — Pandas and NumPy</div>
      <div class="focus-item"><span class="focus-num">04</span>Performance optimization and cloud deployment</div>
      <div class="focus-item"><span class="focus-num">05</span>Accessible, responsive UI design systems</div>
    </div>
  </div>

  <div class="section">
    <div class="section-label">Connect</div>
    <div class="connect-grid">
      <a class="connect-btn" href="https://www.linkedin.com/in/muhammad-imran-5a9083250" target="_blank"><i class="ti ti-brand-linkedin"></i>LinkedIn</a>
      <a class="connect-btn" href="https://www.instagram.com/codebyimran" target="_blank"><i class="ti ti-brand-instagram"></i>Instagram</a>
      <a class="connect-btn" href="https://www.tiktok.com/@codebyimran" target="_blank"><i class="ti ti-brand-tiktok"></i>TikTok</a>
      <a class="connect-btn" href="https://www.facebook.com/share/1EakBCSgxL/" target="_blank"><i class="ti ti-brand-facebook"></i>Facebook</a>
      <a class="connect-btn" href="https://wa.me/923703027584" target="_blank"><i class="ti ti-brand-whatsapp"></i>WhatsApp</a>
      <a class="connect-btn" href="mailto:muhammadimran27584@gmail.com"><i class="ti ti-mail"></i>Gmail</a>
    </div>
  </div>

  <div class="quote">"Code with purpose, design with passion, and build with precision."</div>

</div>
</div>
