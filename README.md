# Teste-Para-se-Tornar-Staff
Teste Kamomedai 🔵🦅
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Formulário para Staff</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f4f6fa;
      padding: 20px;
      max-width: 800px;
      margin: auto;
    }
    h1, p {
      text-align: center;
    }
    label {
      display: block;
      margin: 15px 0 5px;
      font-weight: bold;
    }
    input[type="text"],
    input[type="email"],
    textarea {
      width: 100%;
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 6px;
      resize: vertical;
    }
    button {
      display: block;
      width: 100%;
      padding: 15px;
      font-size: 16px;
      background-color: #007BFF;
      color: white;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      margin-top: 30px;
    }
    button:hover {
      background-color: #0056b3;
    }
    .logo {
      text-align: center;
      margin-bottom: 20px;
    }
    .logo img {
      max-width: 100%;
      height: auto;
      border-radius: 12px;
    }
    .logo h2 {
      color: #007BFF;
      margin-top: 10px;
      font-size: 28px;
    }
  </style>
</head>
<body>
  <div class="logo">
    <img src="sua-imagem-aqui.jpg" alt="Logo Kamomedai">
    <h2>Kamomedai</h2>
  </div>

  <h1>📋 PERGUNTAS PARA STAFF</h1>
  <p>Terminou? Aperte em enviar.</p>
  <form id="staffForm">
    <label for="email">Digite seu e-mail:</label>
    <input type="email" id="email" name="E-mail" required>

    <!-- Perguntas -->
    <script>
      const perguntas = [
        "Qual seu nome e idade?",
        "Você já participou de alguma staff antes? Qual?",
        "Por que quer ser staff no nosso servidor?",
        "Quanto tempo você passa online por dia?",
        "Você está em outros servidores como staff atualmente?",
        "Qual seu fuso horário e disponibilidade?",
        "Como você reage a críticas ou pessoas desrespeitosas?",
        "O que você faria se alguém te desrespeitasse no chat?",
        "Já teve algum problema em servidores? Se sim, qual?",
        "Você sabe manter a calma em discussões?",
        "Já usou bots de moderação como Dyno, MEE6, Carl Bot, etc.?",
        "Tem experiência com comandos ou automações?",
        "Sabe usar o Discord bem (canais, roles, permissões)?",
        "Já organizou eventos ou sorteios? Como foi?",
        "Um membro está xingando outro. O que você faz?",
        "Dois membros estão brigando, e ambos têm razão. E agora?",
        "Um amigo seu quebra as regras. O que você faria?",
        "Você está sozinho online e alguém começa a floodar. Qual seria sua reação?",
        "Como você explicaria as regras para um novato?",
        "O que faria se um moderador começasse a agir de forma errada?",
        "E se um membro insistisse em pedir cargo sem merecer?",
        "O que você mais gosta no servidor?",
        "O que mudaria ou melhoraria aqui?",
        "Como você ajudaria a manter o servidor ativo?",
        "O que significa ser um bom staff pra você?"
      ];

      window.onload = () => {
        const form = document.getElementById('staffForm');
        perguntas.forEach((pergunta, index) => {
          const label = document.createElement('label');
          label.textContent = `${index + 1}. ${pergunta}`;
          const textarea = document.createElement('textarea');
          textarea.name = `Pergunta${index + 1}`;
          form.insertBefore(label, form.lastElementChild);
          form.insertBefore(textarea, form.lastElementChild);
        });
      };
    </script>

    <button type="button" onclick="enviarRespostas()">Enviar</button>
  </form>

  <div class="logo">
    <img src="sua-imagem-aqui.jpg" alt="Logo Kamomedai Final">
    <h2>Kamomedai</h2>
  </div>

  <script>
    function enviarRespostas() {
      const form = document.getElementById('staffForm');
      const formData = new FormData(form);
      let corpoEmail = '';

      for (let [chave, valor] of formData.entries()) {
        corpoEmail += `${chave}: ${valor}\n`;
      }

      const emailDestino = 'jhordylima97@gmail.com';
      const assunto = 'Respostas do Formulário de Staff';
      const mailtoLink = `mailto:${emailDestino}?subject=${encodeURIComponent(assunto)}&body=${encodeURIComponent(corpoEmail)}`;

      window.location.href = mailtoLink;
    }
  </script>
</body>
</html>
