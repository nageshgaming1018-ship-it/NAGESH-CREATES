# NAGESH-CREATES
"Creative graphic design and AI visual creation service
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Nagesh Creates | Ultimate Creative Agency</title>
  <meta name="description" content="Nagesh Creates - Poster Design, AI Image Creation, Thumbnails & Branding. 30+ advanced features in one portfolio.">
  <meta property="og:title" content="Nagesh Creates | Ultimate Creative Agency">
  <meta property="og:description" content="Poster Design, AI Image Creation, Thumbnails & Branding">
  <meta property="og:type" content="website">

  <!-- Favicon -->
  <link rel="icon" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><text y='.9em' font-size='90'>🎨</text></svg>">

  <!-- Preload / Preconnect -->
  <link rel="preconnect" href="https://unpkg.com">
  <link rel="preconnect" href="https://cdn.jsdelivr.net">
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

  <!-- PWA Manifest -->
  <link rel="manifest" href="data:application/manifest+json,%7B%22name%22%3A%22Nagesh%20Creates%22%2C%22short_name%22%3A%22Nagesh%22%2C%22start_url%22%3A%22.%2F%22%2C%22display%22%3A%22standalone%22%2C%22background_color%22%3A%22%23080808%22%2C%22theme_color%22%3A%22%23ff9800%22%2C%22icons%22%3A%5B%7B%22src%22%3A%22icon-192.png%22%2C%22sizes%22%3A%22192x192%22%2C%22type%22%3A%22image%2Fpng%22%7D%5D%7D">

  <!-- AOS Animation -->
  <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
  <!-- GLightbox -->
  <link href="https://cdn.jsdelivr.net/npm/glightbox/dist/css/glightbox.min.css" rel="stylesheet">

  <style>
    :root {
      --bg: #080808; --surface: #181818; --text: #fff; --text-secondary: #ddd;
      --accent: #ff9800; --accent-light: #ffb74d; --nav-bg: rgba(0,0,0,.6);
      --card-bg: #181818; --shadow: 0 4px 30px rgba(0,0,0,0.5);
    }
    .light-mode {
      --bg: #f5f5f5; --surface: #ffffff; --text: #111; --text-secondary: #444;
      --accent: #e65100; --accent-light: #ff9800; --nav-bg: rgba(255,255,255,.85);
      --card-bg: #ffffff; --shadow: 0 4px 30px rgba(0,0,0,0.1);
    }
    * { margin:0; padding:0; box-sizing:border-box; }
    html { scroll-snap-type: y mandatory; scroll-behavior:smooth; }
    body {
      font-family: 'Segoe UI', Arial, sans-serif; background: var(--bg); color: var(--text);
      overflow-x: hidden; transition: background 0.4s, color 0.4s; cursor: none;
    }
    /* Custom cursor */
    .cursor {
      width: 20px; height: 20px; border: 2px solid var(--accent); border-radius: 50%;
      position: fixed; pointer-events: none; z-index: 9999; mix-blend-mode: difference;
      transition: transform 0.15s ease, width 0.2s, height 0.2s; transform: translate(-50%, -50%);
    }
    .cursor.hover { width: 50px; height: 50px; background: rgba(255,152,0,0.15); }
    /* Background animation */
    .bg-animation { position: fixed; inset:0; z-index:-1; overflow:hidden; }
    .bg-animation span {
      position:absolute; border-radius:50%; filter:blur(120px); opacity:0.5;
      animation:float 12s infinite ease-in-out; will-change:transform;
    }
    .bg-animation span:nth-child(1) { width:350px; height:350px; background:#ff9800; top:10%; left:10%; }
    .bg-animation span:nth-child(2) { width:300px; height:300px; background:#ff4d4d; top:60%; right:10%; }
    .bg-animation span:nth-child(3) { width:250px; height:250px; background:#ffaa00; bottom:10%; left:40%; }
    @keyframes float {
      0%,100%{transform:translate(0,0)scale(1)} 50%{transform:translate(-30px,-50px)scale(1.1)}
    }
    /* Navigation */
    nav {
      display:flex; justify-content:space-between; align-items:center; padding:15px 8%;
      background:var(--nav-bg); backdrop-filter:blur(12px); position:sticky; top:0; z-index:1000;
      transition:background 0.3s;
    }
    .logo { font-size:28px; font-weight:bold; color:var(--accent); cursor:pointer; }
    .nav-links { display:flex; list-style:none; gap:20px; flex-wrap:wrap; }
    .nav-links a { color:var(--text); text-decoration:none; font-weight:500; transition:color 0.3s; font-size:14px; }
    .nav-links a:hover { color:var(--accent); }
    .menu-toggle { display:none; font-size:28px; background:none; border:none; color:var(--text); cursor:pointer; }
    .dark-toggle {
      background:none; border:1px solid var(--accent); color:var(--accent);
      padding:6px 12px; border-radius:20px; cursor:pointer; margin-left:15px; font-size:14px;
    }
    /* Mobile menu */
    .mobile-menu {
      position:fixed; inset:0; background:var(--bg); z-index:2000; display:flex;
      flex-direction:column; justify-content:center; align-items:center;
      transform:translateX(100%); transition:transform 0.4s ease;
    }
    .mobile-menu.active { transform:translateX(0); }
    .mobile-menu a { color:var(--text); font-size:28px; margin:20px 0; text-decoration:none; }
    .close-menu { position:absolute; top:20px; right:30px; font-size:36px; background:none; border:none; color:var(--text); }
    /* Hero */
    .hero {
      min-height:100vh; display:flex; align-items:center; justify-content:center;
      text-align:center; padding:20px; flex-direction:column; position:relative; overflow:hidden;
      scroll-snap-align:start;
    }
    .hero-video {
      position:absolute; top:0; left:0; width:100%; height:100%; object-fit:cover;
      z-index:-2; opacity:0.3; pointer-events:none;
    }
    #particles-js { position:absolute; top:0; left:0; width:100%; height:100%; z-index:-1; }
    .hero h1 {
      font-size:70px; background:linear-gradient(90deg, var(--accent), var(--text), var(--accent));
      -webkit-background-clip:text; -webkit-text-fill-color:transparent;
      background-size:200% 200%; animation:gradientShift 3s ease infinite;
    }
    @keyframes gradientShift { 0%{background-position:0% 50%} 50%{background-position:100% 50%} 100%{background-position:0% 50%} }
    .hero .tagline { font-size:20px; color:var(--text-secondary); margin:20px 0; min-height:30px; }
    .btn {
      display:inline-block; padding:12px 28px; background:var(--accent); color:#000;
      text-decoration:none; border-radius:30px; font-weight:bold; margin:8px;
      transition:transform 0.3s, box-shadow 0.3s; cursor:none; position:relative; z-index:2; border:none;
    }
    .btn:hover { transform:translateY(-3px); box-shadow:0 10px 20px rgba(255,152,0,0.3); }
    section { padding:60px 8%; scroll-snap-align:start; }
    .section-title { text-align:center; color:var(--accent); font-size:2.2rem; margin-bottom:40px; }
    /* Glass & Clay */
    .glass { background:rgba(255,255,255,0.05); backdrop-filter:blur(12px); border:1px solid rgba(255,255,255,0.1); }
    .clay {
      background:var(--surface); border-radius:20px;
      box-shadow:8px 8px 16px rgba(0,0,0,0.4), -4px -4px 8px rgba(255,255,255,0.05);
    }
    /* About */
    .about { display:flex; gap:40px; flex-wrap:wrap; align-items:center; }
    .about img { width:320px; border-radius:20px; box-shadow:var(--shadow); background:var(--surface); }
    .about-text { flex:1; }
    .skills { display:flex; flex-wrap:wrap; gap:10px; margin-top:20px; }
    .skills span { background:var(--surface); padding:10px 18px; border-radius:30px; font-size:14px; }
    .stats { display:flex; gap:15px; flex-wrap:wrap; margin-top:25px; }
    .stat { background:var(--surface); padding:20px; border-radius:16px; text-align:center; min-width:100px; }
    .stat .count { font-size:32px; font-weight:bold; color:var(--accent); }
    .grid { display:grid; grid-template-columns:repeat(auto-fit, minmax(250px, 1fr)); gap:25px; }
    .card, .portfolio-card, .price-card { will-change:transform; transition:transform 0.3s, box-shadow 0.3s; }
    .card { background:var(--card-bg); padding:30px; border-radius:20px; box-shadow:var(--shadow); }
    .card:hover { transform:translateY(-8px); }
    .card h3 { color:var(--accent); margin-bottom:10px; }
    .filter-buttons { display:flex; justify-content:center; gap:12px; margin-bottom:30px; flex-wrap:wrap; }
    .filter-btn {
      background:var(--surface); border:none; padding:8px 20px; border-radius:30px;
      color:var(--text); cursor:pointer; transition:all 0.3s;
    }
    .filter-btn.active, .filter-btn:hover { background:var(--accent); color:#000; }
    .portfolio-card { background:var(--card-bg); border-radius:18px; overflow:hidden; box-shadow:var(--shadow); }
    .portfolio-card img { width:100%; height:220px; object-fit:cover; border-radius:12px 12px 0 0; }
    .portfolio-card .info { padding:15px; }
    .portfolio-card h3 { color:var(--accent); }
    .pricing .price-card { background:var(--card-bg); padding:30px; border-radius:20px; text-align:center; }
    .price-card h3 { color:var(--accent); }
    .price { font-size:36px; font-weight:bold; margin:15px 0; }
    .price-card ul { list-style:none; margin:20px 0; color:var(--text-secondary); }
    .price-card li { padding:6px 0; }
    .testimonial { background:var(--card-bg); padding:25px; border-radius:16px; margin:10px; }
    .contact-form { max-width:500px; margin:0 auto; }
    .contact-form input, .contact-form textarea {
      width:100%; padding:12px; margin:10px 0; border-radius:8px;
      border:1px solid #333; background:var(--surface); color:var(--text);
    }
    .back-to-top {
      position:fixed; bottom:30px; right:100px; width:45px; height:45px;
      background:var(--accent); color:#000; border-radius:50%; display:flex;
      align-items:center; justify-content:center; font-size:24px;
      opacity:0; visibility:hidden; transition:all 0.3s; cursor:pointer; z-index:999;
    }
    .back-to-top.show { opacity:1; visibility:visible; }
    .shimmer {
      background:linear-gradient(90deg, var(--surface) 25%, rgba(255,255,255,0.05) 50%, var(--surface) 75%);
      background-size:200% 100%; animation:shimmer 1.5s infinite;
    }
    @keyframes shimmer { 0%{background-position:200% 0} 100%{background-position:-200% 0} }
    @keyframes spin { to{transform:rotate(360deg)} }
    /* Social proof toast */
    .toast {
      position:fixed; bottom:100px; left:20px; background:var(--surface);
      padding:15px 20px; border-radius:12px; box-shadow:var(--shadow); z-index:1500;
      display:flex; align-items:center; gap:10px; transform:translateX(-120%); transition:transform 0.4s ease;
    }
    .toast.show { transform:translateX(0); }
    /* Chat bubble */
    .chat-bubble {
      position:fixed; right:20px; bottom:90px; background:var(--accent); color:#000;
      width:60px; height:60px; border-radius:50%; display:flex; align-items:center; justify-content:center;
      font-size:28px; box-shadow:0 4px 15px rgba(255,152,0,0.4); cursor:pointer; z-index:997;
    }
    .chat-bubble:hover { transform:scale(1.1); }
    /* Context menu */
    .context-menu {
      position:fixed; background:var(--surface); border-radius:12px; padding:8px 0;
      box-shadow:var(--shadow); z-index:9999; display:none; min-width:180px;
    }
    .context-menu a { display:block; padding:8px 20px; color:var(--text); text-decoration:none; cursor:pointer; }
    .context-menu a:hover { background:var(--accent); color:#000; }
    /* Morph shape */
    .morph-shape {
      width:200px; height:200px; background:var(--accent); opacity:0.1; position:fixed;
      bottom:50px; left:-50px; border-radius:30% 70% 70% 30% / 30% 30% 70% 70%;
      animation:morph 8s infinite alternate;
    }
    @keyframes morph {
      0%{border-radius:30% 70% 70% 30% / 30% 30% 70% 70%}
      100%{border-radius:70% 30% 30% 70% / 70% 70% 30% 30%}
    }
    /* Before/After slider */
    .ba-slider { position:relative; width:100%; max-width:600px; margin:0 auto; overflow:hidden; border-radius:20px; }
    .ba-slider img { width:100%; display:block; }
    .ba-slider .img-before { position:absolute; top:0; left:0; height:100%; width:50%; overflow:hidden; }
    .ba-slider .img-before img { width:100%; height:100%; object-fit:cover; }
    .ba-slider input[type=range] { position:absolute; top:0; left:0; width:100%; height:100%; opacity:0; cursor:ew-resize; }
    .ba-slider .divider { position:absolute; top:0; bottom:0; width:3px; background:var(--accent); left:50%; transform:translateX(-50%); pointer-events:none; }
    /* Vote arena */
    .vote-card { text-align:center; cursor:pointer; transition:0.3s; background:var(--surface); border-radius:20px; padding:20px; }
    .vote-card img { width:100%; max-height:200px; object-fit:cover; border-radius:12px; }
    .vote-bar { height:10px; background:var(--accent); margin-top:10px; border-radius:5px; width:50%; transition:width 0.5s; }
    footer { text-align:center; padding:25px; background:#111; }
    @media(max-width:768px) {
      .nav-links, .dark-toggle { display:none; } .menu-toggle { display:block; }
      .hero h1 { font-size:42px; } .back-to-top { right:20px; } .about { flex-direction:column; }
    }
  </style>
</head>
<body>

<!-- Preloader -->
<div id="preloader" style="position:fixed; inset:0; background:var(--bg); z-index:10000; display:flex; align-items:center; justify-content:center; transition:opacity 0.4s;">
  <div style="text-align:center;">
    <div style="width:50px; height:50px; border:4px solid var(--accent); border-top-color:transparent; border-radius:50%; animation:spin 0.8s linear infinite; margin:0 auto 15px;"></div>
    <span style="color:var(--accent); font-weight:bold;">Nagesh Creates</span>
  </div>
</div>

<!-- Scroll Progress Bar -->
<div id="progress-bar" style="position:fixed; top:0; left:0; height:3px; background:var(--accent); z-index:1001; width:0%; transition:width 0.1s linear;"></div>

<!-- Custom cursor -->
<div class="cursor" id="cursor"></div>

<!-- Background blobs -->
<div class="bg-animation"><span></span><span></span><span></span></div>

<!-- Morphing shape -->
<div class="morph-shape"></div>

<!-- Custom context menu -->
<div class="context-menu" id="contextMenu">
  <a id="copyEmail">📧 Copy Email</a>
  <a id="callNow">📞 Call Now</a>
  <a id="shareTwitter">🐦 Share on Twitter</a>
</div>

<!-- Chatbot bubble -->
<div class="chat-bubble" id="chatBubble">💬</div>

<!-- Social proof toast -->
<div class="toast" id="toast">⭐ Someone just booked a Professional package!</div>

<!-- Navigation -->
<nav>
  <div class="logo">Nagesh Creates</div>
  <ul class="nav-links" id="navLinks">
    <li><a href="#about">About</a></li>
    <li><a href="#services">Services</a></li>
    <li><a href="#portfolio">Portfolio</a></li>
    <li><a href="#pricing">Pricing</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#poster-gen">AI Generator</a></li>
    <li><a href="#battle">Battle</a></li>
    <li><a href="#quiz">Quiz</a></li>
    <li><a href="#gallery3d">3D Gallery</a></li>
    <li><a href="#challenge">Challenge</a></li>
    <li><a href="#before-after">Before/After</a></li>
    <li><a href="#voice">Voice</a></li>
    <li><a href="#wish">Wish</a></li>
  </ul>
  <button class="dark-toggle" id="darkToggle">🌓</button>
  <button class="menu-toggle" id="menuToggle">☰</button>
</nav>

<!-- Mobile Menu -->
<div class="mobile-menu" id="mobileMenu">
  <button class="close-menu" id="closeMenu">&times;</button>
  <a href="#about" class="mobile-link">About</a>
  <a href="#services" class="mobile-link">Services</a>
  <a href="#portfolio" class="mobile-link">Portfolio</a>
  <a href="#pricing" class="mobile-link">Pricing</a>
  <a href="#contact" class="mobile-link">Contact</a>
  <a href="#poster-gen" class="mobile-link">AI Generator</a>
  <a href="#battle" class="mobile-link">Design Battle</a>
  <a href="#quiz" class="mobile-link">Quiz</a>
  <a href="#gallery3d" class="mobile-link">3D Gallery</a>
  <a href="#challenge" class="mobile-link">Challenge</a>
  <a href="#before-after" class="mobile-link">Before/After</a>
  <a href="#voice" class="mobile-link">Voice</a>
  <a href="#wish" class="mobile-link">Wish Board</a>
</div>

<!-- Hero -->
<section class="hero" id="hero">
  <video class="hero-video" autoplay loop muted playsinline id="heroVideo" preload="none">
    <source src="showreel.mp4" type="video/mp4">
  </video>
  <div id="particles-js"></div>
  <h1 data-aos="fade-down">Nagesh Creates</h1>
  <div class="tagline" id="typed-strings">
    <span>Poster Design</span><span>AI Image Creation</span><span>YouTube Thumbnails</span>
    <span>Branding & Identity</span><span>Social Media Magic</span>
  </div>
  <span class="tagline" id="typed-output"></span>
  <div data-aos="fade-up" data-aos-delay="200">
    <a class="btn" href="#portfolio" id="viewPortfolioBtn">View Portfolio</a>
    <a class="btn" href="#contact" id="hireMeBtn">Hire Me</a>
  </div>
</section>

<!-- About -->
<section id="about">
  <h2 class="section-title" data-aos="fade-right">About Me</h2>
  <div class="about">
    <img src="your-photo.jpg" alt="Nagesh" data-aos="zoom-in" loading="lazy" onload="this.classList.remove('shimmer')" class="shimmer">
    <div class="about-text" data-aos="fade-left">
      <p>Hi, I'm Nagesh, a creative graphic designer and AI visual creator. I help creators, businesses and brands stand out with eye-catching designs that tell a story.</p>
      <div class="skills">
        <span>Poster Design</span><span>AI Image Creation</span><span>Thumbnail Design</span>
        <span>Social Media</span><span>Marathi Calligraphy</span><span>Logo Design</span>
      </div>
      <div class="stats">
        <div class="stat"><span class="count" id="projectsCount">0</span><br>Projects</div>
        <div class="stat"><span class="count" id="clientsCount">0</span><br>Clients</div>
        <div class="stat"><span class="count" id="creativeCount">0</span><br>Creative</div>
      </div>
    </div>
  </div>
</section>

<!-- Services -->
<section id="services">
  <h2 class="section-title" data-aos="fade-up">Services</h2>
  <div class="grid">
    <div class="card glass" data-aos="flip-left"><h3>🎨 Poster Design</h3><p>Event, promotional & digital posters</p></div>
    <div class="card glass" data-aos="flip-left" data-aos-delay="100"><h3>🤖 AI Image Creation</h3><p>Custom AI-generated visuals</p></div>
    <div class="card glass" data-aos="flip-left" data-aos-delay="200"><h3>🎬 YouTube Thumbnails</h3><p>Click-worthy thumbnails</p></div>
    <div class="card glass" data-aos="flip-left"><h3>📱 Social Media Posts</h3><p>Instagram, Facebook, stories</p></div>
    <div class="card glass" data-aos="flip-left"><h3>✒️ Logo Design</h3><p>Unique brand identities</p></div>
    <div class="card glass" data-aos="flip-left"><h3>🖼️ Photo Editing</h3><p>Retouching & manipulation</p></div>
  </div>
</section>

<!-- Portfolio -->
<section id="portfolio">
  <h2 class="section-title" data-aos="fade-down">Portfolio</h2>
  <div style="text-align:center; margin-bottom:20px;">
    <input type="text" id="portfolioSearch" placeholder="🔍 Search (e.g., gaming, festival)" style="padding:10px 20px; border-radius:30px; border:none; background:var(--surface); color:var(--text); width:250px;">
  </div>
  <div class="filter-buttons" data-aos="fade-up">
    <button class="filter-btn active" data-filter="all">All</button>
    <button class="filter-btn" data-filter="poster">Poster</button>
    <button class="filter-btn" data-filter="ai">AI Art</button>
    <button class="filter-btn" data-filter="thumbnail">Thumbnail</button>
  </div>
  <div class="grid portfolio-container">
    <div class="portfolio-card" data-category="poster" data-keywords="festival event" data-aos="zoom-in">
      <a href="portfolio1.jpg" class="glightbox" data-gallery="portfolio">
        <img src="portfolio1.jpg" alt="Festival Poster" loading="lazy" onload="this.parentElement.classList.remove('shimmer')" class="shimmer">
      </a>
      <div class="info"><h3>Festival Poster</h3></div>
    </div>
    <div class="portfolio-card" data-category="ai" data-keywords="ai artwork surreal" data-aos="zoom-in">
      <a href="portfolio2.jpg" class="glightbox" data-gallery="portfolio">
        <img src="portfolio2.jpg" alt="AI Artwork" loading="lazy" onload="this.parentElement.classList.remove('shimmer')" class="shimmer">
      </a>
      <div class="info"><h3>AI Artwork</h3></div>
    </div>
    <div class="portfolio-card" data-category="thumbnail" data-keywords="youtube gaming" data-aos="zoom-in">
      <a href="portfolio3.jpg" class="glightbox" data-gallery="portfolio">
        <img src="portfolio3.jpg" alt="YouTube Thumbnail" loading="lazy" onload="this.parentElement.classList.remove('shimmer')" class="shimmer">
      </a>
      <div class="info"><h3>YouTube Thumbnail</h3></div>
    </div>
  </div>
</section>

<!-- Testimonials -->
<section>
  <h2 class="section-title" data-aos="fade-up">Testimonials</h2>
  <div class="grid">
    <div class="testimonial" data-aos="fade-right">★★★★★<br>"Amazing poster design! Delivered before deadline."<br><strong>- Rajesh K.</strong></div>
    <div class="testimonial" data-aos="fade-up">★★★★★<br>"The AI artwork was mind-blowing!"<br><strong>- Priya M.</strong></div>
    <div class="testimonial" data-aos="fade-left">★★★★★<br>"Thumbnails that boosted my CTR!"<br><strong>- Amit S.</strong></div>
  </div>
</section>

<!-- Pricing -->
<section id="pricing">
  <h2 class="section-title" data-aos="fade-down">Pricing</h2>
  <div class="grid pricing">
    <div class="price-card clay" data-aos="flip-up"><h3>Starter</h3><div class="price">₹299</div><ul><li>1 Poster</li><li>2 Revisions</li><li>JPG/PNG</li></ul><a class="btn" href="#contact">Get Started</a></div>
    <div class="price-card clay" data-aos="flip-up" data-aos-delay="100"><h3>Professional</h3><div class="price">₹599</div><ul><li>2 Designs</li><li>Unlimited Revisions</li><li>Source File</li></ul><a class="btn" href="#contact">Get Started</a></div>
    <div class="price-card clay" data-aos="flip-up" data-aos-delay="200"><h3>Premium</h3><div class="price">₹999</div><ul><li>5 Designs</li><li>Priority Support</li><li>All Formats</li></ul><a class="btn" href="#contact">Get Started</a></div>
  </div>
</section>

<!-- Feature 1: Instant Poster Generator -->
<section id="poster-gen">
  <h2 class="section-title" data-aos="fade-up">🎨 Instant AI Poster Generator</h2>
  <div style="max-width:600px; margin:0 auto; text-align:center;">
    <input type="text" id="posterName" placeholder="Your name or brand">
    <input type="text" id="posterTagline" placeholder="Tagline / theme">
    <select id="posterStyle"><option>Dark & Fiery</option><option>Neon Cyberpunk</option><option>Minimal Elegant</option><option>Retro Pop</option></select>
    <button class="btn" onclick="generatePoster()">Generate My Poster</button>
    <div style="margin-top:20px; background:var(--surface); border-radius:20px; overflow:hidden;">
      <canvas id="posterCanvas" width="600" height="400" style="width:100%; height:auto;"></canvas>
    </div>
    <a id="downloadPoster" class="btn" style="display:none;" download="my-poster.png">Download Poster</a>
  </div>
</section>

<!-- Feature 2: Live Design Battle -->
<section id="battle">
  <h2 class="section-title" data-aos="fade-up">⚔️ Live Design Battle</h2>
  <div class="grid" style="grid-template-columns:1fr 1fr; align-items:center; gap:20px;">
    <div class="vote-card" onclick="vote('left')">
      <img src="https://picsum.photos/400/300?random=1" alt="Design A"><h3>Design A</h3>
      <div class="vote-bar" id="bar-left">50%</div>
    </div>
    <div style="text-align:center; font-size:2rem;">VS</div>
    <div class="vote-card" onclick="vote('right')">
      <img src="https://picsum.photos/400/300?random=2" alt="Design B"><h3>Design B</h3>
      <div class="vote-bar" id="bar-right">50%</div>
    </div>
  </div>
  <p style="text-align:center; margin-top:10px;">Total votes: <span id="voteCount">0</span></p>
</section>

<!-- Feature 3: Personalised Video Greeting -->
<section id="video-greet">
  <h2 class="section-title" data-aos="fade-up">📹 Personalised Video Greeting</h2>
  <div style="text-align:center;">
    <input type="text" id="greetName" placeholder="Enter your name" style="max-width:300px;">
    <button class="btn" onclick="playGreeting()">Play My Greeting</button>
    <video id="greetingVideo" width="100%" controls style="max-width:600px; border-radius:20px; margin-top:20px; display:none;" muted>
      <source src="https://www.w3schools.com/html/mov_bbb.mp4" type="video/mp4">
    </video>
    <p id="greetingOverlay" style="position:relative; display:none; color:var(--accent); font-size:1.5rem; font-weight:bold; margin-top:-40px;"></p>
  </div>
</section>

<!-- Feature 4: Interactive Brand Quiz -->
<section id="quiz">
  <h2 class="section-title" data-aos="fade-up">🧠 Design Your Brand Quiz</h2>
  <div id="quizContainer" style="max-width:500px; margin:0 auto; text-align:center;">
    <div id="quizStep"><p id="quizQuestion"></p><div id="quizOptions"></div></div>
    <div id="quizResult" style="display:none;">
      <h3>Your Style: <span id="styleResult"></span></h3>
      <p>We recommend <strong id="pkgResult"></strong> package!</p>
      <button class="btn" onclick="resetQuiz()">Retake</button>
    </div>
  </div>
</section>

<!-- Feature 5: 3D Gallery -->
<section id="gallery3d">
  <h2 class="section-title" data-aos="fade-up">🏛️ 3D Museum of Design</h2>
  <div id="three-container" style="width:100%; height:400px; border-radius:20px; overflow:hidden; background:#000;"></div>
</section>

<!-- Feature 6: Community Challenge Wall -->
<section id="challenge">
  <h2 class="section-title" data-aos="fade-up">🏆 Community Challenge Wall</h2>
  <div style="max-width:500px; margin:0 auto; text-align:center;">
    <input type="text" id="challengeTitle" placeholder="Your design title">
    <input type="url" id="challengeImage" placeholder="Image URL (optional)">
    <button class="btn" onclick="submitChallenge()">Submit to #NageshChallenge</button>
  </div>
  <div id="challengeWall" class="grid" style="margin-top:30px;"></div>
</section>

<!-- Feature 7: Before & After Slider -->
<section id="before-after">
  <h2 class="section-title" data-aos="fade-up">🔄 Before & After Magic</h2>
  <div class="ba-slider">
    <img src="https://picsum.photos/600/400?random=3" alt="After">
    <div class="img-before"><img src="https://picsum.photos/600/400?random=4" alt="Before"></div>
    <input type="range" min="0" max="100" value="50" oninput="moveSlider(this.value)">
    <div class="divider" id="dividerLine"></div>
  </div>
</section>

<!-- Feature 8: Live Collaboration -->
<section id="collab">
  <h2 class="section-title" data-aos="fade-up">👥 Live Design Collaboration</h2>
  <div style="max-width:800px; margin:0 auto; border-radius:20px; overflow:hidden; background:#1e1e1e;">
    <iframe style="border:1px solid rgba(0,0,0,0.1);" width="100%" height="450" src="https://www.figma.com/embed?embed_host=share&url=https://www.figma.com/file/your-figma-file" allowfullscreen></iframe>
  </div>
</section>

<!-- Feature 9: Voice Navigation -->
<section id="voice">
  <h2 class="section-title" data-aos="fade-up">🎙️ Voice Navigation</h2>
  <div style="text-align:center;">
    <button class="btn" id="startVoice">Start Listening</button>
    <p id="voiceStatus">Say: "Show me posters" or "Go to pricing"</p>
  </div>
</section>

<!-- Feature 10: Wish Board -->
<section id="wish">
  <h2 class="section-title" data-aos="fade-up">💫 Wish Board – Name Your Price</h2>
  <div style="max-width:500px; margin:0 auto; text-align:center;">
    <input type="text" id="wishNeed" placeholder="What do you need?">
    <input type="number" id="wishPrice" placeholder="Your offer (₹)">
    <button class="btn" onclick="submitWish()">Submit Wish</button>
    <div id="wishList" style="margin-top:20px; text-align:left;"></div>
  </div>
</section>

<!-- Contact -->
<section id="contact">
  <h2 class="section-title" data-aos="fade-up">Contact</h2>
  <div class="contact-form" data-aos="zoom-in">
    <form action="https://formspree.io/f/your-form-id" method="POST">
      <input type="text" name="name" placeholder="Your Name" required>
      <input type="email" name="_replyto" placeholder="Email Address" required>
      <textarea name="message" rows="4" placeholder="Your Message" required></textarea>
      <button type="submit" class="btn">Send Message</button>
    </form>
  </div>
  <p style="text-align:center; margin-top:20px;">📞 9834178749 | 📧 nageshdesign@gmail.com</p>
  <p style="text-align:center;">📷 @nagesh_creates_03</p>
  <div class="calendly-inline-widget" data-url="YOUR_CALENDLY_LINK" style="min-width:320px;height:630px; margin-top:40px;"></div>
</section>

<footer>© 2026 Nagesh Creates. All Rights Reserved.</footer>

<!-- WhatsApp -->
<a href="https://wa.me/919834178749?text=Hi%20Nagesh%2C%20I%27m%20interested%20in%20your%20design%20services." style="position:fixed; right:20px; bottom:20px; background:#25D366; color:white; padding:14px 18px; border-radius:50px; text-decoration:none; font-weight:bold; z-index:998;">WhatsApp</a>

<!-- Back to top -->
<div class="back-to-top" id="backToTop">↑</div>

<!-- Scripts -->
<script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
<script src="https://cdn.jsdelivr.net/npm/glightbox/dist/js/glightbox.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/typed.js@2.0.12"></script>
<script src="https://unpkg.com/countup.js@2.6.2/dist/countUp.umd.js"></script>
<script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/particles.js@2.0.0/particles.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/three@0.152.0/build/three.min.js"></script>
<script src="https://unpkg.com/@lottiefiles/lottie-player@latest/dist/lottie-player.js"></script>
<script src="https://assets.calendly.com/assets/external/widget.js" async></script>

<script>
  // Preloader
  window.addEventListener('load', () => {
    const preloader = document.getElementById('preloader');
    preloader.style.opacity = '0';
    setTimeout(() => preloader.style.display = 'none', 400);
  });

  // Scroll Progress
  const progressBar = document.getElementById('progress-bar');
  window.addEventListener('scroll', () => {
    const scrollPercent = (window.scrollY / (document.documentElement.scrollHeight - window.innerHeight)) * 100;
    progressBar.style.width = scrollPercent + '%';
  });

  // Particles.js
  particlesJS('particles-js', { particles: { number: { value: 50 }, color: { value: '#ff9800' }, shape: { type: 'circle' }, opacity: { value: 0.5 }, size: { value: 3 }, line_linked: { enable: true, color: '#ff9800', opacity: 0.2 }, move: { speed: 2 } } });

  // AOS
  AOS.init({ once: true, duration: 800 });

  // GLightbox
  const lightbox = GLightbox({ selector: '.glightbox' });

  // Typed.js
  new Typed('#typed-output', { stringsElement: '#typed-strings', typeSpeed: 60, backSpeed: 30, loop: true, backDelay: 1500, startDelay: 500 });

  // Dark/Light
  const toggle = document.getElementById('darkToggle');
  toggle.addEventListener('click', () => {
    document.body.classList.toggle('light-mode');
    localStorage.setItem('theme', document.body.classList.contains('light-mode') ? 'light' : 'dark');
  });
  if (localStorage.getItem('theme') === 'light') document.body.classList.add('light-mode');

  // Custom cursor
  const cursor = document.getElementById('cursor');
  document.addEventListener('mousemove', e => { cursor.style.left = e.clientX + 'px'; cursor.style.top = e.clientY + 'px'; });
  document.querySelectorAll('a, button, .btn, .filter-btn, .back-to-top').forEach(el => {
    el.addEventListener('mouseenter', () => cursor.classList.add('hover'));
    el.addEventListener('mouseleave', () => cursor.classList.remove('hover'));
  });

  // Mobile menu
  const menuToggle = document.getElementById('menuToggle');
  const mobileMenu = document.getElementById('mobileMenu');
  const closeMenu = document.getElementById('closeMenu');
  document.querySelectorAll('.mobile-link').forEach(l => l.addEventListener('click', () => mobileMenu.classList.remove('active')));
  menuToggle.addEventListener('click', () => mobileMenu.classList.add('active'));
  closeMenu.addEventListener('click', () => mobileMenu.classList.remove('active'));

  // Back to top
  const backBtn = document.getElementById('backToTop');
  window.addEventListener('scroll', () => backBtn.classList.toggle('show', window.scrollY > 500));
  backBtn.addEventListener('click', () => window.scrollTo({ top: 0, behavior: 'smooth' }));

  // Stats counter
  function animateStats() {
    new CountUp('projectsCount', 50, { duration: 2.5 }).start();
    new CountUp('clientsCount', 20, { duration: 2.5 }).start();
    new CountUp('creativeCount', 100, { suffix: '%', duration: 2.5 }).start();
  }
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(e => { if (e.isIntersecting) { animateStats(); observer.unobserve(e.target); } });
  }, { threshold: 0.5 });
  const statsSection = document.querySelector('.stats');
  if (statsSection) observer.observe(statsSection);

  // Portfolio filter + search
  const filterBtns = document.querySelectorAll('.filter-btn');
  const portfolioCards = document.querySelectorAll('.portfolio-card');
  filterBtns.forEach(btn => {
    btn.addEventListener('click', () => {
      filterBtns.forEach(b => b.classList.remove('active'));
      btn.classList.add('active');
      const filter = btn.dataset.filter;
      portfolioCards.forEach(card => card.style.display = (filter === 'all' || card.dataset.category === filter) ? 'block' : 'none');
    });
  });
  document.getElementById('portfolioSearch').addEventListener('input', (e) => {
    const term = e.target.value.toLowerCase();
    portfolioCards.forEach(card => {
      card.style.display = (term === '' || (card.dataset.keywords || '').includes(term)) ? 'block' : 'none';
    });
  });

  // Parallax blobs
  document.addEventListener('mousemove', (e) => {
    const x = (e.clientX / window.innerWidth - 0.5) * 20;
    const y = (e.clientY / window.innerHeight - 0.5) * 20;
    document.querySelectorAll('.bg-animation span').forEach((span, i) => {
      span.style.transform = `translate(${x * (i + 1) * 0.5}px, ${y * (i + 1) * 0.5}px)`;
    });
  });

  // 3D Tilt
  function applyTilt() {
    document.querySelectorAll('.card, .portfolio-card, .price-card, .hero').forEach(el => {
      el.addEventListener('mousemove', (e) => {
        const rect = el.getBoundingClientRect();
        const x = e.clientX - rect.left, y = e.clientY - rect.top;
        const rx = ((y - rect.height / 2) / (rect.height / 2)) * -5;
        const ry = ((x - rect.width / 2) / (rect.width / 2)) * 5;
        el.style.transform = `perspective(800px) rotateX(${rx}deg) rotateY(${ry}deg) scale(1.02)`;
        el.style.transition = 'transform 0.1s ease';
      });
      el.addEventListener('mouseleave', () => {
        el.style.transform = 'perspective(800px) rotateX(0) rotateY(0) scale(1)';
        el.style.transition = 'transform 0.4s ease';
      });
    });
  }
  document.addEventListener('DOMContentLoaded', applyTilt);

  // Magnetic buttons
  document.querySelectorAll('.btn').forEach(btn => {
    btn.addEventListener('mousemove', (e) => {
      const rect = btn.getBoundingClientRect();
      btn.style.transform = `translate(${(e.clientX - rect.left - rect.width / 2) * 0.3}px, ${(e.clientY - rect.top - rect.height / 2) * 0.3}px)`;
      btn.style.transition = 'transform 0.1s ease';
    });
    btn.addEventListener('mouseleave', () => { btn.style.transform = 'translate(0,0)'; btn.style.transition = 'transform 0.3s ease'; });
  });

  // Dynamic greeting
  const hour = new Date().getHours();
  const greeting = hour < 12 ? 'Good morning!' : hour < 18 ? 'Good afternoon!' : 'Good evening!';
  document.querySelector('#typed-output').innerHTML = `<span>${greeting} Ready to create?</span>`;

  // Visitor counter
  const vc = Math.floor(Math.random() * 10) + 1;
  const vDiv = document.createElement('div');
  vDiv.style.cssText = 'position:fixed; bottom:140px; right:20px; background:var(--surface); padding:8px 15px; border-radius:20px; z-index:997;';
  vDiv.textContent = `🔥 ${vc} visitors now`;
  document.body.appendChild(vDiv);

  // Social proof toast
  setInterval(() => {
    const t = document.getElementById('toast');
    t.classList.add('show');
    setTimeout(() => t.classList.remove('show'), 3000);
  }, 15000);

  // Confetti
  document.getElementById('hireMeBtn').addEventListener('click', () => confetti({ particleCount: 100, spread: 70, origin: { y: 0.6 } }));

  // Context menu
  const ctxMenu = document.getElementById('contextMenu');
  document.addEventListener('contextmenu', (e) => {
    e.preventDefault();
    ctxMenu.style.display = 'block';
    ctxMenu.style.left = e.clientX + 'px';
    ctxMenu.style.top = e.clientY + 'px';
  });
  document.addEventListener('click', () => ctxMenu.style.display = 'none');
  document.getElementById('copyEmail').addEventListener('click', () => { navigator.clipboard.writeText('nageshdesign@gmail.com'); alert('Email copied!'); });
  document.getElementById('callNow').addEventListener('click', () => window.location.href = 'tel:9834178749');
  document.getElementById('shareTwitter').addEventListener('click', () => window.open('https://twitter.com/intent/tweet?text=Check%20out%20Nagesh%20Creates!'));

  // Konami Code
  const konami = ['ArrowUp','ArrowUp','ArrowDown','ArrowDown','ArrowLeft','ArrowRight','ArrowLeft','ArrowRight','b','a'];
  let input = [];
  document.addEventListener('keydown', (e) => {
    input.push(e.key); input.splice(-konami.length - 1, input.length - konami.length);
    if (JSON.stringify(input) === JSON.stringify(konami)) { confetti({ particleCount: 200, spread: 100 }); alert('🎉 Secret unlocked!'); }
  });

  // Audio feedback
  let audioCtx = null;
  document.querySelectorAll('a, button, .btn').forEach(el => el.addEventListener('click', () => {
    if (!audioCtx) audioCtx = new (window.AudioContext || window.webkitAudioContext)();
    const o = audioCtx.createOscillator(), g = audioCtx.createGain();
    o.connect(g); g.connect(audioCtx.destination); o.frequency.value = 600; g.gain.value = 0.1;
    o.start(0); o.stop(audioCtx.currentTime + 0.05);
  }));

  // PWA
  if ('serviceWorker' in navigator) {
    navigator.serviceWorker.register('data:application/javascript;base64,CgpzZWxmLmFkZEV2ZW50TGlzdGVuZXIoJ2luc3RhbGwnLCAoZXZlbnQpID0+IHtldmVudC53YWl0VW50aWwoY2FjaGVzLm9wZW4oJ25hZ2VzaC12MScpLnRoZW4oY2FjaGUgPT4gY2FjaGUuYWRkQWxsKFsnLycsICcvaW5kZXguaHRtbCddKSkpfSk7c2VsZi5hZGRFdmVudExpc3RlbmVyKCdmZXRjaCcsIChldmVudCkgPT4ge2V2ZW50LnJlc3BvbmRXaXRoKGNhY2hlcy5tYXRjaChldmVudC5yZXF1ZXN0KS50aGVuKHJlc3BvbnNlID0+IHJlc3BvbnNlIHx8IGZldGNoKGV2ZW50LnJlcXVlc3QpKSl9KTs=');
  }

  // Lottie
  const lp = document.createElement('lottie-player');
  lp.src = 'https://assets10.lottiefiles.com/packages/lf20_mDnm1A.json';
  lp.style = 'width:80px; height:80px; position:fixed; bottom:200px; right:20px; z-index:997;';
  lp.loop = true; lp.autoplay = true;
  document.body.appendChild(lp);

  // ----- 10 CREATIVE FEATURES -----

  // 1. Poster Generator
  function generatePoster() {
    const canvas = document.getElementById('posterCanvas'), ctx = canvas.getContext('2d');
    const name = document.getElementById('posterName').value || 'Your Name';
    const tagline = document.getElementById('posterTagline').value || 'Creative Design';
    const style = document.getElementById('posterStyle').value;
    const bg = { 'Dark & Fiery': '#1a1a1a', 'Neon Cyberpunk': '#0d0221', 'Minimal Elegant': '#fff', 'Retro Pop': '#f4a261' };
    const tc = { 'Dark & Fiery': '#ff9800', 'Neon Cyberpunk': '#00ffcc', 'Minimal Elegant': '#111', 'Retro Pop': '#264653' };
    ctx.fillStyle = bg[style]; ctx.fillRect(0, 0, 600, 400);
    ctx.fillStyle = tc[style]; ctx.font = 'bold 48px Arial'; ctx.textAlign = 'center'; ctx.fillText(name, 300, 180);
    ctx.font = '24px Arial'; ctx.fillText(tagline, 300, 240);
    ctx.strokeStyle = tc[style]; ctx.lineWidth = 2; ctx.strokeRect(50, 50, 500, 300);
    const dl = document.getElementById('downloadPoster'); dl.style.display = 'inline-block'; dl.href = canvas.toDataURL('image/png');
  }

  // 2. Design Battle
  let lv = 50, rv = 50, tv = 100;
  function vote(side) { side === 'left' ? lv++ : rv++; tv = lv + rv; document.getElementById('bar-left').style.width = Math.round(lv/tv*100)+'%'; document.getElementById('bar-right').style.width = Math.round(rv/tv*100)+'%'; document.getElementById('voteCount').textContent = tv; }

  // 3. Video Greeting
  function playGreeting() {
    const name = document.getElementById('greetName').value || 'friend';
    const v = document.getElementById('greetingVideo'); v.style.display = 'block'; v.play();
    const o = document.getElementById('greetingOverlay'); o.style.display = 'block'; o.textContent = `Hello ${name}!`; setTimeout(() => o.style.display = 'none', 5000);
  }

  // 4. Quiz
  const qq = [{ q: "Your vibe?", o: ['Bold','Minimal','Playful'] },{ q: "Color?", o: ['Dark+Neon','White+Gold','Pastel'] },{ q: "Personality?", o: ['Rebel','Pro','Fun'] }];
  let cq = 0, ans = [];
  function sq() {
    if (cq >= qq.length) { document.getElementById('quizStep').style.display='none'; document.getElementById('quizResult').style.display='block'; document.getElementById('styleResult').textContent = ans.filter(a=>a.includes('Bold')||a.includes('Neon')||a.includes('Rebel')).length>=2?'Cyberpunk':'Elegant'; document.getElementById('pkgResult').textContent = ans.filter(a=>a.includes('Bold')||a.includes('Neon')||a.includes('Rebel')).length>=2?'Premium':'Professional'; return; }
    const q = qq[cq]; document.getElementById('quizQuestion').textContent = q.q;
    const opts = document.getElementById('quizOptions'); opts.innerHTML = '';
    q.o.forEach(o => { const b = document.createElement('button'); b.className='btn'; b.textContent=o; b.onclick=()=>{ans.push(o); cq++; sq();}; opts.appendChild(b); });
  }
  function resetQuiz() { cq=0; ans=[]; document.getElementById('quizStep').style.display='block'; document.getElementById('quizResult').style.display='none'; sq(); }
  sq();

  // 5. Three.js Gallery
  const container3d = document.getElementById('three-container');
  const scene = new THREE.Scene(); scene.background = new THREE.Color(0x080808);
  const camera = new THREE.PerspectiveCamera(75, container3d.clientWidth/container3d.clientHeight, 0.1, 1000); camera.position.z = 5;
  const renderer = new THREE.WebGLRenderer({antialias:true}); renderer.setSize(container3d.clientWidth, container3d.clientHeight); container3d.appendChild(renderer.domElement);
  const loader3d = new THREE.TextureLoader();
  const planes = [];
  ['https://picsum.photos/512/512?random=10','https://picsum.photos/512/512?random=11','https://picsum.photos/512/512?random=12'].forEach((url,i)=>{
    const mat = new THREE.MeshBasicMaterial({map:loader3d.load(url), side:THREE.DoubleSide});
    const geo = new THREE.PlaneGeometry(1.5,1); const plane = new THREE.Mesh(geo,mat);
    plane.position.x = (i-1)*2; scene.add(plane); planes.push(plane);
  });
  let drag=false, px=0;
  container3d.addEventListener('mousedown',e=>{drag=true;px=e.clientX;});
  container3d.addEventListener('mouseup',()=>drag=false);
  container3d.addEventListener('mousemove',e=>{if(!drag)return; planes.forEach(p=>p.rotation.y+=(e.clientX-px)*0.01); px=e.clientX;});
  function anim3d() { requestAnimationFrame(anim3d); renderer.render(scene,camera); } anim3d();

  // 6. Challenge Wall
  function loadChallenges() {
    const wall = document.getElementById('challengeWall'); wall.innerHTML = '';
    JSON.parse(localStorage.getItem('challenges')||'[]').forEach(ch => {
      const c = document.createElement('div'); c.className='card';
      c.innerHTML = `<h3>${ch.title}</h3>${ch.image?`<img src="${ch.image}" style="width:100%; border-radius:12px; max-height:150px; object-fit:cover;">`:''}<p>By community</p>`;
      wall.appendChild(c);
    });
  }
  function submitChallenge() {
    const t = document.getElementById('challengeTitle').value.trim(), i = document.getElementById('challengeImage').value.trim();
    if(!t) return alert('Enter title');
    const ch = JSON.parse(localStorage.getItem('challenges')||'[]'); ch.push({title:t, image:i});
    localStorage.setItem('challenges', JSON.stringify(ch));
    document.getElementById('challengeTitle').value=''; document.getElementById('challengeImage').value=''; loadChallenges();
  }
  loadChallenges();

  // 7. Before/After Slider
  function moveSlider(v) { document.querySelector('.img-before').style.width = v+'%'; document.getElementById('dividerLine').style.left = v+'%'; }

  // 9. Voice
  const voiceBtn = document.getElementById('startVoice'), voiceStatus = document.getElementById('voiceStatus');
  if ('webkitSpeechRecognition' in window || 'SpeechRecognition' in window) {
    const SR = window.SpeechRecognition || window.webkitSpeechRecognition;
    const rec = new SR(); rec.continuous = false; rec.lang = 'en-US';
    voiceBtn.addEventListener('click', () => { rec.start(); voiceStatus.textContent = 'Listening...'; });
    rec.onresult = (e) => {
      const t = e.results[0][0].transcript.toLowerCase(); voiceStatus.textContent = `Heard: "${t}"`;
      if(t.includes('poster')) document.querySelector('#poster-gen').scrollIntoView({behavior:'smooth'});
      else if(t.includes('pricing')) document.querySelector('#pricing').scrollIntoView({behavior:'smooth'});
    };
    rec.onerror = (e) => voiceStatus.textContent = 'Error: '+e.error;
  } else { voiceBtn.disabled = true; voiceStatus.textContent = 'Voice not supported.'; }

  // 10. Wish Board
  function loadWishes() {
    const list = document.getElementById('wishList'); list.innerHTML = '';
    JSON.parse(localStorage.getItem('wishes')||'[]').forEach(w => {
      const d = document.createElement('div'); d.className='card'; d.innerHTML = `<strong>${w.need}</strong><br>Offer: ₹${w.price}`; list.appendChild(d);
    });
  }
  function submitWish() {
    const n = document.getElementById('wishNeed').value.trim(), p = document.getElementById('wishPrice').value;
    if(!n||!p) return alert('Fill all fields');
    const w = JSON.parse(localStorage.getItem('wishes')||'[]'); w.push({need:n, price:p});
    localStorage.setItem('wishes', JSON.stringify(w));
    document.getElementById('wishNeed').value=''; document.getElementById('wishPrice').value=''; loadWishes();
    if(Math.random()<0.1) alert('🎉 Your wish was selected!');
  }
  loadWishes();
</script>

<!-- Structured Data -->
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "ProfessionalService",
  "name": "Nagesh Creates",
  "description": "Creative graphic design and AI visual creation services",
  "url": "https://nageshcreates.example.com",
  "telephone": "+919834178749",
  "email": "nageshdesign@gmail.com"
}
</script>
</body>
</html>
