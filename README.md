<img src="public\assets\imgs\GameB.jpg"


Game Balance — Projeto Individual
1º semestre de Análise e Desenvolvimento de Sistemas (ADS)

Sobre o projeto
Este projeto consiste no desenvolvimento de um site temático focado em tecnologia e conscientização, voltado para educar jovens sobre o universo dos jogos eletrônicos. A proposta é apresentar uma perspectiva equilibrada, explorando tanto os benefícios cognitivos, sociais e de desenvolvimento que os games oferecem quanto os riscos associados ao uso excessivo, tempo de tela e impactos à saúde.

O site contará com seções informativas e um espaço interativo (como um quiz ou formulário de feedback) no qual os usuários poderão registrar seus hábitos de jogo e avaliar sua rotina digital. As respostas registradas serão utilizadas para construir uma dashboard interativa, com gráficos que representam o perfil e o nível de equilíbrio digital dos participantes.

Objetivo
Aplicar, na prática, os conteúdos estudados no primeiro semestre de ADS, principalmente desenvolvimento web (HTML, CSS, JavaScript), lógica de programação, banco de dados (MySQL) e integração entre frontend e backend.

Como o sistema deverá funcionar
O usuário acessa o site e realiza seu cadastro ou login.

Ele navega pelas seções educativas ou responde a um quiz sobre seus hábitos de jogo e bem-estar.

O frontend envia as informações e respostas para a API desenvolvida com Node.js e Express.

A API processa os dados e os registra de forma segura no MySQL.

A dashboard de resultados consulta as informações por meio da API e apresenta gráficos dinâmicos (utilizando Chart.js) destacando o índice de equilíbrio digital.

Como executar (configuração inicial)
Será necessário ter Node.js e acesso a um servidor MySQL configurado para o projeto. Na pasta principal da aplicação, os comandos previstos são:

Bash
npm install
npm start
O funcionamento desses comandos depende dos scripts definidos no package.json