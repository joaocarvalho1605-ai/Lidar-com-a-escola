<!DOCTYPE html><html lang="pt">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Lidar com a Escola - IA Real</title>
<style>
body{font-family:Arial,sans-serif;background:#eef3f8;text-align:center;padding:20px;}
.section{background:white;margin:20px auto;padding:20px;max-width:700px;border-radius:12px;box-shadow:0 6px 14px rgba(0,0,0,0.1);}
input,textarea{width:80%;padding:10px;margin:8px;border-radius:8px;border:1px solid #ccc;}
button{padding:12px 18px;border:none;border-radius:8px;background:#2b6cb0;color:white;cursor:pointer;}
button:hover{background:#1f4f86;}
</style>
</head>
<body>
<h1>Lidar com a Escola</h1>
<p>Estudo com IA real</p><div class="section">
<h2>Falar com a IA</h2>
<select id="plano">
<option value="basic">Plano Estudo IA - 7€</option>
<option value="premium">Plano Tutor IA - 12€</option>
</select><br>
<input id="pergunta" placeholder="Faz a tua pergunta sobre a matéria"><br>
<button onclick="perguntarIA()">Perguntar à IA</button>
<p id="resposta"></p>
</div><script>
async function perguntarIA(){
    const pergunta = document.getElementById('pergunta').value;
    const plano = document.getElementById('plano').value;

    if(!pergunta){
        alert('Escreve uma pergunta!');
        return;
    }

    document.getElementById('resposta').innerText='A IA está a pensar...';

    // Aqui chamarias o teu backend seguro que liga à API da OpenAI ou outra IA
    // Exemplo de fetch para backend:
    /*
    const response = await fetch('/api/perguntar', {
        method:'POST',
        headers:{'Content-Type':'application/json'},
        body:JSON.stringify({ pergunta, plano })
    });
    const data = await response.json();
    document.getElementById('resposta').innerText = data.resposta;
    */

    // Simulação de resposta para testar sem backend
    let respostasBasic=[
        'Pensa nos pontos principais do tema e tenta resumir.',
        'Revê os exemplos que tens na matéria.'
    ];
    let respostasPremium=[
        'Esta é uma explicação detalhada>