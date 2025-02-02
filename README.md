<!DOCTYPE html>
<html lang="it">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>San Valentino - Una Richiesta Speciale</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: linear-gradient(135deg, #f06292, #ba68c8);
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
      color: #fff;
      text-align: center;
    }
    h1 {
      font-size: 2.5em;
      margin-bottom: 0.5em;
    }
    .btn-container {
      display: flex;
      gap: 20px;
      margin-bottom: 1em;
    }
    button {
      background: #fff;
      color: #f06292;
      border: none;
      padding: 1em 2em;
      font-size: 1.2em;
      border-radius: 5px;
      cursor: pointer;
      transition: background 0.3s ease, transform 0.3s ease;
    }
    button:hover {
      background: #f8bbd0;
    }
    .message {
      font-size: 1.5em;
      display: none;
    }
  </style>
</head>
<body>
  <h1>Vuoi essere il mio San Valentino?</h1>
  <div class="btn-container">
    <button id="yesBtn">Si</button>
    <button id="noBtn">No</button>
  </div>
  <div class="message" id="message"></div>
  
  <script>
    const yesBtn = document.getElementById("yesBtn");
    const noBtn = document.getElementById("noBtn");
    const messageDiv = document.getElementById("message");

    yesBtn.addEventListener("click", function() {
      messageDiv.textContent = "ehehehe lo sabía que querías amorcita🌙♥️";
      messageDiv.style.display = "block";
    });

    noBtn.addEventListener("click", function() {
      messageDiv.textContent = "perché🥺?";
      messageDiv.style.display = "block";
    });

    // Fun feature: il pulsante "No" si sposta quando ci si passa sopra
    noBtn.addEventListener("mouseover", function() {
      // Genera un movimento casuale per il pulsante "No"
      const randomX = Math.floor(Math.random() * 300) - 150; // sposta in entrambe le direzioni
      const randomY = Math.floor(Math.random() * 200) - 100;
      noBtn.style.transform = `translate(${randomX}px, ${randomY}px)`;
    });
  </script>
</body>
</html>
