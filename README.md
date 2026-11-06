
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Official portfolio of Nathan Allen Pirtle. Explore my digital presence, creative work and professional journey.">
  <title>Nathan Allen Pirtle | Official Website</title>

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: Arial, sans-serif;
      background: #101322;
      color: #ffffff;
      line-height: 1.7;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    .container {
      width: min(1100px, 90%);
      margin: auto;
    }

    /* Navigation */

    header {
      padding: 22px 0;
      background: #101322;
      position: sticky;
      top: 0;
      z-index: 10;
      border-bottom: 1px solid #ffffff15;
    }

    nav {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 20px;
    }

    .logo {
      font-size: 22px;
      font-weight: bold;
      color: #ffffff;
    }

    .logo span {
      color: #ff9b78;
    }

    .nav-links {
      display: flex;
      gap: 25px;
      list-style: none;
      font-size: 14px;
      color: #d1d4df;
    }

    .nav-links a:hover {
      color: #ff9b78;
    }

    /* Hero */

    .hero {
      min-height: 650px;
      display: flex;
      align-items: center;
      padding: 90px 0;
      background:
        radial-gradient(circle at 85% 30%, #763e6855, transparent 35%),
        radial-gradient(circle at 10% 80%, #e8795840, transparent 35%),
        #101322;
    }

    .hero-content {
      display: grid;
      grid-template-columns: 1.4fr 0.8fr;
      align-items: center;
      gap: 60px;
    }

    .tag {
      color: #ffae91;
      font-size: 13px;
      letter-spacing: 3px;
      text-transform: uppercase;
      margin-bottom: 20px;
    }

    h1 {
      font-size: clamp(42px, 6vw, 68px);
      line-height: 1.15;
      margin-bottom: 25px;
    }

    h1 span {
      color: #ff9b78;
    }

    .hero p {
      color: #c4c7d2;
      font-size: 17px;
      max-width: 560px;
      margin-bottom: 30px;
    }

    .buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 15px;
    }

    .btn {
      display: inline-block;
      padding: 13px 25px;
      border-radius: 30px;
      font-weight: bold;
      font-size: 14px;
      transition: 0.3s;
    }

    .primary {
      background: #ff9675;
      color: #171522;
    }

    .primary:hover {
      background: #ffffff;
      transform: translateY(-3px);
    }

    .secondary {
      border: 1px solid #ffffff55;
      color: white;
    }

    .secondary:hover {
      border-color: #ff9675;
      color: #ff9675;
    }

    /* Profile */

    .profile {
      width: 290px;
      height: 340px;
      border-radius: 30px;
      background: linear-gradient(145deg, #ffb18c, #9f4776, #443c72);
      display: flex;
      justify-content: center;
      align-items: center;
      margin: auto;
      box-shadow: 0 25px 70px #0007;
      border: 5px solid #ffffff20;
    }

    .profile span {
      font-size: 90px;
      font-weight: bold;
      color: white;
      letter-spacing: -5px;
    }

    /* Common sections */

    section {
      padding: 90px 0;
    }

    .section-title {
      text-align: center;
      font-size: 36px;
      margin-bottom: 15px;
    }

    .section-title span {
      color: #ff9b78;
    }

    .section-subtitle {
      text-align: center;
      color: #aeb2c1;
      margin-bottom: 45px;
    }

    /* About */

    .about-card {
      max-width: 800px;
      margin: auto;
      padding: 35px;
      border-radius: 20px;
      background: #1b2032;
      border: 1px solid #ffffff12;
      text-align: center;
    }

    .about-card p {
      color: #c4c7d2;
    }

    /* Skills */

    .skills {
      background: #171b2a;
    }

    .skill-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
    }

    .skill-card {
      background: #22283b;
      padding: 30px 20px;
      text-align: center;
      border-radius: 18px;
      border: 1px solid #ffffff10;
      transition: 0.3s;
    }

    .skill-card:hover {
      transform: translateY(-7px);
      border-color: #ff9b78;
    }

    .skill-card .symbol {
      font-size: 35px;
      margin-bottom: 12px;
    }

    .skill-card p {
      color: #aeb2c1;
      font-size: 14px;
      margin-top: 8px;
    }

    /* Contact */

    .contact-box {
      text-align: center;
      max-width: 650px;
      margin: auto;
    }

    .contact-box p {
      color: #c4c7d2;
      margin: 20px 0 30px;
    }

    footer {
      padding: 25px 0;
      text-align: center;
      background: #0b0e19;
      color: #aeb2c1;
      font-size: 13px;
      border-top: 1px solid #ffffff15;
    }

    /* Mobile responsive */

    @media (max-width: 768px) {
      .nav-links {
        gap: 12px;
        font-size: 12px;
      }

      .hero {
        padding: 65px 0;
      }

      .hero-content {
        grid-template-columns: 1fr;
        text-align: center;
        gap: 45px;
      }

      .hero p {
        margin-left: auto;
        margin-right: auto;
      }

      .buttons {
        justify-content: center;
      }

      .profile {
        width: 230px;
        height: 270px;
      }

      .profile span {
        font-size: 75px;
      }

      .skill-grid {
        grid-template-columns: 1fr;
      }

      section {
        padding: 65px 0;
      }
    }

    @media (max-width: 400px) {
      nav {
        flex-direction: column;
      }

      .nav-links {
        gap: 15px;
      }
    }
  </style>
</head>

<body>

  <header>
    <div class="container">
      <nav>
        <a href="#" class="logo">Nathan<span>.</span></a>

        <ul class="nav-links">
          <li><a href="#home">Home</a></li>
          <li><a href="#about">About</a></li>
          <li><a href="#skills">Skills</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <main>

    <!-- HOME SECTION -->
    <section class="hero" id="home">
      <div class="container hero-content">

        <div>
          <div class="tag">Welcome to my official website</div>

          <h1>
            Hello, I'm<br>
            <span>Nathan Allen Pirtle</span>
          </h1>

          <p>
            Welcome to my personal website. Explore my digital
            presence, creative interests and professional journey.
            Thank you for visiting!
          </p>

          <div class="buttons">
            <a href="#about" class="btn primary">Discover More</a>
            <a href="#contact" class="btn secondary">Get In Touch</a>
          </div>
        </div>

        <div class="profile">
          <span>NA</span>
        </div>

      </div>
    </section>

    <!-- ABOUT SECTION -->
    <section id="about">
      <div class="container">

        <h2 class="section-title">About <span>Me</span></h2>

        <p class="section-subtitle">
          A little introduction
        </p>

        <div class="about-card">
          <p>
            Hello! I'm Nathan Allen Pirtle. This is my official
            online space where you can explore my interests,
            digital presence and creative journey.

            I believe in creativity, continuous learning and
            building meaningful connections through technology
            and digital platforms.

            Feel free to explore my website and connect with me.
          </p>
        </div>

      </div>
    </section>

    <!-- SKILLS SECTION -->
    <section class="skills" id="skills">
      <div class="container">

        <h2 class="section-title">My <span>Interests</span></h2>

        <p class="section-subtitle">
          Things I enjoy exploring
        </p>

        <div class="skill-grid">

          <div class="skill-card">
            <div class="symbol">💻</div>
            <h3>Technology</h3>
            <p>Exploring digital tools and new technologies.</p>
          </div>

          <div class="skill-card">
            <div class="symbol">🌐</div>
            <h3>Digital Media</h3>
            <p>Learning about online platforms and digital trends.</p>
          </div>

          <div class="skill-card">
            <div class="symbol">✨</div>
            <h3>Creativity</h3>
            <p>Discovering new ideas and creative possibilities.</p>
          </div>

        </div>
      </div>
    </section>

    <!-- CONTACT SECTION -->
    <section id="contact">
      <div class="container">

        <div class="contact-box">
          <h2 class="section-title">
            Get In <span>Touch</span>
          </h2>

          <p>
            Thanks for visiting my official website.
            Feel free to connect with me through email.
          </p>

          <!-- Replace with your real email -->
          <a href="mailto:your-email@example.com"
             class="btn primary">
            Send Me an Email ✉
          </a>
        </div>

      </div>
    </section>

  </main>

  <footer>
    <div class="container">
      © <span id="year"></span> Nathan Allen Pirtle.
      All Rights Reserved.
    </div>
  </footer>

  <script>
    document.getElementById("year").textContent =
      new Date().getFullYear();
  </script>

</body>
</html>
