<nav class="navbar">
    <div class="navbar-container">
      <a href="/" class="navbar-brand">Movie Watchlist</a>
      <ul class="navbar-links">
        <li><a href="/" class="nav-link">Home</a></li>
        <li><a href="/movies" class="nav-link">Movies</a></li>
      </ul>
    </div>
  </nav>
  
  <slot />
  
  <style>
  /* Navbar-Container */
  .navbar {
    background-color: #2c2c2c; /* Dunkler Hintergrund */
    color: white;
    padding: 15px 20px; /* Abstand oben/unten und seitlich */
    position: sticky; /* Bleibt beim Scrollen oben */
    top: 0; /* Fixiert an den oberen Rand */
    z-index: 1000; /* Höchste Sichtbarkeit */
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1); /* Leichter Schatten */
  }
  
  /* Inhalt der Navbar */
  .navbar-container {
    display: flex;
    justify-content: space-between; /* Links und Rechts ausrichten */
    align-items: center; /* Vertikal zentriert */
    max-width: 1200px;
    margin: 0 auto; /* Zentriert die Navbar */
  }
  
  /* Markenname */
  .navbar-brand {
    font-size: 1.5rem;
    font-weight: bold;
    text-decoration: none;
    color: #ffffff;
    transition: color 0.3s ease-in-out;
  }
  
  .navbar-brand:hover {
    color: #f39c12; /* Goldener Hover-Effekt */
  }
  
  /* Links */
  .navbar-links {
    list-style: none; /* Entfernt Bullet Points */
    display: flex;
    gap: 20px; /* Abstand zwischen Links */
    margin: 0;
    padding: 0;
  }
  
  .nav-link {
    font-size: 1rem;
    text-decoration: none;
    color: #ffffff;
    padding: 5px 10px;
    border-radius: 5px;
    transition: background-color 0.3s ease-in-out, color 0.3s ease-in-out;
  }
  
  .nav-link:hover {
    background-color: #f39c12; /* Goldener Hover-Effekt */
    color: #000000; /* Schwarzer Text */
  }
  </style>
  