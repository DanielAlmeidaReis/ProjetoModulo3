[index.html](https://github.com/user-attachments/files/28325630/index.html)# ProjetoModulo3
# Projeto Módulo 3 – Low Code/No Code/Vibecode
## 📌 Desafio Escolhido
Calculadora de preços de mercado
---
## 🖥️ Protótipo
<img width="791" height="536" alt="Captura de tela 2026-05-27 150734" src="https://github.com/user-attachments/assets/9fffcb86-4c44-4a87-896b-03a1989c73cc" />
<img width="860" height="522" alt="Captura de tela 2026-05-27 150639" src="https://github.com/user-attachments/assets/de4c974b-359b-4a04-9551-6c365c48897e" />
<img width="779" height="529" alt="Captura de tela 2026-05-27 150834" src="https://github.com/user-attachments/assets/e3a017ae-9450-44af-b378-1a8dc4b1d1d5" />
<img width="760" height="569" alt="Captura de tela 2026-05-27 150924" src="https://github.com/user-attachments/assets/2d8f41d5-a747-4b9a-ad77-922094d13ec9" />
[Upload<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Calculadora de Preços de Mercado</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #E6F0FA; /* azul bem claro para fundo */
      margin: 0;
      padding: 20px;
    }
    h1 {
      text-align: center;
      color: #003366; /* azul escuro para destaque */
    }
    .container {
      background-color: #FFFFFF; /* branco para contraste */
      padding: 20px;
      border-radius: 10px;
      max-width: 500px;
      margin: auto;
      box-shadow: 0 0 10px rgba(0,51,102,0.2);
    }
    input, button {
      padding: 10px;
      margin: 5px 0;
      width: 100%;
      border: none;
      border-radius: 5px;
    }
    input {
      background-color: #F0F8FF; /* azul muito suave */
    }
    button {
      background-color: #3399FF; /* azul vibrante */
      color: #FFFFFF; /* texto branco para contraste */
      cursor: pointer;
      font-weight: bold;
    }
    button:hover {
      background-color: #0066CC; /* azul mais escuro ao passar o mouse */
    }
    .result {
      background-color: #F8FBFF; /* branco-azulado suave */
      padding: 15px;
      border-radius: 8px;
      margin-top: 15px;
      border: 1px solid #CCE0F5;
    }
  </style>
</head>
<body>
  <h1>Calculadora de Preços de Mercado</h1>
  <div class="container">
    <label for="produto">Nome do Produto:</label>
    <input type="text" id="produto" placeholder="Digite o nome do produto">
    
    <label for="preco">Preço do Produto (R$):</label>
    <input type="number" id="preco" placeholder="Digite o preço" step="0.01">
    
    <button onclick="adicionarProduto()">Adicionar Produto</button>
    
    <div class="result">
      <p><strong>Produtos adicionados:</strong></p>
      <ul id="lista"></ul>
      <p><strong>Soma total:</strong> R$ <span id="soma">0.00</span></p>
      <p><strong>Preço médio:</strong> R$ <span id="media">0.00</span></p>
    </div>
  </div>

  <script>
    let produtos = [];

    function adicionarProduto() {
      const nome = document.getElementById('produto').value;
      const preco = parseFloat(document.getElementById('preco').value);

      if (nome && !isNaN(preco)) {
        produtos.push(preco);

        const lista = document.getElementById('lista');
        const item = document.createElement('li');
        item.textContent = `${nome} - R$ ${preco.toFixed(2)}`;
        lista.appendChild(item);

        atualizarResultados();
        document.getElementById('produto').value = '';
        document.getElementById('preco').value = '';
      } else {
        alert("Por favor, insira um nome e um preço válido.");
      }
    }

    function atualizarResultados() {
      const soma = produtos.reduce((acc, val) => acc + val, 0);
      const media = soma / produtos.length;

      document.getElementById('soma').textContent = soma.toFixed(2);
      document.getElementById('media').textContent = media.toFixed(2);
    }
  </script>
</body>
</html>
ing index.html…]()

A página apresenta uma interface limpa contendo dois campos de entrada: um para o Nome do Produto (texto) e outro para o Preço (número). Abaixo deles, há um botão azul "Adicionar Produto" e uma área de resultados que mostra uma lista vazia, a soma total e o preço médio.
---
## ⚙️ Plataforma Utilizada
Gemini PRO modo Canvas
A escolha da ferramenta foi feita porque a I.A utilizada é prática e não teve dificuldades em executar o projeto.
## ✅ Vantagens Identificadas
1. Prototipagem rápida
2. Redução de tempo e custos
3. Facilidade de aprendizado
---
## ⚠️ Limitações Encontradas
1. Limitações de customização
2. Dependência da plataforma
3. Problemas de performance 
---
## 📚 Reflexão Crítica
As limitações encontradas foram sobre a parte de customização do aplicativo, e problemas para executar o aplicativo em outras máquinas, porém conseguimos resolver com a ajuda da própria I.A.
---
## 👥 Colaboração
Lucas Nunes
Daniel Almeida Reis
Felipe	Rodrigues de Sousa
Mathias Magalhães
