<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8"/>
<meta name="viewport" content="width=device-width,initial-scale=1"/>
<title>DigitalIncome — Premium Landing</title>
<meta name="description" content="High converting landing pages for UK small businesses. Design + Code + Deploy." />
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/ScrollTrigger.min.js"></script>

<style>
:root{
  --green-1:#0fa06a; --green-2:#17b980; --bg:#f3fef7; --text:#08311b;
  --card-shadow: 0 12px 40px rgba(6,60,34,0.05);
  --glass: rgba(255,255,255,0.8);
  --max-width:1200px;
  --gap:16px;
  --radius:12px;
  --transition:0.25s ease;
}

/* Reset & base */
*{box-sizing:border-box;margin:0;padding:0}
html,body{height:100%;font-family:Inter,system-ui,Arial,sans-serif;-webkit-font-smoothing:antialiased;background:var(--bg);color:var(--text);-webkit-text-size-adjust:100%}
a{color:inherit;text-decoration:none}
.wrap{max-width:var(--max-width);margin:0 auto;padding:20px}

/* Fluid typography */
h1{font-size:clamp(1.4rem, 2.4vw + 0.8rem, 2.25rem); line-height:1.06}
h2{font-size:clamp(1.1rem, 1.6vw + 0.7rem, 1.5rem)}
p,li{font-size:clamp(0.95rem, 0.9vw + 0.2rem, 1rem)}

/* Header */
.header-wrap{position:sticky;top:12px;z-index:60}
header{display:flex;justify-content:space-between;align-items:center;padding:12px;background:#fff;border-radius:10px;box-shadow:var(--card-shadow)}
.brand{display:flex;align-items:center;gap:10px;font-weight:700;font-size:18px}
.nav{display:flex;gap:18px;align-items:center}
.nav a{font-weight:600;color:var(--text);padding:8px;border-radius:8px}
.nav-cta{background:linear-gradient(90deg,var(--green-1),var(--green-2));color:#fff;padding:10px 14px;border-radius:10px;white-space:nowrap}

/* Mobile nav (hamburger) */
.hamburger{display:none;border:0;background:transparent;font-size:20px;padding:8px;border-radius:8px;cursor:pointer}
.offcanvas{position:fixed;inset:0;background:rgba(3,20,12,0.4);display:none;align-items:flex-end;z-index:70}
.offcanvas-panel{background:#fff;width:100%;max-width:420px;padding:18px;border-top-left-radius:16px;border-top-right-radius:16px;box-shadow:var(--card-shadow);transform:translateY(20px);opacity:0;transition:transform .28s ease,opacity .2s ease}
.offcanvas.show{display:flex}
.offcanvas-panel.show{transform:none;opacity:1}

/* Hero */
.hero{display:grid;grid-template-columns:1fr 440px;gap:28px;align-items:center;padding:36px;background:linear-gradient(180deg,#e9fff0,#f4fbf7);border-radius:12px;margin-top:18px}
.hero h1{margin-bottom:12px}
.hero p.sub{color:#235c43;margin-bottom:8px}
.cta-row{display:flex;gap:12px;margin-top:18px}
.btn{background:linear-gradient(90deg,var(--green-1),var(--green-2));color:#fff;padding:12px 16px;border-radius:10px;border:none;cursor:pointer;font-weight:700}
.btn:active{transform:translateY(1px)}
.btn-outline{background:transparent;border:2px solid var(--green-1);color:var(--green-1);padding:10px 14px;border-radius:10px}

/* Card common */
.card{background:#fff;padding:18px;border-radius:var(--radius);box-shadow:var(--card-shadow)}
.small-card{padding:8px 12px}

/* Grid utilities */
.grid-4{display:grid;grid-template-columns:repeat(4,1fr);gap:14px}
.grid-3{display:grid;grid-template-columns:repeat(3,1fr);gap:14px}
.pricing{display:grid;grid-template-columns:repeat(3,1fr);gap:14px}
.portfolio{display:grid;grid-template-columns:repeat(3,1fr);gap:14px}
.test-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:14px}

/* FAQ */
.faq .q{background:#fff;padding:12px;border-radius:8px;cursor:pointer;border:1px solid #eef8f2;margin-top:8px;display:flex;justify-content:space-between;align-items:center}
.faq .a{display:none;padding:12px;color:#274f3a}

/* Contact */
.contact-grid{display:grid;grid-template-columns:1fr 360px;gap:20px}
form{display:grid;gap:10px;background:#fff;padding:18px;border-radius:12px;box-shadow:var(--card-shadow)}
input,select,textarea{padding:12px;border-radius:8px;border:1px solid #e6f3ea;background:#fbfff9;width:100%;font-size:1rem}
.form-msg{font-weight:700;color:var(--green-1)}

/* Footer */
footer{margin-top:28px;text-align:center;color:#0b3e2b;padding:18px}

/* WhatsApp sticky */
.wa-sticky{position:fixed;right:18px;bottom:18px;background:#25D366;color:#fff;padding:14px;border-radius:50%;box-shadow:0 12px 40px rgba(3,80,45,0.18);z-index:80;text-decoration:none;font-size:20px;display:flex;align-items:center;justify-content:center}

/* Reveal animation helper */
.reveal{opacity:0;transform:translateY(16px);transition:all .6s ease}
.reveal.show{opacity:1;transform:none}

/* Small helpers */
.badges{display:flex;gap:8px;flex-wrap:wrap;margin-top:12px}
.badge{background:#e9fff1;padding:6px 10px;border-radius:999px;font-weight:700;color:var(--green-1)}
.kicker{font-weight:700;color:#2d6f52}

/* Responsive breakpoints */
@media (max-width:1100px){
  .hero{grid-template-columns:1fr 360px}
  .pricing{grid-template-columns:repeat(2,1fr)}
  .grid-4{grid-template-columns:repeat(3,1fr)}
  .grid-3{grid-template-columns:repeat(2,1fr)}
  .portfolio{grid-template-columns:repeat(2,1fr)}
  .test-grid{grid-template-columns:repeat(2,1fr)}
  .contact-grid{grid-template-columns:1fr 320px}
}

@media (max-width:820px){
  .nav{display:none}
  .hamburger{display:inline-flex}
  .hero{grid-template-columns:1fr;padding:28px}
  .pricing{grid-template-columns:1fr}
  .grid-4{grid-template-columns:repeat(2,1fr)}
  .grid-3{grid-template-columns:1fr}
  .portfolio{grid-template-columns:1fr}
  .test-grid{grid-template-columns:1fr}
  .contact-grid{grid-template-columns:1fr}
  .offcanvas-panel{max-width:100%;border-radius:12px}
}

@media (max-width:480px){
  header{padding:10px}
  .wrap{padding:14px}
  .hero{padding:18px}
  .btn{padding:12px 14px}
  input,select,textarea{padding:10px}
  .brand{font-size:16px}
  .kicker{font-size:0.95rem}
}

/* Focus states for accessibility */
a:focus,button:focus,input:focus,select:focus,textarea:focus{outline:3px solid rgba(23,185,115,0.18);outline-offset:2px}
</style>
</head>
<body>
<div class="wrap">

  <!-- Header -->
  <div class="header-wrap">
    <header>
      <div class="brand" aria-hidden="true"><span style="font-size:20px">💸</span><div style="line-height:1">DigitalIncome</div></div>

      <!-- Desktop nav -->
      <nav class="nav" aria-label="Primary navigation">
        <a href="#features">Features</a>
        <a href="#pricing">Pricing</a>
        <a href="#portfolio">Portfolio</a>
        <a href="#process">Process</a>
        <a href="#testimonials">Testimonials</a>
        <a href="#contact">Contact</a>
        <a class="nav-cta" href="#contact">Get Started</a>
      </nav>

      <!-- Hamburger for mobile -->
      <button class="hamburger" id="hamburger" aria-label="Open menu" aria-controls="mobile-menu" aria-expanded="false">☰</button>
    </header>

    <!-- Off-canvas mobile menu -->
    <div class="offcanvas" id="offcanvas" aria-hidden="true">
      <div class="offcanvas-panel" role="dialog" aria-modal="true" id="mobile-menu" aria-labelledby="menuTitle">
        <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:8px">
          <strong id="menuTitle">Menu</strong>
          <button id="closeMenu" aria-label="Close menu" style="background:none;border:0;font-size:20px;cursor:pointer">✕</button>
        </div>
        <nav style="display:flex;flex-direction:column;gap:10px" aria-label="Mobile navigation">
          <a href="#features" class="nav-link">Features</a>
          <a href="#pricing" class="nav-link">Pricing</a>
          <a href="#portfolio" class="nav-link">Portfolio</a>
          <a href="#process" class="nav-link">Process</a>
          <a href="#testimonials" class="nav-link">Testimonials</a>
          <a href="#contact" class="nav-link">Contact</a>
          <a class="nav-cta" href="#contact" style="display:inline-block;margin-top:8px;text-align:center">Get Started</a>
        </nav>
      </div>
    </div>
  </div>

  <!-- Hero -->
  <section class="hero reveal" id="home" aria-label="Hero">
    <div>
      <h1>High-converting Landing Pages for UK Businesses</h1>
      <p class="sub">Design + Code + Deploy — Optimised for conversions, GDPR-ready and mobile-first.</p>
      <div class="cta-row" role="group" aria-label="Call to actions">
        <a class="btn" href="#contact">Get Quote</a>
        <a class="btn-outline" href="#pricing">See Plans</a>
      </div>

      <div style="margin-top:16px;display:flex;gap:12px;align-items:center;flex-wrap:wrap">
        <div class="card small-card">100+ Clients</div>
        <div class="card small-card">4.9 Rating</div>
        <div class="badge" style="padding:8px 12px">UK Ready</div>
      </div>
    </div>

    <div class="card" aria-hidden="false">
      <h3 style="margin-bottom:8px">Lead Capture Demo</h3>
      <p style="color:#275e42;margin-bottom:12px">High converting form + CTA example</p>
      <button class="btn" onclick="alert('Demo clicked')">Try Demo</button>
    </div>
  </section>

  <!-- Features -->
  <section id="features" class="reveal" aria-labelledby="featuresTitle">
    <div class="section-title" id="featuresTitle" style="font-size:1.2rem;font-weight:700;margin-top:18px">Features</div>
    <div class="sub">Everything you need to launch a converting landing page fast.</div>
    <div class="grid-4" style="margin-top:12px">
      <div class="card">⚡ Fast Loading</div>
      <div class="card">📱 Fully Responsive</div>
      <div class="card">🎯 Conversion Focused</div>
      <div class="card">🔌 Integrations (Mailchimp/WA)</div>
    </div>
  </section>

  <!-- Benefits -->
  <section class="reveal" aria-labelledby="benefitsTitle">
    <div class="section-title" id="benefitsTitle" style="margin-top:18px">Benefits</div>
    <div class="sub">Lead capture, selling & follow-up — everything in one funnel.</div>
    <div style="display:flex;gap:12px;flex-wrap:wrap;margin-top:12px">
      <div class="card" style="flex:1;min-width:200px">Lead Generation</div>
      <div class="card" style="flex:1;min-width:200px">Landing + Funnel</div>
      <div class="card" style="flex:1;min-width:200px">UK Optimised</div>
    </div>
  </section>

  <!-- Pricing -->
  <section id="pricing" class="reveal" aria-labelledby="pricingTitle">
    <div class="section-title" id="pricingTitle" style="margin-top:18px">Pricing Plans</div>
    <div class="sub">Simple plans for freelancers, agencies & small businesses.</div>
    <div class="pricing" style="margin-top:12px">
      <div class="card">
        <h3>Basic</h3>
        <p style="font-weight:700;color:var(--green-1)">£49 / one-time</p>
        <ul style="text-align:left;margin-top:8px">
          <li>1-page responsive landing</li>
          <li>Contact form</li>
          <li>2 revisions</li>
        </ul>
        <div style="margin-top:12px"><a class="btn" href="#contact">Order Basic</a></div>
      </div>

      <div class="card" style="border:2px solid rgba(15,105,60,0.08);transform:translateY(-6px)">
        <h3>Standard</h3>
        <p style="font-weight:700;color:var(--green-1)">£129 / one-time</p>
        <ul style="text-align:left;margin-top:8px">
          <li>Figma design + HTML/CSS</li>
          <li>Up to 3 sections + hero</li>
          <li>5 revisions + basic SEO</li>
        </ul>
        <div style="margin-top:12px"><a class="btn" href="#contact">Order Standard</a></div>
      </div>

      <div class="card">
        <h3>Premium</h3>
        <p style="font-weight:700;color:var(--green-1)">£249 / one-time</p>
        <ul style="text-align:left;margin-top:8px">
          <li>Full landing + funnel</li>
          <li>Integrations (Mailchimp/WA)</li>
          <li>Priority support</li>
        </ul>
        <div style="margin-top:12px"><a class="btn" href="#contact">Order Premium</a></div>
      </div>
    </div>
  </section>

  <!-- Portfolio -->
  <section id="portfolio" class="reveal" aria-labelledby="portfolioTitle">
    <div class="section-title" id="portfolioTitle" style="margin-top:18px">Portfolio</div>
    <div class="sub">Selected landing pages & demos</div>
    <div class="portfolio" style="margin-top:12px">
      <div class="card">Shop Landing (Demo)</div>
      <div class="card">Service Landing</div>
      <div class="card">E-commerce Demo</div>
    </div>
  </section>

  <!-- Process -->
  <section id="process" class="reveal" aria-labelledby="processTitle">
    <div class="section-title" id="processTitle" style="margin-top:18px">How It Works</div>
    <div class="sub">A simple 5-step delivery for every project.</div>
    <div class="process" style="display:flex;gap:12px;flex-wrap:wrap;margin-top:12px">
      <div class="card" style="min-width:140px;text-align:center">1. Requirement</div>
      <div class="card" style="min-width:140px;text-align:center">2. Figma Design</div>
      <div class="card" style="min-width:140px;text-align:center">3. Development</div>
      <div class="card" style="min-width:140px;text-align:center">4. Revisions</div>
      <div class="card" style="min-width:140px;text-align:center">5. Launch</div>
    </div>
  </section>

  <!-- Testimonials -->
  <section id="testimonials" class="reveal" aria-labelledby="testTitle">
    <div class="section-title" id="testTitle" style="margin-top:18px">What Clients Say</div>
    <div class="test-grid" style="margin-top:12px">
      <div class="card">"Super fast delivery and great UK-standard design." — Sarah, London</div>
      <div class="card">"Conversion-focused layout helped our campaign." — James, Manchester</div>
      <div class="card">"Perfect responsive design for our shop." — Emma, Leeds</div>
    </div>
  </section>

  <!-- FAQ -->
  <section class="reveal" aria-labelledby="faqTitle">
    <div class="section-title" id="faqTitle" style="margin-top:18px">FAQ</div>
    <div class="faq" style="margin-top:12px">
      <div class="q" tabindex="0">What is delivery time?<span aria-hidden="true">▾</span></div>
      <div class="a">Standard delivery 3–5 business days. Rush delivery available.</div>
      <div class="q" tabindex="0">Do you offer revisions?<span aria-hidden="true">▾</span></div>
      <div class="a">Yes — 2–5 revisions depending on the chosen plan.</div>
      <div class="q" tabindex="0">Can you publish on my domain?<span aria-hidden="true">▾</span></div>
      <div class="a">Yes — we can setup hosting & deploy (Hostinger / Netlify / Vercel).</div>
    </div>
  </section>

  <!-- Trust Badges -->
  <section class="reveal" style="margin-top:18px">
    <div class="section-title">Trust & Guarantee</div>
    <div class="badges" style="margin-top:12px">
      <div class="card badge">GDPR Compliant</div>
      <div class="card badge">Secure Payment</div>
      <div class="card badge">Support 24/7</div>
    </div>
  </section>

  <!-- Blog -->
  <section class="reveal" style="margin-top:18px">
    <div class="section-title">Blog / Tips</div>
    <div class="blog-grid" style="margin-top:12px; display:grid; grid-template-columns:repeat(3,1fr); gap:14px">
      <div class="card">How to improve landing conversions</div>
      <div class="card">Best practices for UK businesses</div>
      <div class="card">Quick SEO tips for landing pages</div>
    </div>
  </section>

  <!-- Contact -->
  <section id="contact" class="reveal" style="margin-top:18px">
    <div class="section-title">Get Your Landing Page</div>
    <div class="sub">Fill the form and we'll send a tailored quote within 24 hours.</div>
    <div class="contact-grid" style="margin-top:12px">
      <form id="leadForm" novalidate>
        <input type="text" name="name" id="name" placeholder="Your full name" required aria-required="true"/>
        <input type="email" name="email" id="email" placeholder="Email address" required aria-required="true"/>
        <input type="tel" name="phone" id="phone" placeholder="WhatsApp / Phone" required aria-required="true"/>
        <select name="plan" id="plan" aria-label="Select plan">
          <option value="basic">Basic — £49</option>
          <option value="standard">Standard — £129</option>
          <option value="premium">Premium — £249</option>
        </select>
        <textarea name="message" id="message" rows="4" placeholder="Project details (optional)"></textarea>
        <button type="submit" class="btn">Send Request</button>
        <div id="formMsg" class="form-msg" aria-live="polite"></div>
      </form>

      <aside class="card" aria-labelledby="whyTitle">
        <h3 id="whyTitle">Why choose us?</h3>
        <ul>
          <li>UK design standard</li>
          <li>Fast turnaround</li>
          <li>Clear pricing</li>
        </ul>
        <p>WhatsApp: <a href="https://wa.me/447700900123" target="_blank" rel="noopener">+44 7700 900123</a></p>
      </aside>
    </div>
  </section>

  <footer>
    © <span id="year"></span> DigitalIncome — All rights reserved
  </footer>
</div>

<!-- WhatsApp sticky -->
<a class="wa-sticky" href="https://wa.me/447700900123" target="_blank" rel="noopener">💬</a>

<script>
/* GSAP scroll animations */
if (window.gsap && window.ScrollTrigger){
  gsap.utils.toArray('.reveal').forEach(elem=>{
    gsap.fromTo(elem,{opacity:0,y:20},{opacity:1,y:0,duration:0.9,scrollTrigger:{trigger:elem,start:"top 85%"}});
  });
}

/* FAQ toggle accessible */
document.querySelectorAll('.faq .q').forEach(q=>{
  q.addEventListener('click', ()=> toggleFAQ(q));
  q.addEventListener('keydown', e=>{ if(e.key==='Enter' || e.key===' ') { e.preventDefault(); toggleFAQ(q); } });
});
function toggleFAQ(q){
  const a = q.nextElementSibling;
  const isOpen = a.style.display === 'block';
  a.style.display = isOpen ? 'none' : 'block';
  q.setAttribute('aria-expanded', String(!isOpen));
}

/* Off-canvas mobile menu controls */
const offcanvas = document.getElementById('offcanvas');
const panel = document.querySelector('.offcanvas-panel');
const hamburger = document.getElementById('hamburger');
const closeMenu = document.getElementById('closeMenu');

function openMenu(){
  offcanvas.classList.add('show');
  panel.classList.add('show');
  offcanvas.setAttribute('aria-hidden','false');
  hamburger.setAttribute('aria-expanded','true');
  // Prevent body scroll on mobile
  document.body.style.overflow = 'hidden';
}
function closeMenuFunc(){
  panel.classList.remove('show');
  offcanvas.classList.remove('show');
  offcanvas.setAttribute('aria-hidden','true');
  hamburger.setAttribute('aria-expanded','false');
  document.body.style.overflow = '';
}
hamburger.addEventListener('click', openMenu);
closeMenu.addEventListener('click', closeMenuFunc);
offcanvas.addEventListener('click', (e)=>{ if(e.target === offcanvas) closeMenuFunc(); });
document.querySelectorAll('.nav-link').forEach(a=> a.addEventListener('click', closeMenuFunc));

/* Form submission simulation with validation */
const leadForm = document.getElementById('leadForm');
const formMsg = document.getElementById('formMsg');

leadForm.addEventListener('submit', (e)=>{
  e.preventDefault();
  formMsg.textContent = '';
  const name = document.getElementById('name').value.trim();
  const email = document.getElementById('email').value.trim();
  const phone = document.getElementById('phone').value.trim();

  if(!name || !email || !phone){
    formMsg.textContent = 'Please fill name, email & phone.';
    return;
  }
  // basic email pattern
  const emailPattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
  if(!emailPattern.test(email)){
    formMsg.textContent = 'Please enter a valid email.';
    return;
  }
  formMsg.textContent = 'Thanks! We\'ll contact you soon.';
  leadForm.reset();
});

/* Current year */
document.getElementById('year').innerText = new Date().getFullYear();

/* Small accessibility: skip to content on keyboard nav (optional) */
// Add if you want: a visually hidden skip link at top (left as comment)
</script>
</body>
</html>
