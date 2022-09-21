# TFMC - Aplicação desenvolvida pela Engenharia da Qualidade Tech Center para análise da criticidade de QNs com base em Lógica Nebulosa/Fuzzy

[17/09 13:07] Karina Gomes
Nova atualização no repositório, agora somos capazes de fazer as interações entre todas as combinações das variáveis (V2):

https://github.com/Karinagkarim/TechnipFMC-test---Karina/blob/83e6ca3dc2c404017e526df4a6c3f67250d50579/CNQ_TFMC.ipynb

Referências utilizadas:

Para Elif statement (junção de if com else em um mesmo loop de interação)

https://www.datacamp.com/tutorial/python-if-elif-else?irclickid=QKdxcWzG2xyNThBzSnzjQ0WLUkDWKU0XbwBlTE0&irgwc=1&utm_medium=affiliate&utm_source=impact&utm_campaign=000000_1-1310690_2-mix_3-all_4-na_5-na_6-na_7-mp_8-affl-ip_9-na_10-bau_11-Admitad%20-%201310690&utm_content=TEXT_LINK

Para lambda function (para chamar funções cujas variáveis serão funções):

https://www.programiz.com/python-programming/anonymous-function

Para Itertools (biblioteca para combinações):

https://www.youtube.com/watch?v=5iWpdouaKrU

https://docs.python.org/3/library/itertools.html

https://linuxhint.com/python-itertools-combinations/

Para Map function (aplicar funções em todos os itens de uma lista:

https://www.hashtagtreinamentos.com/map-no-python?gclid=CjwKCAjw4JWZBhApEiwAtJUN0K-9SXRXdKv2YuVChQcog2gfnS7_aF7Abf2DUlKBOh_wk7h_qGREthoCzboQAvD_BwE

Para tuple function (para indexar a lista após as interações)
https://www.w3schools.com/python/python_tuples_access.asp


Passos futuros estão descritos ao final do código, no repositório. 



17/09/2022 Próximos passos:

1) Definir como vamos tratar os subconjuntos derivados das combinações.

Dúvidas:

a) Como iremos trabalhar com o nível de TRL do equipamento associado à QN?

b) Estamos basicamente considerando os valores mais críticos entre as variáveis, essa seria a melhor estratégia? Acredito que vai depender de como iremos trbalhar com as informações resultantes. Talvez um tempo avaliando os processamentos com nossos bancos de dados reais possa ser um bom indicativo do compartamento dos desvios. Poderíamos buscar pelas variáveis (ou combinações) que mais influenciaram nos desvios por tipo de equipamento e/ou por tipo de processo (SIT x Qualificação), por exemplo.

2) Processar bancos de dados de SIT e qualificação para comparar
CNQ_TFMC.ipynb
Karinagkarim/TechnipFMC-test---Karina

21/09/2022 Validação com o time

1) Dentro do loop da combinação, substituir a ação de selecionar o maior peso entre as duas variáveis para obter o produto entre ambos os pesos. Assim, teremos a influência de ambas as variáveis. Ação pendente

2) Chegamos à conslusão de que a variável TRL é mais um balizador para classificação do comportamento do modelo do que uma variável de influência que gera tomada de decisão, pois, não temos ação/controle sobre o nível de TRL que entra para testes no GOPI.

Qualificação -> TRL 4 ou 5 | SIT -> TRL 6 ou 7

Portanto, Dividiremos as segmentações dos resultados em 2 camadas de análise:

Camada 1: Comportamento por nível de TRL Camada 2: Comportamento por família do produto dentro do nível de TRL

Será necessário retirar o TRL do loop de combinações. Ação Pendente

3) Entrarei em contato com Hugo Moacir e/ou Tomás Aquino para entender como o time de confiabilidade captura e processa os dados que indicam probabilidade de ocorrência de determinado desvio/causa. Ação Pendente

4) Precisamos do banco de dados do SIT de LIZA e de Búzios & Marlim para rodar no modelo e verificar o comportamento. Ação Pendente - Michelle Trugilho

5) Depois que esses dados rodarem no modelo, iremos comparar o comportamento da variável que mais se destacar criticamente dentro do universo de QN com a soma da combinação de outras variáveis que apresentam o produto com maior representatividade que a variável isolada.

EX: QN xxxxx com custo de criticidade 5; QN yyyyyy com a.b=6 e c.a=8

Qual a representatividade que o custo de a+b+c da QN yyyyyy tem em relação ao CNQ da QN xxxxxx?

Ação pendente até a ação 4 ser finalizada

