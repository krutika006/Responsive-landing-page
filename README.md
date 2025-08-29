# Responsive-landing-page
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Interactive Landing Page</title>
  <style>
    /* General Reset */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: Arial, sans-serif;
      line-height: 1.6;
    }

    /* Navigation Styles */
    nav {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 15px 50px;
      background: transparent;
      transition: background 0.3s ease, box-shadow 0.3s ease;
      z-index: 1000;
    }

    nav.scrolled {
      background: #222;
      box-shadow: 0 2px 5px rgba(0,0,0,0.3);
    }

    nav .logo {
      color: #fff;
      font-size: 1.5rem;
      font-weight: bold;
    }

    nav ul {
      list-style: none;
      display: flex;
      gap: 20px;
    }

    nav ul li a {
      color: #fff;
      text-decoration: none;
      font-size: 1rem;
      transition: color 0.3s, border-bottom 0.3s;
    }

    nav ul li a:hover {
      color: #f39c12;
      border-bottom: 2px solid #f39c12;
    }

    /* Hero Section */
    .hero {
      height: 100vh;
      background: url("https://picsum.photos/1600/900?blur") no-repeat center center/cover;
      display: flex;
      align-items: center;
      justify-content: center;
      flex-direction: column;
      text-align: center;
      color: white;
      padding: 0 20px;
    }

    .hero h1 {
      font-size: 3rem;
      margin-bottom: 20px;
    }

    .hero p {
      font-size: 1.2rem;
      margin-bottom: 30px;
    }

    .hero button {
      padding: 10px 20px;
      font-size: 1rem;
      border: none;
      border-radius: 5px;
      background: #f39c12;
      color: white;
      cursor: pointer;
      transition: background 0.3s;
    }

    .hero button:hover {
      background: #e67e22;
    }

    /* Sections */
    section {
      padding: 80px 20px;
      text-align: center;
    }

    section:nth-child(even) {
      background: #f4f4f4;
    }

    /* Responsive */
    @media (max-width: 768px) {
      nav {
        flex-direction: column;
        padding: 10px 20px;
      }

      nav ul {
        flex-direction: column;
        gap: 10px;
        margin-top: 10px;
      }

      .hero h1 {
        font-size: 2rem;
      }

      .hero p {
        font-size: 1rem;
      }
    }
  </style>
</head>
<body>

  <!-- Navigation -->
  <nav id="navbar">
    <div class="logo">MyBrand</div>
    <ul>
      <li><a href="#home">Home</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#services">Services</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <!-- Hero Section -->
  <section class="hero" id="home">
    <h1>Welcome to My Landing Page</h1>
    <p>Scroll down to see the interactive navigation menu in action.</p>
    <button>Get Started</button>
  </section>

  <!-- About Section -->
  <section id="about">
    <h2>About Us</h2>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla id dui ac erat laoreet gravida.</p>
  </section>

  <!-- Services Section -->
  <section id="services">
    <h2>Our Services</h2>
    <p>We provide amazing services to help your business grow.</p>
  </section>

  <!-- Contact Section -->
  <section id="contact">
    <h2>Contact Us</h2>
    <p>Get in touch with us through email or social media!</p>
  </section>

  <!-- JavaScript for Scroll Effect -->
  <script>
    const navbar = document.getElementById('navbar');
    window.addEventListener('scroll', () => {
      if (window.scrollY > 50) {
        navbar.classList.add('scrolled');
      } else {
        navbar.classList.remove('scrolled');
      }
    });
  </script>
  </body>
  </html>
  
  
    
    
    



    
