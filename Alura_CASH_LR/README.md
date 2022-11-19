# Semana 2

## Criando modelo de classificação 👩‍💻

Nessa segunda semana tive alguns perrengues, porém consegui concluir esse modelo de classificação para o Alura Cash. 
Primeiramente eu importei toda as bibliotecas que iria precisar, juntamente com os dados exportados da primeira etapa do projeto. Depois de determinar quais _features_ 
seriam necessárias para o modelo, exclui todas as outras que estariam atrapalhando o aprendizado da nossa máquina. Precisei fazer um tratamento de dados nulos e repetidos, necessitando excluir algumas colunas
desnecessárias. Após terminado esse processo, precisei fazer a identificação e tratamento de _outliers_, conjunto de dados que aprensentam uma quantidade exarcebante das 
demais, e, com isso, acabam atrapalhando nossa classificação. Fiz o _encoding_ de variáveis categóricas, transformando elas em valores numéricos para passar pelo classificador
e, finalmente, cheguei na parte a qual me deparei com problemas: o desbalanceamento de variáveis alvo. Como previsto, nossos dados da variável alvo (PESSOA_INADIMPLENTE) 
possuia uma diferença significativa entre 1 (pessoa inadimplente) e 0 (pessoa não-inadimplente) a qual para 0 tínhamos bem mais dados do que 1. Para solucionar esse problema,
eu fiz uma extensa pesquisa de qual algoritmo seria adequado para o problema. Escolhi o Near Miss, um algoritmo do tipo Undersampling que "consiste manter todos os dados da classe com menor 
frequência e diminuir a quantidade dos que estão na classe de maior frequência, fazendo com que as observações no conjunto possuam dados com a variável alvo equilibrada.".
A aplicação do Near Miss foi bem simples, na verdade. Utilizei sua biblioteca python para selecionar uma nova sequência de dados X e Y balanceado. Após isso, apliquei
no modelo de classificação LogisticRegression, ao qual acredito ser o mais adequado para o problema, e, por fim, fiz a validação do modelo através do Score, Confusion_Matrix e
ROC Curve. 

## Considerações
Foi um projeto bem interessante de se fazer e colocou a prova todo meu conhecimento acerca do assunto. Estou aberta a críticas e melhores soluções. Obrigada por 
acompanhar meu projeto até aqui! 🚀
