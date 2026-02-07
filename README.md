# valentine-<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Valentine Proposal</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      background: radial-gradient(circle at top, #ff4d6d, #590d22);
      display: flex;
      justify-content: center;
      align-items: center;
      font-family: "Segoe UI", sans-serif;
      color: white;
    }

    .box {
      background: rgba(0,0,0,0.3);
      padding: 50px;
      border-radius: 20px;
      text-align: center;
      max-width: 400px;
      backdrop-filter: blur(8px);
      box-shadow: 0 0 30px rgba(255,255,255,0.2);
    }

    h1 {
      margin-bottom: 20px;
      font-size: 30px;
      color: #ffd6e0;
    }

    #type {
      min-height: 60px;
      font-size: 18px;
      margin-bottom: 30px;
    }

    button {
      padding: 12px 28px;
      border: none;
      border-radius: 30px;
      font-size: 16px;
      cursor: pointer;
      margin: 8px;
    }

    .yes {
      background: #ffb703;
      color: #222;
    }

    .no {
      background: transparent;
      color: white;
      border: 2px solid white;
    }

    #reply {
      margin-top: 25px;
      font-size: 22px;
      color: #ffccd5;
      display: none;
    }
  </style>
</head>
<body>
  <div class="box">
    <h1>Hey You 💌</h1>
    <div id="type"></div>
    <button class="yes" onclick="accept()">Yes 💘</button>
    <button class="no" onclick="reject()">No 😅</button>
    <div id="reply"></div>
  </div>

  <script>
    const text = "I've been wanting to ask you something important for a while now... Will you be my Valentine? 💖";
    let i = 0;
    function typeEffect() {
      if (i < text.length) {
        document.getElementById("type").innerHTML += text.charAt(i);
        i++;
        setTimeout(typeEffect, 40);
      }
    }
    typeEffect();

    function accept() {
      const r = document.getElementById("reply");
      r.style.display = "block";
      r.innerHTML = "You said YES?! 😍 I’m the happiest person right now! 💕";
    }

    function reject() {
      const r = document.getElementById("reply");
      r.style.display = "block";
      r.innerHTML = "Ouch 😅 But thanks for being honest. Still wishing you love and smiles 💗";
    }
  </script>
</body>
</html>
