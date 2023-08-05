**Projeto: satisfação dos consumidores de um e-commerce** 🔎🎲

**Objetivo**: a partir de um conjunto de dados de ecommerce do Brasil, realizar análise exploratória, preparar features, indicadores e data set final para a criação de um modelo que prevê a satisfação dos clientes.

**Toolkit do projeto**: python e jupyternotebook

**Fonte dos dados:** dataset público sobre o comércio eletrônico brasileiro durante o período de 2016 a 2018 e está disponível na Kaggle https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

**Etapas do projeto**

1º Preparação dos dados: leitura, união das tabelas, tratamento e seleção das informações utilizadas na análise.

**Dicionário dos dados**

| atributo  | descrição |
| ------------- | ------------- |
|order_status|status do pedido (entregue ou cancelado) (delivered or canceled)|
|order_purchase_timestamp|timestamp (data/hora) da compra de cada item|
|order_delivered_customer_date|data real de entrega do pedido do cliente|
|order_estimated_delievy_date| data de entrega estimada que foi fornecida ao cliente no momento da compra|
|shipping_limit_date|data limite de envio do vendedor para a transferência do pedido ao parceiro logístico|
|payment_sequential|método de pagamento utilizado pelo consumidor|
|payment_type|método de pagamento preferido do cliente|
|payment_installments|número de parcelas de pagamento preferido do cliente|
|payment_value| valor da transação|
|price|custo de cada item|
|freight_value|custo de transporte para cada item (se um pedido tiver mais de um item, o valor do frete é dividido entre os itens)|
|product_category|categoria de cada item|
|product_name_length|número de caracteres extraídos do nome do produto|
|product_description_length|número de caracteres extraídos da descrição do produto|
|product_photos_qty|número de fotos de produtos que foram publicadas|
|review_score|classificação dada por um cliente em uma pesquisa de satisfação que varia de 1 a 5|
|customer_city|cidade do cliente|
|customer_state|estado (uf) do cliente|

2º Análise exploratória: 

**forma de pagamento e valor dos pedidos**

os pedidos pagos majoritariamente por crédito, em média custam 175,00, por débito e os pagamentos por voucher tem a menor representatividade, representando em média 75,00.

a plataforma tem variadedade do mix de produtos no portifólio, contempla até 70 categorias e identifiquei que as mais relevantes em volume de vendas são cama mesa e banho, beleza e saúde, esporte e lazer e moveis decorativos respectivamente, indicando que o segmento doméstico é o carro chefe do marketplace.

O faturamento dos pedidos representam a mediana de 171,00 com um alto desvio padrão, isso possívelmente devido a diversidade de categorias, variação de preço, etc.

**correlações**

foi possível identificar que as variáveis preço e satisfação estão sempre relacionadas, onde os pedidos mais caros tiveram maiores notas de satisfação, as baixas avaliações concentram com pedidos de menor preço, 
bem como a maior parte das boas avaliações (4 e 5) ocorre quando o valor do pagamento e preço tem o mesmo valor.
![image](https://github.com/lauranonato/Projeto-Satisfacao-Consumidor/assets/56266061/4386c28b-93f1-467e-93d2-8016541990e6)


aqui também foi interessante verificar que pedidos com alta avaliação foram entregues até antes que a estimativa de entrega fornecida pela plataforma. Entre as avaliações negativas de 1 e 2, a estimativa de entrega apontava para poucos dias mas os dias de entrega de fato passaram do tempo esperado pelo cliente.
![image](https://github.com/lauranonato/Projeto-Satisfacao-Consumidor/assets/56266061/5d3c7c97-7287-4a64-8955-925f2f2c2bc2)

**tempo de entrega**

O frete custa em média 20,00 e contém muitos outliers chegando a pedidos com frete de 400,00 e grande maioria dos pedidos chegam em até 30 dias de entrega.


3º Feature Engineering: criação de features úteis para o modelo como entrega do produto
 
  -arrival_time: indica se o produto foi entregue com ou sem atraso
 
  -review_score: sinaliza se a avaliação foi boa ou ruim 
 
  transformações de variaveis dummies
  
  -status pedido: transforma em uma variavel numérica
  
  -tipo de pagamento: transforma em uma variavel numérica
  
  
4º Aplicação do modelo: utilizando o modelo de árvore de decisão foi possível identificar que tempo de entrega e atraso da entrega são as variáveis que mais estão influenciando na decisão do cliente avaliar a satisfação com o serviço.
O primeiro teste com o algoritmo obteve uma acurácia de 86% identificando 19.690 registros com satisfação positiva. 
O resultado do modelo foi bastante satisfatório em identificar a avaliação do cliente, dado que no dataset real a maioria das avaliações se concentram de 3,5 a 5.


**Analise desenvolvida com o desafio oferecido pela comunidade Mulheres em Dados:** (https://www.linkedin.com/posts/mulheresemdados_desafio-python-iniciante-activity-6942208393260449792-6M3C?utm_source=linkedin_share&utm_medium=member_desktop_web)
