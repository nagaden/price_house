# price_house
Projeto com foco em datacleaning e pré-processamento de dados. 

O dataset originalmente está no formato json, e a além dos campos com valores nulos, muitos campos possuem dentro de seu próprio valor outros valores aninhados, tal formato é esperado em arquivos desse tipo.

Para a formatação correta da variável 'target' foi necessário antes segmentar os tipos de imóveis, entre apartamentos, comercial, residências, flats etc..

Após a segmentação desses imóveis foi possível obter seu preço dentro da feature "pricingInfos".

Desse ponto em diante foram criados algumas variáveis como "Sale" para saber se o imóvel se tratava de uma venda ou aluguel, entre outros campos referente ao endereço do anúncio.
