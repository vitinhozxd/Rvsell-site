<html>
 <head>  
 </head> 
 <body> 
  <meta charset="UTF-8"> 
  <meta name="viewport" content="width=device-width, initial-scale=1.0"> 
  <title>Loja de Scripts Premium</title> 
  <link rel="stylesheet" href="style.css"> 
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0; padding: 0;
    }
    header {
      background-color: #111;
      color: white;
      padding: 20px;
      text-align: center;
    }
    nav ul {
      list-style: none;
      padding: 0;
    }
    nav li {
      display: inline;
      margin: 0 15px;
    }
    nav a {
      color: green;
      text-decoration: none;
    }
    .card-container {
      display: flex;
      flex-wrap: wrap;
      gap: 20px;
      padding: 20px;
    }
    .card {
      background: 111;
      padding: 20px;
      border-radius: 10px;
      width: 300px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }
    .modal {
      position: fixed;
      z-index: 1000;
      left: 0; top: 0;
      width: 100%; height: 100%;
      background-color: rgba(0,0,0,0.6);
      display: none;
      align-items: center;
      justify-content: center;
    }
    .modal-content {
      background-color: 111;
      padding: 30px;
      border-radius: 10px;
      max-width: 400px;
      width: 90%;
    }
    .close {
      float: right;
      font-size: 24px;
    }
    footer {
      background-color: #111;
      color: green;
      text-align: center;
      padding: 20px;
      margin-top: 40px;
    }
  </style> 
  <header> 
   <h1>Loja de Scripts Rvsell 🚀</h1> 
   <nav> 
    <ul> 
     <li><a href="#produtos">Produtos</a></li> 
     <li><a href="#sobre">Sobre</a></li> 
     <li><a href="#contato">Contato</a></li> 
    </ul> 
   </nav> 
  </header> 
  <main> 
   <section id="produtos"> 
    <h2 style="text-align:center;">Nossos Scripts</h2> 
    <div class="card-container"> 
     <div class="card"> 
      <h3>Macro VIP🩸</h3> 
      <p>Acelere, destrua e jogue no modo brutal. Quem usa, vence. Quem não usa, chora.</p> 
      <button onclick="abrirModal('🩸Macro VIP🩸', '19,99')">Comprar</button> 
     </div> 
     <div class="card"> 
      <h3>Macro ⚙️</h3> 
      <p>Controle absoluto e poder ilimitado. A ferramenta que separa jogadores comuns de verdadeiras lendas.</p> 
      <button onclick="abrirModal('⚙️ Macro ⚙️', '15,99')">Comprar</button> 
     </div> 
     <div class="card"> 
      <h3>DNS-DPI XITADO🥶</h3> 
      <p>Xitado até na conexão! Mais rápido, mais estável, mais vantagem em todas as partidas.</p> 
      <button onclick="abrirModal('🥶DNS-DPI XITADO🥶', '15,00')">Comprar</button> 
     </div> 
     <div class="card"> 
      <h3>DNS 100% vip</h3> 
      <p>Conexão blindada para quem manda no jogo. Sem lag, sem travamento, só vitória!</p> 
      <button onclick="abrirModal('⚡️DNS 100% vip ⚡️', '12,99')">Comprar</button> 
     </div> 
     <div class="card"> 
      <h3>SPACE TEAM 👺</h3> 
      <p>Não é para todos, é para LENDAS. Jogue no modo supremo, domine o cenário e faça história no game.</p> 
      <button onclick="abrirModal('👺 SPACE TEAM 👺', '29,99')">Comprar</button> 
     </div> 
    </div> 
   </section> 
   <section id="sobre" style="padding: 20px;"> 
    <h2>Sobre Nós</h2> 
    <p>💀 Sem enrolação, sem desculpas, só resultado. Cada script, cada macro, cada DNS que oferecemos é testado, otimizado e feito para garantir vantagem máxima, segurança total e domínio absoluto em cada partida. </p> 
   </section> 
   <section id="contato" style="padding: 20px;"> 
    <h2>Contato</h2> 
    <p>Email: suporte@lojascripts.com.br</p> 
    <p>WhatsApp: (38) 99931-4832</p> 
   </section> 
  </main> 
  <footer> 
   <p> 💀 Aqui só entra quem joga para destruir.🔥 Rvsell – O poder está nas suas mãos. </p> 
  </footer> 
  <!-- Modal de Compra --> 
  <div id="modal" class="modal"> 
   <div class="modal-content"> 
    <span onclick="fecharModal()" class="close" style="cursor:pointer;">×</span> 
    <h3 id="tituloProduto"></h3> 
    <p id="precoProduto"></p> 
    <p>Finalize a compra via WhatsApp clicando no botão abaixo:</p> 
    <a id="linkWhatsApp" href="#" target="_blank"> <button style="margin-top: 15px; padding: 10px 20px; background-color: green; color: white; border: none; border-radius: 5px; cursor: pointer;"> Finalizar via WhatsApp </button> </a> 
   </div> 
  </div> 
  <script>
    function abrirModal(produto, preco) {
      document.getElementById('tituloProduto').textContent = produto;
      document.getElementById('precoProduto').textContent = `Preço: R$ ${preco}`;

      // WhatsApp automático
      const mensagem = `Olá! Tenho interesse no produto *${produto}* no valor de R$ ${preco}.`;
      const numero = '5538999314832';
      const linkWhatsApp = document.getElementById('linkWhatsApp');
      linkWhatsApp.href = `https://wa.me/${numero}?text=${encodeURIComponent(mensagem)}`;

      document.getElementById('modal').style.display = 'flex';
    }

    function fecharModal() {
      document.getElementById('modal').style.display = 'none';
    }

    window.onclick = function(event) {
      const modal = document.getElementById('modal');
      if (event.target === modal) {
        fecharModal();
      }
    }
  </script>   
 </body>
</html>