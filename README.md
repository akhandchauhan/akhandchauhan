<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Akhand Chauhan — Data Engineer</title>

<style>
:root{
  --primary:#00bfff;
  --secondary:#1e90ff;
  --ink:#0f172a;
  --glass:rgba(255,255,255,.85);
}

*{box-sizing:border-box}
html,body{
  margin:0;
  font-family:-apple-system,BlinkMacSystemFont,"SF Pro Display","Inter",sans-serif;
  color:var(--ink);
  background:#ffffff;
}

/* ---------- BACKGROUND ---------- */
.grid-background{
  position:fixed;
  inset:0;
  background:
    linear-gradient(rgba(0,191,255,.04) 1px,transparent 1px),
    linear-gradient(90deg,rgba(0,191,255,.04) 1px,transparent 1px);
  background-size:48px 48px;
  animation:gridMove 40s linear infinite;
  z-index:-2;
}
@keyframes gridMove{to{transform:translate(48px,48px)}}

.orb{
  position:fixed;
  width:420px;height:420px;
  background:radial-gradient(circle,var(--primary),transparent 70%);
  opacity:.18;
  filter:blur(90px);
  z-index:-1;
  animation:orbFloat 18s ease-in-out infinite;
}
.orb.one{top:-10%;left:-10%}
.orb.two{bottom:-15%;right:-10%;animation-delay:6s}
@keyframes orbFloat{
  50%{transform:translate(40px,-30px) scale(1.08)}
}

/* ---------- LAYOUT ---------- */
.container{
  max-width:1200px;
  margin:auto;
  padding:90px 28px;
}

/* ---------- HERO ---------- */
header{
  text-align:center;
  margin-bottom:100px;
}
header h1{
  font-size:4.2rem;
  font-weight:800;
  background:linear-gradient(120deg,#020617,var(--primary),var(--secondary));
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
  letter-spacing:-1.8px;
}
header p{
  margin-top:18px;
  font-size:1.4rem;
  color:var(--primary);
}

/* ---------- CARDS ---------- */
.card{
  background:var(--glass);
  backdrop-filter:blur(18px);
  border-radius:28px;
  padding:42px;
  margin-bottom:70px;
  border:1px solid rgba(0,191,255,.18);
  box-shadow:0 30px 70px rgba(0,191,255,.12);
  transition:.5s cubic-bezier(.22,1,.36,1);
}
.card:hover{
  transform:translateY(-10px);
  box-shadow:0 40px 90px rgba(0,191,255,.22);
}

/* ---------- TITLES ---------- */
h2{
  font-size:2.4rem;
  margin-bottom:30px;
  position:relative;
}
h2::after{
  content:"";
  display:block;
  width:60px;
  height:4px;
  margin-top:10px;
  background:linear-gradient(90deg,var(--primary),var(--secondary));
  border-radius:3px;
}

/* ---------- ABOUT ---------- */
.about li{
  list-style:none;
  padding:18px 22px;
  margin-bottom:14px;
  border-left:4px solid var(--primary);
  background:linear-gradient(90deg,rgba(0,191,255,.08),transparent);
  border-radius:12px;
  transition:.35s ease;
}
.about li:hover{
  transform:translateX(10px);
  background:linear-gradient(90deg,rgba(0,191,255,.18),transparent);
}

/* ---------- TECH STACK ---------- */
.tech-grid{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(260px,1fr));
  gap:24px;
}
.tech{
  padding:28px;
  border-radius:20px;
  background:linear-gradient(145deg,rgba(0,191,255,.05),rgba(0,191,255,.1));
  border:1px solid rgba(0,191,255,.18);
}
.tech h3{
  color:var(--primary);
  margin-bottom:18px;
}
.tag{
  display:inline-block;
  margin:6px;
  padding:10px 18px;
  border-radius:999px;
  border:1px solid rgba(0,191,255,.3);
  background:rgba(0,191,255,.08);
  transition:.3s;
}
.tag:hover{
  transform:scale(1.1);
  background:var(--primary);
  color:white;
}

/* ---------- ACHIEVEMENTS ---------- */
.achievements{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
  gap:26px;
}
.badge{
  padding:36px;
  text-align:center;
  border-radius:22px;
  background:linear-gradient(145deg,rgba(0,191,255,.08),rgba(0,191,255,.14));
  transition:.4s;
}
.badge:hover{
  transform:translateY(-12px) scale(1.05);
}
.badge span{
  font-size:3rem;
  display:block;
  margin-bottom:12px;
}

/* ---------- FOOTER ---------- */
footer{
  text-align:center;
  font-size:1.6rem;
  font-weight:600;
  margin-top:100px;
  background:linear-gradient(90deg,var(--primary),var(--secondary),var(--primary));
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
  animation:shine 4s linear infinite;
}
@keyframes shine{to{background-position:200%}}

@media(max-width:768px){
  header h1{font-size:2.8rem}
}
</style>
</head>

<body>
<div class="grid-background"></div>
<div class="orb one"></div>
<div class="orb two"></div>

<div class="container">

<header>
  <h1>Hi, I'm Akhand Chauhan</h1>
  <p>Data Engineer • Cloud • Distributed Systems • MLOps</p>
</header>

<section class="card">
<h2>🧠 About Me</h2>
<ul class="about">
<li>🚀 Production-grade data pipelines</li>
<li>📊 Reliability, observability & scale</li>
<li>☁️ AWS-native data engineering</li>
<li>🔁 Batch & streaming ETL</li>
<li>🧪 MLOps-driven workflows</li>
</ul>
</section>

<section class="card">
<h2>🛠 Tech Stack</h2>
<div class="tech-grid">
  <div class="tech">
    <h3>Languages</h3>
    <span class="tag">Python</span><span class="tag">SQL</span>
    <span class="tag">Pandas</span><span class="tag">NumPy</span>
  </div>
  <div class="tech">
    <h3>Data & Orchestration</h3>
    <span class="tag">PySpark</span><span class="tag">Airflow</span>
  </div>
  <div class="tech">
    <h3>AWS</h3>
    <span class="tag">S3</span><span class="tag">Glue</span>
    <span class="tag">Redshift</span><span class="tag">Athena</span>
    <span class="tag">EMR</span><span class="tag">Kinesis</span>
  </div>
  <div class="tech">
    <h3>MLOps</h3>
    <span class="tag">MLflow</span><span class="tag">DVC</span>
  </div>
  <div class="tech">
    <h3>DevOps</h3>
    <span class="tag">Docker</span><span class="tag">Kubernetes</span>
    <span class="tag">GitHub</span>
  </div>
</div>
</section>

<section class="card">
<h2>🏆 Achievements</h2>
<div class="achievements">
  <div class="badge"><span>🚀</span>Production Systems</div>
  <div class="badge"><span>⚡</span>High Performance</div>
  <div class="badge"><span>🎯</span>Mission Critical</div>
  <div class="badge"><span>🔒</span>Secure & Reliable</div>
</div>
</section>

<footer>
⚡ Engineering data systems that scale, observe, and endure.
</footer>

</div>
</body>
</html>
