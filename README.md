<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Milieu Simulator</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(135deg, #f0f4f8, #d9e2ec);
      color: #102a43;
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 2rem;
    }

    h1 {
      font-size: 2.5rem;
      margin-bottom: 1rem;
    }

    .container {
      background-color: white;
      padding: 2rem;
      border-radius: 16px;
      box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
      max-width: 600px;
      width: 100%;
    }

    select, button {
      width: 100%;
      padding: 1rem;
      font-size: 1rem;
      margin: 1rem 0;
      border-radius: 12px;
      border: 1px solid #bcccdc;
    }

    button {
      background-color: #2f855a;
      color: white;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }

    button:hover {
      background-color: #276749;
    }

    .resultaat {
      margin-top: 1.5rem;
      padding: 1rem;
      background-color: #edf2f7;
      border-left: 5px solid #2f855a;
      border-radius: 8px;
    }
  </style>
</head>

<body>
  <h1>🌿 Milieu Simulator</h1>
  <div class="container">
    <label for="actie">Kies een actie:</label>
    <select id="actie">
      <option value="fiets">Fiets gebruiken i.p.v. auto</option>
      <option value="vlees">Minder vlees eten</option>
      <option value="recycle">Meer recycleren</option>
      <option value="water">Water besparen</option>
      <option value="verlichting">Ledverlichting gebruiken</option>
    </select>
    <button onclick="toonEffect()">Bekijk effect 🌎</button>
    <div id="resultaat" class="resultaat"></div>
  </div>

  <script>
    function toonEffect() {
      const actie = document.getElementById('actie').value;
      const resultaat = document.getElementById('resultaat');

      const effecten = {
        fiets: 'Je vermindert CO₂-uitstoot en verbetert je gezondheid! 🚴‍♂️',
        vlees: 'Minder vlees eten helpt bij het verminderen van methaanuitstoot. 🌱',
        recycle: 'Recycleren bespaart energie en grondstoffen. ♻️',
        water: 'Water besparen is goed voor het milieu én je portemonnee. 💧',
        verlichting: 'Ledlampen verbruiken minder energie en gaan langer mee. 💡'
      };

      resultaat.textContent = effecten[actie];
    }
  </script>
</body>
