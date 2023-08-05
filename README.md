**Projeto: satisfação dos consumidores de um e-commerce** 🔎🎲

**Objetivo**: a partir de um conjunto de dados de ecommerce do Brasil, realizar análise exploratória, preparar features, indicadores e data set final para a criação de um modelo que prevê a satisfação dos clientes.

**Toolkit do projeto**: python e jupyternotebook

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

**Fonte dos dados:** https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

**Analise desenvolvida com o desafio oferecido pela comunidade Mulheres em Dados:** (https://www.linkedin.com/posts/mulheresemdados_desafio-python-iniciante-activity-6942208393260449792-6M3C?utm_source=linkedin_share&utm_medium=member_desktop_web)
