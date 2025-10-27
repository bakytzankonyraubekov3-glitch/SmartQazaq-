indexhtml
<!DOCTYPE html>
<html lang="kk">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>SmartQazaq 🇰🇿</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      text-align: center;
      background: linear-gradient(to bottom, #e0f2ff, #ffffff);
    }
    header {
      background-color: #007acc;
      color: white;
      padding: 20px;
      font-size: 28px;
      font-weight: bold;
      box-shadow: 0 2px 6px rgba(0,0,0,0.2);
    }
    main { padding: 40px 20px; }
    .buttons { margin-bottom: 30px; }
    button {
      background-color: #007acc;
      color: white;
      border: none;
      padding: 14px 28px;
      margin: 12px;
      border-radius: 12px;
      font-size: 18px;
      cursor: pointer;
      transition: 0.3s;
    }
    button:hover { background-color: #005fa3; }
    section { margin-top: 60px; }
    footer {
      background-color: #f2f2f2;
      padding: 15px;
      font-size: 14px;
      color: #555;
    }
  </style>
</head>
<body>
  <header>🇰🇿 SmartQazaq</header>
  <main>
    <h2>Балабақшадан бастап тіл мен дерек тазалығына дейін</h2>
    <p>Таза код. Таза әріп. Таза карта.</p>

    <div class="buttons">
      <button onclick="scrollToSection('map')">🗺️ Интерактивті карта</button>
      <button onclick="scrollToSection('taza')">✍️ Таза Әріп</button>
    </div>

    <section id="map">
      <h3>Интерактивті карта (сыналық нұсқа)</h3>
      <iframe src="https://www.openstreetmap.org/export/embed.html"
        width="90%" height="400" style="border:1px solid #ccc;"></iframe>
    </section>

    <section id="taza">
      <h3>Таза Әріп түрлендіргіш</h3>
      <textarea id="inputText" rows="4" cols="60" placeholder="Мәтінді осында енгізіңіз..."></textarea><br>
      <button onclick="convertText()">Түрлендіру</button>
      <p id="result" style="margin-top:20px; font-weight:bold;"></p>
    </section>
  </main>

  <footer>
    © 2025 SmartQazaq.kz | Ұлттық цифрлық бастама 🇰🇿
  </footer>

  <script>
    function scrollToSection(id) {
      document.getElementById(id).scrollIntoView({behavior: "smooth"});
    }

    function convertText() {
      const text = document.getElementById('inputText').value;
      const converted = text
        .replace(/қ/g, 'q')
        .replace(/ғ/g, 'ǵ')
        .replace(/ң/g, 'ń')
        .replace(/ө/g, 'ó')
        .replace(/ү/g, 'ú')
        .replace(/і/g, 'i');
      document.getElementById('result').innerText = converted;
    }
  </script>
</body>
</html>
