# www.ncredmargem.com.br
<!DOCTYPE html>
<html lang="pt-br">
  <head>
    <meta charset="UTF-8">
    <title>Calculadora de Empréstimo para Aposentados</title>
    <style>
      #header {
        font-size: 4em; /* altere o tamanho conforme necessário */
  font-weight: bold;
  text-align: center;
  }
  #subheader {
    font-size: 2em; /* altere o tamanho conforme necessário */
  font-style: italic;
  text-align: center;
  }
      body {
        background-color: #EFEFEF;
        font-family: Arial, sans-serif;
      }
      h1 {
        color: #333333;
        text-align: center;
        margin-top: 30px;
      }
      form {
        width: 300px;
        margin: 0 auto;
        padding: 20px;
        border-radius: 10px;
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
        background-color: #F5F5F5;
      }
      label {
        display: block;
        margin-bottom: 10px;
      }
      input[type="number"] {
        width: 100%;
        padding: 10px;
        border: 1px solid #CCCCCC;
        border-radius: 5px;
        box-sizing: border-box;
      }
      input[type="submit"] {
        width: 100%;
        padding: 10px;
        background-color: #4CAF50;
        color: #FFFFFF;
        border: none;
        border-radius: 5px;
        box-sizing: border-box;
        cursor: pointer;
      }
      input[type="submit"]:hover {
        background-color: #3E8E41;
      }
      .resultado {
        font-size: 20px;
        font-weight: bold;
        text-align: center;
        margin-top: 20px;
      }
      #whatsapp {
  display: block;
  margin: 0 auto;
  background-color: #4CAF50;
  color: #FFFFFF;
  font-family: Arial, sans-serif;
  font-weight: bold;
  font-size: 16px;
  border: none;
  border-radius: 5px;
  padding: 10px;
  cursor: pointer;
}

#whatsapp:hover {
  background-color: #3E8E41;
}

  display: block;
  margin: 0 auto;
}
/* altera a cor de fundo da caixa de mensagem do WhatsApp */
a.whatsapp-message {
  background-color: #4CAF50;
}


    </style>
  </head>
  <body>
    <div id="header">
      <span style="color: blue; display:inline-block;">N</span>
  <span style="color: orange; display:inline-block;">CRED</span>
    </div>
    <div id="subheader">Soluções Financeiras</div>
  
    <h1>Calculadora de Empréstimo para Aposentados</h1>
    <form>
      <label for="margem">Margem:</label>
      <input type="number" id="margem" name="margem" required>
      <input type="submit" value="Calcular">
      <div class="resultado" id="resultado"></div>
    </form>
    <button id="whatsapp">Envie os Documentos</button>


    <script>
      const whatsappButton = document.querySelector('#whatsapp');

whatsappButton.addEventListener('click', function() {
  const telefone = '17988034077';
  const mensagem = 'Olá, gostaria enviar o documento dessa cliente ';
  const url = `https://wa.me/${telefone}/?text=${encodeURIComponent(mensagem)}`;
  window.location.href = url;
});

      const form = document.querySelector('form');
      const resultado = document.querySelector('#resultado');

      form.addEventListener('submit', function(event) {
        event.preventDefault();
        const margem = parseFloat(document.querySelector('#margem').value);
        const valor_emprestimo = (margem / 0.02396).toFixed(2);
        resultado.textContent = `Valor disponivel para empréstimo de R$ ${valor_emprestimo}`;
      });
    </script>
  </body>
</html>
