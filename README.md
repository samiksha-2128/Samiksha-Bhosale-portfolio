# Samiksha-Bhosale-portfolio
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />

<title>Samiksha Bhosale | Chemical Engineer</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css"/>

<style>

:root{
    --bg:#0d0d0d;
    --card:#161616;
    --text:#ffffff;
    --muted:#b5b5b5;

    --primary:#ff7b00;
    --secondary:#ffb300;

    --border:#2b2b2b;
}

/* GLOBAL */

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:'Poppins',sans-serif;
    scroll-behavior:smooth;
}

body{
    background:var(--bg);
    color:var(--text);
    overflow-x:hidden;
}

/* BACKGROUND */

body::before{
    content:'';
    position:fixed;
    inset:0;

    background-image:url("data:image/svg+xml,%3Csvg width='70' height='70' viewBox='0 0 70 70' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='%23ff7b00' fill-opacity='0.05'%3E%3Cpath d='M35 0l30.3 17.5v35L35 70 4.7 52.5v-35z'/%3E%3C/g%3E%3C/svg%3E");

    z-index:-2;
}

/* FLOATING BUBBLES */

.bubbles{
    position:fixed;
    inset:0;
    overflow:hidden;
    z-index:-1;
    pointer-events:none;
}

.bubble{
    position:absolute;
    bottom:-120px;
    border-radius:50%;
    background:rgba(255,123,0,0.15);
    animation:rise 12s infinite ease-in;
}

.bubble:nth-child(1){
    width:40px;
    height:40px;
    left:10%;
    animation-duration:7s;
}

.bubble:nth-child(2){
    width:20px;
    height:20px;
    left:25%;
    animation-duration:5s;
}

.bubble:nth-child(3){
    width:55px;
    height:55px;
    left:45%;
    animation-duration:10s;
}

.bubble:nth-child(4){
    width:30px;
    height:30px;
    left:60%;
    animation-duration:8s;
}

.bubble:nth-child(5){
    width:25px;
    height:25px;
    left:75%;
    animation-duration:11s;
}

.bubble:nth-child(6){
    width:45px;
    height:45px;
    left:90%;
    animation-duration:9s;
}

@keyframes rise{
    0%{
        transform:translateY(0) scale(1);
        opacity:0;
    }

    50%{
        opacity:1;
    }

    100%{
        transform:translateY(-120vh) scale(1.5);
        opacity:0;
    }
}

/* HEADER */

header{
    position:sticky;
    top:0;
    z-index:999;

    display:flex;
    justify-content:space-between;
    align-items:center;

    padding:20px 8%;

    background:rgba(17,17,17,0.9);
    backdrop-filter:blur(12px);

    border-bottom:1px solid rgba(255,123,0,0.2);
}

.logo{
    font-size:28px;
    font-weight:700;
    color:var(--primary);
}

nav{
    display:flex;
    gap:30px;
}

nav a{
    text-decoration:none;
    color:white;
    position:relative;
    transition:0.3s;
}

nav a::after{
    content:'';
    position:absolute;
    left:0;
    bottom:-5px;
    width:0;
    height:2px;
    background:var(--primary);
    transition:0.3s;
}

nav a:hover{
    color:var(--primary);
}

nav a:hover::after{
    width:100%;
}

/* SECTION */

section{
    padding:100px 8%;
}

.section-title{
    text-align:center;
    margin-bottom:60px;
    font-size:40px;
    color:var(--primary);
}

/* HERO */

.hero{
    min-height:100vh;

    display:flex;
    justify-content:space-between;
    align-items:center;
    gap:50px;
}

.hero-text{
    flex:1;
}

.hero-text p:first-child{
    color:var(--muted);
    font-size:18px;
}

.hero-text h1{
    font-size:70px;
    line-height:1.1;
    margin:15px 0;
}

.hero-text span{
    background:linear-gradient(to right,var(--primary),var(--secondary));
    -webkit-background-clip:text;
    -webkit-text-fill-color:transparent;
}

.subtitle{
    font-size:24px;
    margin-bottom:20px;
}

.tagline{
    color:var(--muted);
    margin-bottom:30px;
}

.socials{
    display:flex;
    gap:20px;
    margin-bottom:30px;
}

.socials a{
    width:50px;
    height:50px;
    border-radius:50%;
    background:#1f1f1f;

    display:flex;
    justify-content:center;
    align-items:center;

    color:var(--primary);
    font-size:22px;

    transition:0.3s;
}

.socials a:hover{
    transform:translateY(-5px);
    background:var(--primary);
    color:white;
}

.btn{
    display:inline-block;

    padding:14px 30px;

    background:linear-gradient(to right,var(--primary),var(--secondary));

    border-radius:40px;

    color:white;
    text-decoration:none;
    font-weight:600;

    transition:0.3s;
}

.btn:hover{
    transform:translateY(-4px);
    box-shadow:0 10px 20px rgba(255,123,0,0.3);
}

/* HERO IMAGE */

.hero-image{
    flex:1;

    display:flex;
    justify-content:center;
    align-items:center;

    position:relative;
}

.blob{
    position:absolute;

    width:430px;
    height:430px;

    background:linear-gradient(135deg,
    rgba(255,123,0,0.5),
    rgba(255,179,0,0.5));

    border-radius:60% 40% 70% 30% / 40% 60% 30% 70%;

    animation:morph 8s ease-in-out infinite;
}

@keyframes morph{

    0%{
        border-radius:60% 40% 70% 30% / 40% 60% 30% 70%;
    }

    50%{
        border-radius:30% 60% 40% 70% / 60% 30% 70% 40%;
    }

    100%{
        border-radius:60% 40% 70% 30% / 40% 60% 30% 70%;
    }
}

.hero-image img{
    width:360px;
    height:360px;

    object-fit:cover;

    border-radius:50%;
    border:5px solid #2b2b2b;

    z-index:2;

    animation:float 4s ease-in-out infinite;

    transition:0.3s;
}

.hero-image img:hover{
    transform:scale(1.03);
    border-color:var(--primary);
}

@keyframes float{

    0%{
        transform:translateY(0);
    }

    50%{
        transform:translateY(-15px);
    }

    100%{
        transform:translateY(0);
    }
}

/* CARDS */

.card{
    background:var(--card);

    border:1px solid var(--border);

    border-radius:20px;

    padding:35px;

    transition:0.3s;
}

.card:hover{
    transform:translateY(-10px);
    border-color:var(--primary);
    box-shadow:0 10px 30px rgba(255,123,0,0.15);
}

/* ABOUT */

.about-content{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:40px;
    align-items:center;
}

.about-image img{
    width:100%;
    border-radius:20px;
}

.about-text p{
    line-height:1.9;
    color:var(--muted);
    margin-bottom:20px;
}

/* EDUCATION */

.edu-grid{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
    gap:30px;
}

.edu-card h3{
    margin-bottom:10px;
}

.edu-card p{
    color:var(--muted);
}

/* SKILLS */

.skills-grid{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(260px,1fr));
    gap:30px;
}

.skill-card{
    text-align:center;
}

.skill-icon{
    font-size:50px;
    color:var(--primary);
    margin-bottom:20px;
}

.progress{
    width:100%;
    height:10px;
    background:#222;
    border-radius:20px;
    overflow:hidden;
    margin-top:15px;
}

.progress span{
    display:block;
    height:100%;
    background:linear-gradient(to right,var(--primary),var(--secondary));
}

/* PROJECTS */

.projects{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(300px,1fr));
    gap:30px;
}

.project-card h3{
    margin-bottom:15px;
}

.project-card p{
    color:var(--muted);
    line-height:1.8;
}

/* FOOTER */

footer{
    padding:30px;
    text-align:center;
    border-top:1px solid #222;
    color:#777;
}

/* REVEAL */

.reveal{
    opacity:0;
    transform:translateY(40px);
    transition:1s;
}

.reveal.active{
    opacity:1;
    transform:translateY(0);
}

/* MOBILE */

@media(max-width:950px){

    .hero{
        flex-direction:column-reverse;
        text-align:center;
    }

    .about-content{
        grid-template-columns:1fr;
    }

    nav{
        gap:15px;
        flex-wrap:wrap;
        justify-content:center;
    }

    header{
        flex-direction:column;
        gap:15px;
    }

    .hero-text h1{
        font-size:50px;
    }

    .socials{
        justify-content:center;
    }

    .blob{
        width:320px;
        height:320px;
    }

    .hero-image img{
        width:280px;
        height:280px;
    }
}

</style>
</head>

<body>

<!-- BUBBLES -->

<div class="bubbles">
<div class="bubble"></div>
<div class="bubble"></div>
<div class="bubble"></div>
<div class="bubble"></div>
<div class="bubble"></div>
<div class="bubble"></div>
</div>

<!-- HEADER -->

<header>

<div class="logo">Portfolio.</div>

<nav>
<a href="#home">Home</a>
<a href="#about">About</a>
<a href="#education">Education</a>
<a href="#skills">Skills</a>
<a href="#projects">Projects</a>
</nav>

</header>

<!-- HERO -->

<section class="hero" id="home">

<div class="hero-text">

<p>Welcome to my Website</p>

<h1>
Samiksha <span>Bhosale</span>
</h1>

<div class="subtitle">
<i class="fa-solid fa-flask"></i>
Chemical Engineer
</div>

<p class="tagline">
Creative Thinker • Future Process Engineer • Tech Enthusiast
</p>

<div class="socials">

<a href="https://linkedin.com/in/samiksha-bhosale-o1528" target="_blank">
<i class="fa-brands fa-linkedin-in"></i>
</a>

<a href="https://github.com/samiksha-2126/EDS" target="_blank">
<i class="fa-brands fa-github"></i>
</a>

<a href="mailto:samibhosale2808@gmail.com">
<i class="fa-solid fa-envelope"></i>
</a>

</div>



<div class="hero-image">

<div class="blob"></div>

<img src="image.jpg" alt="Samiksha Bhosale">

</div>

</section>

<!-- ABOUT -->

<section id="about" class="reveal">

<h2 class="section-title">About Me</h2>

<div class="about-content">

<div class="about-image">
<img src="image.jpeg" alt="Samiksha Bhosale">
</div>

<div class="about-text card">

<p>
Hi! I am Samiksha Shivaji Bhosale, currently pursuing B.Tech in Chemical Engineering.
I enjoy combining chemistry, technology, creativity, and problem solving.
</p>

<p>
I am passionate about process engineering, programming, design, and innovation.
I love building creative projects and learning modern technologies.
</p>

<p>
📍 Pune, Maharashtra
<br><br>
<p>
📞 8766075416</p>
<br><br>
✉️ samibhosale2808@gmail.com
</p>

</div>

</div>

</section>

<!-- EDUCATION -->

<section id="education" class="reveal">

<h2 class="section-title">Education</h2>

<div class="edu-grid">

<div class="edu-card card">
<h3>MIT Academy of Engineering</h3>
<p>B.Tech Chemical Engineering Pursing</p>
</div>

<div class="edu-card card">
<h3>Rasiklal M. Dhariwal English Medium School And Junior College</h3>
<p>12th(Higher Secondary Education) Completed</p>
</div>

<div class="edu-card card">
<h3>Amrutwel Global School</h3>
<p>10th(Secondary Education) Completed</p>
</div>

</div>

</section>

<!-- SKILLS -->

<section id="skills" class="reveal">

<h2 class="section-title">Skills</h2>

<div class="skills-grid">

<div class="skill-card card">
<div class="skill-icon">
<i class="fa-solid fa-industry"></i>
</div>

<h3>Process Design</h3>

<div class="progress">
<span style="width:90%"></span>
</div>
</div>

<div class="skill-card card">
<div class="skill-icon">
<i class="fa-solid fa-temperature-high"></i>
</div>

<h3>Drawing</h3>

<div class="progress">
<span style="width:85%"></span>
</div>
</div>

<div class="skill-card card">
<div class="skill-icon">
<i class="fa-brands fa-html5"></i>
</div>

<h3>HTML/CSS</h3>

<div class="progress">
<span style="width:95%"></span>
</div>
</div>

<div class="skill-card card">
<div class="skill-icon">
<i class="fa-brands fa-js"></i>
</div>

<h3>JavaScript</h3>

<div class="progress">
<span style="width:85%"></span>
</div>
</div>

<div class="skill-card card">
<div class="skill-icon">
<i class="fa-brands fa-python"></i>
</div>

<h3>Python</h3>

<div class="progress">
<span style="width:91%"></span>
</div>
</div>

<div class="skill-card card">
<div class="skill-icon">
<i class="fa-solid fa-video"></i>
</div>

<h3>Video Editing</h3>

<div class="progress">
<span style="width:82%"></span>
</div>
</div>

</div>

</section>

<!-- PROJECTS -->

<section id="projects" class="reveal">

<h2 class="section-title">Projects</h2>

<div class="projects">

<div class="project-card card">

<h3>Smart Chemical Waste Segregator</h3>

<p>
AI based waste classification system for smart laboratories and industries.
</p>

</div>

<div class="project-card card">

<h3>"""Development of a Bio-Composite Smart Capillary Matrix for Passive Evaporative Cooling in Zero Energy Buildings."""</h3>

<p>
To create a Air conditioning system that rely on water for cooling and reforms Air purification  with zero carbon emissions
</p>

</div>


</div>

</section>

<!-- FOOTER -->

<footer>

© 2026 Samiksha Bhosale | Designed with Chemical Precision ⚗️

</footer>

<script>

/* REVEAL ANIMATION */

const reveals = document.querySelectorAll('.reveal');

window.addEventListener('scroll', () => {

reveals.forEach(reveal => {

const windowHeight = window.innerHeight;
const revealTop = reveal.getBoundingClientRect().top;

if(revealTop < windowHeight - 100){
reveal.classList.add('active');
}

});

});

</script>

</body>
</html>
