<script>
  const movies = [
    {
      title: "Sternenwanderer",
      year: 2025,
      length: "143 Minuten",
      poster: "/images/Sternenwanderer.png",
    },
    {
      title: "Das verborgene Königreich",
      year: 2023,
      length: "128 Minuten",
      poster: "/images/Das-verborgene-Koenigreich.png",
    },
    {
      title: "Die Zeitreise",
      year: 2022,
      length: "152 Minuten",
      poster: "/images/Die-Zeitreise.png",
    },
    {
      title: "Das letzte Abenteuer",
      year: 2024,
      length: "137 Minuten",
      poster: "/images/Das-letzte-Abenteuer.png",
    },
    {
      title: "Mord in der Metropole",
      year: 2022,
      duration: "110 Minuten",
      poster: "/images/Mord-in-der-Metropole.png"
    },
    {
      title: "Die Schattenvilla",
      year: 2023,
      duration: "95 Minuten",
      poster: "/images/Die-Schattenvilla.png"
    },
    {
      title: "Liebessturm",
      year: 2021,
      duration: "120 Minuten",
      poster: "/images/Liebessturm.png"
    },
    {
      title: "Der Untergang von Helios",
      year: 2024,
      duration: "140 Minuten",
      poster: "/images/Der-Untergang-von-Helios.png"
    }
  ];
</script>

<div class="container mt-5">
  <h2 class="text-center mb-4">Movies</h2>
  <div class="movie-grid">
    {#each movies as movie}
      <div class="movie-card">
        <img src={movie.poster} class="movie-poster" alt={movie.title} />
        <div class="card-body">
          <h5 class="card-title">{movie.title}</h5>
          <p class="card-text">Erscheinungsjahr: {movie.year}</p>
          <p class="card-text">Dauer: {movie.duration}</p>
        </div>
      </div>
    {/each}
  </div>
</div>

<style>
  .movie-grid {
    display: flex; /* Aktiviert das Flexbox-Layout */
    flex-wrap: wrap; /* Karten umbrechen, falls kein Platz ist */
    justify-content: space-between; /* Lücken zwischen Karten gleichmäßig verteilen */
    gap: 20px; /* Abstand zwischen den Karten */
    color: violet;
  }
  
  /* Einzelne Karte */
  .movie-card {
    flex: 1 1 calc(25% - 20px); /* 4 Karten pro Reihe, mit Abstand */
    max-width: calc(25% - 20px); /* Maximale Breite einer Karte */
    background-color: #1e1e1e; /* Dunkler Hintergrund */
    color: orange;
    border: 2px solid #444; /* Rahmen um die Karte */
    border-radius: 8px; /* Abgerundete Ecken */
    overflow: hidden;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2); /* Schatten */
    transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
  }
  
  /* Hover-Effekt */
  .movie-card:hover {
    transform: scale(1.05); /* Vergrößerung bei Hover */
    box-shadow: 0 8px 16px rgba(0, 0, 0, 0.4); /* Größerer Schatten bei Hover */
  }
  
  /* Poster-Bild */
  .movie-poster {
    width: 100%; /* Bild passt zur Breite der Karte */
    height: 300px; /* Einheitliche Höhe für alle Bilder */
    object-fit: cover; /* Bild wird proportional angepasst */
  }
  
  /* Text-Bereich */
  .card-body {
    padding: 15px; /* Abstand im Textbereich */
    text-align: center; /* Zentriert den Text */
  }
</style>
