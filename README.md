<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Invitación de Boda - Xavier & Mariangeles</title>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&family=Open+Sans&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      font-family: 'Open Sans', sans-serif;
      scroll-behavior: smooth;
      background: #fffdf8;
      color: #333;
    }
    section, header, footer {
      scroll-margin-top: 80px;
    }
    header {
      background: url('https://th.bing.com/th/id/OIP.y9M-Z7NcE5Ey0xj-xkfnoQHaHa?rs=1&pid=ImgDetMain') center/cover no-repeat;
      height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      color: white;
      padding: 0 20px;
    }
    header h1 {
      font-family: 'Playfair Display', serif;
      font-size: 4rem;
      margin: 0.5em 0;
      text-shadow: 2px 2px 6px rgba(0, 0, 0, 0.6);
    }
    header p {
      font-size: 1.7rem;
      text-shadow: 1px 1px 4px rgba(0, 0, 0, 0.5);
    }
    section {
      padding: 5em 2em;
      max-width: 900px;
      margin: 0 auto;
      border-radius: 24px;
      box-shadow: 0 0 20px rgba(0,0,0,0.05);
      margin-bottom: 2em;
      opacity: 0;
      transform: translateY(40px);
      transition: opacity 0.8s ease-out, transform 0.8s ease-out;
      background: #ffffffee;
    }
    section.visible {
      opacity: 1;
      transform: translateY(0);
    }
    h2 {
      font-family: 'Playfair Display', serif;
      font-size: 2.2rem;
      margin-bottom: 1em;
      text-align: center;
    }
    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 1em;
    }
    .gallery img {
      width: 100%;
      border-radius: 12px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
      transition: transform 0.3s ease;
    }
    .gallery img:hover {
      transform: scale(1.05);
    }
    .info {
      font-size: 1.1em;
      line-height: 1.8em;
    }
    .calendar {
      text-align: center;
      font-size: 1.4em;
      background: #ffe8d6;
      padding: 1em;
      border-radius: 12px;
      margin-top: 1em;
      font-weight: bold;
    }
    .formulario input, .formulario textarea {
      width: 100%;
      padding: 12px;
      margin: 10px 0;
      border: 1px solid #ccc;
      border-radius: 8px;
      font-size: 1rem;
    }
    .formulario button {
      padding: 12px 20px;
      background-color: #ce9178;
      color: white;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      font-size: 1rem;
    }
    .formulario button:hover {
      background-color: #b07d65;
    }
    footer {
      text-align: center;
      background-color: #f3eee7;
      padding: 40px 20px;
      font-size: 1.1em;
    }
  </style>
  <script>
    document.addEventListener('DOMContentLoaded', function () {
      const observer = new IntersectionObserver(entries => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            entry.target.classList.add('visible');
          }
        });
      }, { threshold: 0.1 });

      document.querySelectorAll('section').forEach(section => {
        observer.observe(section);
      });
    });
  </script>
</head>
<body>

<header>
  <h1>Xavier & Mariangeles</h1>
  <p>¡Nos casamos! 21 de Junio · Lugar: Nuestra Casa</p>
</header>

<section>
  <h2>Nuestra Historia</h2>
  <p class="info">Después de un viaje lleno de amor, aventuras y aprendizaje, hemos decidido dar el siguiente paso. Queremos compartir este momento tan especial con ustedes.</p>
</section>

<section>
  <h2>Galería</h2>
  <div class="gallery">
    <img src="https://source.unsplash.com/400x300/?couple,love" alt="Foto 1">
    <img src="https://source.unsplash.com/400x300/?wedding,romantic" alt="Foto 2">
    <img src="https://source.unsplash.com/400x300/?nature,love" alt="Foto 3">
  </div>
</section>

<section>
  <h2>Detalles del Evento</h2>
  <div class="info">
    <p><strong>Fecha:</strong></p>
    <div class="calendar">Viernes 21 de Junio</div>
    <p><strong>Hora:</strong> Por decidir</p>
    <p><strong>Lugar:</strong> Nuestra casa (la dirección se compartirá personalmente)</p>
    <p><strong>Comida:</strong> Tradicional nicaragüense 🇳🇮</p>
    <p><strong>Vestimenta:</strong> Hombres: cotona | Mujeres: Huipil Nicaragüense</p>
  </div>
</section>

<section>
  <h2>Regalos</h2>
  <p class="info">Tu presencia es nuestro mayor regalo, pero si deseas traernos algo, será recibido con mucho cariño. Algo útil, simbólico o hecho por ti ❤️</p>
</section>

<section>
  <h2>Confirmación de Asistencia</h2>
  <form class="formulario" action="https://formsubmit.co/tu-correo@gmail.com" method="POST">
    <input type="text" name="nombre" placeholder="Tu nombre" required>
    <input type="email" name="correo" placeholder="Tu correo" required>
    <textarea name="mensaje" placeholder="¿Nos quieres decir algo?" rows="4"></textarea>
    <button type="submit">Confirmar Asistencia</button>
    <input type="hidden" name="_captcha" value="false">
    <input type="hidden" name="_next" value="https://tuusuario.github.io/boda-invitacion/gracias.html">
  </form>
</section>

<footer>
  <p>Con cariño, Xavier & Mariangeles · 2025</p>
</footer>

</body>
</html>
