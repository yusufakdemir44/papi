<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8">
  <title>Papatyalar Açıyor</title>
  <style>
    body {
      margin: 0;
      background-color: #000;
      overflow: hidden;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      height: 100vh;
      font-family: 'Segoe UI', sans-serif;
    }

    #touchButton {
      padding: 12px 30px;
      font-size: 18px;
      background: #fff;
      border: none;
      border-radius: 20px;
      cursor: pointer;
      margin-bottom: 20px;
      box-shadow: 0 0 15px rgba(255,255,255,0.2);
      transition: background 0.3s;
      z-index: 10;
    }

    #touchButton:hover {
      background: #f0f0f0;
    }

    svg {
      width: 400px;
      height: auto;
    }

    .flower {
      opacity: 0;
      transform: scale(0.4);
      transform-origin: center;
      transition: all 0.8s ease-out;
    }

    .flower.show {
      opacity: 1;
      transform: scale(1);
    }
  </style>
</head>
<body>

  <button id="touchButton">🌼 Dokun</button>

  <svg viewBox="0 0 200 250">
    <!-- Ağaç gövdesi -->
    <line x1="100" y1="250" x2="100" y2="180" stroke="#5a381e" stroke-width="6" />

    <!-- Dallar -->
    <line x1="100" y1="200" x2="60" y2="150" stroke="#5a381e" stroke-width="2" />
    <line x1="100" y1="190" x2="140" y2="140" stroke="#5a381e" stroke-width="2" />
    <line x1="100" y1="185" x2="80" y2="120" stroke="#5a381e" stroke-width="1.5" />
    <line x1="100" y1="185" x2="120" y2="110" stroke="#5a381e" stroke-width="1.5" />
    <line x1="100" y1="180" x2="100" y2="90" stroke="#5a381e" stroke-width="1.2" />

    <!-- Papatyalar -->
    <g class="flower" id="f1">
      <circle cx="60" cy="150" r="6" fill="white" />
      <circle cx="60" cy="150" r="2" fill="yellow" />
    </g>
    <g class="flower" id="f2">
      <circle cx="140" cy="140" r="6" fill="white" />
      <circle cx="140" cy="140" r="2" fill="yellow" />
    </g>
    <g class="flower" id="f3">
      <circle cx="80" cy="120" r="5.5" fill="white" />
      <circle cx="80" cy="120" r="2" fill="yellow" />
    </g>
    <g class="flower" id="f4">
      <circle cx="120" cy="110" r="5.5" fill="white" />
      <circle cx="120" cy="110" r="2" fill="yellow" />
    </g>
    <g class="flower" id="f5">
      <circle cx="100" cy="90" r="5.5" fill="white" />
      <circle cx="100" cy="90" r="2" fill="yellow" />
    </g>
    <g class="flower" id="f6">
      <circle cx="110" cy="95" r="4.5" fill="white" />
      <circle cx="110" cy="95" r="2" fill="yellow" />
    </g>
    <g class="flower" id="f7">
      <circle cx="90" cy="100" r="4.5" fill="white" />
      <circle cx="90" cy="100" r="2" fill="yellow" />
    </g>
    <g class="flower" id="f8">
      <circle cx="105" cy="125" r="5" fill="white" />
      <circle cx="105" cy="125" r="2" fill="yellow" />
    </g>
    <g class="flower" id="f9">
      <circle cx="95" cy="135" r="5" fill="white" />
      <circle cx="95" cy="135" r="2" fill="yellow" />
    </g>
    <g class="flower" id="f10">
      <circle cx="115" cy="145" r="5" fill="white" />
      <circle cx="115" cy="145" r="2" fill="yellow" />
    </g>
  </svg>

  <script>
    const button = document.getElementById("touchButton");
    const flowers = document.querySelectorAll(".flower");

    button.addEventListener("click", () => {
      button.style.display = "none";

      flowers.forEach((flower, index) => {
        setTimeout(() => {
          flower.classList.add("show");
        }, index * 300);
      });
    });
  </script>
</body>
</html>
