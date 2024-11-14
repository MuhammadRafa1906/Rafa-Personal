<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Navigation Menu with About Section</title>
  
  <style>
    /* Global Reset */
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }
    body {
      font-family: Arial, sans-serif;
      background-color: #f0f3f5;
      color: #333;
    }

    /* Navbar Container */
    nav {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 15px 20px;
      background-color: #007acc;
      color: #fff;
    }

    /* Logo */
    .logo {
      font-size: 1.5em;
      font-weight: bold;
    }

    /* Navigation Links */
    .nav-links {
      display: flex;
      list-style: none;
    }
    .nav-links li {
      margin-left: 20px;
    }
    .nav-links a {
      color: #fff;
      text-decoration: none;
      font-size: 1em;
      padding: 5px 10px;
      transition: background-color 0.3s ease;
    }
    .nav-links a:hover {
      background-color: #005b99;
      border-radius: 4px;
    }

    /* Mobile Menu Toggle Button */
    .menu-toggle {
      display: none;
      font-size: 1.5em;
      cursor: pointer;
    }

    /* Responsive Styling */
    @media (max-width: 768px) {
      .nav-links {
        display: none;
        flex-direction: column;
        width: 100%;
        text-align: center;
        background-color: #007acc;
      }
      .nav-links li {
        margin: 10px 0;
      }
      .menu-toggle {
        display: block;
      }
    }

    /* Show Menu on Mobile when Active */
    .nav-links.active {
      display: flex;
    }

    /* Main Content and iframe Styles */
    main {
      padding: 20px;
      max-width: 800px;
      margin: 20px auto;
    }
    .about-content {
      display: none; /* Hidden by default */
    }
    .about-content iframe {
      width: 100%;
      height: 600px;
      border: none;
    }
  </style>
</head>
<body>
  
  <!-- Navbar Section -->
  <nav>
    <div class="logo">@mhmmdrafaa._</div>
    <ul class="nav-links">
      <li><a href="menu.html">Home</a></li>
      <li><a href="Projek Baru.html" onclick="showAbout()">Isi Cerita</a></li>
      <li><a href="about.html">About</a></li>
      <li><a href="test.html">Contact</a></li>
    </ul>
    <div class="menu-toggle" onclick="toggleMenu()">☰</div>
  </nav>
  
  <!-- Main Content -->
  <main>
    <section id="home">
      <h1>Welcome to My Website</h1>
      <p>This is a sample page with a responsive navigation menu.</p>
    </section>
    
    <!-- About Section with Embedded Projek Baru.html -->
    <section id="about-section" class="about-content">
      <h2>About Us</h2>
      <iframe src="Projek Baru.html" title="About Content"></iframe>
    </section>
  </main>
  <!-- Home Section with Embedded menu.html -->
  <section id="about-section" class="about-content">
    <h2>Home</h2>
    <iframe src="menu.html" title="Home Content"></iframe>
  </section>
</main>

  <footer style="text-align: center; padding: 10px; color: #777;">
    <p>&copy; 2024 Rafa Website</p>
  </footer>

  <script>
    // Toggle Mobile Menu
    function toggleMenu() {
      const navLinks = document.querySelector('.nav-links');
      navLinks.classList.toggle('active');
    }

    // Show About Section with Projek Baru.html
    function showAbout() {
      document.getElementById('about-section').style.display = 'block';
      window.scrollTo(0, document.getElementById('about-section').offsetTop);
    }
  </script>
</body>
</html>
