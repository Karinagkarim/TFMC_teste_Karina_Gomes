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


