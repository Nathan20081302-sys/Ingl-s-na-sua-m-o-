<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Inglês na sua Mão</title>

<style>
body{margin:0;font-family:Arial;background:#f4f6f8}
header{background:#1e90ff;color:#fff;text-align:center;padding:40px}
section{max-width:900px;margin:auto;padding:30px}
.card{background:#fff;padding:25px;border-radius:10px;margin-bottom:20px;box-shadow:0 4px 10px rgba(0,0,0,.1)}
h2{color:#1e90ff}
footer{background:#222;color:#fff;text-align:center;padding:15px}
.btn{display:inline-block;background:#1e90ff;color:#fff;padding:12px 25px;border-radius:6px;text-decoration:none}

/* CHAT IA */
#chatbot{position:fixed;bottom:20px;right:20px;width:300px}
#chat-header{background:#1e90ff;color:#fff;padding:10px;border-radius:10px 10px 0 0;cursor:pointer}
#chat-body{display:none;background:#fff;height:280px;overflow-y:auto;padding:10px;border:1px solid #ccc}
#chat-input{display:flex}
#chat-input input{flex:1;padding:8px;border:none;border-top:1px solid #ccc}
#chat-input button{background:#1e90ff;color:#fff;border:none;padding:8px}
.bot{color:#1e90ff;margin:6px 0}
.user{text-align:right;margin:6px 0}
</style>
</head>

<body>

<header>
<h1>Inglês na sua Mão</h1>
<p>Professor Nathanael Rodrigues Brito</p>
</header>

<section>

<div class="card">
<h2>Sobre o Curso</h2>
<p>
Curso de inglês criado para quem quer aprender do zero de forma simples e prática,
com aulas organizadas e apoio de uma IA Professora.
</p>
</div>

<div class="card">
<h2>IA Professora</h2>
<p>
A IA Professora auxilia os alunos 24h por dia, ensinando vocabulário,
frases, conversação básica e corrigindo respostas.
</p>
</div>

<div class="card">
<h2>Benefícios</h2>
<ul>
<li>Inglês do básico ao intermediário</li>
<li>IA Professora 24h</li>
<li>Aulas práticas</li>
<li>Aprenda no seu ritmo</li>
<li>Suporte pelo WhatsApp</li>
</ul>
</div>

<div class="card">
<h2>Planos e Valores</h2>
<p>🟦 Básico: R$ 120/mês</p>
<p>🟩 Completo: R$ 150/mês</p>
<p>🟨 Premium: R$ 200/mês</p>
<p>Matrícula: R$ 50</p>
</div>

<div class="card">
<h2>Contato</h2>
<a class="btn" href="https://wa.me/5511954957984" target="_blank">Falar no WhatsApp</a>
</div>

</section>

<footer>
© 2026 – Inglês na sua Mão
</footer>

<!-- CHATBOT -->
<div id="chatbot">
<div id="chat-header" onclick="toggle()">🤖 IA Professora</div>
<div id="chat-body">
<div class="bot">Olá 👋 Quer aprender inglês? Digite: alfabeto, cumprimentos ou frases.</div>
</div>
<div id="chat-input">
<input id="msg" placeholder="Digite aqui...">
<button onclick="send()">Enviar</button>
</div>
</div>

<script>
function toggle(){
  const c=document.getElementById("chat-body");
  c.style.display=c.style.display==="none"?"block":"none";
}
function send(){
  const i=document.getElementById("msg");
  const m=i.value.toLowerCase();
  if(!m)return;
  const c=document.getElementById("chat-body");
  c.innerHTML+=`<div class="user">${i.value}</div>`;
  let r="Digite: alfabeto, cumprimentos ou frases.";
  if(m.includes("alfabeto")) r="A B C D E F G...";
  if(m.includes("cumprimentos")) r="Hello = Olá | Hi = Oi";
  if(m.includes("frases")) r="My name is... = Meu nome é...";
  c.innerHTML+=`<div class="bot">${r}</div>`;
  c.scrollTop=c.scrollHeight;
  i.value="";
}
</script>

</body>
</html>
