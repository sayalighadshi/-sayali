# -sayali
Precision Power Marketing


<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Precision Power Marketing | Premium Digital Agency</title>

<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&family=Poppins:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css">
<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>

<style>
*{margin:0;padding:0;box-sizing:border-box}
:root{
  --dark:#050816;
  --navy:#0f172a;
  --gold:#facc15;
  --cyan:#38bdf8;
  --pink:#ec4899;
  --white:#fff;
  --muted:#94a3b8;
  --glass:rgba(255,255,255,.09);
}
html{scroll-behavior:smooth}
body{
  font-family:'Poppins',sans-serif;
  background:var(--dark);
  color:var(--white);
  overflow-x:hidden;
}
body::before{
  content:"";
  position:fixed;
  inset:0;
  background:
  radial-gradient(circle at 20% 20%,rgba(56,189,248,.25),transparent 30%),
  radial-gradient(circle at 80% 30%,rgba(236,72,153,.25),transparent 30%),
  radial-gradient(circle at 50% 90%,rgba(250,204,21,.18),transparent 30%);
  z-index:-2;
}
body::after{
  content:"";
  position:fixed;
  inset:0;
  background:linear-gradient(120deg,transparent,rgba(255,255,255,.04),transparent);
  animation:bgMove 8s infinite linear;
  z-index:-1;
}
@keyframes bgMove{from{transform:translateX(-100%)}to{transform:translateX(100%)}}

/* PRELOADER */
#preloader{
  position:fixed;
  inset:0;
  background:#020617;
  display:flex;
  justify-content:center;
  align-items:center;
  flex-direction:column;
  z-index:9999;
}
.loader{
  width:80px;height:80px;
  border:5px solid #1e293b;
  border-top:5px solid var(--gold);
  border-radius:50%;
  animation:spin 1s linear infinite;
}
#preloader h2{
  margin-top:20px;
  color:var(--gold);
  letter-spacing:2px;
}
@keyframes spin{to{transform:rotate(360deg)}}

/* NAVBAR */
nav{
  position:fixed;
  width:100%;
  top:0;
  z-index:1000;
  padding:18px 8%;
  display:flex;
  justify-content:space-between;
  align-items:center;
  background:rgba(2,6,23,.75);
  backdrop-filter:blur(16px);
  border-bottom:1px solid rgba(255,255,255,.1);
}
.logo{
  font-family:'Playfair Display',serif;
  font-size:26px;
  color:var(--gold);
}
nav ul{
  display:flex;
  gap:24px;
  list-style:none;
}
nav a{
  color:white;
  text-decoration:none;
  font-size:14px;
}
nav a:hover{color:var(--gold)}
.menu{display:none;font-size:26px}

/* COMMON */
section{padding:90px 8%}
.title{text-align:center;margin-bottom:50px}
.title h2{
  font-size:36px;
  color:var(--gold);
  font-family:'Playfair Display',serif;
}
.title p{color:var(--muted);margin-top:10px}
.btn{
  display:inline-block;
  padding:13px 28px;
  border-radius:30px;
  background:linear-gradient(135deg,var(--gold),#f97316);
  color:#111;
  font-weight:700;
  text-decoration:none;
  margin:8px;
  box-shadow:0 10px 30px rgba(250,204,21,.25);
}
.btn.alt{
  background:transparent;
  color:white;
  border:1px solid rgba(255,255,255,.3);
}

/* HERO */
.hero{
  min-height:100vh;
  display:flex;
  align-items:center;
  justify-content:center;
  text-align:center;
  padding:130px 8% 80px;
}
.hero h1{
  font-size:60px;
  line-height:1.1;
  font-family:'Playfair Display',serif;
}
.hero h1 span{color:var(--gold)}
.hero p{
  max-width:760px;
  margin:25px auto;
  color:#cbd5e1;
  font-size:18px;
}
.hero-box{
  background:var(--glass);
  border:1px solid rgba(255,255,255,.12);
  padding:45px;
  border-radius:30px;
  box-shadow:0 25px 80px rgba(0,0,0,.35);
}

/* GRID CARDS */
.grid{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(240px,1fr));
  gap:25px;
}
.card{
  background:var(--glass);
  border:1px solid rgba(255,255,255,.12);
  padding:28px;
  border-radius:24px;
  transition:.4s;
}
.card:hover{
  transform:translateY(-10px);
  border-color:var(--gold);
}
.card i{
  font-size:35px;
  color:var(--gold);
  margin-bottom:15px;
}
.card h3{margin-bottom:10px}
.card p{color:#cbd5e1;font-size:14px}

/* ABOUT */
.about{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:40px;
  align-items:center;
}
.about img{
  width:100%;
  border-radius:30px;
}
.about p{color:#cbd5e1;line-height:1.8}

/* PROCESS */
.step{
  counter-increment:item;
  position:relative;
}
.step::before{
  content:counter(item);
  width:42px;height:42px;
  display:flex;
  justify-content:center;
  align-items:center;
  background:var(--gold);
  color:#111;
  border-radius:50%;
  font-weight:800;
  margin-bottom:15px;
}

/* STATS */
.stats{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(180px,1fr));
  gap:25px;
  text-align:center;
}
.stat h2{
  font-size:42px;
  color:var(--gold);
}
.stat p{color:#cbd5e1}

/* TESTIMONIAL */
.testimonial{
  max-width:750px;
  margin:auto;
  text-align:center;
  background:var(--glass);
  padding:40px;
  border-radius:25px;
}
.testimonial p{color:#cbd5e1;font-size:18px}
.testimonial h4{margin-top:20px;color:var(--gold)}

/* PRICING */
.price{
  text-align:center;
}
.price h2{font-size:38px;color:var(--gold)}
.price ul{
  list-style:none;
  margin:20px 0;
}
.price li{
  padding:8px;
  color:#cbd5e1;
}

/* FAQ */
.faq-item{
  background:var(--glass);
  margin-bottom:15px;
  border-radius:15px;
  overflow:hidden;
}
.faq-question{
  padding:20px;
  cursor:pointer;
  display:flex;
  justify-content:space-between;
}
.faq-answer{
  display:none;
  padding:0 20px 20px;
  color:#cbd5e1;
}

/* DASHBOARD */
.dashboard{
  background:var(--glass);
  border-radius:30px;
  padding:30px;
}

/* CONTACT */
.contact{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:30px;
}
input,textarea{
  width:100%;
  padding:15px;
  margin-bottom:15px;
  border:none;
  border-radius:12px;
  outline:none;
}
textarea{height:130px}
iframe{
  width:100%;
  height:320px;
  border:0;
  border-radius:20px;
}

/* FOOTER */
footer{
  background:#020617;
  padding:50px 8%;
  text-align:center;
  border-top:1px solid rgba(255,255,255,.1);
}
.social a{
  color:white;
  font-size:24px;
  margin:10px;
}
.social a:hover{color:var(--gold)}

/* WHATSAPP */
.whatsapp{
  position:fixed;
  right:22px;
  bottom:22px;
  background:#25d366;
  color:white;
  width:58px;
  height:58px;
  border-radius:50%;
  display:flex;
  justify-content:center;
  align-items:center;
  font-size:30px;
  text-decoration:none;
  z-index:999;
}

/* RESPONSIVE */
@media(max-width:850px){
  nav ul{
    display:none;
    position:absolute;
    top:70px;
    left:0;
    width:100%;
    background:#020617;
    flex-direction:column;
    padding:25px;
  }
  nav ul.active{display:flex}
  .menu{display:block}
  .hero h1{font-size:38px}
  .about,.contact{grid-template-columns:1fr}
}
</style>
</head>

<body>

<div id="preloader">
  <div class="loader"></div>
  <h2>Precision Power Marketing</h2>
</div>

<nav>
  <div class="logo">Precision Power</div>
  <ul id="navLinks">
    <li><a href="#home">Home</a></li>
    <li><a href="#about">About</a></li>
    <li><a href="#services">Services</a></li>
    <li><a href="#portfolio">Portfolio</a></li>
    <li><a href="#pricing">Pricing</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
  <div class="menu" onclick="toggleMenu()"><i class="fa-solid fa-bars"></i></div>
</nav>

<section class="hero" id="home">
  <div class="hero-box">
    <h1>Premium Digital Marketing <span>Agency Website</span></h1>
    <p>We help brands grow online with powerful web design, SEO, social media marketing, ads, automation, and premium digital strategies.</p>
    <a href="#contact" class="btn">Get Started</a>
    <a href="https://www.instagram.com/sayalivikasghadshi" target="_blank" class="btn alt">
      <i class="fa-brands fa-instagram"></i> @sayalivikasghadshi
    </a>
  </div>
</section>

<section id="about">
  <div class="about">
    <div>
      <div class="title" style="text-align:left">
        <h2>About Our Agency</h2>
        <p>Professional marketing solutions for modern businesses.</p>
      </div>
      <p>Precision Power Marketing is a premium digital marketing agency focused on helping businesses increase visibility, generate leads, and build powerful online brands. We combine creativity, technology, and strategy to deliver beautiful and result-driven digital experiences.</p>
      <br>
      <a href="#services" class="btn">Explore Services</a>
    </div>
    <img src="https://images.unsplash.com/photo-1556761175-b413da4baf72?auto=format&fit=crop&w=900&q=80">
  </div>
</section>

<section id="services">
  <div class="title">
    <h2>Our Services</h2>
    <p>Everything your business needs to grow online.</p>
  </div>
  <div class="grid">
    <div class="card"><i class="fa-solid fa-laptop-code"></i><h3>Website Design</h3><p>Modern, responsive, premium business websites.</p></div>
    <div class="card"><i class="fa-solid fa-chart-line"></i><h3>SEO Marketing</h3><p>Rank higher on Google and increase organic traffic.</p></div>
    <div class="card"><i class="fa-brands fa-instagram"></i><h3>Social Media</h3><p>Instagram, Facebook, and content marketing strategy.</p></div>
    <div class="card"><i class="fa-solid fa-bullhorn"></i><h3>Paid Ads</h3><p>Google Ads and social ads for lead generation.</p></div>
    <div class="card"><i class="fa-solid fa-envelope"></i><h3>Email Marketing</h3><p>Automated campaigns, newsletters, and offers.</p></div>
    <div class="card"><i class="fa-solid fa-robot"></i><h3>Automation</h3><p>Smart tools, CRM flows, and business automation.</p></div>
  </div>
</section>

<section>
  <div class="title">
    <h2>Why Choose Us</h2>
    <p>Premium design, smart strategy, and measurable results.</p>
  </div>
  <div class="grid">
    <div class="card"><i class="fa-solid fa-gem"></i><h3>Premium UI/UX</h3><p>Luxury layouts with professional brand identity.</p></div>
    <div class="card"><i class="fa-solid fa-bolt"></i><h3>Fast Performance</h3><p>Optimized website experience for users.</p></div>
    <div class="card"><i class="fa-solid fa-shield-halved"></i><h3>Trusted Quality</h3><p>Reliable work with modern business standards.</p></div>
  </div>
</section>

<section>
  <div class="title">
    <h2>Our Marketing Process</h2>
  </div>
  <div class="grid" style="counter-reset:item">
    <div class="card step"><h3>Discovery</h3><p>We understand your brand and goals.</p></div>
    <div class="card step"><h3>Strategy</h3><p>We create a custom growth roadmap.</p></div>
    <div class="card step"><h3>Execution</h3><p>We design, launch, and promote campaigns.</p></div>
    <div class="card step"><h3>Growth</h3><p>We track results and improve performance.</p></div>
  </div>
</section>

<section id="portfolio">
  <div class="title">
    <h2>Portfolio / Case Studies</h2>
  </div>
  <div class="grid">
    <div class="card"><h3>Beauty Brand Campaign</h3><p>Improved social media engagement and sales.</p></div>
    <div class="card"><h3>Business Website</h3><p>Created a modern lead-generation website.</p></div>
    <div class="card"><h3>SEO Growth Project</h3><p>Boosted search visibility and traffic.</p></div>
  </div>
</section>

<section>
  <div class="stats">
    <div class="stat"><h2 data-target="500">0</h2><p>Projects</p></div>
    <div class="stat"><h2 data-target="98">0</h2><p>Client Satisfaction</p></div>
    <div class="stat"><h2 data-target="10">0</h2><p>Years Experience</p></div>
    <div class="stat"><h2 data-target="24">0</h2><p>Support Hours</p></div>
  </div>
</section>

<section>
  <div class="title">
    <h2>Client Testimonials</h2>
  </div>
  <div class="testimonial">
    <p id="review">“Amazing premium website and marketing service. Very professional work!”</p>
    <h4 id="client">— Happy Client</h4>
  </div>
</section>

<section id="pricing">
  <div class="title">
    <h2>Pricing Plans</h2>
  </div>
  <div class="grid">
    <div class="card price"><h3>Starter</h3><h2>₹4,999</h2><ul><li>Basic Website</li><li>SEO Setup</li><li>Contact Form</li></ul><a class="btn" href="#contact">Choose</a></div>
    <div class="card price"><h3>Business</h3><h2>₹9,999</h2><ul><li>Premium Website</li><li>Social Media</li><li>Analytics</li></ul><a class="btn" href="#contact">Choose</a></div>
    <div class="card price"><h3>Pro</h3><h2>₹19,999</h2><ul><li>Full Marketing</li><li>Ads Strategy</li><li>Automation</li></ul><a class="btn" href="#contact">Choose</a></div>
  </div>
</section>

<section>
  <div class="title">
    <h2>Marketing Dashboard</h2>
  </div>
  <div class="dashboard">
    <canvas id="chart"></canvas>
  </div>
</section>

<section>
  <div class="title">
    <h2>Blog</h2>
  </div>
  <div class="grid">
    <div class="card"><h3>How SEO Helps Business</h3><p>Learn how search ranking increases leads.</p></div>
    <div class="card"><h3>Instagram Growth Tips</h3><p>Build your brand using social media.</p></div>
    <div class="card"><h3>Website Design Trends</h3><p>Modern UI ideas for business websites.</p></div>
  </div>
</section>

<section>
  <div class="title">
    <h2>Our Team</h2>
  </div>
  <div class="grid">
    <div class="card"><i class="fa-solid fa-user-tie"></i><h3>Sayali Ghadshi</h3><p>Founder & Web Developer</p></div>
    <div class="card"><i class="fa-solid fa-pen-nib"></i><h3>Creative Designer</h3><p>Branding & UI Design</p></div>
    <div class="card"><i class="fa-solid fa-chart-pie"></i><h3>Marketing Expert</h3><p>SEO & Ads Strategy</p></div>
  </div>
</section>

<section>
  <div class="title">
    <h2>FAQ</h2>
  </div>
  <div class="faq-item">
    <div class="faq-question">Do you create websites? <i class="fa-solid fa-plus"></i></div>
    <div class="faq-answer">Yes, we create professional business, portfolio, and e-commerce websites.</div>
  </div>
  <div class="faq-item">
    <div class="faq-question">Do you provide digital marketing? <i class="fa-solid fa-plus"></i></div>
    <div class="faq-answer">Yes, we provide SEO, social media, ads, branding, and marketing strategy.</div>
  </div>
  <div class="faq-item">
    <div class="faq-question">Is this website mobile responsive? <i class="fa-solid fa-plus"></i></div>
    <div class="faq-answer">Yes, this website works on desktop, tablet, and mobile devices.</div>
  </div>
</section>

<section id="contact">
  <div class="title">
    <h2>Contact Us</h2>
    <p>Let’s build your premium digital brand.</p>
  </div>
  <div class="contact">
    <form onsubmit="sendMessage(event)">
      <input type="text" placeholder="Your Name" required>
      <input type="email" placeholder="Your Email" required>
      <input type="text" placeholder="Subject" required>
      <textarea placeholder="Your Message" required></textarea>
      <button class="btn" type="submit">Send Message</button>
    </form>
    <iframe src="https://www.google.com/maps?q=Mumbai,India&output=embed"></iframe>
  </div>
</section>

<footer>
  <h2 class="logo">Precision Power Marketing</h2>
  <p>Premium Digital Marketing & Website Development Agency</p>
  <br>
  <p>Email: ghadshisayali2@gmail.com</p>
  <p>Instagram: 
    <a style="color:#facc15" href="https://www.instagram.com/sayalivikasghadshi" target="_blank">
      @sayalivikasghadshi
    </a>
  </p>
  <div class="social">
    <a href="https://www.instagram.com/sayalivikasghadshi" target="_blank"><i class="fa-brands fa-instagram"></i></a>
    <a href="#"><i class="fa-brands fa-facebook"></i></a>
    <a href="#"><i class="fa-brands fa-linkedin"></i></a>
    <a href="#"><i class="fa-brands fa-x-twitter"></i></a>
  </div>
  <p>© 2026 Precision Power Marketing. All Rights Reserved.</p>
</footer>

<a class="whatsapp" href="https://wa.me/917977193279" target="_blank">
  <i class="fa-brands fa-whatsapp"></i>
</a>

<script>
window.addEventListener("load",()=>{
  setTimeout(()=>{
    document.getElementById("preloader").style.display="none";
  },1200);
});

function toggleMenu(){
  document.getElementById("navLinks").classList.toggle("active");
}

document.querySelectorAll(".faq-question").forEach(q=>{
  q.addEventListener("click",()=>{
    const ans=q.nextElementSibling;
    ans.style.display=ans.style.display==="block"?"none":"block";
  });
});

const counters=document.querySelectorAll(".stat h2");
counters.forEach(counter=>{
  let target=+counter.dataset.target;
  let count=0;
  let speed=target/80;
  function update(){
    count+=speed;
    if(count<target){
      counter.innerText=Math.ceil(count)+"+";
      requestAnimationFrame(update);
    }else{
      counter.innerText=target+"+";
    }
  }
  update();
});

const reviews=[
  {
    text:"“Amazing premium website and marketing service. Very professional work!”",
    client:"— Happy Client"
  },
  {
    text:"“Our brand looks more powerful online after working with this agency.”",
    client:"— Business Owner"
  },
  {
    text:"“Beautiful design, smooth animations, and great marketing strategy.”",
    client:"— Startup Founder"
  }
];

let r=0;
setInterval(()=>{
  r=(r+1)%reviews.length;
  document.getElementById("review").innerText=reviews[r].text;
  document.getElementById("client").innerText=reviews[r].client;
},3000);

new Chart(document.getElementById("chart"),{
  type:"line",
  data:{
    labels:["Jan","Feb","Mar","Apr","May","Jun"],
    datasets:[{
      label:"Website Traffic",
      data:[120,190,300,420,620,850],
      borderColor:"#facc15",
      backgroundColor:"rgba(250,204,21,.15)",
      fill:true,
      tension:.4
    }]
  },
  options:{
    responsive:true,
    plugins:{legend:{labels:{color:"#fff"}}},
    scales:{
      x:{ticks:{color:"#fff"},grid:{color:"rgba(255,255,255,.1)"}},
      y:{ticks:{color:"#fff"},grid:{color:"rgba(255,255,255,.1)"}}
    }
  }
});

function sendMessage(e){
  e.preventDefault();
  alert("Thank you! Your message has been submitted.");
}
</script>

</body>
</html>
