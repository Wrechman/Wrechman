<Doctype.html>
<html>
<head>
  <title>My Links</title>
  <style>
    body {
      font-family: 'Courier New', monospace;
      margin: 0;
      padding: 0;
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      background-color: #000000;
      overflow: hidden;
    }
    
    .container {
      width: 100%;
      height: 100vh;
      background-color: rgba(0, 0, 0, 0.7);
      border-radius: 8px;
      box-shadow: 0 2px 4px rgba(0, 0, 0, 0.7);
      position: relative;
    }
    
    h1, h2, a {
      color: #00ff00;
      text-align: center;
      margin: 0;
      letter-spacing: 2px;
      font-weight: bold;
      padding-top: 20px;
      text-shadow: 0 0 5px #00ff00;
      animation: glitch 0.5s infinite;
    }
    
    ul {
      list-style-type: none;
      padding: 0;
      margin-top: 30px;
      text-align: center;
    }
    
    li {
      margin-bottom: 20px;
      position: relative;
    }
    
    a {
      display: inline-block;
      text-decoration: none;
      padding: 10px 20px;
      border-radius: 4px;
      transition: color 0.3s ease;
      position: relative;
      z-index: 1;
    }
    
    a:hover {
      color: #00cc00;
    }
    
    .digital-rain {
      position: absolute;
      width: 100%;
      height: 100%;
      background: black;
      overflow: hidden;
      z-index: -1;
    }
    
    .digit {
      position: absolute;
      font-size: 16px;
      color: #00ff00;
      animation: digitalRain 10s infinite linear;
    }
    
    .arrow {
      position: absolute;
      width: 20px;
      height: 20px;
      transform: rotate(-45deg); /* Updated rotation angle */
      border-bottom: 2px solid #00ff00;
      border-right: 2px solid #00ff00;
      animation: arrowSwoop 1s infinite;
      z-index: 0;
    }
    
    @keyframes digitalRain {
      0% {
        transform: translateY(-10vh);
      }
      100% {
        transform: translateY(110vh);
      }
    }
    
    @keyframes glitch {
      0% {
        transform: translate(0);
        opacity: 1;
      }
      25% {
        transform: translate(-2px, 2px);
        opacity: 0.9;
      }
      50% {
        transform: translate(-2px, -2px);
        opacity: 0.8;
      }
      75% {
        transform: translate(2px, -2px);
        opacity: 0.9;
      }
      100% {
        transform: translate(0);
        opacity: 1;
      }
    }
    
    @keyframes arrowSwoop {
      0% {
        transform: translateY(-10px);
        opacity: 0;
      }
      50% {
        transform: translateY(5px);
        opacity: 1;
      }
      100% {
        transform: translateY(0);
        opacity: 0;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>WRECHMAN</h1>
    <h2>My Links</h2>
    <ul>
      <li>
        <a href="https://www.youtube.com/channel/UCoBqZ-Z-wdJifnfe7LzMyfw">YouTube</a>
        <span class="arrow" style="left: calc(50% - 10px); top: 30px;"></span>
      </li>
      <li>
        <a href="https://www.twitch.tv/wrechman_">Twitch</a>
        <span class="arrow" style="left: calc(50% - 10px); top: 30px;"></span>
      </li>
      <li>
        <a href="https://www.mariokart64.com/mk64/players/3342">My MK64 Rankings</a>
        <span class="arrow" style="left: calc(50% - 10px); top: 30px;"></span>
      </li>
    </ul>
    <div class="digital-rain">
      
      <script>
        const characters = "0123456789";
        const digitCount = 100;

        for (let i = 0; i < digitCount; i++) {
          const digit = document.createElement('span');
          digit.textContent = characters.charAt(Math.floor(Math.random() * characters.length));
          digit.classList.add('digit');
          digit.style.top = `${Math.floor(Math.random() * 100)}vh`;
          digit.style.left = `${Math.floor(Math.random() * 100)}vw`;
          document.querySelector('.digital-rain').appendChild(digit);
        }
      </script>
    </div>
  </div>
</body>
</html>
