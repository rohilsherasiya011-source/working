<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
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
}
*{box-sizing:border-box;margin:0;padding:0}
html,body{height:100%;font-family:Inter,system-ui,Arial,sans-serif;-webkit-font-smoothing:antialiased;background:var(--bg);color:var(--text)}
a{color:inherit;text-decoration:none}
.wrap{max-width:1200px;margin:0 auto;padding:20px}

/* Header */
header{display:flex;justify-content:space-between;align-items:center;padding:12px;background:#fff;border-radius:10px;box-shadow:var(--card-shadow);position:sticky;top:12px;z-index:40}
header .brand{display:flex;align-items:center;gap:10px;font-weight:700;font-size:18px}
nav{display:flex;gap:18px;align-items:center}
nav a{font-weight:600;color:var(--text)}
.nav-cta{background:linear-gradient(90deg,var(--green-1),var(--green-2));color:#fff;padding:10px 14px;border-radius:10px;}

/* Hero */
.hero{display:grid;grid-template-columns:1fr 460px;gap:28px;align-items:center;padding:36px;background:linear-gradient(180deg,#e9fff0,#f4fbf7);border-radius:12px;margin-top:18px}
.hero h1{font-size:34px;line-height:1.06;margin-bottom:12px}
.hero p{color:#235c43}
.cta-row{display:flex;gap:12px;margin-top:18px}
.btn{background:linear-gradient(90deg,var(--green-1),var(--green-2));color:#fff;padding:12px 16px;border-radius:10px;border:none;cursor:pointer}
.btn-outline{background:transparent;border:2px solid var(--green-1);color:var(--green-1);padding:10px 14px;border-radius:10px}

/* Cards & grids */
.card{background:#fff;padding:18px;border-radius:12px;box-shadow:var(--card-shadow)}
.grid-4{display:grid;grid-template-columns:repeat(4,1fr);gap:14px}
.grid-3{display:grid;grid-template-columns:repeat(3,1fr);gap:14px}

/* Sections */
section{margin-top:28px}
.section-title{font-size:22px;margin-bottom:8px;font-weight:600}
.sub{color:#2d6f52;margin-bottom:14px}

/* Pricing */
.pricing{display:grid;grid-template-columns:repeat(3,1fr);gap:14px}

/* Portfolio */
.portfolio{display:grid;grid-template-columns:repeat(3,1fr);gap:14px}

/* Process */
.process{display:flex;gap:12px;flex-wrap:wrap}

/* Testimonials */
.test-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:14px}

/* FAQ */
.faq .q{background:#fff;padding:12px;border-radius:8px;cursor:pointer;border:1px solid #eef8f2;margin-top:8px}
.faq .a{display:none;padding:12px;color:#274f3a}

/* Blog */
.blog-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:14px}

/* Contact */
.contact-grid{display:grid;grid-template-columns:1fr 360px;gap:20px}
form{display:grid;gap:10px;background:#fff;padding:18px;border-radius:12px;box-shadow:var(--card-shadow)}
input,select,textarea{padding:10px;border-radius:8px;border:1px solid #e6f3ea;background:#fbfff9;width:100%}
.form-msg{font-weight:600;color:var(--green-1)}

/* Footer */
footer{margin-top:28px;text-align:center;color:#0b3e2b;padding:18px}

/* WhatsApp sticky */
.wa-sticky{position:fixed;right:18px;bottom:18px;background:#25D366;color:#fff;padding:14px;border-radius:50%;box-shadow:0 12px 40px rgba(3,80,45,0.18);z-index:80;text-decoration:none;font-size:20px;display:flex;align-items:center;justify-content:center}

/* Utility & responsiveness */
.badges{display:flex;gap:8px;flex-wrap:wrap;margin-top:12px}
.badge{background:#e9fff1;padding:6px 10px;border-radius:999px;font-weight:700;color:var(--green-1)}
.reveal{opacity:0;transform:translateY(16px);transition:all .6s ease}
.reveal.show{opacity:1;transform:none}

@media(max-width:980px){
  .hero{grid-template-columns:1fr;padding:24px}
  .grid-4{grid-template-columns:repeat(2,1fr)}
  .grid-3{grid-template-columns:1fr}
  .contact-grid{grid-template-columns:1fr}
}
@media(max-width:480px){
  .hero h1{font-size:24px}
  nav{display:none}
}
</style>
</head>
<body>
<div class="wrap">
  <!-- Header -->
  <header>
    <div class="brand"><span style="font-size:20px">💸</span><div>DigitalIncome</div></div>
    <nav>
      <a href="#features">Features</a>
      <a href="#pricing">Pricing</a>
      <a href="#portfolio">Portfolio</a>
      <a href="#process">Process</a>
      <a href="#testimonials">Testimonials</a>
      <a href="#contact">Contact</a>
      <a class="nav-cta" href="#contact">Get Started</a>
    </nav>
  </header>

  <!-- Hero -->
  <section class="hero" id="home">
    <div>
      <h1>High-converting Landing Pages for UK Businesses</h1>
      <p class="sub">Design + Code + Deploy — Optimised for conversions, GDPR-ready and mobile-first.</p>
      <div class="cta-row">
        <a class="btn" href="#contact">Get Quote</a>
        <a class="btn-outline" href="#pricing">See Plans</a>
      </div>
      <div style="margin-top:16px;display:flex;gap:12px;align-items:center">
        <div class="card" style="padding:8px 12px">100+ Clients</div>
        <div class="card" style="padding:8px 12px">4.9 Rating</div>
        <div class="badge" style="padding:8px 12px">UK Ready</div>
      </div>
    </div>
    <div class="card">
      <h3 style="margin-bottom:8px">Lead Capture Demo</h3>
      <p style="color:#275e42;margin-bottom:12px">High converting form + CTA example</p>
      <button class="btn" onclick="alert('Demo clicked')">Try Demo</button>
    </div>
  </section>

  <!-- Features -->
  <section id="features" class="reveal">
    <div class="section-title">Features</div>
    <div class="sub">Everything you need to launch a converting landing page fast.</div>
    <div class="grid-4" style="margin-top:12px">
      <div class="card">⚡ Fast Loading</div>
      <div class="card">📱 Fully Responsive</div>
      <div class="card">🎯 Conversion Focused</div>
      <div class="card">🔌 Integrations (Mailchimp/WA)</div>
    </div>
  </section>

  <!-- Benefits -->
  <section class="reveal">
    <div class="section-title">Benefits</div>
    <div class="sub">Lead capture, selling & follow-up — everything in one funnel.</div>
    <div style="display:flex;gap:12px;flex-wrap:wrap;margin-top:12px">
      <div class="card" style="flex:1">Lead Generation</div>
      <div class="card" style="flex:1">Landing + Funnel</div>
      <div class="card" style="flex:1">UK Optimised</div>
    </div>
  </section>

  <!-- Pricing -->
  <section id="pricing" class="reveal">
    <div class="section-title">Pricing Plans</div>
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
  <section id="portfolio" class="reveal">
    <div class="section-title">Portfolio</div>
    <div class="sub">Selected landing pages & demos</div>
    <div class="portfolio" style="margin-top:12px">
      <div class="card">Shop Landing (Demo)</div>
      <div class="card">Service Landing</div>
      <div class="card">E-commerce Demo</div>
    </div>
  </section>

  <!-- Process -->
  <section id="process" class="reveal">
    <div class="section-title">How It Works</div>
    <div class="sub">A simple 5-step delivery for every project.</div>
    <div class="process" style="margin-top:12px">
      <div class="card" style="min-width:140px;text-align:center">1. Requirement</div>
      <div class="card" style="min-width:140px;text-align:center">2. Figma Design</div>
      <div class="card" style="min-width:140px;text-align:center">3. Development</div>
      <div class="card" style="min-width:140px;text-align:center">4. Revisions</div>
      <div class="card" style="min-width:140px;text-align:center">5. Launch</div>
    </div>
  </section>

  <!-- Testimonials -->
  <section id="testimonials" class="reveal">
    <div class="section-title">What Clients Say</div>
    <div class="test-grid" style="margin-top:12px">
      <div class="card">"Super fast delivery and great UK-standard design." — Sarah, London</div>
      <div class="card">"Conversion-focused layout helped our campaign." — James, Manchester</div>
      <div class="card">"Perfect responsive design for our shop." — Emma, Leeds</div>
    </div>
  </section>

  <!-- FAQ -->
  <section class="reveal">
    <div class="section-title">FAQ</div>
    <div class="faq" style="margin-top:12px">
      <div class="q">What is delivery time?</div>
      <div class="a">Standard delivery 3–5 business days. Rush delivery available.</div>
      <div class="q">Do you offer revisions?</div>
      <div class="a">Yes — 2–5 revisions depending on the chosen plan.</div>
      <div class="q">Can you publish on my domain?</div>
      <div class="a">Yes — we can setup hosting & deploy (Hostinger / Netlify / Vercel).</div>
    </div>
  </section>

  <!-- Trust Badges -->
  <section class="reveal">
    <div class="section-title">Trust & Guarantee</div>
    <div class="badges" style="margin-top:12px">
      <div class="card badge">GDPR Compliant</div>
      <div class="card badge">Secure Payment</div>
      <div class="card badge">Support 24/7</div>
    </div>
  </section>

  <!-- Blog -->
  <section class="reveal">
    <div class="section-title">Blog / Tips</div>
    <div class="blog-grid" style="margin-top:12px">
      <div class="card">How to improve landing conversions</div>
      <div class="card">Best practices for UK businesses</div>
      <div class="card">Quick SEO tips for landing pages</div>
    </div>
  </section>

  <!-- Contact -->
  <section id="contact" class="reveal">
    <div class="section-title">Get Your Landing Page</div>
    <div class="sub">Fill the form and we'll send a tailored quote within 24 hours.</div>
    <div class="contact-grid" style="margin-top:12px">
      <form id="leadForm" novalidate>
        <input type="text" name="name" placeholder="Your full name" required />
        <input type="email" name="email" placeholder="Email address" required />
        <input type="tel" name="phone" placeholder="WhatsApp / Phone" required />
        <select name="plan">
          <option value="basic">Basic — £49</option>
          <option value="standard">Standard — £129</option>
          <option value="premium">Premium — £249</option>
        </select>
        <textarea name="message" rows="4" placeholder="Project details (optional)"></textarea>
        <button type="submit" class="btn">Send Request</button>
        <div id="formMsg" class="form-msg" aria-live="polite"></div>
      </form>
      <aside class="card">
        <h3>Why choose us?</h3>
        <ul>
          <li>UK design standard</li>
          <li>Fast turnaround</li>
          <li>Clear pricing</li>
        </ul>
        <p>WhatsApp: <a href="https://wa.me/447700900123" target="_blank">+44 7700 900123</a></p>
      </aside>
    </div>
  </section>

  <footer>
    © <span id="year"></span> DigitalIncome — All rights reserved
  </footer>
</div>

<!-- WhatsApp sticky -->
<a class="wa-sticky" href="https://wa.me/447700900123" target="_blank">💬</a>

<script>
// GSAP scroll animations
gsap.utils.toArray('.reveal').forEach(elem=>{
  gsap.fromTo(elem,{opacity:0,y:20},{opacity:1,y:0,duration:1,scrollTrigger:{trigger:elem,start:"top 80%"}});
});

// FAQ toggle
document.querySelectorAll('.faq .q').forEach(q=>{
  q.addEventListener('click',()=>{ q.nextElementSibling.style.display = q.nextElementSibling.style.display === 'block' ? 'none':'block'; });
});

// Form submission simulation
document.getElementById('leadForm').addEventListener('submit', e=>{
  e.preventDefault();
  document.getElementById('formMsg').innerText = "Thanks! We'll contact you soon.";
  e.target.reset();
});

// Current year
document.getElementById('year').innerText = new Date().getFullYear();
</script>

</body>
</html>
