# parbhu-kirpa-gas-repair
`parbhu-kirpa-gas-repair.html`
```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Parbhu Kirpa Gas &amp; Repair</title>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap" rel="stylesheet" />
<style>
  /* Reset and base */
  *, *::before, *::after {
    margin: 0; padding: 0; box-sizing: border-box;
  }
  body {
    font-family: 'Poppins', sans-serif;
    background: linear-gradient(135deg, #f0f4f8, #d9e4f5);
    color: #223344;
    display: flex;
    flex-direction: column;
    min-height: 100vh;
    scroll-behavior: smooth;
  }
  a {
    color: inherit;
    text-decoration: none;
  }
  a:hover, a:focus {
    text-decoration: underline;
    outline: none;
  }

  header {
    background: #1e3a8a;
    color: #f0f4f8;
    text-align: center;
    padding: 24px 20px;
    font-size: 2rem;
    font-weight: 700;
    letter-spacing: 0.1em;
    box-shadow: 0 4px 12px rgba(30,58,138,0.6);
    position: sticky;
    top: 0;
    z-index: 100;
  }

  nav {
    background: #274690;
    display: flex;
    justify-content: center;
    box-shadow: 0 3px 8px rgba(39,70,144,0.5);
  }
  nav a {
    display: inline-block;
    padding: 16px 26px;
    font-weight: 600;
    font-size: 1.1rem;
    color: #cbd6ef;
    transition: background-color 0.4s, color 0.3s ease;
    border-bottom: 3px solid transparent;
    border-radius: 0 0 8px 8px;
  }
  nav a:hover, nav a:focus {
    background-color: #1a2e6e;
    color: #dbe9ff;
    border-bottom: 3px solid #82c0ff;
    outline: none;
  }

  .hero {
    position: relative;
    background: url('https://images.pexels.com/photos/2445116/pexels-photo-2445116.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260') center/cover no-repeat;
    min-height: 320px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-align: center;
    color: #edf4ff;
    padding: 80px 20px 90px;
    border-radius: 0 0 48px 48px;
    box-shadow: inset 0 0 0 1000px rgba(30,58,138,0.55);
  }
  .hero h1 {
    font-size: 3.6rem;
    font-weight: 800;
    letter-spacing: 0.1em;
    margin-bottom: 16px;
    text-shadow: 1px 1px 8px rgba(0,0,0,0.6);
  }
  .hero p {
    font-size: 1.3rem;
    max-width: 480px;
    margin: 0 auto 40px;
    font-weight: 500;
    text-shadow: 1px 1px 6px rgba(0,0,0,0.4);
    line-height: 1.4;
  }
  .btn-primary {
    background: linear-gradient(90deg, #4f8ef7 0%, #184ccf 100%);
    color: white;
    padding: 16px 48px;
    font-size: 1.25rem;
    font-weight: 700;
    border: none;
    border-radius: 36px;
    cursor: pointer;
    box-shadow:
      0 8px 24px rgba(72,122,235,0.6);
    transition: background 0.3s ease, box-shadow 0.25s ease;
  }
  .btn-primary:hover, .btn-primary:focus {
    background: linear-gradient(90deg, #3a75e2 0%, #0f38a4 100%);
    box-shadow:
      0 10px 30px rgba(30,58,138,0.8);
    outline: none;
  }

  main {
    flex-grow: 1;
    max-width: 900px;
    margin: 40px auto 60px;
    padding: 0 20px;
  }

  section {
    margin-bottom: 56px;
    background: #ffffffdd;
    padding: 32px 32px 40px;
    border-radius: 24px;
    box-shadow:
      8px 12px 20px rgba(100,140,220,0.12);
    backdrop-filter: saturate(180%) blur(12px);
  }

  h2 {
    font-size: 2.4rem;
    margin-bottom: 28px;
    font-weight: 800;
    color: #184ccf;
    letter-spacing: 0.07em;
    border-left: 12px solid #4f8ef7;
    padding-left: 18px;
  }

  ul.service-list {
    list-style: none;
  }
  ul.service-list li {
    font-size: 1.18rem;
    color: #324a6e;
    position: relative;
    padding-left: 38px;
    margin-bottom: 20px;
    font-weight: 600;
  }
  ul.service-list li::before {
    content: "🔧";
    position: absolute;
    font-size: 1.65rem;
    left: 0;
    top: 3px;
  }

  .features {
    display: flex;
    flex-wrap: wrap;
    gap: 26px;
    justify-content: center;
  }
  .feature-box {
    flex: 1 1 220px;
    background: #e8edff;
    border-radius: 20px;
    padding: 30px 24px;
    font-weight: 700;
    color: #174092;
    text-align: center;
    box-shadow:
      12px 12px 18px #c4caff,
      -12px -12px 18px #ffffff;
    transition: transform 0.4s ease, box-shadow 0.4s ease;
    user-select: none;
    font-size: 1.2rem;
    border: 2px solid transparent;
    cursor: default;
  }
  .feature-box:hover, .feature-box:focus {
    transform: translateY(-9px);
    box-shadow:
      3px 3px 10px #a2b5e8,
      -3px -3px 10px #f9fbff;
    border-color: #4f8ef7;
    outline: none;
  }

  form {
    max-width: 640px;
    margin: 0 auto;
    padding: 36px 36px 40px;
    background: #e9efffdd;
    border-radius: 24px;
    box-shadow:
      12px 12px 22px rgba(100,140,255,0.15),
      -12px -12px 22px #ffffff;
    backdrop-filter: saturate(200%) blur(15px);
  }
  form label {
    display: block;
    margin-bottom: 10px;
    font-weight: 700;
    font-size: 1.1rem;
    color: #224585;
  }
  form input, form textarea {
    width: 100%;
    padding: 16px 20px;
    margin-bottom: 26px;
    font-size: 1.14rem;
    font-family: 'Poppins', sans-serif;
    border-radius: 18px;
    border: none;
    background:
      linear-gradient(145deg, #f7fbff, #dbe6ff);
    box-shadow:
      8px 8px 12px #c8d3f7,
      -8px -8px 12px #ffffff;
    transition: box-shadow 0.35s ease;
  }
  form input:focus, form textarea:focus {
    outline: none;
    box-shadow:
      3px 3px 10px #8ca1f9,
      -3px -3px 10px #f4f8ff;
  }
  form textarea {
    min-height: 88px;
    resize: vertical;
  }
  form button {
    width: 100%;
    background: #184ccf;
    color: white;
    font-size: 1.3rem;
    font-weight: 800;
    padding: 18px 28px;
    border: none;
    border-radius: 36px;
    cursor: pointer;
    box-shadow:
      0 10px 28px #3a77e5;
    transition: background 0.3s ease, box-shadow 0.3s ease;
  }
  form button:hover, form button:focus {
    background: #113a9a;
    box-shadow:
      0 12px 34px #1644b4;
    outline: none;
  }
  .contact-info {
    font-weight: 700;
    text-align: center;
    margin-bottom: 28px;
    font-size: 1.18rem;
    color: #224585;
  }
  .contact-info a {
    font-weight: 800;
    color: #3b6dd8;
    border-bottom: 1.8px solid transparent;
    transition: border-color 0.3s ease;
  }
  .contact-info a:hover, .contact-info a:focus {
    border-color: #4f8ef7;
    outline: none;
  }

  footer {
    background: #1e3a8a;
    color: #d4dafa;
    text-align: center;
    padding: 22px 20px;
    font-size: 1.05rem;
    font-weight: 600;
    letter-spacing: 0.1em;
    margin-top: auto;
    box-shadow: 0 -3px 10px rgba(30,58,138,0.65);
  }

  /* Responsive */
  @media (max-width: 620px) {
    .hero h1 {
      font-size: 2.6rem;
    }
    .hero p {
      font-size: 1.1rem;
      max-width: 320px;
    }
    section {
      margin-bottom: 36px;
      padding: 28px 20px;
    }
    h2 {
      font-size: 1.8rem;
      padding-left: 14px;
      border-left-width: 8px;
    }
    .feature-box {
      flex-basis: 100%;
      font-size: 1.1rem;
      padding: 24px 18px;
    }
    form {
      padding: 28px 22px 32px 22px;
      max-width: 100%;
    }
  }
</style>
</head>
<body>
<header>Parbhu Kirpa Gas &amp; Repair</header>
<nav>
  <a href="#services" tabindex="0">Services</a>
  <a href="#why-us" tabindex="0">Why Us</a>
  <a href="#contact" tabindex="0">Contact</a>
</nav>
<section class="hero" aria-label="Hero section">
  <h1>Fast &amp; Reliable Gas Stove Repair</h1>
  <p>Expert technicians fixing your gas stove safely and efficiently. We bring your kitchen back to life!</p>
  <button class="btn-primary" onclick="document.getElementById('contact').scrollIntoView({behavior:'smooth'});" aria-label="Request Service">Request Service</button>
</section>
<main>
  <section id="services" aria-labelledby="services-heading">
    <h2 id="services-heading">Our Gas Stove Repair Services</h2>
    <ul class="service-list" role="list">
      <li>Ignition Issues: Fixing faulty igniters and spark modules for consistent lighting</li>
      <li>Flame Adjustment: Ensuring even and optimal cooking flames</li>
      <li>Gas Leak Detection &amp; Repair: Prioritizing your safety with thorough inspections</li>
      <li>Burner Replacement: Repairing or replacing damaged burners</li>
      <li>Thermocouple &amp; Safety Valve Repair: Maintaining necessary safety controls</li>
      <li>Cleaning &amp; Maintenance: Removing grease and debris to extend stove life</li>
      <li>Expert Consultation: Advice on proper stove care and maintenance</li>
    </ul>
  </section>
  <section id="why-us" aria-labelledby="whyus-heading">
    <h2 id="whyus-heading">Why Choose Us?</h2>
    <div class="features" role="list">
      <div class="feature-box" role="listitem" tabindex="0" aria-label="Certified and Experienced Technicians">🔧 Certified &amp; Experienced Technicians</div>
      <div class="feature-box" role="listitem" tabindex="0" aria-label="Prompt and Reliable Service">⏱️ Prompt &amp; Reliable Service</div>
      <div class="feature-box" role="listitem" tabindex="0" aria-label="Competitive Pricing and Transparent Quotes">💰 Competitive Pricing &amp; Transparent Quotes</div>
      <div class="feature-box" role="listitem" tabindex="0" aria-label="Safety First Approach">🛡️ Safety First Approach</div>
      <div class="feature-box" role="listitem" tabindex="0" aria-label="Supports All Major Brands">✔️ All Major Brands Supported</div>
    </div>
  </section>
  <section id="contact" aria-labelledby="contact-heading">
    <h2 id="contact-heading">Contact Us</h2>
    <p class="contact-info">Phone: <a href="tel:+917508216088" aria-label="Call phone number 7508216088">+91 75082 16088</a> | Email: <a href="mailto:service@gasstoverepair.com" aria-label="Email service at gas stove repair dot com">service@gasstoverepair.com</a></p>
    <form id="contactForm" aria-label="Service request form">
      <label for="name">Your Name<span aria-hidden="true" style="color:#184ccf;"> *</span></label>
      <input type="text" id="name" name="name" required placeholder="Full Name" autocomplete="name" aria-required="true" />
      <label for="email">Your Email<span aria-hidden="true" style="color:#184ccf;"> *</span></label>
      <input type="email" id="email" name="email" required placeholder="email@example.com" autocomplete="email" aria-required="true" />
      <label for="phone">Phone Number</label>
      <input type="tel" id="phone" name="phone" placeholder="Optional" autocomplete="tel" pattern="[+0-9\s-]{7,15}" title="Enter a valid phone number" />
      <label for="message">Describe Your Issue<span aria-hidden="true" style="color:#184ccf;"> *</span></label>
      <textarea id="message" name="message" rows="4" required placeholder="Briefly describe the problem..." aria-required="true"></textarea>
      <button type="submit" aria-label="Submit service request form">Submit Request</button>
    </form>
  </section>
</main>
<footer>
  &copy; 2024 Parbhu Kirpa Gas &amp; Repair. All rights reserved.
</footer>
<script>
  document.getElementById('contactForm').addEventListener('submit', function(e) {
    e.preventDefault();
    const name = this.name.value.trim();
    const email = this.email.value.trim();
    const message = this.message.value.trim();
    if (!name || !email || !message) {
      alert('Please fill in all required fields.');
      return;
    }
    const emailPattern = /^[^\\s@]+@[^\\s@]+\\.[^\\s@]+$/;
    if (!emailPattern.test(email)) {
      alert('Please enter a valid email address.');
      return;
    }
    alert(`Thank you, ${name}! Your service request has been received. We will contact you shortly.`);
    this.reset();
  });
</script>
</body>
</html>

```

