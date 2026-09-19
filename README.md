# Portfolio
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Piyush Priyadarshi | DevOps Cloud Engineer</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500;600;700&family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">

<style>
:root{
    --bg:#030712;
    --panel:#07101f;
    --panel2:#0a1425;
    --cyan:#00eaff;
    --purple:#8b5cf6;
    --green:#39ff88;
    --blue:#3b82f6;
    --pink:#ff3cac;
    --text:#e5f7ff;
    --muted:#7890a7;
    --border:rgba(0,234,255,.18);
}

*{
    box-sizing:border-box;
    margin:0;
    padding:0;
}

html{
    scroll-behavior:smooth;
}

body{
    min-height:100vh;
    color:var(--text);
    background:
        radial-gradient(circle at 15% 10%,rgba(0,234,255,.09),transparent 25%),
        radial-gradient(circle at 85% 20%,rgba(139,92,246,.10),transparent 25%),
        radial-gradient(circle at 50% 100%,rgba(57,255,136,.05),transparent 30%),
        var(--bg);
    font-family:Inter,Segoe UI,sans-serif;
    overflow-x:hidden;
}

body::before{
    content:"";
    position:fixed;
    inset:0;
    pointer-events:none;
    opacity:.12;
    background-image:
        linear-gradient(rgba(0,234,255,.08) 1px,transparent 1px),
        linear-gradient(90deg,rgba(0,234,255,.08) 1px,transparent 1px);
    background-size:45px 45px;
    mask-image:linear-gradient(to bottom,black,transparent 90%);
}

/* ================= NAV ================= */

nav{
    position:sticky;
    top:0;
    z-index:100;
    height:68px;
    display:flex;
    align-items:center;
    justify-content:space-between;
    padding:0 5vw;
    background:rgba(3,7,18,.78);
    backdrop-filter:blur(18px);
    border-bottom:1px solid rgba(0,234,255,.12);
}

.logo{
    font-family:"JetBrains Mono",monospace;
    font-weight:700;
    color:var(--cyan);
    letter-spacing:-1px;
}

.logo span{
    color:var(--purple);
}

.status{
    display:flex;
    align-items:center;
    gap:9px;
    font:500 12px "JetBrains Mono",monospace;
    color:#9bb1c7;
}

.status-dot{
    width:8px;
    height:8px;
    border-radius:50%;
    background:var(--green);
    box-shadow:0 0 12px var(--green);
    animation:pulse 1.5s infinite;
}

/* ================= HERO ================= */

.hero{
    max-width:1400px;
    margin:auto;
    padding:80px 5vw 45px;
}

.eyebrow{
    display:inline-flex;
    align-items:center;
    gap:8px;
    padding:7px 13px;
    border:1px solid rgba(0,234,255,.22);
    border-radius:999px;
    background:rgba(0,234,255,.045);
    color:var(--cyan);
    font:600 11px "JetBrains Mono",monospace;
    letter-spacing:1.2px;
    text-transform:uppercase;
}

h1{
    margin-top:22px;
    max-width:900px;
    font-size:clamp(42px,7vw,88px);
    line-height:.95;
    letter-spacing:-5px;
}

.gradient{
    background:linear-gradient(100deg,var(--cyan),#ffffff 40%,var(--purple));
    -webkit-background-clip:text;
    color:transparent;
}

.hero-sub{
    margin-top:25px;
    max-width:780px;
    color:#91a7bb;
    line-height:1.8;
    font-size:16px;
}

.hero-sub strong{
    color:#d9f9ff;
}

/* ================= METRICS ================= */

.metrics{
    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:14px;
    margin-top:40px;
}

.metric{
    position:relative;
    overflow:hidden;
    min-height:135px;
    padding:22px;
    border:1px solid var(--border);
    border-radius:14px;
    background:linear-gradient(145deg,rgba(8,20,37,.92),rgba(4,11,23,.9));
    box-shadow:inset 0 0 25px rgba(0,234,255,.025);
    transition:.35s;
}

.metric:hover{
    transform:translateY(-5px);
    border-color:rgba(0,234,255,.45);
    box-shadow:
        0 15px 45px rgba(0,0,0,.35),
        0 0 35px rgba(0,234,255,.07);
}

.metric::after{
    content:"";
    position:absolute;
    width:100px;
    height:100px;
    right:-50px;
    top:-50px;
    border-radius:50%;
    background:var(--cyan);
    filter:blur(55px);
    opacity:.1;
}

.metric-number{
    font:700 34px "JetBrains Mono",monospace;
    color:#fff;
}

.metric-number.cyan{color:var(--cyan)}
.metric-number.green{color:var(--green)}
.metric-number.purple{color:#a78bfa}

.metric-label{
    margin-top:10px;
    color:#8299af;
    font-size:12px;
    text-transform:uppercase;
    letter-spacing:1px;
}

/* ================= SECTION ================= */

.section{
    max-width:1400px;
    margin:auto;
    padding:55px 5vw;
}

.section-title{
    display:flex;
    align-items:center;
    gap:14px;
    margin-bottom:25px;
}

.section-title h2{
    font-size:24px;
    letter-spacing:-1px;
}

.section-title span{
    font:500 11px "JetBrains Mono",monospace;
    color:var(--cyan);
    padding:5px 9px;
    border:1px solid rgba(0,234,255,.2);
    border-radius:5px;
}

/* ================= PIPELINE ================= */

.pipeline-wrapper{
    position:relative;
    overflow:hidden;
    padding:35px 25px 45px;
    border:1px solid rgba(0,234,255,.16);
    border-radius:20px;
    background:
        linear-gradient(180deg,rgba(9,19,35,.95),rgba(3,9,20,.98));
}

.pipeline{
    position:relative;
    display:grid;
    grid-template-columns:
        1fr
        .45fr
        1fr
        .45fr
        1fr
        .45fr
        1fr
        .45fr
        1fr;
    align-items:center;
    min-width:900px;
}

.node{
    position:relative;
    min-height:145px;
    padding:20px;
    display:flex;
    flex-direction:column;
    justify-content:center;
    gap:9px;
    border:1px solid rgba(255,255,255,.1);
    border-radius:15px;
    background:rgba(8,17,31,.96);
    box-shadow:0 10px 35px rgba(0,0,0,.25);
    transition:.3s;
}

.node:hover{
    transform:translateY(-7px) scale(1.015);
    border-color:var(--cyan);
    box-shadow:0 0 30px rgba(0,234,255,.14);
}

.node-icon{
    width:38px;
    height:38px;
    display:grid;
    place-items:center;
    border-radius:10px;
    border:1px solid rgba(0,234,255,.25);
    background:rgba(0,234,255,.05);
    color:var(--cyan);
}

.node h3{
    font-size:14px;
}

.node p{
    font:11px "JetBrains Mono",monospace;
    color:#718aa2;
    line-height:1.6;
}

.connector{
    height:3px;
    position:relative;
    background:linear-gradient(
        90deg,
        rgba(0,234,255,.08),
        rgba(0,234,255,.7),
        rgba(139,92,246,.7),
        rgba(0,234,255,.08)
    );
    box-shadow:0 0 10px rgba(0,234,255,.25);
}

.packet{
    position:absolute;
    top:50%;
    left:-10px;
    width:8px;
    height:8px;
    border-radius:50%;
    background:white;
    box-shadow:
        0 0 8px white,
        0 0 18px var(--cyan),
        0 0 28px var(--cyan);
    transform:translateY(-50%);
    animation:packetMove 2.1s linear infinite;
}

/* ================= SECURITY ================= */

.security-grid{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:15px;
}

.security-card{
    position:relative;
    overflow:hidden;
    padding:24px;
    min-height:175px;
    border:1px solid rgba(57,255,136,.17);
    border-radius:16px;
    background:linear-gradient(145deg,rgba(8,22,26,.95),rgba(4,13,21,.95));
}

.security-card::before{
    content:"";
    position:absolute;
    top:-100%;
    left:0;
    width:100%;
    height:60%;
    background:linear-gradient(
        transparent,
        rgba(57,255,136,.16),
        transparent
    );
    animation:scan 2.4s linear infinite;
}

.security-top{
    display:flex;
    justify-content:space-between;
    align-items:center;
}

.security-name{
    font:600 15px "JetBrains Mono",monospace;
    color:#d8ffe7;
}

.check{
    width:27px;
    height:27px;
    display:grid;
    place-items:center;
    border-radius:50%;
    color:var(--green);
    border:1px solid rgba(57,255,136,.45);
    box-shadow:0 0 14px rgba(57,255,136,.18);
    animation:checkPulse 1.5s infinite;
}

.security-value{
    margin-top:28px;
    font:700 30px "JetBrains Mono",monospace;
    color:var(--green);
}

.security-desc{
    margin-top:7px;
    font-size:11px;
    color:#6f8990;
}

/* ================= AZURE ================= */

.azure-layout{
    display:grid;
    grid-template-columns:1.2fr .8fr;
    gap:18px;
}

.azure-map{
    min-height:400px;
    position:relative;
    overflow:hidden;
    padding:30px;
    border:1px solid rgba(59,130,246,.25);
    border-radius:20px;
    background:
        radial-gradient(circle at 50% 50%,rgba(59,130,246,.1),transparent 50%),
        rgba(4,12,26,.95);
}

.azure-map-title{
    font:600 12px "JetBrains Mono",monospace;
    color:#70a9ff;
    margin-bottom:25px;
}

.azure-network{
    position:absolute;
    inset:90px 50px 45px;
    border:1px dashed rgba(59,130,246,.35);
    border-radius:25px;
    transform:perspective(700px) rotateX(8deg);
}

.azure-node{
    position:absolute;
    min-width:135px;
    padding:17px;
    border:1px solid rgba(59,130,246,.45);
    border-radius:12px;
    background:rgba(7,22,43,.94);
    box-shadow:
        0 15px 35px rgba(0,0,0,.45),
        inset 0 0 25px rgba(59,130,246,.06);
    transition:.3s;
}

.azure-node:hover{
    transform:translateZ(30px) translateY(-5px);
    border-color:#60a5fa;
    box-shadow:0 0 35px rgba(59,130,246,.2);
}

.azure-node strong{
    display:block;
    font-size:13px;
    color:#dbeafe;
}

.azure-node small{
    display:block;
    margin-top:5px;
    font:10px "JetBrains Mono",monospace;
    color:#6282a5;
}

.vmss{
    top:35px;
    left:40px;
}

.vnet{
    top:145px;
    left:50%;
    transform:translateX(-50%);
}

.appgw{
    top:35px;
    right:40px;
}

.lb{
    bottom:30px;
    left:50%;
    transform:translateX(-50%);
}

.azure-line{
    position:absolute;
    height:1px;
    background:#2585ff;
    opacity:.5;
    transform-origin:left;
    box-shadow:0 0 8px #2585ff;
}

.line-a{
    width:170px;
    top:95px;
    left:175px;
    transform:rotate(35deg);
}

.line-b{
    width:170px;
    top:95px;
    right:175px;
    transform:rotate(145deg);
}

.line-c{
    width:110px;
    top:205px;
    left:50%;
    transform:rotate(90deg);
}

/* ================= SKILLS ================= */

.skill-panel{
    padding:25px;
    border:1px solid rgba(139,92,246,.18);
    border-radius:18px;
    background:rgba(8,13,28,.92);
}

.skill{
    margin-bottom:20px;
}

.skill:last-child{
    margin-bottom:0;
}

.skill-head{
    display:flex;
    justify-content:space-between;
    margin-bottom:8px;
    font:500 11px "JetBrains Mono",monospace;
}

.skill-head span:last-child{
    color:var(--cyan);
}

.bar{
    height:6px;
    border-radius:999px;
    overflow:hidden;
    background:#101c2d;
}

.bar-fill{
    height:100%;
    width:0;
    border-radius:inherit;
    background:linear-gradient(90deg,var(--purple),var(--cyan));
    box-shadow:0 0 12px rgba(0,234,255,.35);
    animation:loadBar 1.7s ease forwards;
}

/* ================= COST ================= */

.cost{
    margin-top:20px;
    padding:25px;
    border:1px solid rgba(255,60,172,.18);
    border-radius:18px;
    background:
        linear-gradient(135deg,rgba(255,60,172,.035),rgba(139,92,246,.04)),
        #070d1b;
}

.cost-head{
    display:flex;
    justify-content:space-between;
    align-items:center;
}

.cost-title{
    font:600 13px "JetBrains Mono",monospace;
}

.cost-value{
    font:700 32px "JetBrains Mono",monospace;
    color:#f0abff;
}

.cost-chart{
    display:flex;
    align-items:end;
    gap:8px;
    height:100px;
    margin-top:25px;
}

.cost-bar{
    flex:1;
    height:var(--h);
    border-radius:4px 4px 0 0;
    background:linear-gradient(to top,var(--purple),var(--pink));
    opacity:.65;
    animation:barPulse 2s ease-in-out infinite alternate;
}

/* ================= FOOTER ================= */

footer{
    max-width:1400px;
    margin:auto;
    padding:35px 5vw 55px;
    display:flex;
    justify-content:space-between;
    gap:20px;
    border-top:1px solid rgba(255,255,255,.06);
    color:#587087;
    font:11px "JetBrains Mono",monospace;
}

footer strong{
    color:var(--cyan);
}

/* ================= ANIMATIONS ================= */

@keyframes packetMove{
    from{left:-10px}
    to{left:calc(100% + 10px)}
}

@keyframes scan{
    from{top:-100%}
    to{top:160%}
}

@keyframes pulse{
    0%,100%{
        opacity:.5;
        transform:scale(.85);
    }
    50%{
        opacity:1;
        transform:scale(1.1);
    }
}

@keyframes checkPulse{
    0%,100%{box-shadow:0 0 5px rgba(57,255,136,.1)}
    50%{box-shadow:0 0 22px rgba(57,255,136,.4)}
}

@keyframes loadBar{
    to{width:var(--width)}
}

@keyframes barPulse{
    from{opacity:.45}
    to{opacity:.9}
}

/* ================= RESPONSIVE ================= */

@media(max-width:1000px){

    .metrics{
        grid-template-columns:repeat(2,1fr);
    }

    .security-grid{
        grid-template-columns:1fr;
    }

    .azure-layout{
        grid-template-columns:1fr;
    }
}

@media(max-width:650px){

    nav{
        padding:0 20px;
    }

    .hero{
        padding-top:55px;
    }

    h1{
        letter-spacing:-3px;
    }

    .metrics{
        grid-template-columns:1fr;
    }

    .pipeline-wrapper{
        overflow-x:auto;
    }

    .pipeline{
        min-width:950px;
    }

    footer{
        flex-direction:column;
    }
}
</style>
</head>

<body>

<!-- NAV -->
<nav>
    <div class="logo">
        PIYUSH<span>_DEVOPS</span>
    </div>

    <div class="status">
        <span class="status-dot"></span>
        OPEN TO DEVOPS OPPORTUNITIES
    </div>
</nav>


<!-- HERO -->
<header class="hero">

    <div class="eyebrow">
        ◉ AZURE CLOUD · DEVOPS · IaC · CI/CD
    </div>

    <h1>
        Building
        <span class="gradient">Reliable Cloud</span>
        Infrastructure.
    </h1>

    <p class="hero-sub">
        <strong>Piyush Priyadarshi</strong> — DevOps & Cloud Engineer
        focused on Azure infrastructure, Terraform automation,
        CI/CD engineering, security integration and highly available
        cloud architectures.
    </p>


    <div class="metrics">

        <div class="metric">
            <div class="metric-number cyan">3.5+</div>
            <div class="metric-label">
                Years of Industrial Excellence
            </div>
        </div>

        <div class="metric">
            <div class="metric-number green">HA</div>
            <div class="metric-label">
                High Availability Architect
            </div>
        </div>

        <div class="metric">
            <div class="metric-number purple">IaC</div>
            <div class="metric-label">
                Terraform Automation
            </div>
        </div>

        <div class="metric">
            <div class="metric-number cyan">CI/CD</div>
            <div class="metric-label">
                GitHub Actions + Azure DevOps
            </div>
        </div>

    </div>
</header>


<!-- PIPELINE -->
<section class="section">

    <div class="section-title">
        <h2>Production Delivery Pipeline</h2>
        <span>LIVE FLOW</span>
    </div>

    <div class="pipeline-wrapper">

        <div class="pipeline">

            <!-- GitHub -->
            <div class="node">

                <div class="node-icon">
                    <svg width="22" height="22" viewBox="0 0 24 24" fill="currentColor">
                        <path d="M12 .5C5.65.5.5 5.65.5 12c0 5.08 3.29 9.39 7.86 10.91.58.1.79-.25.79-.56v-2.02c-3.2.7-3.87-1.36-3.87-1.36-.53-1.35-1.28-1.71-1.28-1.71-1.05-.72.08-.71.08-.71 1.16.08 1.77 1.19 1.77 1.19 1.03 1.77 2.69 1.26 3.35.96.1-.75.4-1.26.73-1.55-2.55-.29-5.23-1.28-5.23-5.69 0-1.26.45-2.28 1.19-3.08-.12-.29-.52-1.46.11-3.04 0 0 .97-.31 3.18 1.18a11.1 11.1 0 0 1 5.79 0c2.21-1.5 3.18-1.18 3.18-1.18.63 1.58.23 2.75.11 3.04.74.8 1.19 1.82 1.19 3.08 0 4.42-2.69 5.4-5.25 5.69.41.35.78 1.05.78 2.12v3.14c0 .31.21.67.8.56A11.51 11.51 0 0 0 23.5 12C23.5 5.65 18.35.5 12 .5z"/>
                    </svg>
                </div>

                <h3>GitHub</h3>
                <p>CODE / BRANCH / PR</p>

            </div>


            <div class="connector">
                <div class="packet"></div>
            </div>


            <!-- Terraform -->
            <div class="node">

                <div class="node-icon">
                    ◈
                </div>

                <h3>Terraform</h3>
                <p>PLAN → VALIDATE → APPLY</p>

            </div>


            <div class="connector">
                <div class="packet"></div>
            </div>


            <!-- CI -->
            <div class="node">

                <div class="node-icon">
                    ⚙
                </div>

                <h3>CI/CD Engine</h3>
                <p>GITHUB ACTIONS<br>AZURE DEVOPS</p>

            </div>


            <div class="connector">
                <div class="packet"></div>
            </div>


            <!-- Security -->
            <div class="node">

                <div class="node-icon">
                    ◉
                </div>

                <h3>Security Gate</h3>
                <p>TRIVY · GITLEAKS<br>SONARQUBE · TFSEC</p>

            </div>


            <div class="connector">
                <div class="packet"></div>
            </div>


            <!-- Cost -->
            <div class="node">

                <div class="node-icon">
                    $
                </div>

                <h3>Infracost</h3>
                <p>COST VISIBILITY<br>BEFORE DEPLOYMENT</p>

            </div>

        </div>

    </div>

</section>


<!-- SECURITY -->
<section class="section">

    <div class="section-title">
        <h2>Continuous Security Layer</h2>
        <span>SHIFT LEFT</span>
    </div>

    <div class="security-grid">

        <div class="security-card">

            <div class="security-top">
                <div class="security-name">TRIVY</div>
                <div class="check">✓</div>
            </div>

            <div class="security-value">CLEAN</div>
            <div class="security-desc">
                Container & dependency vulnerability scanning
            </div>

        </div>


        <div class="security-card">

            <div class="security-top">
                <div class="security-name">GITLEAKS</div>
                <div class="check">✓</div>
            </div>

            <div class="security-value">SECURE</div>
            <div class="security-desc">
                Secrets detection before code reaches production
            </div>

        </div>


        <div class="security-card">

            <div class="security-top">
                <div class="security-name">SONARQUBE</div>
                <div class="check">✓</div>
            </div>

            <div class="security-value">PASS</div>
            <div class="security-desc">
                Code quality and static analysis gate
            </div>

        </div>

    </div>

</section>


<!-- AZURE ARCHITECTURE -->
<section class="section">

    <div class="section-title">
        <h2>Azure High Availability Architecture</h2>
        <span>3D CLOUD MAP</span>
    </div>


    <div class="azure-layout">

        <div class="azure-map">

            <div class="azure-map-title">
                AZURE / PRODUCTION NETWORK TOPOLOGY
            </div>

            <div class="azure-network">

                <div class="azure-line line-a"></div>
                <div class="azure-line line-b"></div>
                <div class="azure-line line-c"></div>


                <div class="azure-node vmss">

                    <strong>VMSS</strong>

                    <small>
                        AUTO SCALING
                    </small>

                </div>


                <div class="azure-node vnet">

                    <strong>VNet</strong>

                    <small>
                        NETWORK CORE
                    </small>

                </div>


                <div class="azure-node appgw">

                    <strong>App Gateway</strong>

                    <small>
                        L7 ROUTING
                    </small>

                </div>


                <div class="azure-node lb">

                    <strong>Load Balancer</strong>

                    <small>
                        L4 TRAFFIC
                    </small>

                </div>

            </div>

        </div>


        <!-- SKILLS -->
        <div class="skill-panel">

            <div class="skill">

                <div class="skill-head">
                    <span>TERRAFORM / IaC</span>
                    <span>STRONG</span>
                </div>

                <div class="bar">
                    <div
                        class="bar-fill"
                        style="--width:92%">
                    </div>
                </div>

            </div>


            <div class="skill">

                <div class="skill-head">
                    <span>AZURE CLOUD</span>
                    <span>STRONG</span>
                </div>

                <div class="bar">
                    <div
                        class="bar-fill"
                        style="--width:90%">
                    </div>
                </div>

            </div>


            <div class="skill">

                <div class="skill-head">
                    <span>GITHUB ACTIONS</span>
                    <span>STRONG</span>
                </div>

                <div class="bar">
                    <div
                        class="bar-fill"
                        style="--width:88%">
                    </div>
                </div>

            </div>


            <div class="skill">

                <div class="skill-head">
                    <span>AZURE DEVOPS</span>
                    <span>STRONG</span>
                </div>

                <div class="bar">
                    <div
                        class="bar-fill"
                        style="--width:86%">
                    </div>
                </div>

            </div>


            <div class="skill">

                <div class="skill-head">
                    <span>LINUX</span>
                    <span>PROFICIENT</span>
                </div>

                <div class="bar">
                    <div
                        class="bar-fill"
                        style="--width:80%">
                    </div>
                </div>

            </div>


            <div class="skill">

                <div class="skill-head">
                    <span>CLOUD SECURITY</span>
                    <span>PROFICIENT</span>
                </div>

                <div class="bar">
                    <div
                        class="bar-fill"
                        style="--width:78%">
                    </div>
                </div>

            </div>

        </div>

    </div>


    <!-- COST -->
    <div class="cost">

        <div class="cost-head">

            <div class="cost-title">
                INFRACOST / ESTIMATED CLOUD SPEND
            </div>

            <div class="cost-value">
                ↓ 18.4%
            </div>

        </div>


        <div class="cost-chart">

            <div class="cost-bar" style="--h:45%"></div>
            <div class="cost-bar" style="--h:58%"></div>
            <div class="cost-bar" style="--h:70%"></div>
            <div class="cost-bar" style="--h:63%"></div>
            <div class="cost-bar" style="--h:78%"></div>
            <div class="cost-bar" style="--h:55%"></div>
            <div class="cost-bar" style="--h:38%"></div>
            <div class="cost-bar" style="--h:30%"></div>

        </div>

    </div>

</section>


<!-- FOOTER -->
<footer>

    <div>
        <strong>PIYUSH PRIYADARSHI</strong>
        <br>
        DEVOPS · AZURE · TERRAFORM
    </div>

    <div>
        AUTOMATE · SECURE · OBSERVE · SCALE
    </div>

</footer>

</body>
</html>
