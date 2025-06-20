# task3-portfolio
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Muqaddas Imtiaz Portfolio</title>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; scroll-behavior: smooth; }
    body { font-family: 'Segoe UI', sans-serif; background: #f7f9fc; color: #333; }
    header { background: #1a1a2e; color: white; padding: 1.5rem; text-align: center; position: sticky; top: 0; z-index: 1000; }
    nav a { color: white; margin: 0 15px; text-decoration: none; font-weight: 500; }
    section { padding: 3rem 1rem; max-width: 1100px; margin: auto; display: none; }
    section.active { display: block; }
    .profile-pic { width: 140px; border-radius: 50%; display: block; margin: 1rem auto; }
    .tagline { font-style: italic; color: #666; margin: 1rem 0; text-align: center; }
    .links a { display: inline-block; margin: 0.5rem 10px; color: #007acc; text-decoration: none; font-weight: 500; }
    .section-title { text-align: center; font-size: 2rem; margin-bottom: 2rem; color: #1a1a2e; }
    .skills-container { display: flex; flex-wrap: wrap; gap: 1rem; justify-content: center; }
    .skill-card { background: white; border-radius: 12px; box-shadow: 0 4px 15px rgba(0,0,0,0.1); padding: 1rem; width: 180px; text-align: center; transition: transform 0.3s; }
    .skill-card:hover { transform: translateY(-5px); }
    .skill-card img { width: 50px; height: 50px; margin-bottom: 10px; }
    .project-card img { width: 100%; border-radius: 10px; margin-bottom: 10px; }
    .projects-container { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 1.5rem; }
    .project-card { background: white; padding: 1.5rem; border-radius: 10px; box-shadow: 0 0 10px rgba(0,0,0,0.1); transition: transform 0.3s; }
    .project-card:hover { transform: translateY(-5px); }
    table { margin: 2rem auto; border-collapse: collapse; width: 100%; max-width: 800px; box-shadow: 0 0 10px rgba(0,0,0,0.1); }
    th, td { border: 1px solid #999; padding: 12px; text-align: center; }
    th { background: #1a1a2e; color: white; }
    tr:nth-child(even) { background-color: #f2f2f2; }
    .buttons { text-align: center; margin-top: 2rem; }
    button { padding: 10px 20px; font-size: 16px; border: none; background: #1a1a2e; color: white; cursor: pointer; border-radius: 5px; margin: 5px; }
    footer { text-align: center; padding: 1rem; background: #1a1a2e; color: white; margin-top: 3rem; font-size: 0.9rem; }
    form { display: flex; flex-direction: column; gap: 10px; max-width: 400px; margin: auto; }
    input, textarea { padding: 10px; font-size: 14px; border-radius: 5px; border: 1px solid #ccc; }
    #backToTop { position: fixed; bottom: 30px; right: 30px; display: none; background: #333; color: #fff; padding: 10px 15px; border: none; border-radius: 50%; cursor: pointer; }
    .dark-mode { background: #111; color: #eee; }
    @media (max-width: 600px) { .skills-container { flex-direction: column; align-items: center; } }
  </style>
</head>
<body>
  <header>
    <h1>Muqaddas Imtiaz</h1>
    <nav>
      <a href="#" onclick="showPage('home')">Home</a>
      <a href="#" onclick="showPage('about')">About</a>
      <a href="#" onclick="showPage('skills')">Skills</a>
      <a href="#" onclick="showPage('projects')">Projects</a>
      <a href="#" onclick="showPage('comments')">Comments</a>
      <a href="#" onclick="showPage('contact')">Contact</a>
      <a href="#" onclick="toggleDarkMode()">🌓</a>
    </nav>
  </header>

  <section id="home" class="active">
    <img src="mypic.jpg" alt="Profile Picture" class="profile-pic" />
    <h2 class="section-title"><span id="typing"></span></h2>
    <p class="tagline">"Turning ideas into code and making them work beautifully."</p>
    <div class="buttons">
      <button onclick="showPage('about')">About Me</button>
    </div>
  </section>

  <section id="about">
    <h2 class="section-title">About Me</h2>
    <p style="text-align: center; max-width: 700px; margin: auto;">
      I'm <strong>Muqaddas Imtiaz</strong>, a passionate BS Data Science student and a dedicated Web Development Intern at Digital Empowerment Pakistan. I create responsive, visually appealing websites using HTML, CSS, and JavaScript, and also work with backend tools like Python and MySQL. My dream is to become a strong, skilled, and self-independent full-stack developer — while proudly living as a hijabi girl, a wise and responsible daughter, and a support system for my family. I believe in hard work, learning consistently, and using technology to make lives better — especially for girls like me.
    </p>

    <h3 class="section-title">🎓 Education</h3>
    <table>
      <thead>
        <tr>
          <th>Grade</th>
          <th>Percentage</th>
          <th>Board</th>
          <th>Institute</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Matriculation</td>
          <td>68%</td>
          <td>Federal Board</td>
          <td>Army Public School North Campus Malir Cantt Karachi</td>
        </tr>
        <tr>
          <td>Intermediate</td>
          <td>74%</td>
          <td>Nawabshah Board</td>
          <td>Govt Girls Degree College Nawabshah</td>
        </tr>
        <tr>
          <td>BS Data Science</td>
          <td>Ongoing</td>
          <td>—</td>
          <td>University (Name Optional)</td>
        </tr>
      </tbody>
    </table>
    <div class="links" style="text-align:center;">
      <a href="https://github.com/Muqadas-g" target="_blank">GitHub</a>
      <a href="https://www.linkedin.com/in/muqaddas-imtiaz-5635b0301?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app" target="_blank">LinkedIn</a>
    </div>
  </section>

  <section id="skills">
    <h2 class="section-title">My Skills</h2>
    <div class="skills-container">
      <div class="skill-card"><img src="html.jpg" alt="HTML"><h4>HTML</h4></div>
      <div class="skill-card"><img src="css.jpg" alt="CSS"><h4>CSS</h4></div>
      <div class="skill-card"><img src="JS.jpg" alt="JavaScript"><h4>JavaScript</h4></div>
      <div class="skill-card"><img src="python.jpg" alt="Python"><h4>Python</h4></div>
      <div class="skill-card"><img src="java.jpg" alt="Java"><h4>Java</h4></div>
      <div class="skill-card"><img src="C.jpg" alt="C Language"><h4>C Language</h4></div>
      <div class="skill-card"><img src="mysql.jpg" alt="MySQL"><h4>MySQL</h4></div>
    </div>
  </section>

  <section id="projects">
    <h2 class="section-title">Projects</h2>
    <div class="projects-container">
      <div class="project-card">
        <img src="project1.jpg" alt="Project 1">
        <h3>Glamour Wardrobe</h3>
        <p>A static e-commerce website designed using HTML and CSS, showcasing clothing products with responsive design.</p>
      </div>
      <div class="project-card">
        <img src="project2.jpg" alt="Project 2">
        <h3>Muqaddas Portfolio</h3>
        <p>A personal portfolio website built with a dark theme, skill cards, project section, and contact form.</p>
      </div>
      <div class="project-card">
        <img src="RedBLueNimGAme.jpg" alt="Red Blue Nim Game">
        <h3>Red Blue Nim Game</h3>
        <p>A Python-based logical game using object-oriented programming, hosted on GitHub with discussion and issue tracker.</p>
        <a href="https://github.com/Muqadas-g/Red-blue-Nim-game/issues/5" target="_blank">View Game</a>
      </div>
      </div>
  </section>

  <section id="comments">
    <h2 class="section-title">Comments</h2>
    <form>
      <input type="text" placeholder="Your Name" required>
      <textarea rows="5" placeholder="Your Comments" required></textarea>
      <button type="submit">Submit</button>
    </form>
  </section>

  <section id="contact">
    <h2 class="section-title">Contact Me</h2>
    <p style="text-align:center;">
      <strong>Email:</strong> imtiazmuskan525@gmail.com@gmail.com<br>
      <strong>Phone:</strong> +92-311-3014709<br>
      <strong>Location:</strong> Nawabshah, Pakistan
    </p>
    <form>
      <input type="text" placeholder="Full Name" required>
      <input type="email" placeholder="Email Address" required>
      <textarea rows="5" placeholder="Your Message" required></textarea>
      <button type="submit">Send</button>
    </form>
  </section>

  <footer>
    &copy; 2025 Muqaddas Imtiaz. All Rights Reserved.
  </footer>

  <button id="backToTop" onclick="scrollToTop()">↑</button>

  <script>
    const sections = document.querySelectorAll('section');
    function showPage(id) {
      sections.forEach(section => section.classList.remove('active'));
      document.getElementById(id).classList.add('active');
      window.scrollTo(0, 0);
    }

    function toggleDarkMode() {
      document.body.classList.toggle('dark-mode');
    }

    function scrollToTop() {
      window.scrollTo({ top: 0, behavior: 'smooth' });
    }

    const backToTop = document.getElementById("backToTop");
    window.onscroll = () => {
      backToTop.style.display = window.scrollY > 300 ? "block" : "none";
    };

    // Typing effect
    const typingElement = document.getElementById("typing");
    const phrases = ["Web Developer", "Data Science Student", "Tech Learner"];
    let i = 0, j = 0, currentPhrase = "", isDeleting = false;

    function typeEffect() {
      currentPhrase = phrases[i];
      if (isDeleting) {
        typingElement.textContent = currentPhrase.substring(0, j--);
        if (j < 0) {
          isDeleting = false;
          i = (i + 1) % phrases.length;
        }
      } else {
        typingElement.textContent = currentPhrase.substring(0, j++);
        if (j > currentPhrase.length) {
          isDeleting = true;
          setTimeout(typeEffect, 1000);
          return;
        }
      }
      setTimeout(typeEffect, isDeleting ? 60 : 120);
    }
    typeEffect();
  </script>
</body>
</html>
