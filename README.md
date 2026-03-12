# Lidar-com-a-escola
Aqui podemos estudar juntos e sem limites 

## O que é este projeto

Lidar-com-a-escola é um site para ajudar estudantes a estudar melhor, organizar a escola e preparar testes.

## Ferramentas grátis

- Calculadora de média
- Cronómetro de estudo
- Curiosidades científicas

## Ferramenta premium

Os estudantes podem colocar a matéria que estão a estudar e o site cria automaticamente um quiz para treinar.

## Preço

30 dias grátis

Depois:
12€ por mês

## Objetivo

Ajudar estudantes a estudar melhor e tornar o estudo mais fácil e divertido.
async function perguntarIA(pergunta){

let resposta = await fetch("https://api.openai.com/v1/chat/completions",{
method:"POST",
headers:{
"Content-Type":"application/json",
"Authorization":"Bearer A_TUA_CHAVE_API"
},
body: JSON.stringify({
model:"gpt-4o-mini",
messages:[{role:"user",content:pergunta}]
})
})

let dados = await resposta.json()

return dados.choices[0].message.content
}
