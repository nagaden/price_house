# price_house
Projeto com foco em datacleaning e pré-processamento de dados. 

O dataset originalmente está no formato json, e a além dos campos com valores nulos, muitos campos possuem dentro de seu próprio valor outros valores aninhados, tal formato é esperado em arquivos desse tipo.

Para a formatação correta da variável 'target' foi necessário antes segmentar os tipos de imóveis, entre apartamentos, comercial, residências, flats etc..

Após a segmentação desses imóveis foi possível obter seu preço dentro da feature "pricingInfos".

Desse ponto em diante foram criados algumas variáveis como "Sale" para saber se o imóvel se tratava de uma venda ou aluguel, entre outros campos referente ao endereço do anúncio.

Outra forma simples de se aproveitar para preencher valores até então nulos, foi utilizar outros campos como (Bairro, LocationID) para atualizar valores de outros registros com as mesmas características porém não estavam preenchidos. Exemplo, cliente 1234 na rua X com CEP 999. Cliente 5678 na rua X com CEP n/a, posso aproveitar a informação do primeiro cliente.

O campo LocationID forneceu muitas informações importantes, foi apenas uma questão de quebrar a string no tamanho certo.

Para criação do modelo utilizei RandomForest para tal, antes dele testei também decisionTree e XGBRegressor, em combinação disso para os campos categóricos, tratei com HotEnconding por oferecer a melhor performance em questão da criação do modelo. Então combinei randomForest com os campos encodados pelo HotEncoding. 
