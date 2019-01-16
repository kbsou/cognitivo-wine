# cognitivo-wine

### Como foi a definição da sua estratégia de modelagem?

A estratégia foi definida atravé da análise das variáveis, presente no notebook `2_Exploração_Dados.ipynb`. Decidi por modelar o problema através de uma regressão, pois acredito que desta seja mais fácil generalizar o problema.

### Como foi definida a função de custo utilizada?

Utilizei o `RMSE` pois se trata de um problema de regressão e não encontrei a necessidade de utilizar uma função de custo mais especial.

### Qual foi o critério utilizado na seleção do modelo final?

Criei três modelos, um para o dataset inteiro, e mais dois para cada tipo de vinho, na tentativa de explorar a diferença nas variáveis explicativas para melhorar a performance.

Testei regressão linear Múltipla, de Ridge, Lasso, Florestas Aleatórias e Boosting

Nos três casos a melhor generalização foi nos modelos de Florestas Aleatórias.

Como entendi que a idéia era explorar as relações e não conseguir as melhores métricas a qualquer custo, não fui *full kaggle* e deixei de utilizar modelos mais complexos ou fazer buscas longas de hierparâmetros.

### Qual foi o critério utilizado para validação do modelo? Por que escolheu utilizar este método?

Utilizei 15% da base, escolhidos aleatóriamente, como dados *out of sample* para validação. Utilizei este percentual, pois é sufciente para ter uma boa validação (~1k pontos)

### Quais evidências você possui de que seu modelo é suficientemente bom?

O Modelo com a melhor generalização, foi o de Floresta Aleatória, mantendo $r^2$ próximo a .5 na validação, sendo esta uma performance razoável.

O problema deste tipo de modelo é que ele não generaliza bem para escores não vistos, logo se, por exemplo, tivéssemos vários vinhos nota 10 para classificar, o modelo, provavelmente, erraria, pois não temos nenhum vinho '10' no treino.

Analisando a importância das variáveis dos três modelos, podemos ver que o teor alcóolico é de principal importância, seguid do variáveis diferentes para cada tipo de vinho.

Me parece que o escore dos vinhos não segue uma relação muito clara com as variáveis dadas, o que faz certo sentido, pois se trata de uma medida subjetiva para cada avaliador humano.