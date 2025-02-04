<!doctype html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Pregunta</title>
    <style>
      body {
        font-family: Arial, sans-serif;
        background: blue;
        text-align: center;
        margin-top: 50px;
        transition: background 0.5s ease;
      }
      #pregunta {
        font-size: 24px;
      }
      .boton {
        font-size: 20px;
        padding: 10px;
        margin: 10px;
        cursor: pointer;
        transition: all 0.3s ease;
      }
      #gifContainer {
        margin-top: 20px;
      }
    </style>
  </head>
  <body>
    <h1 id="pregunta">¿Quieres ser mi San Valentín (casarnos)?</h1>
    <button id="si" class="boton" onclick="respuestaSi()">Sí</button>
    <button id="no" class="boton" onclick="respuestaNo()">No</button>
    <div id="gifContainer"></div>

    <script>
      let mensajes = [
        "¿Estás segura?",
        "¿Pero por qué no :c?",
        "¿Ni un poquito?",
        "¡Por favor di que sí!",
        "Por favor amor :c.",
        "Porque eres tan mala :(",
        "Pofisss", "Te amoooo, dale a sí pofis🥺🥺🥺",
        "Pofissssss😭😭😭", "Sabes, deja así, presiona no :c",
        "Porqueeee le disteee", "😭😭😭", "Un elefante se balanceaba sobre la...",
        "tela de una araña", "Pofisss confía en mí, dale a sí",
        "¿No confías en mí?🥺🥺😭", "Jjjj no vas a poder presionarlo más",
        "¿En serio no quieres?", "Si llegaste hasta acá manda foto😭😭😭",
      ];
      let index = 0;
      let sizeSi = 20;
      let sizeNo = 20;

      function respuestaSi() {
        document.body.style.background = "red";
        document.body.style.backgroundImage = "url('https://www.transparenttextures.com/patterns/hearts.png')";
        document.getElementById("pregunta").innerText = "¡Sí! Te amoooooo 💖💕💖😘😘🥰 Nos casamos en 5 años 💍💍💍💍";
        document.getElementById("si").remove();
        document.getElementById("no").remove();
        document.getElementById("gifContainer").innerHTML =
          '<img src="https://i.pinimg.com/originals/b6/d1/8a/b6d18a4cd66953302c5b1420ca9947c5.gif" alt="GIF final" style="width: 150px;">';
      }

      function respuestaNo() {
        if (index < mensajes.length) {
          document.getElementById("pregunta").innerText = mensajes[index];
          index++;
          sizeSi += 10;
          sizeNo -= 2;
          document.getElementById("si").style.fontSize = sizeSi + "px";
          document.getElementById("no").style.fontSize = sizeNo + "px";

          if (index === 6) {
            document.getElementById("gifContainer").innerHTML =
              '<img src="https://i.pinimg.com/originals/d5/79/aa/d579aa6558775ef99a765fab7b6088e0.gif" alt="GIF 1">';
          }

          if (index === 13) {
            document.getElementById("gifContainer").innerHTML =
              '<img src="https://i.pinimg.com/originals/ec/25/b2/ec25b2a6b3680b1e262799fac04bdd46.gif" alt="GIF 2">';
          }
        } else {
          alert("😭😭😭😭😭");
        }
      }
    </script>
  </body>
</html>
