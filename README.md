# data-science-series-temporais

![Badge em Desenvolvimento](http://img.shields.io/static/v1?label=STATUS&message=EM%20DESENVOLVIMENTO&color=GREEN&style=for-the-badge)

![Badge code size](https://img.shields.io/github/languages/code-size/fab-souza/data-science-series-temporais)
![Badge de Atualização](https://img.shields.io/github/last-commit/fab-souza/data-science-series-temporais)

| :placard: Vitrine.Dev |    |
| -------------  | --- |
| :sparkles: Nome        | **Data Science: análise de séries temporais**
| :label: Tecnologias | python
| :rocket: URL         | 
| :fire: Desafio     | Conteúdo do curso [Data Science: análise de séries temporais](https://www.alura.com.br/curso-online-data-science-series-temporais)

![](https://user-images.githubusercontent.com/67301805/212129044-2344ace3-b75c-42ac-b14e-32a228d09ac1.jpg)

## Sobre o curso 📚

Neste curso, do instrutor [Guilherme Lima](https://www.linkedin.com/in/guilherme-lima-458925178/), foi utilizado sete datasets de diferentes setores, por exemplo uma revendedora de carros, um comércio de chocolate e de uma cafeteria.

![image](https://user-images.githubusercontent.com/67301805/212133115-320d4f75-a412-440c-86b9-709eeeac5075.png)
![image](https://user-images.githubusercontent.com/67301805/212133541-3fc12593-1765-48e3-9aeb-4b94027631e8.png)
![image](https://user-images.githubusercontent.com/67301805/212134153-0c15b7ff-0031-4c9f-995e-7d6354fb33e8.png)

Para analisar suas vendas, diárias ou mensais, o número de assinantes da newsletter, verificar se há tendências e sazonalidade, assim como, gerar e interpretar gráficos com técnicas de decomposição e correlação de séries temporais. 

![image](https://user-images.githubusercontent.com/67301805/212133362-93ce705e-efd7-413c-986d-4b03256cdcdc.png)
![image](https://user-images.githubusercontent.com/67301805/212137116-dc6deee0-5f2a-4e41-95b4-d4f1899ce346.png)



## Minha prática 👩🏻‍💻

Para treinar o que aprendi, utilizei datasets disponíveis no [Kaggle](https://www.kaggle.com/), um referente às vendas diárias, semanais, mensais e por hora de uma [farmácia](https://www.kaggle.com/datasets/milanzdravkovic/pharma-sales-data) e o outro, com os registros de uma [panificadora](https://www.kaggle.com/datasets/hosubjeong/bakery-sales).

Começando pelos dados de venda diária da farmácia, há 2106 linhas e 13 variáveis no dataset, em que oito delas (M01AB, M01AE, N02BA, N02BA, N02BE, N05B, N05C, R03, R06) referem-se ao volume vendido de cada categoria de medicamento, eles estão no formato decimal, porque, segundo o criador do dataset, no país de origem dos dados, é permitido a venda de comprimidos individuais em embalagem. Enquanto as demais variáveis são sobre a data, com o mês, ano e etc.

![image](https://user-images.githubusercontent.com/67301805/213557799-d02d1025-84fb-4117-a305-a26fb0612c4c.png)

Após um rápido tratamento dos dados, a conversão de *string* para *date* e a tradução das variáveis, plotei um  gráfico para cada medicamento e percebi que não obteria algo semelhante ao gráfico feito durante o curso. No caso da Alucar, era a simulação de um negócio em crescimento, pois, ao longo do tempo, o número de vendas foi aumentando. Como apresenta o gráfico feito durante o curso:

![image](https://user-images.githubusercontent.com/67301805/213761386-2a17ca35-7af0-4b37-9b8b-7df1eb72ae1d.png)

Diferente do Alucar, nos dados da farmácia, eu consegui identificar um leve aumento de venda dos medicamentos tipo R03, um queda de venda do N02BA e uma periodicidade nos medicamentos N02BE e R06.

![image](https://user-images.githubusercontent.com/67301805/213762029-634f7713-b492-4a95-b66b-b5f6cbf83c06.png)
![image](https://user-images.githubusercontent.com/67301805/213761705-d007c7da-26ff-4bf0-b336-2a19bd2faab8.png)
![image](https://user-images.githubusercontent.com/67301805/213761756-3148c95e-7bdf-4657-8346-c924e2cc5de7.png)
![image](https://user-images.githubusercontent.com/67301805/213762082-03401a85-b906-481f-b04d-ca8784d447df.png)

A forma que encontrei para emular o gráfico feito no curso, fiz uma lista vazia para receber o valor acumulado de venda do R03 a cada dia e depois plotei o gráfico entre as datas e os valores da lista.

![image](https://user-images.githubusercontent.com/67301805/213779613-9d0aac37-f352-493b-9adc-4e5cc7ade96d.png)



## Ferramentas utilizadas 🧰
<p> <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a> 
    <a href="https://pandas.pydata.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/2ae2a900d2f041da66e950e4d48052658d850630/icons/pandas/pandas-original.svg" alt="pandas" width="40" height="40"/> </a>
    </p>
