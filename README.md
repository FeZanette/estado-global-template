# template-estado-global
### link do codesandbox
https://codesandbox.io/s/estado-global-template-ykpd4w


RESOLUÇÃO PASSO-A-PASSO:

1. Analisar a estrutura do código:

App ->  Router ->   Mercadinho  ->  CardFrutas
                    Carrinho    ->  CardCarrinho

2. Arquivo frutaria.json tem um array com 3 objetos com: id, name, url e price

3. Passar por props as informações que vem do Mercadinho para o CardFrutas:
- No Mercadinho, em <FrutasContainer>, fazer o map do estado frutas e retorna o <CardFrutas/> com a key e passa as props com as informações (image, name, price, id, comprar). Com isso, os Cards serão renderizados.
- No CardFrutas, substituir as strings pelas props (image, name, price, id, comprar) dentro do CardContainer. As props já estão sendo chamadas desestruturadas na função CardFrutas.

4. Router é o pai comum de Mercadinho e Carrinho. Criar no Router o estado carrinho e passar nos Route por props.
- No Mercadinho e no Carrinho, receber por props desestruturada o estado e a função na função Mercadinho e Carrinho.
- No Mercadinho descomentar a função comprar 
- No Carrinho descomentar a variável precoTotal e a função remover

5. No Carrinho, fazer o map do estado carrinho que vem do Router e retorna o CardCarrinho com a key e passar as props com as informações (id, url, name, amount, price, remover).
- No CardCarrinho, substituir as strings pelas props (id, url, name, amount, price, remover) dentro do CardContainer. As props já estão sendo chamadas desestruturadas na função CardCarrinho.

