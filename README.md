# Projeto Full Stack - Front-end

Projeto desenvolvido para a disciplina de Desenvolvimento Full Stack. Esta etapa consiste na criação da interface do usuário (Client-side) utilizando HTML5 e JavaScript assíncrono (Fetch API) para se conectar à API do Back-end.

---

## 🛠️ Configuração e Inicialização do Projeto

Siga os passos abaixo para construir a estrutura inicial do front-end:

### Criar a pasta do projeto e acessar
```bash

mkdir fullstack-frontend
cd fullstack-frontend

## 💻 Estrutura do Código

Crie um arquivo chamado index.html na raiz do projeto e adicione o seguinte código:

"<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Saudação Full Stack</title>
</head>
<body>

    <h1>Projeto Full Stack</h1>

    <input type="text" id="nome" placeholder="Digite seu nome">

    <button onclick="enviar()">
        Enviar
    </button>

    <h2 id="resultado"></h2>

    <script>
        async function enviar() {
            const nome = document.getElementById('nome').value;

            // Faz a requisição POST para o servidor Back-end rodando na porta 3000
            const resposta = await fetch('http://localhost:3000/saudacao', {
                method: 'POST',
                headers: {
                    'Content-Type': 'application/json'
                },
                body: JSON.stringify({ nome })
            });

            const dados = await resposta.json();

            // Exibe a mensagem retornada pela API na tela
            document.getElementById('resultado').innerText = dados.mensagem;
        }
    </script>
</body>
</html>"

## 🗃️ Versionamento com Git

## Inicializar o repositório Git

git init

# Configurar o arquivo .gitignore

node_modules/

# Realizar o primeiro commit

git add .
git commit -m "Projeto inicial"

## Criando Repositórios no GitHub

Criar:

## Conectando repositório local ao GitHub

git remote add origin URL_DO_REPOSITORIO

## Enviando projeto para o GitHub

git branch -M main
git push -u origin main