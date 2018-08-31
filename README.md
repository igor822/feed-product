Feed de produtos
==========================

Venho por meio desta proposta, apresentar uma soluão para e-commerces na facilitação para o tráfego de dados entre serviços. 

Inspirado pelo [Google Merchant](https://www.google.com.br/retail/solutions/merchant-center/) podemos criar um padrão para que seja disponível em cada loja que aderir, um arquivo json com informações de produtos.

Com o objetivo de facilitar para que qualquer serviço possa encontrar as informações mais globais de um produto sem prejudicar a performance de um servidor ao ser feita uma requisição de um robô, como pudemos ver com a utilização de [Feed RSS](https://pt.wikipedia.org/wiki/RSS)

## Exemplo

```json
{
    "id": 123,
    "title": "Test 1",
    "description": "Test description",
    "link": "http://store.com/link/product",
    "image_link": "http://store.com/link/product.jpg",
    "price": "100.00 BRL",
    "promo_price": "90.00 BRL",
    "availability": "in_stock",
    "ean": "123456790"
}
```

## Beneficiados

Ao existir um "feed" de produtos, serviços como [Buscapé](https://www.buscape.com.br/), [Admatic](https://www.admatic.com.br/) ou qualquer serviço de monitoração de preços poderá se beneficiar com esse padrão, excluindo a necessidade de criar um robô para fazer o mesmo.

## Campos

| Atributo      | Descrição                                                                         |
|-              |-                                                                                  |
| Id            | Id único do produto, podendo utilizar o sku como referência                       | 
| Title         | Nome do produto                                                                   |
| Description   | Detalhes do produto                                                               |
| Link          | Url direta do produto                                                             |
| Image link    | Link da imagem principal do produto                                               |
| Price         | Preço final do produto com formato `12.00 BRL`                                    |
| Promo price   | Preço promocional do produto, mesmo formato do preço                              |
| Availability  | Disponibilidade do produto, podendo ser `in_stock`, `out_of_stock` ou `pre_order` |
| Ean           | Identificação global do produto                                                   |
