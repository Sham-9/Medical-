<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>MedLink Kerala | Medical Student Network</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Space+Grotesk:wght@500;600;700&display=swap');

    :root {
      --ink: #18352f;
      --muted: #6c817b;
      --green: #146c55;
      --green-dark: #0b493a;
      --mint: #dff3e9;
      --lime: #d5ee75;
      --cream: #fffaf0;
      --orange: #f39b59;
      --line: #e7eee8;
      --white: #ffffff;
      --shadow: 0 18px 50px rgba(24, 53, 47, 0.10);
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      background: var(--cream);
      color: var(--ink);
      font-family: "DM Sans", sans-serif;
      line-height: 1.5;
    }

    h1, h2, h3, h4, button, .logo {
      font-family: "Space Grotesk", sans-serif;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    button {
      border: 0;
      cursor: pointer;
    }

    .container {
      width: min(1180px, calc(100% - 40px));
      margin-inline: auto;
    }

    .topbar {
      background: var(--green-dark);
      color: #d9f0df;
      font-size: 13px;
      padding: 9px 0;
    }

    .topbar-inner {
      display: flex;
      justify-content: space-between;
      gap: 20px;
    }

    .navbar {
      padding: 20px 0;
      background: rgba(255, 250, 240, 0.9);
      backdrop-filter: blur(12px);
      position: sticky;
      top: 0;
      z-index: 20;
      border-bottom: 1px solid rgba(231, 238, 232, 0.8);
    }

    .nav-inner {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 24px;
    }

    .logo {
      display: flex;
      align-items: center;
      gap: 10px;
      font-size: 21px;
      font-weight: 700;
      color: var(--green-dark);
    }

    .logo-mark {
      width: 38px;
      height: 38px;
      display: grid;
      place-items: center;
      background: var(--lime);
      color: var(--green-dark);
      border-radius: 12px 12px 12px 3px;
      font-size: 20px;
    }

    .nav-links {
      display: flex;
      gap: 25px;
      align-items: center;
      color: var(--muted);
      font-size: 14px;
      font-weight: 600;
    }

    .nav-links a:hover {
      color: var(--green);
    }

    .nav-actions {
      display: flex;
      align-items: center;
      gap: 10px;
    }

    .btn {
      padding: 12px 18px;
      border-radius: 10px;
      font-weight: 700;
      font-size: 14px;
      transition: transform .2s, box-shadow .2s, background .2s;
    }

    .btn:hover {
      transform: translateY(-2px);
    }

    .btn-outline {
      color: var(--green);
      background: transparent;
      border: 1px solid #bfd5c9;
    }

    .btn-primary {
      color: white;
      background: var(--green);
      box-shadow: 0 8px 20px rgba(20, 108, 85, .2);
    }

    .btn-lime {
      color: var(--green-dark);
      background: var(--lime);
    }

    .mobile-menu {
      display: none;
      background: transparent;
      color: var(--green-dark);
      font-size: 25px;
    }

    .hero {
      padding: 75px 0 65px;
      overflow: hidden;
      position: relative;
    }

    .hero::before {
      content: "";
      position: absolute;
      width: 500px;
      height: 500px;
      border-radius: 50%;
      background: #e8f5d3;
      top: -210px;
      right: -180px;
      z-index: -1;
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1.05fr .95fr;
      align-items: center;
      gap: 65px;
    }

    .eyebrow {
      color: var(--orange);
      text-transform: uppercase;
      letter-spacing: 2px;
      font-size: 12px;
      font-weight: 700;
      margin-bottom: 18px;
    }

    .hero h1 {
      font-size: clamp(42px, 6vw, 76px);
      line-height: .98;
      letter-spacing: -3px;
      max-width: 680px;
      margin-bottom: 25px;
    }

    .hero h1 span {
      color: var(--green);
      position: relative;
    }

    .hero h1 span::after {
      content: "";
      position: absolute;
      left: 0;
      bottom: -3px;
      height: 7px;
      width: 100%;
      background: var(--lime);
      z-index: -1;
      transform: rotate(-2deg);
    }

    .hero-text {
      max-width: 560px;
      color: var(--muted);
      font-size: 17px;
      margin-bottom: 30px;
    }

    .hero-buttons {
      display: flex;
      gap: 12px;
      flex-wrap: wrap;
    }

    .hero-note {
      display: flex;
      align-items: center;
      gap: 12px;
      margin-top: 27px;
      color: var(--muted);
      font-size: 13px;
    }

    .avatars {
      display: flex;
    }

    .avatar {
      width: 31px;
      height: 31px;
      display: grid;
      place-items: center;
      border-radius: 50%;
      color: white;
      font-size: 10px;
      font-weight: 700;
      border: 2px solid var(--cream);
      margin-left: -8px;
    }

    .avatar:first-child {
      margin-left: 0;
    }

    .avatar-a { background: #e87957; }
    .avatar-b { background: #387a72; }
    .avatar-c { background: #c29448; }
    .avatar-d { background: #815f95; }

    .dashboard-card {
      background: var(--white);
      border: 1px solid #e4eee6;
      border-radius: 25px;
      padding: 20px;
      box-shadow: var(--shadow);
      transform: rotate(2deg);
    }

    .dashboard-head {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding-bottom: 17px;
      border-bottom: 1px solid var(--line);
    }

    .dashboard-head h3 {
      font-size: 16px;
    }

    .status {
      color: var(--green);
      background: var(--mint);
      border-radius: 20px;
      padding: 6px 10px;
      font-size: 11px;
      font-weight: 700;
    }

    .dash-welcome {
      background: var(--green);
      color: white;
      border-radius: 16px;
      padding: 22px;
      margin: 18px 0;
      position: relative;
      overflow: hidden;
    }

    .dash-welcome::after {
      content: "✚";
      position: absolute;
      right: 25px;
      bottom: -25px;
      color: rgba(255,255,255,.12);
      font-size: 120px;
    }

    .dash-welcome p {
      color: #bee3cf;
      font-size: 12px;
      margin-bottom: 5px;
    }

    .dash-welcome h3 {
      font-size: 24px;
    }

    .quick-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 11px;
    }

    .quick-item {
      background: #f7faf6;
      border: 1px solid var(--line);
      border-radius: 13px;
      padding: 16px;
    }

    .quick-icon {
      color: var(--orange);
      font-size: 20px;
      margin-bottom: 7px;
    }

    .quick-item strong {
      display: block;
      font-size: 13px;
    }

    .quick-item small {
      color: var(--muted);
      font-size: 11px;
    }

    .section {
      padding: 75px 0;
    }

    .section-heading {
      display: flex;
      justify-content: space-between;
      align-items: end;
      gap: 20px;
      margin-bottom: 30px;
    }

    .section-heading h2 {
      font-size: clamp(28px, 4vw, 43px);
      line-height: 1.05;
      letter-spacing: -1.5px;
    }

    .section-heading p {
      max-width: 430px;
      color: var(--muted);
      font-size: 14px;
    }

    .district-section {
      background: #f0f7ee;
    }

    .district-search {
      min-width: 245px;
      padding: 13px 15px;
      border: 1px solid #d7e4d8;
      border-radius: 10px;
      font: inherit;
      outline: none;
      background: white;
    }

    .district-grid {
      display: grid;
      grid-template-columns: repeat(7, 1fr);
      gap: 12px;
    }

    .district {
      background: white;
      border: 1px solid #e0ebe1;
      border-radius: 13px;
      padding: 17px 12px;
      text-align: center;
      transition: .2s;
    }

    .district:hover {
      background: var(--green);
      color: white;
      transform: translateY(-4px);
    }

    .district-icon {
      color: var(--orange);
      font-size: 20px;
      margin-bottom: 8px;
    }

    .district strong {
      display: block;
      font-size: 12px;
    }

    .district small {
      color: var(--muted);
      font-size: 10px;
    }

    .district:hover small {
      color: #c4dfd0;
    }

    .features-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 16px;
    }

    .feature-card {
      padding: 25px 21px;
      background: white;
      border: 1px solid var(--line);
      border-radius: 16px;
    }

    .feature-card:nth-child(2) {
      background: var(--green);
      color: white;
    }

    .feature-card:nth-child(2) p {
      color: #c7e4d5;
    }

    .feature-number {
      color: var(--orange);
      font-size: 12px;
      font-weight: 700;
      margin-bottom: 35px;
    }

    .feature-card h3 {
      font-size: 18px;
      margin-bottom: 9px;
    }

    .feature-card p {
      color: var(--muted);
      font-size: 13px;
    }

    .community {
      background: var(--green-dark);
      color: white;
      position: relative;
      overflow: hidden;
    }

    .community::after {
      content: "KERALA";
      position: absolute;
      right: -20px;
      bottom: -55px;
      color: rgba(255,255,255,.04);
      font-family: "Space Grotesk";
      font-weight: 700;
      font-size: 150px;
      letter-spacing: -10px;
    }

    .community-grid {
      display: grid;
      grid-template-columns: .8fr 1.2fr;
      gap: 70px;
      align-items: center;
    }

    .community h2 {
      font-size: clamp(30px, 4vw, 47px);
      line-height: 1.05;
      margin-bottom: 18px;
    }

    .community p {
      color: #b8d8c7;
      max-width: 450px;
      margin-bottom: 25px;
    }

    .post-list {
      display: grid;
      gap: 12px;
    }

    .post {
      display: flex;
      gap: 15px;
      align-items: flex-start;
      padding: 17px;
      background: rgba(255,255,255,.09);
      border: 1px solid rgba(255,255,255,.12);
      border-radius: 13px;
    }

    .post-avatar {
      width: 38px;
      height: 38px;
      flex: 0 0 38px;
      border-radius: 10px;
      display: grid;
      place-items: center;
      background: var(--lime);
      color: var(--green-dark);
      font-weight: 700;
    }

    .post h4 {
      font-size: 14px;
      margin-bottom: 3px;
    }

    .post p {
      font-size: 12px;
      margin: 0;
      color: #b8d8c7;
    }

    .events-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 16px;
    }

    .event-card {
      background: white;
      border: 1px solid var(--line);
      border-radius: 15px;
      padding: 20px;
    }

    .event-date {
      display: inline-block;
      background: var(--mint);
      color: var(--green);
      border-radius: 8px;
      padding: 7px 10px;
      font-size: 11px;
      font-weight: 700;
      margin-bottom: 18px;
    }

    .event-card h3 {
      font-size: 17px;
      margin-bottom: 8px;
    }

    .event-card p {
      color: var(--muted);
      font-size: 13px;
      margin-bottom: 18px;
    }

    .event-location {
      color: var(--green);
      font-size: 12px;
      font-weight: 700;
    }

    .cta {
      background: var(--lime);
      padding: 57px 0;
    }

    .cta-inner {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 30px;
    }

    .cta h2 {
      font-size: clamp(27px, 4vw, 42px);
      line-height: 1.05;
      max-width: 600px;
    }

    .cta p {
      color: #536c45;
      margin-top: 10px;
    }

    footer {
      padding: 28px 0;
      background: #f4f7ed;
      color: var(--muted);
      font-size: 13px;
    }

    .footer-inner {
      display: flex;
      justify-content: space-between;
      gap: 20px;
    }

    .modal {
      position: fixed;
      inset: 0;
      display: none;
      place-items: center;
      background: rgba(11, 73, 58, .55);
      z-index: 50;
      padding: 20px;
    }

    .modal.open {
      display: grid;
    }

    .modal-box {
      width: min(440px, 100%);
      background: white;
      border-radius: 20px;
      padding: 28px;
      position: relative;
    }

    .modal-box h2 {
      margin-bottom: 8px;
    }

    .modal-box p {
      color: var(--muted);
      font-size: 14px;
      margin-bottom: 20px;
    }

    .modal-box input,
    .modal-box select {
      width: 100%;
      padding: 13px;
      margin-bottom: 12px;
      border: 1px solid var(--line);
      border-radius: 9px;
      font: inherit;
      background: white;
    }

    .close {
      position: absolute;
      right: 19px;
      top: 15px;
      background: none;
      color: var(--muted);
      font-size: 22px;
    }

    @media (max-width: 900px) {
      .nav-links {
        display: none;
      }

      .mobile-menu {
        display: block;
      }

      .hero-grid,
      .community-grid {
        grid-template-columns: 1fr;
      }

      .dashboard-card {
        max-width: 550px;
        margin: auto;
      }

      .district-grid {
        grid-template-columns: repeat(4, 1fr);
      }

      .features-grid {
        grid-template-columns: repeat(2, 1fr);
      }
    }

    @media (max-width: 600px) {
      .container {
        width: min(100% - 28px, 1180px);
      }

      .topbar-inner,
      .footer-inner,
      .cta-inner,
      .section-heading {
        display: block;
      }

      .topbar-inner span:last-child,
      .section-heading p,
      .cta .btn {
        display: block;
        margin-top: 12px;
      }

      .nav-actions .btn-outline {
        display: none;
      }

      .hero {
        padding-top: 48px;
      }

      .hero h1 {
        font-size: 47px;
        letter-spacing: -2px;
      }

      .district-grid {
        grid-template-columns: repeat(2, 1fr);
      }

      .features-grid,
      .events-grid {
        grid-template-columns: 1fr;
      }

      .community-grid {
        gap: 35px;
      }

      .dashboard-card {
        transform: none;
      }

      .cta-inner .btn {
        display: inline-block;
      }
    }
  </style>
</head>
<body>
  <div class="topbar">
    <div class="container topbar-inner">
      <span>Kerala's student-powered medical network</span>
      <span>Free for medical students across Kerala</span>
    </div>
  </div>

  <nav class="navbar">
    <div class="container nav-inner">
      <a class="logo" href="#">
        <span class="logo-mark">✚</span>
        MedLink Kerala
      </a>

      <div class="nav-links">
        <a href="#districts">Districts</a>
        <a href="#features">What We Do</a>
        <a href="#community">Community</a>
        <a href="#events">Events</a>
      </div>

      <div class="nav-actions">
        <button class="btn btn-outline" onclick="openModal()">Log in</button>
        <button class="btn btn-primary" onclick="openModal()">Join network</button>
        <button class="mobile-menu" onclick="toggleMobile()">☰</button>
      </div>
    </div>
  </nav>

  <main>
    <section class="hero">
      <div class="container hero-grid">
        <div>
          <div class="eyebrow">Students. Connected. Across Kerala.</div>
          <h1>Medicine is better when we learn <span>together.</span></h1>
          <p class="hero-text">
            A trusted communication network for medical students, interns and young healthcare professionals from every district of Kerala.
          </p>

          <div class="hero-buttons">
            <button class="btn btn-primary" onclick="openModal()">Create your profile →</button>
            <a class="btn btn-outline" href="#districts">Explore districts</a>
          </div>

          <div class="hero-note">
            <div class="avatars">
              <span class="avatar avatar-a">AN</span>
              <span class="avatar avatar-b">RS</span>
              <span class="avatar avatar-c">JM</span>
              <span class="avatar avatar-d">+2k</span>
            </div>
            <span>Join 2,000+ students already connected</span>
          </div>
        </div>

        <div class="dashboard-card">
          <div class="dashboard-head">
            <h3>Student dashboard</h3>
            <span class="status">● Live network</span>
          </div>

          <div class="dash-welcome">
            <p>Good morning, future doctor</p>
            <h3>What are you looking for?</h3>
          </div>

          <div class="quick-grid">
            <div class="quick-item">
              <div class="quick-icon">⌕</div>
              <strong>Find a study group</strong>
              <small>128 active groups</small>
            </div>
            <div class="quick-item">
              <div class="quick-icon">◉</div>
              <strong>Ask the community</strong>
              <small>642 discussions</small>
            </div>
            <div class="quick-item">
              <div class="quick-icon">▣</div>
              <strong>Share resources</strong>
              <small>4,200+ materials</small>
            </div>
            <div class="quick-item">
              <div class="quick-icon">✦</div>
              <strong>Find opportunities</strong>
              <small>36 new this week</small>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="section district-section" id="districts">
      <div class="container">
        <div class="section-heading">
          <div>
            <div class="eyebrow">One state, one network</div>
            <h2>Find your medical community.</h2>
          </div>
          <input class="district-search" id="districtSearch" placeholder="Search a district..." />
        </div>

        <div class="district-grid" id="districtGrid"></div>
      </div>
    </section>

    <section class="section" id="features">
      <div class="container">
        <div class="section-heading">
          <div>
            <div class="eyebrow">Built for your journey</div>
            <h2>Everything students need to move forward.</h2>
          </div>
          <p>From your first anatomy class to internship applications, MedLink Kerala makes the right connection easier to find.</p>
        </div>

        <div class="features-grid">
          <article class="feature-card">
            <div class="feature-number">01 / CONNECT</div>
            <h3>Meet your people</h3>
            <p>Connect with students from your college, district or field of interest.</p>
          </article>

          <article class="feature-card">
            <div class="feature-number">02 / LEARN</div>
            <h3>Study smarter</h3>
            <p>Build focused study groups and access notes, question banks and peer guidance.</p>
          </article>

          <article class="feature-card">
            <div class="feature-number">03 / DISCOVER</div>
            <h3>Find opportunities</h3>
            <p>Explore workshops, research projects, observerships and internships.</p>
          </article>

          <article class="feature-card">
            <div class="feature-number">04 / CONTRIBUTE</div>
            <h3>Give back</h3>
            <p>Share knowledge, mentor juniors and support the next generation of doctors.</p>
          </article>
        </div>
      </div>
    </section>

    <section class="section community" id="community">
      <div class="container community-grid">
        <div>
          <div class="eyebrow">The community pulse</div>
          <h2>Real conversations from students like you.</h2>
          <p>Ask questions, exchange ideas and stay informed about what is happening across Kerala's medical campuses.</p>
          <button class="btn btn-lime" onclick="openModal()">Join the conversation →</button>
        </div>

        <div class="post-list">
          <article class="post">
            <div class="post-avatar">AN</div>
            <div>
              <h4>Any good resources for pharmacology revision?</h4>
              <p>Ananya Nair · Government Medical College, Kozhikode · 12 replies</p>
            </div>
          </article>

          <article class="post">
            <div class="post-avatar">VK</div>
            <div>
              <h4>Looking for two students to join our anatomy study group.</h4>
              <p>Vishnu Krishnan · Amrita Institute, Kochi · 8 replies</p>
            </div>
          </article>

          <article class="post">
            <div class="post-avatar">FM</div>
            <div>
              <h4>Research assistant opportunity in pediatric cardiology.</h4>
              <p>Fathima M. · Thrissur · Opportunity · 24 interested</p>
            </div>
          </article>
        </div>
      </div>
    </section>

    <section class="section" id="events">
      <div class="container">
        <div class="section-heading">
          <div>
            <div class="eyebrow">Mark your calendar</div>
            <h2>Upcoming across the state.</h2>
          </div>
          <p>Keep up with events, workshops and academic sessions happening near you.</p>
        </div>

        <div class="events-grid">
          <article class="event-card">
            <span class="event-date">SEP 21, 2026</span>
            <h3>Kerala Medical Students Summit</h3>
            <p>A full-day gathering on innovation, public health and the future of medicine.</p>
            <div class="event-location">📍 Thiruvananthapuram</div>
          </article>

          <article class="event-card">
            <span class="event-date">SEP 28, 2026</span>
            <h3>Clinical Case Discussion Series</h3>
            <p>Peer-led case discussions covering emergency medicine and internal medicine.</p>
            <div class="event-location">📍 Online · Open to all districts</div>
          </article>

          <article class="event-card">
            <span class="event-date">OCT 04, 2026</span>
            <h3>Research Methods Bootcamp</h3>
            <p>Learn study design, statistics and how to turn a clinical question into research.</p>
            <div class="event-location">📍 Ernakulam</div>
          </article>
        </div>
      </div>
    </section>

    <section class="cta">
      <div class="container cta-inner">
        <div>
          <h2>Your next useful connection is closer than you think.</h2>
          <p>Join students from all 14 districts of Kerala.</p>
        </div>
        <button class="btn btn-primary" onclick="openModal()">Join MedLink Kerala →</button>
      </div>
    </section>
  </main>

  <footer>
    <div class="container footer-inner">
      <span>© 2026 MedLink Kerala</span>
      <span>Built for students who care about better healthcare.</span>
    </div>
  </footer>

  <div class="modal" id="modal">
    <div class="modal-box">
      <button class="close" onclick="closeModal()">×</button>
      <h2>Join MedLink Kerala</h2>
      <p>Create your student profile and start connecting with your medical community.</p>

      <form onsubmit="submitForm(event)">
        <input type="text" placeholder="Full name" required />
        <input type="email" placeholder="Email address" required />
        <select required>
          <option value="">Select your district</option>
          <option>Thiruvananthapuram</option>
          <option>Kollam</option>
          <option>Pathanamthitta</option>
          <option>Alappuzha</option>
          <option>Kottayam</option>
          <option>Idukki</option>
          <option>Ernakulam</option>
          <option>Thrissur</option>
          <option>Palakkad</option>
          <option>Malappuram</option>
          <option>Kozhikode</option>
          <option>Wayanad</option>
          <option>Kannur</option>
          <option>Kasaragod</option>
        </select>
        <button class="btn btn-primary" type="submit" style="width:100%">Create profile</button>
      </form>
    </div>
  </div>

  <script>
    const districts = [
      ["Thiruvananthapuram", "South Kerala"],
      ["Kollam", "South Kerala"],
      ["Pathanamthitta", "South Kerala"],
      ["Alappuzha", "South Kerala"],
      ["Kottayam", "Central Kerala"],
      ["Idukki", "High Range"],
      ["Ernakulam", "Central Kerala"],
      ["Thrissur", "Central Kerala"],
      ["Palakkad", "North Kerala"],
      ["Malappuram", "North Kerala"],
      ["Kozhikode", "North Kerala"],
      ["Wayanad", "High Range"],
      ["Kannur", "North Kerala"],
      ["Kasaragod", "North Kerala"]
    ];

    const districtGrid = document.getElementById("districtGrid");
    const search = document.getElementById("districtSearch");

    function renderDistricts(value = "") {
      const filtered = districts.filter(([name]) =>
        name.toLowerCase().includes(value.toLowerCase())
      );

      districtGrid.innerHTML = filtered.map(([name, region]) => `
        <button class="district" onclick="selectDistrict('${name}')">
          <div class="district-icon">⌖</div>
          <strong>${name}</strong>
          <small>${region}</small>
        </button>
      `).join("");
    }

    function selectDistrict(name) {
      alert(`The ${name} medical student community will open here.`);
    }

    function openModal() {
      document.getElementById("modal").classList.add("open");
    }

    function closeModal() {
      document.getElementById("modal").classList.remove("open");
    }

    function submitForm(event) {
      event.preventDefault();
      alert("Profile creation is ready to connect to your backend.");
      closeModal();
    }

    function toggleMobile() {
      const links = document.querySelector(".nav-links");
      links.style.display = links.style.display === "flex" ? "none" : "flex";
      links.style.position = "absolute";
      links.style.top = "78px";
      links.style.left = "14px";
      links.style.right = "14px";
      links.style.padding = "18px";
      links.style.flexDirection = "column";
      links.style.background = "white";
      links.style.borderRadius = "12px";
      links.style.boxShadow = "var(--shadow)";
    }

    document.getElementById("modal").addEventListener("click", event => {
      if (event.target.id === "modal") closeModal();
    });

    search.addEventListener("input", event => renderDistricts(event.target.value));
    renderDistricts();
  </script>
</body>
</html>
```
