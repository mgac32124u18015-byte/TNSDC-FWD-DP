<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Digital Portfolio</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial', sans-serif;
        }

        body {
            line-height: 1.6;
            color: #333;
        }

        header {
            background: linear-gradient(135deg, #2c3e50, #3498db);
            color: white;
            text-align: center;
            padding: 4rem 1rem;
        }

        header h1 {
            font-size: 2.5rem;
            margin-bottom: 0.5rem;
        }

        header p {
            font-size: 1.2rem;
        }

        nav {
            background: #f4f4f4;
            padding: 1rem;
            position: sticky;
            top: 0;
            z-index: 100;
        }

        nav ul {
            list-style: none;
            display: flex;
            justify-content: center;
            gap: 2rem;
        }

        nav a {
            text-decoration: none;
            color: #333;
            font-weight: bold;
        }

        nav a:hover {
            color: #3498db;
        }

        section {
            padding: 3rem 1rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        h2 {
            text-align: center;
            margin-bottom: 2rem;
            color: #2c3e50;
        }

        .skills-grid, .projects-grid, .experience-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
        }

        .skill-card, .project-card, .experience-card {
            background: #f9f9f9;
            padding: 1.5rem;
            border-radius: 8px;
            text-align: center;
            transition: transform 0.3s;
        }

        .skill-card:hover, .project-card:hover, .experience-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }

        .contact-form {
            max-width: 600px;
            margin: 0 auto;
        }

        .contact-form input, .contact-form textarea {
            width: 100%;
            padding: 0.8rem;
            margin-bottom: 1rem;
            border: 1px solid #ddd;
            border-radius: 4px;
        }

        .contact-form button {
            background: #3498db;
            color: white;
            border: none;
            padding: 0.8rem 1.5rem;
            border-radius: 4px;
            cursor: pointer;
        }

        .contact-form button:hover {
            background: #2c3e50;
        }

        footer {
            background: #2c3e50;
            color: white;
            text-align: center;
            padding: 1rem;
            margin-top: 2rem;
        }

        @media (max-width: 768px) {
            nav ul {
                flex-direction: column;
                text-align: center;
                gap: 1rem;
            }

            header h1 {
                font-size: 1.8rem;
            }

            header p {
                font-size: 1rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>John Doe</h1>
        <p>Technology Enthusiast & Business Professional</p>
    </header>

    <nav>
        <ul>
            <li><a href="#about">About</a></li>
            <li><a href="#skills">Skills</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#experience">Experience</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>

    <section id="about">
        <h2>About Me</h2>
        <p style="text-align: center; max-width: 800px; margin: 0 auto;">
            I'm a passionate professional with expertise in technology and business strategy. With a background in software development and business analysis, I bridge the gap between technical solutions and business needs, delivering impactful results.
        </p>
    </section>

    <section id="skills">
        <h2>Skills</h2>
        <div class="skills-grid">
            <div class="skill-card">HTML5 & CSS3</div>
            <div class="skill-card">JavaScript</div>
            <div class="skill-card">Python</div>
            <div class="skill-card">Business Analysis</div>
            <div class="skill-card">Project Management</div>
            <div class="skill-card">Data Analytics</div>
        </div>
    </section>

    <section id="projects">
        <h2>Projects</h2>
        <div class="projects-grid">
            <div class="project-card">
                <h3>E-Commerce Platform</h3>
                <p>Developed a full-stack e-commerce website using HTML, CSS, JavaScript, and Node.js, improving user engagement by 30%.</p>
            </div>
            <div class="project-card">
                <h3>Business Dashboard</h3>
                <p>Created a data visualization dashboard using Python and Power BI to provide actionable business insights.</p>
            </div>
            <div class="project-card">
                <h3>Portfolio Website</h3>
                <p>Designed and developed this responsive portfolio to showcase my skills and projects effectively.</p>
            </div>
        </div>
    </section>

    <section id="experience">
        <h2>Experience</h2>
        <div class="experience-grid">
            <div class="experience-card">
                <h3>Software Developer</h3>
                <p>Tech Solutions Inc. | 2023 - Present</p>
                <p>Developed scalable web applications and collaborated with cross-functional teams.</p>
            </div>
            <div class="experience-card">
                <h3>Business Analyst</h3>
                <p>Global Enterprises | 2021 - 2023</p>
                <p>Conducted market analysis and optimized business processes for efficiency.</p>
            </div>
        </div>
    </section>

    <section id="contact">
        <h2>Contact Me</h2>
        <form class="contact-form" id="contactForm">
            <input type="text" id="name" placeholder="Your Name" required>
            <input type="email" id="email" placeholder="Your Email" required>
            <textarea id="message" placeholder="Your Message" rows="5" required></textarea>
            <button type="submit">Send Message</button>
        </form>
    </section>

    <footer>
        <p>&copy; 2025 John Doe. All rights reserved.</p>
    </footer>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('nav a').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                const targetId = this.getAttribute('href').substring(1);
                const targetSection = document.getElementById(targetId);
                targetSection.scrollIntoView({ behavior: 'smooth' });
            });
      });

        // Contact form submission
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            const name = document.getElementById('name').value;
            const email = document.getElementById('email').value;
            const message = document.getElementById('message').value;

            // Simple form validation and alert (replace with actual backend logic)
            if (name && email && message) {
                alert(`Thank you, ${name}! Your message has been sent.`);
                this.reset();
            } else {
                alert('Please fill out all fields.');
            }
        });
    </script>
</body>
</html>
