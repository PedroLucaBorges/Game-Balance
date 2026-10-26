# AGENTS.md

## Visão geral

O projeto tem como objetivo criar uma aplicação que mostre como os videogames influenciam a vida das pessoas, apresentando seus benefícios e possíveis impactos negativos. Esse projeto busca conscientizar sobre o uso responsável dos jogos, mostrando como eles podem ajudar na criatividade, no raciocínio e na socialização, mas também como o uso excessivo pode prejudicar a saúde e os estudos. O público principal são jovens que gostam de videogames.

## Tecnologias

- HTML: estrutura das páginas do site.
- CSS: design, cores, fontes e organização visual.
- JavaScript: funcionalidades e interações do site.
- Visual Studio Code: ambiente de desenvolvimento do projeto.
- Trello: organização das tarefas e acompanhamento do progresso.
- MySQL: banco de dados
-Git e Github - gerenciar e guardar o projeto
-API web-data-viz
-Chart.JS: gráficos
-Opencode: IA

## Comandos

Não entendi o que colocar aqui.

## Arquitetura

Explique como o projeto está organizado e como uma funcionalidade deve ser implementada.
Inclua informações como:
- Estrutura das principais pastas
- Responsabilidade de cada pasta
- Fluxo de uma requisição
- Onde criar novos arquivos
- Como os diretórios se relacionam

O projeto está no padraõ web-data-viz : front-end separado do back-en, e o back-end dividido em rotas, controllers e models

app.js: sobe o servidor Express, carrega o .env, serve a pasta public e registra as rotas.
.env: configurações e credenciais (banco, porta)
database/: scripts SQL para criar o banco de dados e as tabelas.
public/: telas HTML, CSS, JS do front (fetch e gráficos com Chart.js) e imagens.
src/database/config.js: conexão com o MySQL.
src/routes/: define os endereços da API e liga cada um a um controller.
src/controllers/: recebe a requisição, valida os dados e chama o model.
src/models/: contém os comandos SQL, é a única camada que acessa o banco.

O puclic só fala com a API por fetch. A route chama o controller, o controller chama o model e o model usa o config.js para acessar o banco.

COMO IMPLEMENTAR UMA FUNCIONALIDADE

Criar ou ajustar a tabela em database/script.sql
Criar o model com o SQL (src/models).
Criar o controller com a validação (src/controlles).
Criar a route com os endereços (src/route) e registrá-la no app.js.
Criar a tela em public/ e o JS que chama a API
Testar o endpoint e depois a tela.

TELA: public/.
ESTILO: public/css. 
SCRIPT DO FRONT: public/js/. API: src/routes, src/controllers e src/models. TABELA: database/script.sql.

Regra prática: cada funcionalidade ganha uma route, um controller e um model com o mesmo nome, mais a tela e o JS no public

## Padrões de desenvolvimento

VARIÁVEIS

Usar let.
Usar == e !== nas comparações.

NOMENCLATURA

Arquivos: minúsculos, sem acentos nem espaços (ex.: dashboard.html). JS do back-end em camelCase com o sufixo da camada (ex.: quizController.js, quizModel.js).
Variáveis e funções: camelCase (ex.: salvarResposta).
Constantes fixas: MAIUSCULAS_COM_UNDERLINE.
Tabelas e colunas do banco: minúsculas com underline (ex.: resposta_quiz).
IDs e classes no HTML/CSS: minúsculas com hífen (ex.: btn-enviar).

ORGANIZAÇÃO E SEGURANÇA

SQL só no model, validação no controller, endereços na route.
Indentação de 2 espaços e uso de ponto e vírgula.
consultas SQL parametrizadas.

COMMITS

Em português, no imperativo, no formato tipo: descrição.
Tipos: feat, fix, style, refactor e docs.
Exemplos: feat: adiciona cadastro de usuário / fix: corrige validação do e-mail.
Commits pequenos, um por funcionalidade, com push ao final de cada etapa.

## Cuidados e restrições

NÃO FAZER

Não enviar o .env para o GitHub.
Não montar SQL concatenando texto; usar consultas parametrizadas.
Não instalar bibliotecas novas sem avisar.
Não trocar a stack nem usar frameworks de front-end.
Não apagar, renomear ou mover arquivos sem avisar.
Não fazer push nem mexer no histórico do Git sem eu pedir.

ATENÇÃO ANTES DE ALTERAR

Ler a estrutura do projeto antes de criar arquivos.
Mostrar o plano e esperar minha confirmação antes de implementar.
Mostrar o script antes de alterar o banco; nunca rodar DROP, DELETE ou TRUNCATE sem confirmação.
Avisar antes de mexer em app.js, config.js e package.json.
Explicar a causa dos erros em vez de só corrigir.
Dizer como testar cada mudança.


## Regra geral: 

Antes de implementar qualquer alteração, siga as tecnologias, a arquitetura, as convenções e as restrições descritas neste documento.

Se alguma informação estiver ausente, analise o código existente e siga os padrões já adotados no projeto.

Em caso de dúvida ou conflito entre este documento e o código existente, pare e pergunte antes de alterar.