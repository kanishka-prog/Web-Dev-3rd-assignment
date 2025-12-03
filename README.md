WEB DEV ASSIGNMENT III
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Responsive Portfolio</title>
  <style>
    :root {
      --primary: #0db0e6;
      --dark: #111;
      --light: #f5f5f5;
      --font-lg: 2rem;
      --font-md: 1.2rem;
      --font-sm: 1rem;
    }

    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: var(--light);
      color: var(--dark);
    }

    /* NAVBAR */
    nav {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1rem 2rem;
      background: white;
      position: sticky;
      top: 0;
      z-index: 100;
      box-shadow: 0 2px 6px rgba(0,0,0,0.1);
    }

    nav a {
      margin-left: 1.5rem;
      text-decoration: none;
      color: var(--dark);
      font-size: var(--font-md);
      transition: color .3s ease;
    }

    nav a:hover {
      color: var(--primary);
    }

    /* HERO SECTION */
    .hero {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding: 10vh 2rem;
      background: linear-gradient(to bottom right, #e3f7ff, #ffffff);
      animation: fadeIn 1.5s ease;
    }

    .hero h1 {
      font-size: 3rem;
      margin-bottom: 1rem;
    }

    .hero p {
      font-size: var(--font-md);
      max-width: 500px;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    /* ABOUT GRID SECTION */
    .about {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 2rem;
      padding: 4rem 2rem;
      align-items: center;
    }

    .about img {
      width: 100%;
      border-radius: 10px;
    }

    .about-text h2 {
      font-size: var(--font-lg);
      margin-bottom: 1rem;
    }

    .about-text p {
      font-size: var(--font-sm);
      line-height: 1.6;
    }

    /* PROJECTS - FLEXBOX */
    .projects {
      padding: 4rem 2rem;
      background: white;
    }

    .project-list {
      display: flex;
      flex-wrap: wrap;
      gap: 2rem;
      justify-content: center;
    }

    .project {
      background: var(--light);
      padding: 1.5rem;
      width: 300px;
      border-radius: 10px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.1);
      transition: transform .3s ease;
    }

    .project:hover {
      transform: translateY(-10px);
    }

    .project h3 {
      margin-top: 0;
    }

    /* CONTACT */
    .contact {
      text-align: center;
      padding: 3rem 2rem;
    }

    .contact button {
      padding: .8rem 2rem;
      font-size: var(--font-md);
      background: var(--primary);
      border: none;
      border-radius: 5px;
      color: white;
      cursor: pointer;
      transition: background .3s ease, transform .3s ease;
    }

    .contact button:hover {
      background: #098ab8;
      transform: scale(1.05);
    }

    /* MEDIA QUERIES */
    @media (max-width: 768px) {
      .about {
        grid-template-columns: 1fr;
        text-align: center;
      }
    }
  </style>
</head>
<body>

  <nav>
    <div class="logo"><strong>Portfolio</strong></div>
    <div>
      <a href="#about">About</a>
      <a href="#projects">Projects</a>
      <a href="#contact">Contact</a>
    </div>
  </nav>

  <section class="hero">
    <h1>Hello, I'm Kanishka</h1>
    <p>Aspiring developer creating interactive and responsive web designs.</p>
  </section>

  <section id="about" class="about">
    <img src="https://via.placeholder.com/400" alt="Profile" />
    <div class="about-text">
      <h2>About Me</h2>
      <p>
        I specialize in front-end development and love building responsive layouts
        using modern CSS techniques like Flexbox, Grid, and animations.
      </p>
    </div>
  </section>

  <section id="projects" class="projects">
    <h2 style="text-align:center;font-size:var(--font-lg)">Projects</h2>
    <div class="project-list">
      <div class="project">
        <h3>Project One</h3>
        <p>A sample project showcasing responsive UI design.</p>
      </div>
      <div class="project">
        <h3>Project Two</h3>
        <p>Interactive animations using CSS transitions and keyframes.</p>
      </div>
      <div class="project">
        <h3>Project Three</h3>
        <p>A Flexbox and Grid powered layout demonstration.</p>
      </div>
    </div>
  </section>

  <section id="contact" class="contact">
    <h2 style="font-size:var(--font-lg)">Get in Touch</h2>
    <button>Contact Me</button>
  </section>

</body>
</html>

