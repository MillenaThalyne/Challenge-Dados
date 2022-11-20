# Challenge Dados
Esse projeto é desenvolvido através do Challenge de Ciência de Dados da Alura. 
Este tem como objetivo fazer a classificação de pessoas inadimplentes da empresa Alura Cash, através de um modelo de Machine Learning.
Ele será desenvolvido através da base de dados disponibilizada pela Alura, porém eu farei o tratamento dos dados e todo o resto do projeto sozinha.

> **Data de início** : 29/08/22 

> **Linguagem utilizada** : Python 

> **Banco de dados** : MySQL

> **Visualização de dados** : Power BI

# Semana 1
## Adicionando Banco de Dados e Tratando no Workbench 

Nessa primeira semana, comecei a organizar os passos que deveriam ser feitos com os dados. Notei algumas inconsistências: dados nulos, dados incertos e incoerentes, além de visivelmente não terem algum critério de organização. 
Minha primeira contribuição foi visualizar a situação, o que os dados queriam me dizer. Dessa forma, descobri que tínhamos informações de inúmeras pessoas, suas condições financeiras, quanto tempo trabalhavam na empresa e se elas já haviam sido inadimplentes no passado. Além de ter a discrição de empréstimos e suas finalidades.
A partir disso, é possível pensarmos a possibilidade de fazer uma predição, mais a frente nas semanas, das pessoas que estão sendo inadimplentes ou terão a intenção no futuro.
Uni as tabelas a partir do campo entre elas em comum (ID), utilizando a tabela IDS, usando INNER JOIN. Agora possuo todos os dados correspondente às pessoas. Exportei para CSV e a primeira semana do desafio está concluída! 🚀🔥 

# Semana 2
## Criando modelo de Classificação 
Nessa segunda semana tive alguns perrengues, porém consegui concluir esse modelo de classificação para o Alura Cash. Primeiramente eu importei toda as bibliotecas que iria precisar, juntamente com os dados exportados da primeira etapa do projeto. Depois de determinar quais features seriam necessárias para o modelo, exclui todas as outras que estariam atrapalhando o aprendizado da nossa máquina. Precisei fazer um tratamento de dados nulos e repetidos, necessitando excluir algumas colunas desnecessárias. Após terminado esse processo, precisei fazer a identificação e tratamento de outliers, conjunto de dados que aprensentam uma quantidade exarcebante das demais, e, com isso, acabam atrapalhando nossa classificação. Fiz o encoding de variáveis categóricas, transformando elas em valores numéricos para passar pelo classificador e, finalmente, cheguei na parte a qual me deparei com problemas: o desbalanceamento de variáveis alvo. Como previsto, nossos dados da variável alvo (PESSOA_INADIMPLENTE) possuia uma diferença significativa entre 1 (pessoa inadimplente) e 0 (pessoa não-inadimplente) a qual para 0 tínhamos bem mais dados do que 1. Para solucionar esse problema, eu fiz uma extensa pesquisa de qual algoritmo seria adequado para o problema. Escolhi o Near Miss, um algoritmo do tipo Undersampling que "consiste manter todos os dados da classe com menor frequência e diminuir a quantidade dos que estão na classe de maior frequência, fazendo com que as observações no conjunto possuam dados com a variável alvo equilibrada.". A aplicação do Near Miss foi bem simples, na verdade. Utilizei sua biblioteca python para selecionar uma nova sequência de dados X e Y balanceado. Após isso, apliquei no modelo de classificação LogisticRegression, ao qual acredito ser o mais adequado para o problema, e, por fim, fiz a validação do modelo através do Score, Confusion_Matrix e ROC Curve.

#alurachallengedados1
