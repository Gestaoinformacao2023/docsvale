# Modelo de documentação

<h1>Modelo de documentação</h1> 

<p align="center">
  <img src="https://img.shields.io/static/v1?label=Databricks&message=platform&color=orange&style=for-the-badge&logo=databricks"/>
  <img src="https://img.shields.io/static/v1?label=Python%20SQL&message=library&color=blue&style=for-the-badge&logo=python"/>
  <img src="https://img.shields.io/static/v1?label=Spark%20SQL&message=framework&color=yellow&style=for-the-badge&logo=apache-spark"/>
  <img src="https://img.shields.io/static/v1?label=PySpark&message=framework&color=blue&style=for-the-badge&logo=apache-spark"/>
  <img src="https://img.shields.io/static/v1?label=Power%20Apps&message=framework&color=blue&style=for-the-badge&logo=microsoft"/>
  <img src="https://img.shields.io/static/v1?label=Power%20Automate&message=tool&color=blue&style=for-the-badge&logo=microsoft"/>
  <img src="https://img.shields.io/static/v1?label=Power%20BI&message=tool&color=yellow&style=for-the-badge&logo=power-bi"/>
  <img src="http://img.shields.io/static/v1?label=TESTES&message=%3E100&color=GREEN&style=for-the-badge"/>
  <img src="http://img.shields.io/static/v1?label=STATUS&message=EM%20DESENVOLVIMENTO&color=RED&style=for-the-badge"/>
  <img src="http://img.shields.io/static/v1?label=STATUS&message=CONCLUIDO&color=GREEN&style=for-the-badge"/>
</p>


> Status do Projeto: :heavy_check_mark: :warning: (concluido, em desenvolvimento, etc)

### Tópicos 

:small_blue_diamond: [Descrição do projeto](#descrição-do-projeto)

:small_blue_diamond: [Pré-requisitos](#pré-requisitos)

:small_blue_diamond: [Origem e Especificação dos Dados](#origem-e-especificação-dos-dados)

:small_blue_diamond: [Ambiente de Desenvolvimento](#ambiente-de-desenvolvimento)
... 


## <a id="descrição-do-projeto"></a>Descrição do projeto 

<p align="justify">
   Este documento visa detalhar todos os objetivos do Projeto Análise do Covid Mundial de um ponto de vista técnico, listando as soluções, premissas e atividades de execução durante a elaboração do projeto.
</p>

## <a id="pré-requisitos"></a>Pré-requisitos

<p align="justify">
  Com o objetivo de quantificar a progressão da COVID-19 em âmbito global, nos foi solicitada uma análise exploratória dos dados. Mapeamos o contágio e avanço da doença mundialmente, classificando os principais países de acordo com critérios como sexo e raça. Além disso, detalhamos as estatísticas por país, separando-as por estados e regiões e destacando os principais eventos em uma linha do tempo.
</p>

## <a id="origem-e-especificação-dos-dados"></a>Origem e Especificação dos Dados

<p align="justify">
   Teremos um arquivo Excel que foi obtido pelo Kaggle. Você pode acessar e baixar o dataset diretamente a partir deste <a href="https://www.kaggle.com/datasets/imdevskp/corona-virus-report" target="_blank">link</a>. Os arquivos disponíveis estão no formato Xlsx e devem seguir um layout específico, que está detalhadamente especificado neste documento.
</p>

## <a id="ambiente-de-desenvolvimento"></a>Ambiente de Desenvolvimento

<p align="justify">
   Jupyter Notebook e Microsoft Power Bi.
</p>

## Funcionalidades

:heavy_check_mark: Funcionalidade 1  

:heavy_check_mark: Funcionalidade 2  

:heavy_check_mark: Funcionalidade 3  

:heavy_check_mark: Funcionalidade 4  

## Layout da Aplicação :dash:

> Link do deploy da aplicação. Exemplo com netlify: (https://colab.research.google.com/drive/1KWrzLNsES9QYDs36YjI5uD5F8qBv-mhJ?usp=sharing)



## Pré-requisitos

:warning: Certifique-se de usar para desenvolvimento [Python](https://www.python.org/downloads/) e [Databricks](https://databricks.com/).


...

Liste todas as dependencias e libs que o usuário deve ter instalado na máquina antes de rodar a aplicação 

## Como rodar a aplicação :arrow_forward:

No terminal, clone o projeto: 

```
[https://github.com/Gestaoinformacao2023/docsvale]
```

... 
Coloque um passo a passo para rodar a sua aplicação. **Dica: clone o próprio projeto e verfique se o passo a passo funciona**

##🚀 Usando o Git para Clonar e Versionar no GitHub
Git é uma ferramenta essencial de controle de versão distribuído. Ele permite aos desenvolvedores rastrear e gerenciar as mudanças no código ao longo do tempo. Abaixo, detalharei como você pode clonar um projeto e gerenciar seu código usando Git e GitHub.

🔍 Pré-requisitos:
Git: Certifique-se de que o Git esteja instalado em sua máquina. Se não, faça o download e instale a partir do site oficial.
📥 Como clonar um repositório:
Abra o terminal ou prompt de comando em sua máquina.
Navegue até o diretório onde deseja clonar o repositório.
Execute o comando:
bash
Copy code
git clone https://github.com/Gestaoinformacao2023/docsvale
🔄 Usando o Git para Versionamento:
git status: Use esse comando para verificar o status dos seus arquivos. Ele irá mostrar quais arquivos foram modificados, quais são novos e quais estão prontos para serem "commitados".

git add [NOME_DO_ARQUIVO/.]: Use esse comando para adicionar arquivos ao "staging area". Se você usar git add ., todos os arquivos modificados serão adicionados.

git commit -m "Sua mensagem descritiva aqui": Crie um novo "commit" com os arquivos que foram adicionados ao "staging area". A mensagem deve descrever claramente as alterações que foram feitas.

git push: Envie seus commits para o repositório remoto no GitHub.

git pull: Use esse comando para buscar as últimas alterações do repositório remoto.

🛠️ Dependências e Bibliotecas:
Antes de rodar a aplicação, certifique-se de instalar todas as dependências e bibliotecas necessárias. Isso pode variar de projeto para projeto, por isso, é fundamental consultar a documentação do projeto ou o arquivo package.json (para projetos Node.js) para obter uma lista completa.

🚀 Como rodar a aplicação:
Clone o projeto:

bash
Copy code
git clone https://github.com/Gestaoinformacao2023/docsvale
Navegue até o diretório do projeto:

bash
Copy code
cd [nome-do-diretorio-do-projeto]
Instale as dependências (a maneira exata pode variar com base no projeto):

bash
Copy code
npm install
Execute a aplicação:

bash
Copy code
npm start
🧪 Como rodar os testes:
Navegue até o diretório do projeto (se ainda não estiver nele):

bash
Copy code
cd [nome-do-diretorio-do-projeto]
Execute os testes:

bash
Copy code
npm test
Lembre-se: os comandos específicos para rodar a aplicação e os testes podem variar com base na configuração e nas ferramentas usadas no projeto. Certifique-se de consultar a documentação do projeto para obter instruções detalhadas.

Você pode copiar e colar o conteúdo acima em seu arquivo README.md no GitHub para fornecer instruções detalhadas para colaboradores e usuários.






### Usuários: 

|name|email|password|token|avatar|
| -------- |-------- |-------- |-------- |-------- |
|Lais Lima|laislima98@hotmail.com|lais123|true|https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcS9-U_HbQAipum9lWln3APcBIwng7T46hdBA42EJv8Hf6Z4fDT3&usqp=CAU|

... 

Se quiser, coloque uma amostra do banco de dados 

## Iniciando/Configurando banco de dados

Se for necessário configurar algo antes de iniciar o banco de dados insira os comandos a serem executados 

## Linguagens, dependencias e libs utilizadas :books:

- [React](https://pt-br.reactjs.org/docs/create-a-new-react-app.html)
- [React PDF](https://react-pdf.org/)

...

Liste as tecnologias utilizadas no projeto que **não** forem reconhecidas pelo Github 

## Resolvendo Problemas :exclamation:

Em [issues]() foram abertos alguns problemas gerados durante o desenvolvimento desse projeto e como foram resolvidos. 

## Tarefas em aberto

Se for o caso, liste tarefas/funcionalidades que ainda precisam ser implementadas na sua aplicação

:memo: Tarefa 1 

:memo: Tarefa 2 

:memo: Tarefa 3 

## Desenvolvedores/Contribuintes :octocat:

Liste o time responsável pelo desenvolvimento do projeto

| [<img src="https://avatars2.githubusercontent.com/u/46378210?s=400&u=071f7791bb03f8e102d835bdb9c2f0d3d24e8a34&v=4" width=115><br><sub>Diana Regina</sub>](https://github.com/Diana-ops) |  [<img src="https://avatars2.githubusercontent.com/u/46378210?s=400&u=071f7791bb03f8e102d835bdb9c2f0d3d24e8a34&v=4" width=115><br><sub>Diana Regina</sub>](https://github.com/Diana-ops) |  [<img src="https://avatars2.githubusercontent.com/u/46378210?s=400&u=071f7791bb03f8e102d835bdb9c2f0d3d24e8a34&v=4" width=115><br><sub>Diana Regina</sub>](https://github.com/Diana-ops) |
| :---: | :---: | :---: 

## Licença 

The [MIT License]() (MIT)

Copyright :copyright: Ano - Titulo do Projeto
