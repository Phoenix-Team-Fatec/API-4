# API-4

<span id="topo">
<h1 align="center"> FATEC SJC - 4º Semestre ADS - Lumen </h1>
<br>

## 📍 Objetivo

<h4>Desenvolver uma plataforma web para gestão de projetos da FAPG (Fundação de Apoio à Pesquisa e Gestão)</h4>

<br>
<br>

 <h2> ➯ Backlog do Produto </h2> 

| Rank | Prioridade | US | Estimativa | Sprint | Requisitos do parceiro | Cenário de teste 1 | Cenário de teste 2 |
|------|------------|----|------------|--------|--------------------------|---------------------|---------------------|
| #01  | Alta       | Como usuário do sistema, quero fazer login com credenciais seguras, para proteger as informações dos projetos. | 15 Horas | 1 | RF5, RNF1  | **Ação:** Usuário acessa a página de cadastro e preenche os campos obrigatórios (nome, sobrenome, email, senha).<br><br>**Resultado esperado:** Sistema cria a conta e exibe mensagem de sucesso. | **Ação:** Usuário insere email e senha cadastrados na página de login.<br><br>**Resultado esperado:** Sistema redireciona para a dashboard e exibe boas-vindas. |
| #02  | Alta       | Como coordenador, quero cadastrar um novo projeto, para organizar melhor as iniciativas da FAPG. | 15 Horas | 1 |  RF1, RNF1 | **Ação:** Coordenador acessa "Cadastrar Projeto" e preenche nome e descrição.<br><br>**Resultado esperado:** Projeto aparece na listagem após cadastro. | **Ação:** Coordenador tenta cadastrar sem nome.<br><br>**Resultado esperado:** Sistema exibe erro de campo obrigatório. |
| #03  | Alta       | Como coordenador, quero listar todos os projetos cadastrados. | 20 Horas | 1 |  RF4, RNF1 | **Ação:** Coordenador acessa a listagem de projetos.<br><br>**Resultado esperado:** Todos os projetos cadastrados são exibidos. | **Ação:** Novo projeto é adicionado em outra aba.<br><br>**Resultado esperado:** Listagem é atualizada automaticamente sem refresh. |
| #04  | Alta       | Como membro da equipe, quero cadastrar etapas e tarefas dentro de um projeto. | 20 Horas | 1 |  RF5, RNF1  | **Ação:** Cria etapa "Desenvolvimento" e tarefa "Criar API".<br><br>**Resultado esperado:** Tarefa aparece aninhada sob a etapa no projeto. | **Ação:** Membro não-coordenador tenta criar etapa.<br><br>**Resultado esperado:** Acesso negado. |
| #05  | Média      | Como coordenador da equipe, quero dividir uma tarefa em sub-tarefas, para detalhar melhor as etapas do trabalho e facilitar o acompanhamento. | 30 Horas | 2 | RF5, RNF1 | **Ação:** Coordenador seleciona "Dividir tarefa" e adiciona subtarefas.<br><br>**Resultado esperado:** Subtarefas aparecem aninhadas à tarefa principal. | **Ação:** Membro da equipe visualiza a tarefa dividida.<br><br>**Resultado esperado:** Status das subtarefas é exibido por "Pendente", "Em Progresso", "Concluído". |
| #06  | Média      | Como coordenador da equipe, quero associar uma tarefa a suas respectivas datas e seus responsáveis. | 15 Horas | 2 |RF5, RNF1 | **Ação:** Ao criar uma tarefa, um coordenador consegue escolher uma data de início e fim.<br><br>**Resultado esperado:** Tarefa é cadastrada com prazos de entrega. | **Ação:** Associa tarefa "Design" ao membro "João" com prazo de 01/05 a 15/05.<br><br>**Resultado esperado:** Tarefa aparece no calendário de João com alertas. |
| #07  | Média      | Como coordenador ou membro da equipe, quero associar e filtrar os projetos por área de atuação, para encontrar rapidamente os projetos relacionados a um campo específico. | 30 Horas | 2 | RF4, RNF1  | **Ação:** Seleciona filtro "Saúde".<br><br>**Resultado esperado:** Exibe apenas projetos com tag "Saúde". | **Ação:** Tenta associar área inexistente.<br><br>**Resultado esperado:** Sistema sugere áreas cadastradas. |
| #08  | Média      | Como coordenador, quero editar ou excluir um projeto, para manter os dados atualizados e remover registros obsoletos ou incorretos. | 15 Horas | 2 | RF3, RNF1, RNF2  | **Ação:** Exclui projeto e confirma com senha.<br><br>**Resultado esperado:** Projeto vai para "Lixeira" por 30 dias. | **Ação:** Edita o nome do projeto "Lumen" para "OAK-RH".<br><br>**Resultado esperado:** O nome do projeto muda conforme novo nome escolhido. |
| #09  | Média      | Como membro da equipe, quero atualizar o status de uma tarefa, para manter o acompanhamento do progresso. | 20 Horas | 3 | RF5, RNF1 | **Ação:** Membro muda status de "Em progresso" para "Revisão".<br><br>**Resultado esperado:** Sistema notifica o revisor. | **Ação:** Membro muda status de "Em progresso" para "Concluído".<br><br>**Resultado esperado:** Sistema aumenta porcentagem de progresso do projeto. |
| #10 | Média      | Como coordenador, quero recuperar um projeto excluído, para restaurar informações importantes caso a exclusão tenha sido um erro. | 30 Horas | 3 | RF2, RNF1, RNF2 | **Ação:** Na lixeira, clica em "Restaurar" no projeto "Beta".<br><br>**Resultado esperado:** Projeto volta com todas as relações intactas. | **Ação:** Após 30 dias, sistema remove projeto.<br><br>**Resultado esperado:** Log de auditoria registrado. |







<br>
<br>

<br>
<br>
 <h2>  ➯ Requisitos Funcionais</h2>

| Nº Requisito   | Requisito do Parceiro |
| :----: | :----: |
| RF1  |  Cadastrar projetos da FAPG, incluindo informações como nome do projeto, descrição, área de atuação, responsáveis, status, etc. |
| RF2  | Permitir a recuperação de dados de projetos de forma intuitiva e eficiente. |
| RF3  | Permitir a atualização e exclusão de dados dos projetos cadastrados. |
| RF4  | - Visualizar projetos por **área de atuação** <br> - Visualizar projetos por **responsáveis** <br> - Visualizar projetos por **status**. <br> - Acompanhar o **andamento das atividades** dos projetos.|
| RF5  | Permitir o acesso do usuário ao sistema e suas funcionalidades 

<br>
<br>

 <h2> ➯ Requisitos Não Funcionais</h2>

| Nº Requisito   | Requisito do Parceiro |
| :----: | :----: |
| RNF1 | O sistema deve ser fácil de usar, com uma interface intuitiva e acessível. |
| RNF2 |  Garantir a privacidade e segurança dos dados dos projetos e usuários. |
| RNF3 | O sistema deve ser capaz de converter linguagem natural em chamadas de funções, sem o uso de APIs externas. |
| RNF4 | Extrair parâmetros da mensagem do usuário para execução de funções, sem o uso de APIs externas. |
| RNF5 |  O sistema deve ser capaz de orquestrar chamadas de funções de forma eficiente e organizada. |



<br>

## ➯ MVP
<span id="mvp">

![SPRINT 4 OAK-RH](https://github.com/user-attachments/assets/b359f3fc-e7fb-4454-9191-14775412ec45)


## ➯ Backlog das Sprints


<a href="Sprint1/README.md" style="text-decoration: none;">
  <img align="left" title="folder" height="30px" src="https://cdn-icons-png.flaticon.com/512/3767/3767084.png"/>
  <span style="font-size: 18px; font-weight: bold;">Sprint 1 - Metodologia, tecnologias, protótipo, cadastro de usuários, cadastro de projetos, cadastro de tarefas, login, interface e banco de dados</span>
</a>
<br><br>
<a href="Sprint2/README.md" style="text-decoration: none;">
  <img align="left" title="folder" height="30px" src="https://cdn-icons-png.flaticon.com/512/3767/3767084.png"/>
  <span style="font-size: 18px; font-weight: bold;">Sprint 2 - Subtarefas, Filtros, Edição e Exclusão de Projetos, Áreas de Atuação e Associação de tarefas a usuários.</span>
</a>
<a href="Sprint3/README.md" style="text-decoration: none;">
  <img align="left" title="folder" height="30px" src="https://cdn-icons-png.flaticon.com/512/3767/3767084.png"/>
  <span style="font-size: 18px; font-weight: bold;">Sprint 2 - Subtarefas, Filtros, Edição e Exclusão de Projetos, Áreas de Atuação e Associação de tarefas a usuários.</span>
</a>





<br>


## 🛠️ Tecnologias

As seguintes ferramentas, linguagens, bibliotecas e tecnologias foram usadas na construção do projeto:



 
* <p>
  <img align="left" title="figma-logo" height="30px" src="https://user-images.githubusercontent.com/76211125/227502784-c94d5e2d-2e39-449b-ba85-053b9106b979.png"/>
   Figma - Prototipação
 </p>

* <p>
   <img align="left" title="github-dark" height="30px" src="https://user-images.githubusercontent.com/76211125/227561942-1503fb74-eb8e-41d1-936e-bf22bc2d70eb.png#gh-dark-mode-only"/>
   <img align="left" title="github-light" height="30px" src="https://user-images.githubusercontent.com/76211125/227561896-a90cea71-7431-4908-ac8d-71fc02603eeb.png#gh-light-mode-only"/>
   GitHub - Versionamento
 </p>

* <p>
   <img align="left" title="vscode" height="30px" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/vscode/vscode-original.svg"/>
   Vscode - IDE
 </p>

* <p>
   <img align="left" title="vscode" height="30px" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/postgresql/postgresql-original.svg"/>
  PostgreSQL - Banco de dados
 </p>
 
* <p>
   <img align="left" title="vscode" height="30px" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-original.svg"/>
  Node.js - Ambiente de execução de JavaScript
 </p>

 * <p>
   <img align="left" title="vscode" height="30px" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg"/> 
   JavaScript - Linguagem de programação interpretada de alto nível
 </p>

 * <p>
   <img align="left" title="vscode" height="30px" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original.svg"/> 
   React - Biblioteca de código aberto para interfaces gráficas
 </p>
 
 * <p>
   <img align="left" title="vscode" height="30px" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/typescript/typescript-original.svg"/> 
   TypeScript - Linguagem de programação de código aberto
 </p>

 * <p>
   <img align="left" title="firebase" height="30px" src="https://github.com/devicons/devicon/blob/master/icons/firebase/firebase-plain.svg"/> 
   FireBase - Linguagem de programação de código aberto
 </p>


<br>



<span id="equipe">

## :busts_in_silhouette: Equipe

|    Função     | Nome                     |                               LinkedIn                                |                     GitHub                     |
| :----------:  | :----------------------- | :-------------------------------------------------------------------: | :--------------------------------------------: |
|  Dev Team   | Guilherme Sato              |[<img height="30px" src="https://github.com/tandpfun/skill-icons/blob/main/icons/LinkedIn.svg">](https://www.linkedin.com/in/guilherme-sato-42b609292/)|      [<img align="center" height="30px" src="https://github.com/tandpfun/skill-icons/blob/main/icons/Github-Dark.svg"/>](https://github.com/thenewjapzzz)     |
|   Dev Team     | Gustavo Villela           |[<img height="30px" src="https://github.com/tandpfun/skill-icons/blob/main/icons/LinkedIn.svg">](https://www.linkedin.com/in/gustavo-villela-a9314b268/)|      [<img align="center" height="30px" src="https://github.com/tandpfun/skill-icons/blob/main/icons/Github-Dark.svg"/>](https://github.com/TaldoGus)       | 
|  Product Owner     | Samuel Alkmin                 |[<img height="30px" src="https://github.com/tandpfun/skill-icons/blob/main/icons/LinkedIn.svg">](https://www.linkedin.com/in/samuel-alkmin-machado-52743a292/)|      [<img align="center" height="30px" src="https://github.com/tandpfun/skill-icons/blob/main/icons/Github-Dark.svg"/>](https://github.com/samekmd)        |
| Dev Team    | Matheus Andrade                 |[<img height="30px" src="https://github.com/tandpfun/skill-icons/blob/main/icons/LinkedIn.svg">](https://www.linkedin.com/in/matheus-santos-b1a65b1ba/)|      [<img align="center" height="30px" src="https://github.com/tandpfun/skill-icons/blob/main/icons/Github-Dark.svg"/>](https://github.com/MatheusAndrade1999)      | 
| Scrum Master | Vinicius Peretta                 |[<img height="30px" src="https://github.com/tandpfun/skill-icons/blob/main/icons/LinkedIn.svg">](https://www.linkedin.com/in/vinicius-assis-peretta-5a2436227/)|      [<img align="center" height="30px" src="https://github.com/tandpfun/skill-icons/blob/main/icons/Github-Dark.svg"/>](https://github.com/Peretta)        |
| Dev Team | Pedro Machado                 |[<img height="30px" src="https://github.com/tandpfun/skill-icons/blob/main/icons/LinkedIn.svg">](https://www.linkedin.com/in/pedro-henrique-machado-martins-968855305/)|      [<img align="center" height="30px" src="https://github.com/tandpfun/skill-icons/blob/main/icons/Github-Dark.svg"/>](https://github.com/PedrooMachado23)        |
| Dev Team | Larissa Colucci                 |[<img height="30px" src="https://github.com/tandpfun/skill-icons/blob/main/icons/LinkedIn.svg">](https://www.linkedin.com/in/larissa-colucci-996393295/)|      [<img align="center" height="30px" src="https://github.com/tandpfun/skill-icons/blob/main/icons/Github-Dark.svg"/>](https://github.com/LarissaCGomes)        |
| Dev Team | João Victor                 |[<img height="30px" src="https://github.com/tandpfun/skill-icons/blob/main/icons/LinkedIn.svg">](https://www.linkedin.com/in/jo%C3%A3o-victor-menezes-88a6b9264/)|      [<img align="center" height="30px" src="https://github.com/tandpfun/skill-icons/blob/main/icons/Github-Dark.svg"/>](https://github.com/jvictormo)        |

 

→ [Voltar ao topo](#topo)
