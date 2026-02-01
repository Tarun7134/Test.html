<!DOCTYPE html>  
<html>  
<head>  
  <title>Valentine 💖</title>  
  
  <style>  
    body {  
      text-align: center;  
      font-family: Arial, sans-serif;  
      background: #ffe6ea;  
      height: 100vh;  
      overflow: hidden;  
    }  
  
    button {  
      padding: 15px 30px;  
      font-size: 18px;  
      margin: 20px;  
      cursor: pointer;  
    }  
  
    /* ❤️ HEART */  
    .heart {  
      position: absolute;  
      bottom: 50px;  
      left: 50%;  
      width: 20px;  
      height: 20px;  
      background: red;  
      transform: rotate(45deg);  
      animation: fly 2s linear forwards;  
    }  
  
    .heart::before,  
    .heart::after {  
      content: "";  
      width: 20px;  
      height: 20px;  
      background: red;  
      border-radius: 50%;  
      position: absolute;  
    }  
  
    .heart::before {  
      top: -10px;  
      left: 0;  
    }  
  
    .heart::after {  
      left: -10px;  
      top: 0;  
    }  
  
    @keyframes fly {  
      0% { opacity: 1; }  
      100% {  
        transform: translateY(-300px) rotate(45deg);  
        opacity: 0;  
      }  
    }  
  </style>  
</head>  
  
<body>  
  
  <h1 id="text">Will you be my Valentine? 💘</h1>  
  
  <button onclick="yesClick()">Yes 💕</button>  
  
  <script>  
    function yesClick() {  
      document.getElementById("text").innerText =  
        "Yayyy 💖 You said YES!";  
  
      // create hearts  
      for (let i = 0; i < 15; i++) {  
        let heart = document.createElement("div");  
        heart.className = "heart";  
        heart.style.left = Math.random() * window.innerWidth + "px";  
        document.body.appendChild(heart);  
  
        setTimeout(() => {  
          heart.remove();  
        }, 2000);  
      }  
    }  
  </script>  
  
</body>  
</html>  
