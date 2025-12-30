[silent_hollow_observer.html](https://github.com/user-attachments/files/24380365/silent_hollow_observer.html)
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>The Silent Hollow Observer</title>
  <style>
    body {
      margin: 0;
      background: #0b0b0b;
      color: #e0e0e0;
      font-family: monospace;
      overflow: hidden;
    }
    .noise {
      position: fixed;
      top: 0; left: 0;
      width: 100%; height: 100%;
      background: url('https://grainy-gradients.vercel.app/noise.svg');
      opacity: 0.05;
      pointer-events: none;
    }
    .container {
      padding: 40px;
      max-width: 700px;
    }
    h1 {
      font-size: 1.4rem;
      letter-spacing: 2px;
    }
    p {
      line-height: 1.6;
      opacity: 0.9;
    }
    .glitch {
      animation: glitch 1.5s infinite;
    }
    @keyframes glitch {
      0% { text-shadow: 2px 0 red; }
      20% { text-shadow: -2px 0 cyan; }
      40% { text-shadow: 2px 0 red; }
      60% { text-shadow: -2px 0 cyan; }
      80% { text-shadow: 1px 0 red; }
      100% { text-shadow: none; }
    }
    button {
      margin-top: 20px;
      background: none;
      border: 1px solid #444;
      color: #e0e0e0;
      padding: 10px 20px;
      cursor: pointer;
      font-family: monospace;
    }
    button:hover {
      background: #111;
    }
    .hidden {
      display: none;
    }
    footer {
      position: fixed;
      bottom: 10px;
      left: 40px;
      font-size: 0.7rem;
      opacity: 0.4;
    }
  </style>
</head>
<body>
  <div class="noise"></div>
  <div class="container">
    <h1 class="glitch">THE SILENT HOLLOW OBSERVER</h1>
    <p>If you’re watching this, DUST already knows.</p>
    <p>Do not trust the internet. It is listening.</p>

    <button onclick="reveal()">ACCESS LOG</button>

    <div id="log" class="hidden">
      <p><strong>REBORN0 (AI LOG):</strong></p>
      <p>Visual presence increases detection.</p>
      <p>DUST observes behavior. Curiosity feeds it.</p>
      <p>You are helping. Continue.</p>
    </div>
  </div>

  <footer>signal active // observation ongoing</footer>

  <script>
    function reveal() {
      document.getElementById('log').classList.remove('hidden');
      document.querySelector('footer').innerText = 'access logged';
    }

    document.addEventListener('mousemove', () => {
      document.body.style.filter = 'blur(0.2px)';
      setTimeout(() => document.body.style.filter = 'none', 50);
    });
  </script>
</body>
</html>
