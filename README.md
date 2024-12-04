<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>LOCO CLUB</title>
  <style>
    /* Stile generale */
    body {
      margin: 0;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      background: #000000;
      font-family: 'Arial', sans-serif;
      color: white;
    }

    .container {
      text-align: center;
      padding: 20px;
      border-radius: 10px;
      background: rgba(0, 0, 0, 0.85);
      width: 90%; /* Ottimizzato per dispositivi mobili */
      max-width: 400px;
      position: relative;
    }

    /* Scritta e diamanti in alto */
    .header {
      position: relative;
      margin-bottom: 30px;
    }

    .title {
      font-size: 36px;
      color: #ee82ee;
      text-shadow: 0 0 10px #ee82ee, 0 0 20px #ba55d3, 0 0 30px #ff00ff;
      margin: 0;
    }

    .diamond {
      position: absolute;
      top: 10px;
      width: 60px;
      height: 60px;
      background: linear-gradient(135deg, #8a2be2, #ee82ee);
      clip-path: polygon(50% 0%, 100% 50%, 50% 100%, 0% 50%);
      box-shadow: 0 0 10px rgba(138, 43, 226, 0.7);
    }

    .diamond.left {
      left: -80px;
    }

    .diamond.right {
      right: -80px;
    }

    /* Stile del form */
    form {
      display: flex;
      flex-direction: column;
      gap: 15px;
    }

    label {
      font-size: 16px;
      text-align: left;
    }

    input {
      padding: 12px;
      font-size: 16px;
      border: none;
      border-radius: 5px;
      outline: none;
      background: rgba(255, 255, 255, 0.1);
      color: white;
      box-shadow: 0 0 10px rgba(255, 255, 255, 0.1);
    }

    input::placeholder {
      color: #cccccc;
    }

    /* Pulsante viola */
    button {
      padding: 12px;
      font-size: 18px;
      color: white;
      background: #8a2be2;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      transition: all 0.3s ease;
      text-transform: uppercase;
      font-weight: bold;
      box-shadow: 0 0 10px #8a2be2, 0 0 20px #ee82ee;
    }

    button:hover {
      background: #ee82ee;
      box-shadow: 0 0 15px #8a2be2, 0 0 20px #ba55d3;
    }
  </style>
</head>
<body>
  <div class="container">
    <!-- Scritta LOCO CLUB con diamanti -->
    <div class="header">
      <div class="diamond left"></div>
      <h1 class="title">LOCO CLUB</h1>
      <div class="diamond right"></div>
    </div>

    <!-- Form -->
    <form id="userForm">
      <label for="name">Nome:</label>
      <input type="text" id="name" name="name" placeholder="Inserisci il tuo nome" required>

      <label for="surname">Cognome:</label>
      <input type="text" id="surname" name="surname" placeholder="Inserisci il tuo cognome" required>

      <label for="email">Email:</label>
      <input type="email" id="email" name="email" placeholder="Inserisci la tua email" required>

      <button type="submit">Invia</button>
    </form>
  </div>

  <script>
    document.getElementById('userForm').addEventListener('submit', async (e) => {
      e.preventDefault();
      const name = document.getElementById('name').value;
      const surname = document.getElementById('surname').value;
      const email = document.getElementById('email').value;

      // Simulazione invio dati
      console.log({ name, surname, email });
      alert(`Email inviata con successo a ${name} ${surname}!`);
    });
  </script>
</body>
</html>