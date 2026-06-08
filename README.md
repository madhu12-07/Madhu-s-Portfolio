# Madhu's Portfolio
"My Personal portfolio showcasing my projects and technical skills"
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Madhubala Raghavi K</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,700;0,900;1,700&family=DM+Sans:wght@300;400;500&family=DM+Mono:wght@400;500&display=swap" rel="stylesheet"/>
<style>
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}

:root{
  /* Warm golds */
  --gold-bright:#FBCF84;
  --gold-mid:#DDB26A;
  --gold-deep:#D8973C;

  /* Deep blues */
  --navy:#1E355F;
  --ocean:#004E64;

  /* Cool lights */
  --sky:#B2C8ED;
  --ice:#C7DDEB;
  --pale-blue:#ECFAFF;
  --cool-light:#E0E5E9;
  --grey-blue:#9EABB4;
  --steel:#D3DBE6;

  /* Warm lights */
  --cream:#FFFAE3;

  /* Warm darks */
  --burgundy:#29090A;
  --wine:#72393F;
  --rust:#A9634A;

  /* Main composition choices */
  --bg: var(--cream);
  --surface: #fff;
  --text-dark: var(--navy);
  --text-body: #3a4a62;
  --text-muted: var(--grey-blue);
  --accent: var(--gold-deep);
  --accent-light: var(--gold-bright);
  --highlight: var(--ocean);
  --border: var(--steel);
}

html{scroll-behavior:smooth}

body{
  font-family:'DM Sans',sans-serif;
  background:var(--cream);
  color:var(--text-dark);
  overflow-x:hidden;
  cursor:none;
}

/* ── Custom Cursor ── */
#cur-dot{
  position:fixed;width:10px;height:10px;
  background:var(--gold-deep);border-radius:50%;
  pointer-events:none;z-index:9999;
  transform:translate(-50%,-50%);
  transition:transform .15s,width .2s,height .2s,background .2s;
}
#cur-ring{
  position:fixed;width:36px;height:36px;
  border:1.5px solid var(--gold-mid);border-radius:50%;
  pointer-events:none;z-index:9998;
  transform:translate(-50%,-50%);
  opacity:.5;
  transition:border-color .3s;
}
body:has(a:hover) #cur-dot{width:14px;height:14px;background:var(--ocean)}
body:has(a:hover) #cur-ring{border-color:var(--ocean);opacity:.7}

/* ── Nav ── */
nav{
  position:fixed;top:0;left:0;right:0;z-index:200;
  height:68px;
  display:flex;align-items:center;justify-content:space-between;
  padding:0 6vw;
  background:rgba(255,250,227,.9);
  backdrop-filter:blur(20px);
  border-bottom:1px solid var(--steel);
}
.logo{
  font-family:'Playfair Display',serif;
  font-size:1rem;font-weight:700;
  color:var(--navy);letter-spacing:.02em;
}
.logo span{color:var(--gold-deep)}
.nav-links{display:flex;gap:2.2rem;list-style:none}
.nav-links a{
  font-family:'DM Mono',monospace;
  font-size:.65rem;font-weight:500;
  letter-spacing:.14em;text-transform:uppercase;
  color:var(--grey-blue);text-decoration:none;
  transition:color .2s;
}
.nav-links a:hover{color:var(--gold-deep)}

/* ── Hero ── */
#hero{
  min-height:100vh;
  display:grid;grid-template-columns:1fr 1fr;
  padding-top:68px;
  position:relative;overflow:hidden;
}

.hero-left{
  background:var(--navy);
  display:flex;flex-direction:column;justify-content:center;
  padding:6rem 5vw 6rem 7vw;
  position:relative;overflow:hidden;
}
.hero-left::before{
  content:'';
  position:absolute;top:-100px;right:-100px;
  width:400px;height:400px;
  border-radius:50%;
  background:radial-gradient(circle, rgba(251,207,132,.12) 0%, transparent 70%);
}
.hero-left::after{
  content:'MK';
  position:absolute;bottom:-1rem;left:-1.5rem;
  font-family:'Playfair Display',serif;
  font-size:14rem;font-weight:900;font-style:italic;
  color:rgba(255,255,255,.03);
  line-height:1;
  pointer-events:none;
  user-select:none;
}

.hero-tag{
  display:inline-flex;align-items:center;gap:.6rem;
  margin-bottom:2.5rem;
}
.hero-tag-line{width:24px;height:1px;background:var(--gold-deep)}
.hero-tag-text{
  font-family:'DM Mono',monospace;
  font-size:.65rem;letter-spacing:.2em;text-transform:uppercase;
  color:var(--gold-mid);
}

.hero-name{
  font-family:'Playfair Display',serif;
  font-size:clamp(2.8rem,5.5vw,5rem);
  font-weight:900;line-height:.95;
  color:#fff;
  margin-bottom:1.4rem;
}
.hero-name em{
  font-style:italic;
  color:var(--gold-bright);
}

.hero-role{
  font-family:'DM Mono',monospace;
  font-size:.72rem;letter-spacing:.22em;text-transform:uppercase;
  color:var(--sky);margin-bottom:2rem;
}

.hero-desc{
  font-size:.95rem;line-height:1.85;
  color:rgba(178,200,237,.75);
  max-width:420px;margin-bottom:3rem;
}

.hero-btns{display:flex;gap:.8rem;flex-wrap:wrap}
.btn{
  padding:.75rem 1.8rem;
  font-family:'DM Mono',monospace;
  font-size:.65rem;font-weight:500;letter-spacing:.12em;text-transform:uppercase;
  text-decoration:none;cursor:none;
  transition:all .25s;display:inline-block;border:none;
}
.btn-gold{background:var(--gold-deep);color:var(--cream)}
.btn-gold:hover{background:var(--gold-bright);color:var(--navy)}
.btn-outline{
  border:1px solid rgba(178,200,237,.3);
  color:rgba(178,200,237,.7);background:transparent;
}
.btn-outline:hover{border-color:var(--gold-mid);color:var(--gold-mid)}

.hero-right{
  background:var(--cream);
  display:flex;flex-direction:column;
  justify-content:center;align-items:flex-start;
  padding:6rem 7vw 6rem 5vw;
  position:relative;
}
.hero-right::before{
  content:'';position:absolute;
  bottom:0;right:0;
  width:60%;height:60%;
  background:linear-gradient(135deg, var(--pale-blue) 0%, transparent 70%);
  pointer-events:none;
}

.stats-vertical{display:flex;flex-direction:column;gap:3rem;position:relative;z-index:1}
.stat-row{display:flex;align-items:flex-end;gap:1.2rem}
.stat-big{
  font-family:'Playfair Display',serif;
  font-size:4.5rem;font-weight:900;font-style:italic;
  color:var(--navy);line-height:1;
}
.stat-info{}
.stat-label{
  font-family:'DM Mono',monospace;
  font-size:.6rem;letter-spacing:.16em;text-transform:uppercase;
  color:var(--grey-blue);margin-bottom:.2rem;
}
.stat-desc{font-size:.82rem;color:var(--text-body);font-weight:500}

.hero-decor{
  position:absolute;top:3rem;right:4rem;
  display:flex;flex-direction:column;gap:.5rem;
  opacity:.5;
}
.decor-square{width:8px;height:8px;background:var(--gold-mid)}
.decor-square:nth-child(2){background:var(--sky);margin-left:12px}
.decor-square:nth-child(3){background:var(--steel)}

/* ── Section Base ── */
.section{padding:8rem 7vw}
.section-inner{max-width:1120px;margin:0 auto}
.sec-eyebrow{
  display:flex;align-items:center;gap:.8rem;
  margin-bottom:1rem;
}
.sec-eye-num{
  font-family:'DM Mono',monospace;
  font-size:.6rem;letter-spacing:.22em;text-transform:uppercase;
  color:var(--gold-deep);
}
.sec-eye-line{flex:1;max-width:40px;height:1px;background:var(--gold-deep);opacity:.4}
.sec-title{
  font-family:'Playfair Display',serif;
  font-size:clamp(2rem,3.5vw,3rem);
  font-weight:900;line-height:1.05;
  color:var(--navy);
  margin-bottom:3.5rem;
}
.sec-title em{font-style:italic;color:var(--gold-deep)}

/* ── Skills ── */
#skills{background:var(--surface)}

.skills-wrap{display:flex;flex-wrap:wrap;gap:.6rem}
.skill-tag{
  font-family:'DM Mono',monospace;
  font-size:.72rem;font-weight:500;letter-spacing:.08em;
  padding:.55rem 1.25rem;
  border:1px solid var(--steel);
  color:var(--navy);
  background:var(--cream);
  transition:all .22s;cursor:default;
  position:relative;overflow:hidden;
}
.skill-tag::before{
  content:'';position:absolute;inset:0;
  background:var(--navy);
  transform:translateX(-101%);
  transition:transform .22s ease;
  z-index:0;
}
.skill-tag span{position:relative;z-index:1}
.skill-tag:hover{color:#fff;border-color:var(--navy)}
.skill-tag:hover::before{transform:translateX(0)}

/* ── Education ── */
#education{background:var(--cream)}
.edu-list{display:flex;flex-direction:column}
.edu-item{
  display:grid;grid-template-columns:180px 1fr;
  gap:2.5rem;
  padding:2.5rem 0;
  border-bottom:1px solid var(--steel);
  transition:all .2s;
  position:relative;
}
.edu-item:first-child{border-top:1px solid var(--steel)}
.edu-item::after{
  content:'';position:absolute;left:0;top:0;bottom:0;
  width:3px;background:var(--gold-deep);
  transform:scaleY(0);transition:transform .25s;
  transform-origin:top;
}
.edu-item:hover::after{transform:scaleY(1)}
.edu-item:hover{padding-left:1rem}

.edu-year{
  font-family:'DM Mono',monospace;
  font-size:.65rem;letter-spacing:.14em;text-transform:uppercase;
  color:var(--grey-blue);padding-top:.35rem;
}
.edu-degree{
  font-family:'Playfair Display',serif;
  font-size:1.1rem;font-weight:700;
  color:var(--navy);margin-bottom:.35rem;line-height:1.3;
}
.edu-school{font-size:.88rem;color:var(--text-body);margin-bottom:.7rem}
.edu-score{
  display:inline-block;
  font-family:'DM Mono',monospace;
  font-size:.65rem;letter-spacing:.12em;text-transform:uppercase;
  padding:.3rem .8rem;
  background:var(--pale-blue);
  color:var(--ocean);
  border:1px solid var(--ice);
}

/* ── Certificates ── */
#certificates{
  background:var(--navy);
  position:relative;overflow:hidden;
}
#certificates::before{
  content:'';position:absolute;
  top:-200px;right:-200px;
  width:600px;height:600px;border-radius:50%;
  background:radial-gradient(circle, rgba(251,207,132,.07) 0%, transparent 65%);
}
#certificates .sec-eye-num{color:var(--gold-bright)}
#certificates .sec-eye-line{background:var(--gold-mid)}
#certificates .sec-title{color:#fff}
#certificates .sec-title em{color:var(--gold-bright)}

.certs-grid{
  display:grid;
  grid-template-columns:repeat(auto-fill,minmax(260px,1fr));
  gap:1px;
  background:rgba(255,255,255,.06);
}
.cert-card{
  background:var(--navy);
  padding:2.2rem;
  transition:background .25s;
  border-top:2px solid transparent;
  position:relative;overflow:hidden;
}
.cert-card::before{
  content:'';position:absolute;bottom:0;left:0;right:0;
  height:2px;background:linear-gradient(90deg, var(--gold-mid), var(--gold-bright));
  transform:scaleX(0);transition:transform .3s;
  transform-origin:left;
}
.cert-card:hover{background:#17294d}
.cert-card:hover::before{transform:scaleX(1)}
.cert-date{
  font-family:'DM Mono',monospace;
  font-size:.62rem;letter-spacing:.16em;text-transform:uppercase;
  color:var(--gold-mid);margin-bottom:.9rem;
}
.cert-name{
  font-family:'Playfair Display',serif;
  font-size:1rem;font-weight:700;
  color:#fff;line-height:1.4;
}

/* ── Projects ── */
#projects{background:var(--cool-light)}
.projects-grid{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:1.5rem;
}
.project-card{
  background:var(--surface);
  padding:3rem;
  border:1px solid var(--steel);
  position:relative;overflow:hidden;
  transition:all .25s;
}
.project-card:first-child{
  border-top:3px solid var(--gold-deep);
}
.project-card:last-child{
  border-top:3px solid var(--gold-mid);
}
.project-card:hover{
  transform:translateY(-4px);
  box-shadow:0 20px 60px rgba(30,53,95,.1);
}
.proj-num{
  font-family:'Playfair Display',serif;
  font-size:5rem;font-weight:900;font-style:italic;
  color:var(--steel);line-height:1;
  margin-bottom:1.5rem;
}
.proj-stack{
  font-family:'DM Mono',monospace;
  font-size:.62rem;letter-spacing:.16em;text-transform:uppercase;
  margin-bottom:.6rem;
}
.project-card:first-child .proj-stack{color:var(--gold-deep)}
.project-card:last-child .proj-stack{color:var(--gold-mid)}
.proj-title{
  font-family:'Playfair Display',serif;
  font-size:1.15rem;font-weight:700;
  color:var(--navy);line-height:1.35;margin-bottom:1.5rem;
}
.proj-pts{list-style:none;display:flex;flex-direction:column;gap:.6rem}
.proj-pts li{
  font-size:.88rem;color:var(--text-body);
  padding-left:1.2rem;position:relative;line-height:1.6;
}
.proj-pts li::before{
  content:'';position:absolute;left:0;top:.65rem;
  width:5px;height:5px;border-radius:50%;
}
.project-card:first-child .proj-pts li::before{background:var(--gold-mid)}
.project-card:last-child .proj-pts li::before{background:var(--gold-bright)}

/* ── Workshops ── */
#workshops{background:var(--surface)}
.ws-grid{
  display:grid;
  grid-template-columns:repeat(auto-fill,minmax(230px,1fr));
  gap:1rem;
}
.ws-card{
  padding:1.8rem;
  border:1px solid var(--steel);
  background:var(--cream);
  display:flex;align-items:flex-start;gap:1rem;
  transition:all .22s;
  position:relative;overflow:hidden;
}
.ws-card::before{
  content:'';position:absolute;top:0;left:0;right:0;
  height:2px;
  background:linear-gradient(90deg, var(--gold-bright), var(--sky));
  transform:scaleX(0);transition:transform .3s;transform-origin:left;
}
.ws-card:hover{border-color:var(--gold-mid);transform:translateY(-3px)}
.ws-card:hover::before{transform:scaleX(1)}
.ws-icon{
  width:8px;height:8px;border-radius:50%;
  background:var(--gold-deep);flex-shrink:0;margin-top:.55rem;
}
.ws-name{font-size:.9rem;font-weight:500;color:var(--navy);line-height:1.55}

/* ── About Me ── */
#additional{
  background:var(--navy);
  position:relative;overflow:hidden;
}
#additional::after{
  content:'';position:absolute;
  bottom:-150px;left:-150px;
  width:500px;height:500px;border-radius:50%;
  background:radial-gradient(circle, rgba(0,78,100,.35) 0%, transparent 65%);
}
#additional .sec-eye-num{color:var(--gold-bright)}
#additional .sec-eye-line{background:var(--gold-mid)}
#additional .sec-title{color:#fff}
#additional .sec-title em{color:var(--gold-bright)}

.about-grid{
  display:grid;grid-template-columns:repeat(3,1fr);gap:1.5rem;
  position:relative;z-index:1;
}
.about-card{
  padding:2.5rem;
  border:1px solid rgba(255,255,255,.08);
  background:rgba(255,255,255,.04);
  border-left:3px solid var(--gold-mid);
  transition:background .25s;
}
.about-card:nth-child(2){border-left-color:var(--ice)}
.about-card:nth-child(3){border-left-color:var(--rust)}
.about-card:hover{background:rgba(255,255,255,.07)}
.about-text{
  font-size:.95rem;color:rgba(199,221,235,.8);line-height:1.75;
}

/* ── Contact ── */
#contact{
  background:var(--cream);
  padding:8rem 7vw;
  position:relative;overflow:hidden;
}
#contact::before{
  content:'';
  position:absolute;top:0;right:0;bottom:0;
  width:38%;
  background:linear-gradient(160deg, var(--pale-blue) 0%, var(--ice) 40%, transparent 85%);
  pointer-events:none;
}
.contact-inner{max-width:680px;position:relative;z-index:1}
.contact-eyebrow{
  display:flex;align-items:center;gap:.8rem;margin-bottom:1rem;
}
.contact-eyebrow-line{width:24px;height:1px;background:var(--gold-deep)}
.contact-eyebrow-text{
  font-family:'DM Mono',monospace;
  font-size:.62rem;letter-spacing:.2em;text-transform:uppercase;color:var(--gold-deep);
}
.contact-title{
  font-family:'Playfair Display',serif;
  font-size:clamp(2.5rem,5vw,4rem);
  font-weight:900;line-height:1;
  color:var(--navy);margin-bottom:.6rem;
}
.contact-title em{font-style:italic;color:var(--gold-deep)}
.contact-sub{
  font-size:.92rem;color:var(--grey-blue);
  margin-bottom:3rem;letter-spacing:.04em;
}
.contact-btns{display:flex;gap:.8rem;flex-wrap:wrap;margin-bottom:4rem}
.cbtn{
  padding:.85rem 2rem;
  font-family:'DM Mono',monospace;
  font-size:.65rem;font-weight:500;letter-spacing:.12em;text-transform:uppercase;
  text-decoration:none;cursor:none;transition:all .25s;
}
.cbtn-fill{background:var(--navy);color:var(--cream)}
.cbtn-fill:hover{background:var(--gold-deep);color:var(--cream)}
.cbtn-ghost{
  border:1.5px solid var(--navy);
  color:var(--navy);background:transparent;
}
.cbtn-ghost:hover{border-color:var(--gold-deep);color:var(--gold-deep)}

.contact-info{
  display:flex;gap:3rem;flex-wrap:wrap;
  padding-top:3rem;border-top:1px solid var(--steel);
}
.ci{}
.ci-label{
  font-family:'DM Mono',monospace;
  font-size:.58rem;letter-spacing:.16em;text-transform:uppercase;
  color:var(--grey-blue);margin-bottom:.4rem;
}
.ci-val{font-size:.9rem;font-weight:500;color:var(--navy)}
.ci-val a{color:var(--navy);text-decoration:none;transition:color .2s}
.ci-val a:hover{color:var(--gold-deep)}

/* ── Footer ── */
footer{
  background:var(--burgundy);
  color:rgba(255,255,255,.25);
  text-align:center;
  padding:1.4rem;
  font-family:'DM Mono',monospace;
  font-size:.58rem;letter-spacing:.14em;text-transform:uppercase;
}

/* ── Reveal animations ── */
.r{opacity:0;transform:translateY(28px);transition:opacity .7s ease,transform .7s ease}
.r.v{opacity:1;transform:none}
.r-left{opacity:0;transform:translateX(-28px);transition:opacity .7s ease,transform .7s ease}
.r-left.v{opacity:1;transform:none}

/* ── Responsive ── */
@media(max-width:900px){
  /* Nav */
  .nav-links{display:none}

  /* Hero */
  #hero{grid-template-columns:1fr}
  .hero-right{display:none}
  .hero-left{padding:5rem 6vw 4rem}
  .hero-name{font-size:clamp(2.4rem,10vw,3.6rem)}

  /* Sections */
  .section{padding:5rem 6vw}

  /* Projects */
  .projects-grid{grid-template-columns:1fr}
  .project-card{padding:2rem}

  /* About */
  .about-grid{grid-template-columns:1fr}

  /* Education */
  .edu-item{grid-template-columns:1fr;gap:.4rem}
  .edu-year{padding-top:0}

  /* Certs */
  .certs-grid{grid-template-columns:1fr 1fr}

  /* Contact */
  #contact{padding:5rem 6vw}
  #contact::before{display:none}
  .contact-info{gap:1.5rem}
  .contact-title{font-size:clamp(2rem,8vw,3rem)}
}

@media(max-width:560px){
  /* Hero */
  .hero-left{padding:4rem 5vw 3rem}
  .hero-desc{font-size:.88rem}
  .hero-btns{flex-direction:column;gap:.6rem}
  .btn{text-align:center}

  /* Sections */
  .section{padding:4rem 5vw}
  .sec-title{font-size:1.7rem}

  /* Certs */
  .certs-grid{grid-template-columns:1fr}

  /* Workshops */
  .ws-grid{grid-template-columns:1fr}

  /* Projects */
  .project-card{padding:1.6rem}
  .proj-num{font-size:3.5rem}

  /* Contact */
  #contact{padding:4rem 5vw}
  .contact-btns{flex-direction:column;gap:.6rem}
  .cbtn{text-align:center}
  .contact-info{flex-direction:column;gap:1.2rem}

  /* Footer */
  footer{font-size:.52rem;padding:1.2rem .8rem}
}
</style>
</head>
<body>

<div id="cur-dot"></div>
<div id="cur-ring"></div>

<nav>
  <div class="logo">Madhubala <span>Raghavi</span> K</div>
  <ul class="nav-links">
    <li><a href="#skills">Skills</a></li>
    <li><a href="#education">Education</a></li>
    <li><a href="#certificates">Certs</a></li>
    <li><a href="#projects">Projects</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<!-- HERO -->
<section id="hero">
  <div class="hero-left">
    <div class="hero-tag r">
      <span class="hero-tag-line"></span>
      <span class="hero-tag-text">Open to Internships</span>
    </div>
    <h1 class="hero-name r" style="transition-delay:.1s">
      Madhubala<br/><em>Raghavi K</em>
    </h1>
    <p class="hero-role r" style="transition-delay:.18s">Computer Science Student</p>
    <p class="hero-desc r" style="transition-delay:.26s">
      Enthusiastic CS student with hands-on experience in Oracle APEX, SQL, and web development — seeking opportunities to grow through practical, real-world collaboration.
    </p>
    <div class="hero-btns r" style="transition-delay:.34s">
      <a href="#projects" class="btn btn-gold">View Projects</a>
      <a href="mailto:007.madhukrishnan@gmail.com" class="btn btn-outline">Get in Touch</a>
    </div>
  </div>

  <div class="hero-right">
    <div class="hero-decor">
      <div class="decor-square"></div>
      <div class="decor-square"></div>
      <div class="decor-square"></div>
    </div>
    <div class="stats-vertical">
      <div class="stat-row r" style="transition-delay:.2s">
        <div class="stat-big">5+</div>
        <div class="stat-info">
          <div class="stat-label">Certificates</div>
          <div class="stat-desc">Industry courses</div>
        </div>
      </div>
      <div class="stat-row r" style="transition-delay:.32s">
        <div class="stat-big">2</div>
        <div class="stat-info">
          <div class="stat-label">Projects</div>
          <div class="stat-desc">Live applications</div>
        </div>
      </div>
      <div class="stat-row r" style="transition-delay:.44s">
        <div class="stat-big">79<span style="font-size:2rem">%</span></div>
        <div class="stat-info">
          <div class="stat-label">CGPA</div>
          <div class="stat-desc">Academic score</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- SKILLS -->
<section id="skills" class="section">
  <div class="section-inner">
    <div class="sec-eyebrow r">
      <span class="sec-eye-num">01 — What I Know</span>
      <span class="sec-eye-line"></span>
    </div>
    <h2 class="sec-title r" style="transition-delay:.06s">Technical <em>Expertise</em></h2>
    <div class="skills-wrap r" style="transition-delay:.14s">
      <div class="skill-tag"><span>HTML</span></div>
      <div class="skill-tag"><span>CSS</span></div>
      <div class="skill-tag"><span>Python</span></div>
      <div class="skill-tag"><span>Java</span></div>
      <div class="skill-tag"><span>C &amp; C++</span></div>
      <div class="skill-tag"><span>Oracle APEX</span></div>
      <div class="skill-tag"><span>SQL</span></div>
      <div class="skill-tag"><span>Web Designing</span></div>
      <div class="skill-tag"><span>Microsoft Office</span></div>
      <div class="skill-tag"><span>Canva Art</span></div>
      <div class="skill-tag"><span>Data Analytics</span></div>
      <div class="skill-tag"><span>Data Visualization</span></div>
    </div>
  </div>
</section>

<!-- EDUCATION -->
<section id="education" class="section">
  <div class="section-inner">
    <div class="sec-eyebrow r">
      <span class="sec-eye-num">02 — Where I Studied</span>
      <span class="sec-eye-line"></span>
    </div>
    <h2 class="sec-title r" style="transition-delay:.06s">Academic <em>Background</em></h2>
    <div class="edu-list">
      <div class="edu-item r">
        <div class="edu-year">2024 – Present</div>
        <div>
          <div class="edu-degree">B.Sc. Computer Science (3rd Year)</div>
          <div class="edu-school">Aladi Aruna College of Liberal Arts &amp; Science (Co-ed.)</div>
          <span class="edu-score">CGPA 79%</span>
        </div>
      </div>
      <div class="edu-item r" style="transition-delay:.08s">
        <div class="edu-year">2023 – 2024</div>
        <div>
          <div class="edu-degree">HSC (Higher Secondary Certificate)</div>
          <div class="edu-school">West Tirunelveli Higher Secondary School, Nallur</div>
          <span class="edu-score">52%</span>
        </div>
      </div>
      <div class="edu-item r" style="transition-delay:.16s">
        <div class="edu-year">2022 – 2023</div>
        <div>
          <div class="edu-degree">SSLC (Secondary School)</div>
          <div class="edu-school">Sri Ramakrishna Matric Higher Secondary School, Alangulam</div>
          <span class="edu-score">60%</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- CERTIFICATES -->
<section id="certificates" class="section">
  <div class="section-inner">
    <div class="sec-eyebrow r">
      <span class="sec-eye-num">03 — What I Earned</span>
      <span class="sec-eye-line"></span>
    </div>
    <h2 class="sec-title r" style="transition-delay:.06s">Credentials &amp; <em>Courses</em></h2>
    <div class="certs-grid r" style="transition-delay:.14s">
      <div class="cert-card">
        <div class="cert-date">November 2025</div>
        <div class="cert-name">Naan Mudhalvan – Oracle APEX Certificate</div>
      </div>
      <div class="cert-card">
        <div class="cert-date">October 2025</div>
        <div class="cert-name">Python Full Stack Development Course</div>
      </div>
      <div class="cert-card">
        <div class="cert-date">June – July 2025</div>
        <div class="cert-name">UI/UX Design Basics</div>
      </div>
      <div class="cert-card">
        <div class="cert-date">July 2025</div>
        <div class="cert-name">English Communication Course</div>
      </div>
      <div class="cert-card">
        <div class="cert-date">February 2020</div>
        <div class="cert-name">Programming in C &amp; C++ (SUITS)</div>
      </div>
    </div>
  </div>
</section>

<!-- PROJECTS -->
<section id="projects" class="section">
  <div class="section-inner">
    <div class="sec-eyebrow r">
      <span class="sec-eye-num">04 — What I Built</span>
      <span class="sec-eye-line"></span>
    </div>
    <h2 class="sec-title r" style="transition-delay:.06s">Featured <em>Work</em></h2>
    <div class="projects-grid r" style="transition-delay:.14s">
      <div class="project-card">
        <div class="proj-num">01</div>
        <div class="proj-stack">Oracle APEX · SQL</div>
        <div class="proj-title">Students Data Management System (Heart Failure Analysis)</div>
        <ul class="proj-pts">
          <li>Built a web application using Oracle APEX and SQL</li>
          <li>Entered student data and generated analytical reports</li>
        </ul>
      </div>
      <div class="project-card">
        <div class="proj-num">02</div>
        <div class="proj-stack">Oracle APEX · Data Viz</div>
        <div class="proj-title">Data Analytics and Visualization</div>
        <ul class="proj-pts">
          <li>Created a data analysis project using SQL and Oracle APEX</li>
          <li>Analyzed student data and generated detailed reports</li>
          <li>Designed bar, pie, and line charts for visualization</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<!-- WORKSHOPS -->
<section id="workshops" class="section">
  <div class="section-inner">
    <div class="sec-eyebrow r">
      <span class="sec-eye-num">05 — How I Trained</span>
      <span class="sec-eye-line"></span>
    </div>
    <h2 class="sec-title r" style="transition-delay:.06s">Workshops &amp; <em>Webinars</em></h2>
    <div class="ws-grid">
      <div class="ws-card r">
        <div class="ws-icon"></div>
        <div class="ws-name">UI/UX Fundamentals</div>
      </div>
      <div class="ws-card r" style="transition-delay:.07s">
        <div class="ws-icon"></div>
        <div class="ws-name">Hands-on Training of Web Designing</div>
      </div>
      <div class="ws-card r" style="transition-delay:.14s">
        <div class="ws-icon"></div>
        <div class="ws-name">Chatbot Development Basics</div>
      </div>
      <div class="ws-card r" style="transition-delay:.21s">
        <div class="ws-icon"></div>
        <div class="ws-name">Full Stack Development Basics</div>
      </div>
    </div>
  </div>
</section>

<!-- ABOUT ME -->
<section id="additional" class="section">
  <div class="section-inner">
    <div class="sec-eyebrow r">
      <span class="sec-eye-num">06 — Who I Am</span>
      <span class="sec-eye-line"></span>
    </div>
    <h2 class="sec-title r" style="transition-delay:.06s">About <em>Me</em></h2>
    <div class="about-grid">
      <div class="about-card r">
        <div class="about-text">Strong communication and teamwork skills that make every collaboration productive and enjoyable.</div>
      </div>
      <div class="about-card r" style="transition-delay:.08s">
        <div class="about-text">Quick learner who adapts rapidly to new technologies and thrives in dynamic environments.</div>
      </div>
      <div class="about-card r" style="transition-delay:.16s">
        <div class="about-text">Passionate about problem solving and building beautiful, functional web experiences.</div>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="contact-inner">
    <div class="contact-eyebrow r">
      <span class="contact-eyebrow-line"></span>
      <span class="contact-eyebrow-text">Let's Talk</span>
    </div>
    <h2 class="contact-title r" style="transition-delay:.08s">
      Let's <em>Connect</em>
    </h2>
    <p class="contact-sub r" style="transition-delay:.14s">Open to internships &amp; learning opportunities</p>
    <div class="contact-btns r" style="transition-delay:.2s">
      <a href="mailto:007.madhukrishnan@gmail.com" class="cbtn cbtn-fill">Send Email</a>
      <a href="https://github.com/madhu12-07" target="_blank" class="cbtn cbtn-ghost">GitHub Profile</a>
    </div>
    <div class="contact-info r" style="transition-delay:.28s">
      <div class="ci">
        <div class="ci-label">Email</div>
        <div class="ci-val"><a href="mailto:007.madhukrishnan@gmail.com">007.madhukrishnan@gmail.com</a></div>
      </div>
      <div class="ci">
        <div class="ci-label">GitHub</div>
        <div class="ci-val"><a href="https://github.com/madhu12-07" target="_blank">madhu12-07</a></div>
      </div>
      <div class="ci">
        <div class="ci-label">Location</div>
        <div class="ci-val">Alangulam, Tamil Nadu</div>
      </div>
    </div>
  </div>
</section>

<footer>© 2025 Madhubala Raghavi K &nbsp;·&nbsp; All rights reserved</footer>

<script>
/* ── Cursor ── */
const dot=document.getElementById('cur-dot');
const ring=document.getElementById('cur-ring');
let rx=0,ry=0,mx=0,my=0;
document.addEventListener('mousemove',e=>{
  mx=e.clientX;my=e.clientY;
  dot.style.left=mx+'px';dot.style.top=my+'px';
});
(function loop(){
  rx+=(mx-rx)*.1;ry+=(my-ry)*.1;
  ring.style.left=rx+'px';ring.style.top=ry+'px';
  requestAnimationFrame(loop);
})();

/* ── Scroll reveal ── */
const obs=new IntersectionObserver(entries=>{
  entries.forEach(e=>{if(e.isIntersecting)e.target.classList.add('v')});
},{threshold:.1});
document.querySelectorAll('.r,.r-left').forEach(el=>obs.observe(el));

/* ── Smooth scroll on nav ── */
document.querySelectorAll('a[href^="#"]').forEach(a=>{
  a.addEventListener('click',e=>{
    e.preventDefault();
    const t=document.querySelector(a.getAttribute('href'));
    if(t)t.scrollIntoView({behavior:'smooth'});
  });
});
</script>
</body>
</html>
