<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Standard Better Health</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      margin: 0;
      padding: 0;
      background: #f7f9fa;
      color: #333;
    }

    header {
      background: #004d66;
      color: white;
      padding: 30px 20px;
      text-align: center;
    }

    header h1 {
      margin: 0;
      font-size: 36px;
    }

    header p {
      margin: 5px 0 0;
      font-size: 18px;
    }

    nav ul {
      list-style-type: none;
      padding: 0;
    }

    nav ul li {
      display: inline;
      margin: 0 15px;
    }

    nav ul li a {
      color: white;
      text-decoration: none;
    }

    section {
      padding: 40px 20px;
      max-width: 1000px;
      margin: auto;
      opacity: 0;
      transform: translateY(30px);
      transition: opacity 1s ease, transform 1s ease;
    }

    section.visible {
      opacity: 1;
      transform: translateY(0);
    }

    h2 {
      color: #004d66;
      margin-bottom: 20px;
    }

    .contact p {
      line-height: 1.8;
      font-size: 16px;
    }

    form {
      max-width: 600px;
      margin: 20px auto;
      background: #fff;
      padding: 20px;
      border-radius: 8px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    }

    label {
      display: block;
      margin: 10px 0 5px;
    }

    input, textarea {
      width: 100%;
      padding: 10px;
      border: 1px solid #ddd;
      border-radius: 4px;
    }

    button {
      background: #004d66;
      color: white;
      padding: 10px 15px;
      border: none;
      border-radius: 4px;
      cursor: pointer;
    }

    button:hover {
      background: #003a50;
    }

    .footer {
      background: #004d66;
      color: white;
      text-align: center;
      padding: 15px;
      font-size: 14px;
    }

    .footer a {
      color: white;
      text-decoration: none;
      padding: 0 10px;
    }

    .footer a:hover {
      text-decoration: underline;
    }

    @media (max-width: 768px) {
      header h1 {
        font-size: 28px;
      }

      .footer {
        font-size: 12px;
      }

      form {
        padding: 15px;
      }
    }

    @media (max-width: 480px) {
      header {
        padding: 20px 10px;
      }

      section {
        padding: 20px 10px;
      }
    }

    html {
      scroll-behavior: smooth;
    }
  </style>
</head>
<body>

  <header>
    <h1>Standard Better Health</h1>
    <p>Empowering Health. Enhancing Lives.</p>
    <nav>
      <ul>
        <li><a href="#about">About Us</a></li>
        <li><a href="#services">Our Services</a></li>
        <li><a href="#contact">Contact Us</a></li>
      </ul>
    </nav>
  </header>

  <section id="about" class="fade-in">
    <h2>About Us</h2>
    <p>
      At Standard Better Health, our mission is to provide top-tier health services that promote well-being and preventative care for individuals and families. 
      Based in Baltimore, Maryland, we are committed to compassion, excellence, and community health solutions.
    </p>
  </section>

  <section id="services" class="fade-in">
    <h2>Our Services</h2>
    <ul>
      <li>Primary Healthcare</li>
      <li>Health Screenings & Diagnostics</li>
      <li>Vaccinations</li>
      <li>Nutrition & Wellness Programs</li>
      <li>Patient Education</li>
    </ul>
  </section>

  <section id="contact" class="fade-in">
    <h2>Contact Us</h2>
    <p><strong>Henry Ihekuna – Owner</strong></p>
    <p>Address: 4301 Belair Rd, Baltimore, MD 21206</p>
    <p>Phone: <a href="tel:+14434499672">(443) 449-9672</a></p>
    <p>Email: <a href="mailto:info@standardbetterhealth.com">info@standardbetterhealth.com</a></p>
    <p>Website: <a href="http://www.standardbetterhealth.com" target="_blank">www.standardbetterhealth.com</a></p>

    <h3>Send Us a Message</h3>
    <form action="mailto:info@standardbetterhealth.com" method="post" enctype="text/plain">
      <label for="name">Name:</label>
      <input type="text" id="name" name="name" required><br><br>

      <label for="email">Email:</label>
      <input type="email" id="email" name="email" required><br><br>

      <label for="message">Message:</label><br>
      <textarea id="message" name="message" rows="4" required></textarea><br><br>

      <button type="submit">Send Message</button>
    </form>
  </section>

  <div class="footer">
    <p>&copy; 2025 Standard Better Health. All rights reserved.</p>
    <p>
      <a href="https://www.facebook.com" target="_blank">Facebook</a> |
      <a href="https://twitter.com" target="_blank">Twitter</a> |
      <a href="https://www.linkedin.com" target="_blank">LinkedIn</a>
    </p>
  </div>

  <script>
    document.addEventListener("DOMContentLoaded", () => {
      const sections = document.querySelectorAll("section");
      
      const onScroll = () => {
        sections.forEach((section) => {
          if (section.getBoundingClientRect().top < window.innerHeight - 100) {
            section.classList.add("visible");
          }
        });
      };

      window.addEventListener("scroll", onScroll);
      onScroll(); // Trigger on page load
    });
  </script>

</body>
</html>
