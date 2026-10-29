# Estatística descritiva — EBAC, módulo 13

Análise de 1.107 registros de produtos de um supermercado chileno, com pandas,
Matplotlib e Plotly. Material original do curso preservado.

## Como executar

```powershell
python -m pip install -r requirements.txt
python analise.py
```

Abra `Resolucao_M13.ipynb` para acompanhar os cálculos em etapas.
Para exportar também a imagem do treemap, com Chrome instalado:

```powershell
python analise.py --exportar-mapa
```

## Entrega

- `resultados/boxplot.png`: distribuição dos preços de lácteos.
- `resultados/barras.png`: desconto médio por categoria, incluindo descontos zero.
- `resultados/mapa.png`: imagem do treemap.
- `resultados/mapa_interativo.html`: treemap completo, utilizável sem internet.
- `resultados/interpretacao.md`: respostas e interpretação dos resultados.
- `resultados/outliers.csv`: os 43 registros acima do limite de 6.119.
- Tabelas CSV com estatísticas por categoria e descontos por categoria/marca.

## Principais resultados e critérios

A média de preço supera a mediana da própria categoria em seis categorias.
Em `comidas-preparadas`, fica abaixo (3.095,04 contra 3.290,00).
Lácteos têm o maior desvio padrão amostral (3.925,82), média 2.385,22 e
mediana 989,00. Os 43 outliers superiores correspondem a 9,62% dos 447
registros da categoria. O boxplot usa a regra de 1,5 vez o intervalo interquartil.
Congelados apresentam o maior desconto médio (154,03 na unidade da base).

O treemap usa categoria e marca como hierarquia, quantidade como área e desconto
médio como cor. As médias dos níveis superiores são ponderadas pela quantidade.

Há 294 preços normais zero e duas linhas duplicadas. Ambos foram preservados
para reproduzir a base didática; não se presume que preço zero indique gratuidade.
A tabela `sensibilidade_sem_precos_zero.csv` mostra uma análise complementar
apenas com preços positivos. Não há valores ausentes. O desvio padrão usa ddof=1.
Preços não foram convertidos para reais; desconto não foi tratado como percentual.

Repositório: https://github.com/oPauLoHiga/ebac_estatistica
