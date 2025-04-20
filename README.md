<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Texto Acessível</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      padding: 20px;
    }

    #conteudo {
      color: black;
      background-color: white;
      font-size: 18px;
    }

    button {
      margin: 5px;
      padding: 10px;
      font-size: 16px;
    }
  </style>
</head>
<body>

  <h1>Melhorando a Acessibilidade</h1>
  <div id="conteudo">
    Este é um exemplo de texto cujo tamanho e cor podem ser alterados para melhorar a acessibilidade.
  </div>

  <!-- Botão para mudar cor do texto -->
  <button onclick="mudarCorTexto()">Alterar Cor do Texto</button>

  <script>
    const cores = [
      { texto: 'black', fundo: 'white' },
      { texto: 'white', fundo: 'black' },
      { texto: '#004466', fundo: '#ffffff' }, // azul escuro
      { texto: '#2e2e2e', fundo: '#f5f5f5' }, // cinza escuro no fundo claro
    ];

    let corAtual = 0;

    function mudarCorTexto() {
      corAtual = (corAtual + 1) % cores.length;
      const conteudo = document.getElementById("conteudo");
      conteudo.style.color = cores[corAtual].texto;
      conteudo.style.backgroundColor = cores[corAtual].fundo;
    }
  </script>

</body>
</html>

