# <!DOCTYPE html><html lang="pt">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Lidar com a Escola</title><style>
body{
font-family: Arial, Helvetica, sans-serif;
margin:0;
background:#eef3f8;
text-align:center;
}

header{
background:#2b6cb0;
color:white;
padding:25px;
}

h1{margin:0}

.section{
background:white;
margin:25px auto;
padding:25px;
max-width:700px;
border-radius:12px;
box-shadow:0 6px 14px rgba(0,0,0,0.1);
}

button{
padding:12px 18px;
border:none;
border-radius:8px;
background:#2b6cb0;
color:white;
font-size:16px;
cursor:pointer;
}

button:hover{
background:#1f4f86;
}

input, textarea{
padding:10px;
margin:6px;
width:80%;
border-radius:8px;
border:1px solid #ccc;
}

img{
max-width:100%;
border-radius:10px;
margin-top:10px;
}

.plan{
border:2px solid #2b6cb0;
padding:15px;
margin:10px;
border-radius:10px;
}
</style></head><body><header>
<h1>📚 Lidar com a Escola</h1>
<p>Aqui podemos estudar juntos e sem limites</p>
</header><div class="section">
<h2>Calculadora de Média</h2>
<input id="n1" placeholder="Nota 1">
<input id="n2" placeholder="Nota 2">
<input id="n3" placeholder="Nota 3"><br>
<button onclick="calcMedia()">Calcular Média</button>
<p id="mediaResultado"></p>
</div><div class="section">
<h2>Gerador de Quiz com IA (simulação)</h2>
<p>Coloca um texto da matéria e a IA cria perguntas.</p>
<textarea id="materia" rows="5" placeholder="Ex: A fotossíntese é o processo... "></textarea><br>
<button onclick="gerarQuiz()">Criar Quiz</button>
<div id="quiz"></div>
</div><div class="section">
<h2>Falar com a IA (simulação)</h2>
<input id="pergunta" placeholder="Faz uma pergunta sobre a matéria">
<button onclick="perguntarIA()">Perguntar</button>
<p id="resposta"></p>
</div><div class="section">
<h2>Curiosidade Científica</h2>
<button onclick="curiosidade()">Mostrar curiosidade</button>
<p id="facto"></p>
</div><div class="section">
<h2>Planos</h2><div class="plan">
<h3>Plano Estudo IA</h3>
<p>7€ / mês</p>
<p>✔ Criar quizzes automaticamente</p>
<p>✔ Criar testes de estudo</p>
</div><div class="plan">
<h3>Plano Tutor IA</h3>
<p>12€ / mês</p>
<p>✔ Conversar com IA</p>
<p>✔ Fazer perguntas diretas</p>
<p>✔ Explicações da matéria</p>
</div><p>30 dias grátis</p>
</div><div class="section">
<h2>Motivação para estudar</h2>
<img src="https://images.unsplash.com/photo-1503676260728-1c00da094a0b">
<p>O estudo abre portas para o futuro.</p><img src="https://images.unsplash.com/photo-1523240795612-9a054b0db644">
<p>Aprender pode ser divertido quando usamos boas ferramentas.</p>
</div><script>

function calcMedia(){
let a = Number(document.getElementById("n1").value)
let b = Number(document.getElementById("n2").value)
let c = Number(document.getElementById("n3").value)

let media = (a+b+c)/3

if(!isNaN(media)){
document.getElementById("mediaResultado").innerText = "A tua média é: " + media.toFixed(2)
}
}

function gerarQuiz(){
let texto = document.getElementById("materia").value

let quizHTML = ""

quizHTML += "<p><b>Pergunta 1:</b> O que significa o texto que escreveste?</p>"
quizHTML += "<p><b>Pergunta 2:</b> Explica a ideia principal da matéria.</p>"
quizHTML += "<p><b>Pergunta 3:</b> Dá um exemplo relacionado com este tema.</p>"


document.getElementById("quiz").innerHTML = quizHTML
}

function perguntarIA(){
let pergunta = document.getElementById("pergunta").value

let resposta = "Boa pergunta! A resposta depende da matéria, mas tenta rever os conceitos principais e exemplos."

if(pergunta.length > 0){
document.getElementById("resposta").innerText = resposta
}
}

function curiosidade(){
let factos = [
"Um polvo tem três corações.",
"A luz do Sol demora cerca de 8 minutos a chegar à Terra.",
"O cérebro humano tem cerca de 86 mil milhões de neurónios.",
"Os tubarões existem há mais tempo que as árvores."
]

let f = factos[Math.floor(Math.random()*factos.length)]

document.getElementById("facto").innerText = f
}

</script></body>
</html>