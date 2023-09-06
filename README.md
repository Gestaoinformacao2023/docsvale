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
:small_blue_diamond: [Layout da Aplicação](#layout-da-aplicação)

:small_blue_diamond: [Descrição do projeto](#descrição-do-projeto)

:small_blue_diamond: [Pré-requisitos](#pré-requisitos)

:small_blue_diamond: [Origem e Especificação dos Dados](#origem-e-especificação-dos-dados)

:small_blue_diamond: [Ambiente de Desenvolvimento](#ambiente-de-desenvolvimento)

:small_blue_diamond: [Modelo da Arquitetura Sugerida](#modelo-da-arquitetura-sugerida)

:small_blue_diamond: [Dicionário de Dados](#dicionario-de-dados)   

:small_blue_diamond: [Processo e Desenvolvimento](#processo-e-desenvolvimento) 
... 

## Layout da Aplicação

[Link do deploy da aplicação. Exemplo com netlify.](https://colab.research.google.com/drive/1KWrzLNsES9QYDs36YjI5uD5F8qBv-mhJ?usp=sharing)

## <a id="Descrição do projeto"></a>descrição-do-projeto

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

## Pré-requisitos

:warning: Certifique-se de usar para desenvolvimento [Python](https://www.python.org/downloads/) e [Databricks](https://databricks.com/).



## <a id="modelo-da-arquitetura-sugerida"></a>Modelo da Arquitetura Sugerida

<p align="justify">
<img width="414" alt="image" src="https://github.com/Gestaoinformacao2023/docsvale/assets/144237804/21b43255-daa7-4dd8-b0f7-7cc52455449e">
</p>

## <a id="dicionario-de-dados"></a>Dicionário de Dados

<p align="justify">
<img width="415" alt="image" src="https://github.com/Gestaoinformacao2023/docsvale/assets/144237804/2206e88e-2be2-4968-850b-693c9674f47f">
</p>





## <a id="processo-e-desenvolvimento"></a>Processo e Desenvolvimento
<p align="justify">
As atividades desenvolvidas para a conclusão do projeto foram as seguintes:
1. Criação da function de extração de dados do Twitter.
(a) Para extração de dados do twitter foi registrada uma conta de desenvolvedor no twitter, para
obter a API de extração.
(b) Essa API foi executada dentro de um código python na function, para converte-los para texto
e traduzir em um algoritmo que utiliza a API Google Translate. Em seguida, os dados são
enviados para um modelo de aprendizado de máquina por meio de um endpoint, a fim de serem
categorizados. Assim finalmente podem ser enviados para o banco de dados do cosmosDB.
2. Criação do Power Apps para receber reclamações de clientes;
(a) Na plataforma do Power Apps foi criado um template para receber a entrada de dados de
reclamações de clientes.
(b) O app foi criado com cinco campos de entrada, sendo o primeiro destinado ao email do cliente,
outro para o perfil do Twitter(caso ele possua), dois criados em forma de Lista Suspensa -
a primeira lista apresenta os Produtos que o sistema oferece, a segunda seus Tipos que são
filtrados pelo Produto selecionado. O último campo é um Input Text destinado a receber o
texto da narrativa do reclamante.
3. Criação do fluxo no Power Automate para extrair dados de reclamação do email e do app;
(a) Foram criados dois fluxos no Power Automate, ambos com uma trigger que é acionada toda
vez que uma reclamação é remetida no app e/ou um e-mail é recebido no endereço cadastrado.
(b) O fluxo do app coleta as informações inseridas através dele no Sharepoint e faz o envio desses
dados para serem armazenadas no CosmosDB.
(c) O fluxo do e-mail coleta os dados do endereço de e-mail do remetente, o assunto e corpo do
e-mail e sua hora de recebimento. Em seguida armazena essas informações no Sharepoint e no
CosmosDB.
4. Criação de collection no CosmosDb;
(a) Foram criadas duas collections uma para receber os dados brutos, e outra para receber os
dados categorizados pelo machine learning.
5. Tratamento de dados de reclamações de clientes, treinamento e implementação modelo de machine
learning;
(a) No azure machine learning notebook foi feito o tratamento de dados, no qual foram extraídos
valores nulos, renomeadas colunas, seleção de atributos, padronização de dados, vetorização
de dados de linguagem natural, separação da base em treino e teste, entre outros.
(b) Ainda no Machine learning Studio, foi treinado o modelo de regressão logística multinomial,
foi validado, e preparado o ambiente de deploy. Ao fim foi implementado e gerado o endpoint
de consumo do modelo.
6. Integrar endpoint do modelo de machine learning com azure functions;
(a) A integração do modelo de machine learning com o Azure Functions é uma maneira eficiente
de implantar um modelo de aprendizado de máquina em uma arquitetura serverless. Essa
integração foi realizada através do uso de um endpoint do modelo, que pode ser chamado pelo
Azure Functions. O Azure Functions permite que o modelo seja executado apenas quando
necessário, reduzindo os custos e aumentando a eficiência da solução.
(b) O código do azure functions utiliza o endpoint em uma etapa do processo, na qual os dados o
twitter já foram extraídos, o algoritmo de tradução de texto já foi executado, convertendo o
texto para lingua inglesa. Então finalmente é feito um request ao modelo de machine learning
enviando os dados do twitter para o modelo.
7. Integrar o fluxo de dados com CosmosDB;
(a) Todas as conexões necessárias para que fosse integrado os dados que entravam através do e-
mail e do app com o banco de dados(CosmosDB) foram feitas através dos próprios conectores
existentes nas ferramentas utilizadas para essa solução, sendo elas o Power Apps e Power
Automate.
8. Criar dashboard do PowerBI;
(a) Realiza-se o estabelecimento de conexão com o banco de dados Cosmos DB por meio das
credenciais fornecidas, visando à extração dos dados para fins de análise
(b) Executa-se a fase de limpeza e formatação de colunas e tabelas no Power Query, com o intuito
de prosseguir na elaboração do painel de controle no Power BI.



</p>
...



## Como rodar a aplicação :arrow_forward:

No terminal, clone o projeto: 

```
[https://github.com/Gestaoinformacao2023/docsvale]
```

# 🚀 Usando o Git para Clonar e Versionar no GitHub

**Git** é uma ferramenta essencial de controle de versão distribuído. Ele permite aos desenvolvedores rastrear e gerenciar as mudanças no código ao longo do tempo. Abaixo, detalharei como você pode clonar um projeto e gerenciar seu código usando Git e GitHub.

## 🔍 Pré-requisitos

- **Git**: Certifique-se de que o Git esteja instalado em sua máquina. Se não, faça o [download e instale a partir do site oficial](https://git-scm.com/).

## 📥 Como clonar um repositório

1. Abra o terminal ou prompt de comando em sua máquina.
2. Navegue até o diretório onde deseja clonar o repositório.
3. Execute o comando:
 
### git clone https://github.com/Gestaoinformacao2023/docsvale

## 🔄 Usando o Git para Versionamento

1. `git status`: Use esse comando para verificar o status dos seus arquivos.
2. `git add [NOME_DO_ARQUIVO/.]`: Use esse comando para adicionar arquivos ao "staging area".
3. `git commit -m "Sua mensagem descritiva aqui"`: Crie um novo "commit" com os arquivos.
4. `git push`: Envie seus commits para o repositório remoto no GitHub.
5. `git pull`: Use esse comando para buscar as últimas alterações do repositório remoto.
   
### git clone https://github.com/Gestaoinformacao2023/docsvale

# 🛠️ Dependências e Bibliotecas

Antes de rodar a aplicação, certifique-se de instalar todas as dependências e bibliotecas necessárias.

### git clone https://github.com/Gestaoinformacao2023/docsvale

# 🚀 Como rodar a aplicação

1. **Clone o projeto**:
### git clone https://github.com/Gestaoinformacao2023/docsvale

2. **Navegue até o diretório do projeto**:

### cd [nome-do-diretorio-do-projeto]

3. **Instale as dependências**:

### npm install


4. **Execute a aplicação**:

### npm start


# 🧪 Como rodar os testes

1. **Navegue até o diretório do projeto (se ainda não estiver nele)**:

### cd [nome-do-diretorio-do-projeto]


2. **Execute os testes**:

### npm test

Lembre-se: os comandos específicos para rodar a aplicação e os testes podem variar com base na configuração e nas ferramentas usadas no projeto. Certifique-se de consultar a documentação do projeto para obter instruções detalhadas.

Agora você pode copiar este conteúdo e colar no README ou qualquer outro arquivo Markdown do GitHub. Ele foi formatado especificamente para se parecer bem no GitHub.






marcell https://ibb.co/pb2NQCL



### Usuários: 

| name | email | 
| ----- | ----- |
| Flavio Assis | flavio.assis@vale.com | 
| Marcell Felipe | C0669610@vale.com | 
| Marcos Lourenço | marcos.lourenco@vale.com | 



## Linguagens, dependencias e libs utilizadas :books:

- [SQL](https://www.w3schools.com/sql/)
- [Databricks](https://databricks.com/)
- [PySpark](https://spark.apache.org/docs/latest/api/python/index.html)




## Tarefas em aberto

Se for o caso, liste tarefas/funcionalidades que ainda precisam ser implementadas na sua aplicação

:memo: Tarefa 1 

:memo: Tarefa 2 

:memo: Tarefa 3 

## Desenvolvedores/Contribuintes :octocat:

Liste o time responsável pelo desenvolvimento do projeto

| [<img src="https://github.com/Gestaoinformacao2023/docsvale/assets/144237804/abf7538f-2cc6-44af-80ef-a82e08a70048" width=115><br><sub>Flávio</sub>](https://github.com/link-do-perfil-do-flavio) | [<img src="https://github.com/Gestaoinformacao2023/docsvale/assets/144237804/e68dd04a-6d18-421b-8d9c-86a440dae2e0" width=115><br><sub>Marcos</sub>](https://github.com/link-do-perfil-do-marcos) | [<img src="https://github.com/Gestaoinformacao2023/docsvale/assets/144237804/000c1b93-e8f9-421a-bad2-e21f98b3b75c" width=115><br><sub>Marcell</sub>](https://github.com/link-do-perfil-do-marcell) |
| :---: | :---: | :---: |






## Licença 

The [Vale]() (Vale)

Copyright :copyright: 2023 - Modelo de documentação
