# Resultados da análise

Base: 1107 registros. Registros duplicados completos: 2.
Valores ausentes por coluna: {'title': 0, 'Marca': 0, 'Preco_Normal': 0, 'Preco_Desconto': 0, 'Preco_Anterior': 0, 'Desconto': 0, 'Categoria': 0}.
Zeros de desconto foram mantidos, conforme a orientação do curso.
Há 294 preços normais iguais a zero. Eles foram mantidos no
cálculo principal para reproduzir a base do exercício, mas não devem ser interpretados
automaticamente como produtos gratuitos. A tabela sensibilidade_sem_precos_zero.csv
permite comparar o efeito de excluí-los sem substituir os resultados principais.
Os preços são da base chilena; não foram convertidos para reais.

## Média e mediana
Cada média é comparada à mediana da própria categoria.

                            quantidade        media  mediana  desvio_padrao media_vs_mediana
Categoria                                                                                   
belleza-y-cuidado-personal         239  1783.556485   1569.0    2210.041719            acima
comidas-preparadas                  46  3095.043478   3290.0    2019.911428           abaixo
congelados                         235  2108.042553   1519.0    2111.539896            acima
frutas                              19  1724.473684   1195.0    1639.151114            acima
instantaneos-y-sopas                57   765.491228    439.0    1170.232869            acima
lacteos                            447  2385.219239    989.0    3925.816164            acima
verduras                            64  1343.296875   1180.0    1012.699625            acima

## Maior dispersão e boxplot
A categoria lacteos apresenta o maior desvio padrão amostral: 3925.82.
Sua média é 2385.22 e sua mediana é 989.00.
Média acima da mediana é compatível com uma cauda de preços altos; a comparação
isolada não prova o formato da distribuição. O desvio padrão é sensível aos extremos.
Nas três categorias com maior desvio (lacteos, belleza-y-cuidado-personal e congelados),
a média supera a mediana. No boxplot de lácteos, a mediana fica próxima à base da
caixa e há uma longa cauda superior: os preços altos elevam a média.

Q1 = 269.00; Q3 = 2609.00; IQR = 2340.00.
Limites de Tukey: -3241.00 e 6119.00.
Foram identificados 43 outliers entre 447 preços válidos
(9.62%). Os pontos além dos bigodes são esses registros;
os bigodes terminam nos valores observados dentro dos limites.
Outliers não são necessariamente erros e foram preservados na análise.

## Descontos
Maior média de desconto: congelados (154.03).
A média inclui produtos sem desconto. Não foi atribuída unidade percentual
à coluna Desconto sem confirmação no material.
No treemap, clique numa categoria para explorar marcas e passe o mouse para ver
o desconto médio. Área representa quantidade, não soma das médias de desconto.
