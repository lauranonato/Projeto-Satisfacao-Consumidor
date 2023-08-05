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


3º Feature Engineering: criação de features úteis para o modelo como entrega do produto
 
  -arrival_time: indica se o produto foi entregue com ou sem atraso
 
  -review_score: sinaliza se a avaliação foi boa ou ruim 
 
  transformações de variaveis dummies
  
  -status pedido: transforma em uma variavel numérica
  
  -tipo de pagamento: transforma em uma variavel numérica
  
  
4º Aplicação do modelo: utilizando o modelo de árvore de decisão foi possível identificar que tempo de entrega e atraso da entrega são as variáveis que mais estão influenciando na decisão do cliente avaliar a satisfação com o serviço.
O primeiro teste com o algoritmo obteve uma acurácia de 86% identificando 19.690 registros com satisfação positiva. 
O resultado do modelo foi bastante satisfatório em identificar a avaliação do cliente, dado que no dataset real a maioria das avaliações se concentram entre 4 e 5.
 <img src="https://github.com/lauranonato/Projeto-Satisfacao-Consumidor/assets/56266061/104d1628-79f8-4b7c-a059-ac1c2fce2dff"width="200" /> 



**Analise desenvolvida com o desafio oferecido pela comunidade Mulheres em Dados:** (https://www.linkedin.com/posts/mulheresemdados_desafio-python-iniciante-activity-6942208393260449792-6M3C?utm_source=linkedin_share&utm_medium=member_desktop_web)
