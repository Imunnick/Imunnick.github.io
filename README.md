<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>KMA Store - Universo</title>
  <link href="https://fonts.googleapis.com/css2?family=Urbanist:wght@300;700;900&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    body {
      font-family: 'Urbanist', sans-serif;
      background: black;
      color: white;
      overflow: hidden;
    }
    header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 30px 60px;
      z-index: 10;
      position: relative;
    }
    header h1 {
      font-weight: 900;
      font-size: 32px;
    }
    nav a {
      margin-left: 32px;
      text-decoration: none;
      color: white;
      font-weight: 400;
      font-size: 14px;
      letter-spacing: 1px;
      transition: color 0.3s ease;
    }
    nav a:hover {
      color: #999;
    }
    .hero {
      position: relative;
      width: 100vw;
      height: 100vh;
      background: url('/mnt/data/Universo KMA_ Estilo e Futuro.png') no-repeat center center/cover;
      display: flex;
      justify-content: center;
      align-items: center;
      text-align: center;
      opacity: 0;
      animation: fadeIn 3s ease-in forwards;
    }
    .hero::after {
      content: '';
      position: absolute;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.7);
      top: 0;
      left: 0;
      z-index: 1;
    }
    .hero-content {
      position: relative;
      z-index: 2;
    }
    .hero-content h2 {
      font-size: 48px;
      font-weight: 900;
      margin-bottom: 24px;
    }
    .hero-content button {
      background: transparent;
      border: 2px solid white;
      color: white;
      padding: 14px 40px;
      font-size: 16px;
      font-weight: bold;
      border-radius: 30px;
      cursor: pointer;
      transition: all 0.4s ease;
    }
    .hero-content button:hover {
      background: white;
      color: black;
    }

    @keyframes fadeIn {
      0% {
        opacity: 0;
        transform: scale(1.05);
      }
      100% {
        opacity: 1;
        transform: scale(1);
      }
    }

    /* Transição ao clicar */
    .universe-enter {
      position: fixed;
      top: 0;
      left: 0;
      width: 100vw;
      height: 100vh;
      background: black;
      z-index: 999;
      display: flex;
      justify-content: center;
      align-items: center;
      animation: portalEnter 2.2s ease forwards;
    }

    .universe-enter span {
      color: white;
      font-size: 24px;
      opacity: 0;
      animation: textBlink 1s ease infinite;
    }

    @keyframes portalEnter {
      0% {
        opacity: 0;
        transform: scale(1);
      }
      50% {
        opacity: 1;
        transform: scale(1.5);
      }
      100% {
        opacity: 1;
        transform: scale(1);
      }
    }

    @keyframes textBlink {
      0%, 100% {
        opacity: 0;
      }
      50% {
        opacity: 1;
      }
    }
  </style>
</head>
<body>
  <header>
    <h1>KMA</h1>
    <nav>
      <a href="#">HISTÓRIA</a>
      <a href="#">LINHAS EXCLUSIVAS</a>
      <a href="#">STREETWEAR</a>
      <a href="#">2000's</a>
      <a href="#">EVENTOS</a>
      <a href="#">INFO</a>
    </nav>
  </header>

  <section class="hero">
    <div class="hero-content">
      <h2>DOMINAMOS O DRIP. <br>CRIAMOS O FUTURO.</h2>
      <button onclick="entrarUniverso()">ENTRAR NO UNIVERSO KMA</button>
    </div>
  </section>

  <div id="portal" style="display: none;" class="universe-enter">
    <span>CARREGANDO UNIVERSO KMA...</span>
  </div>

  <script>
    function entrarUniverso() {
      const portal = document.getElementById('portal');
      portal.style.display = 'flex';
      setTimeout(() => {
        window.location.href = '/home.html'; // Redireciona para o site real
      }, 2200);
    }
  </script>
</body>
</html>

