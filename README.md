# cognitivo-wine

### Como foi a definição da sua estratégia de modelagem?

A estratégia foi definida atravé da análise das variáveis, presente no notebook `2_Exploração_Dados.ipynb`. Decidi por modelar o problema através de uma regressão, pois acredito que desta seja mais fácil generalizar o problema.

### Como foi definida a função de custo utilizada?

Utilizei o `RMSE` pois a variável resposta é limitada.

### Qual foi o critério utilizado na seleção do modelo final?

Ainda não estou satisfeito com o modelos apresentados, porém dentre eles, o modelo de Florestas Aleatórias apresentou um melhor $r^2$ e correlação entre previsão e realidade. 

### Qual foi o critério utilizado para validação do modelo? Por que escolheu utilizar este método?

Utilizei 15% da base, escolhidos aleatóriamente, como dados *out of sample* para validação. Utilizei este percentual, pois é sufciente para ter uma boa validação (~1k pontos)

### Quais evidências você possui de que seu modelo é suficientemente bom?

Ainda não estou contente com o modelo. Creio que consigo melhorar a performance do mesmo através de algumas transformações das variáveis ou modelando os tipos Tinto e Branco separadamente.

O Melhor modelo atualmente tem $r^2 = .48$ 