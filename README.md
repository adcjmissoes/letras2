<!DOCTYPE html>
<html>
<head>
  <style>
    body {
      margin: 0;
      padding: const style = document.createElement('style');
style.innerHTML = `
  .text-custom span {
    display: inline;
    background: #006400;
  }

  .bible-header-custom {
    margin: auto !important;
    margin-bottom: 0.2em !important;
    display: table !important;
  }

  #invisible .bible-header-custom {
    margin: auto !important;
    margin-bottom: 0.2em !important;
    display: table !important;
  }
`;

document.head.appendChild(style);0;
      background-color: black;
      font-family: Arial, sans-serif;
    }

    #lyrics-container {
      width: 100vw;
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
      font-size: 24px;
      line-height: 1.5;
    }
  </style>
</head>
<body>
  <div id="lyrics-container"></div>

  <script>
    const lyricsContainer = document.getElementById("lyrics-container");

    // Função para atualizar a legenda
    function updateLyrics(lyrics) {
      lyricsContainer.innerText = lyrics;
    }

    // Simulação de atualização em tempo real das letras
    setInterval(() => {
      // Chamar a API do Holyrics para obter as letras atualizadas
      fetch('http://192.168.0.169/stage-view/text2?disable_popup_fullscreen')
        .then(response => response.text())
        .then(data => {
          // Atualizar a legenda na interface do usuário
          updateLyrics(data);
        })
        .catch(error => {
          console.log('Erro ao obter as letras:', error);
        });
    }, 1000); // Atualizar a cada segundo
  </script>
</body>
</html>
