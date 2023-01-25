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
![image](https://user-images.githubusercontent.com/67301805/213884762-3bda9a8b-902f-4f66-9bf1-fca58a16e107.png)

Visualizar os gráficos separadamente e ter que procurá-los ao longo da página acaba se tornando um ‘atrito’ na hora de analisar os dados, por isso também aprendemos como plotar os gráficos juntos e facilitar a visualização.

![grafico triplo](https://user-images.githubusercontent.com/67301805/214390422-84c35ec1-3f0e-4cc6-bf5b-c80bfb3705db.png)






## Minha prática 👩🏻‍💻

Para treinar o que aprendi, utilizei datasets disponíveis no [Kaggle](https://www.kaggle.com/), um referente às vendas diárias, semanais, mensais e por hora de uma [farmácia](https://www.kaggle.com/datasets/milanzdravkovic/pharma-sales-data) e mais um com os registros de uma [panificadora](https://www.kaggle.com/datasets/hosubjeong/bakery-sales).

Começando pelos dados de venda mensal de farmácia, há 70 linhas e 9 variáveis no dataset, em que oito delas (M01AB, M01AE, N02BA, N02BE, N05B, N05C, R03, R06) referem-se ao volume vendido de categorias de medicamento.


* M01AB - Produtos antiinflamatórios e anti reumáticos, não esteróides, derivados do ácido acético e substâncias relacionadas;
* M01AE - Produtos antiinflamatórios e anti reumáticos, não esteróides, derivados do ácido propiônico;
* N02BA - Outros analgésicos e antipiréticos, Ácido salicílico e derivados;
* N02BE/B - Outros analgésicos e antipiréticos, Pirazolonas e Anilidas;
* N05B - Drogas psicolépticas, Drogas ansiolíticas;
* N05C - Medicamentos psicolépticos, medicamentos hipnóticos e sedativos;
* R03 - Medicamentos para doenças obstrutivas das vias aéreas;
* R06 - Anti-histamínicos de uso sistêmico.

![dataframe1](https://user-images.githubusercontent.com/67301805/214155586-f807ee91-9e5e-4adb-adab-7055bd5223dd.png)

Eles estão no formato decimal, porque, segundo o criador do dataset, no país de origem dos dados, é permitida a venda de comprimidos individuais em embalagem.

Após um rápido tratamento dos dados, conversão de *string* para *date* e a tradução de variável, plotei um gráfico para cada medicamento e escolhi trabalhar com o R03, porque ele foi o único que apresentou vendas em crescimento. Até o início de 2019, é possível observar uma inclinação positiva das vendas e depois, até o término do dataset, há um número menor de vendas desses produtos.

![graficoR03](https://user-images.githubusercontent.com/67301805/214155774-dbcc4074-35db-452b-b8ca-a2ec0976cc8c.png)

Para aprofundar essa análise, usei a função *.diff()* nas vendas mensais do R03. Essa função calcula a diferença entre os registros do dataframe, retirando a necessidade de fazer um *for* ou de criar algo ‘na unha’ para executar este cálculo. Fazer esta operação significa decompor os dados, que é uma forma de verificar quanto foi o aumento das vendas do medicamento. Ao plotar o gráfico, observa-se que não houve um aumento constante das vendas, na maior parte dele, os registros oscilam próximos as escalas 100 e -100, porém ao longo do tempo, os picos de vendas ficam próximos a 100 e ultrapassa essa marca mais vezes do que na queda de vendas, até chegar ao final de 2018, em que houve o ápice das vendas e depois a redução desses números.

![grafico 2 editado](https://user-images.githubusercontent.com/67301805/214289241-c022a9d2-c551-4bbe-97e5-935f4e1aa53f.jpg)

Fiz o mesmo processo para o medicamento N02BA, porém ao contrário do que aconteceu com o R03, a venda deste produto vai decaindo ao longo da análise.

![graficoN02BA](https://user-images.githubusercontent.com/67301805/214647248-dc2689e9-b992-4977-9761-e6d364b4aa7e.png)

Passando para o medicamento R06, ele apresenta uma sazonalidade, pois suas vendas são baixas no começo e final de ano, mas são altas a partir do mês de maio, aproximadamente. 

![graficoR06](https://user-images.githubusercontent.com/67301805/214676634-acf701fb-7602-441c-b6f0-82f74dcd322c.png)

Ao pesquisar o que são medicamentos Anti-histamínicos de uso sistêmico, eles são indicados para tratamento de: rinite alérgica, asma e urticária (Fonte: [UFJF](https://www.ufjf.br/farmacologia/files/2015/03/Anti-histam%C3%ADnicos.pdf)). 
Porém não consegui identificar o que pode causar as vendas sazonais, já que essas doenças podem ser causadas através da inalação de substâncias, pelos de animais, mofo, uso de outros medicamentos, entre outros fatores ([rinite alérgica](https://www.google.com/search?q=rinite%2Bal%C3%A9rgica%2Bcausa&rlz=1C1GCEA_enBR852BR852&ei=i5XRY6zRBs_S1sQPmva36A8&ved=0ahUKEwjswueAzOP8AhVPqZUCHRr7Df0Q4dUDCA8&uact=5&oq=rinite%2Bal%C3%A9rgica%2Bcausa&gs_lcp=Cgxnd3Mtd2l6LXNlcnAQAzIECAAQHjIECAAQHjIECAAQHjIECAAQHjIECAAQHjIECAAQHjIECAAQHjIECAAQHjIECAAQHjIECAAQHjoLCC4QgAQQsQMQgwE6BQgAEIAEOgsIABCABBCxAxCDAToICAAQgAQQsQM6BAgAEEM6DgguEIAEELEDEMcBENEDOggILhCABBCxAzoHCC4QsQMQQzoKCAAQsQMQgwEQQzoHCAAQsQMQQzoKCAAQgAQQsQMQCjoHCAAQgAQQCjoPCAAQgAQQDRCxAxCxAxAKOgwIABCABBANELEDEAo6CQgAEIAEEA0QCkoECEEYAEoECEYYAFAAWOxrYL9vaABwAXgAgAG2AYgBlRaSAQQwLjIxmAEAoAEBwAEB&sclient=gws-wiz-serp), [asma](https://www.google.com/search?q=asma%2Bcausa&rlz=1C1GCEA_enBR852BR852&ei=25XRY5vjGvjV1sQPi5WS4Ac&ved=0ahUKEwjbvI6nzOP8AhX4qpUCHYuKBHwQ4dUDCA8&uact=5&oq=asma%2Bcausa&gs_lcp=Cgxnd3Mtd2l6LXNlcnAQAzIGCAAQBxAeMgYIABAHEB4yBggAEAcQHjIJCAAQBxAeEPEEMgQIABAeMgQIABAeMgQIABAeMgQIABAeMgQIABAeMgQIABAeOgoIABBHENYEELADSgQIQRgASgQIRhgAUPgLWJQQYPcRaAJwAHgAgAGEAYgBgwSSAQMwLjSYAQCgAQHIAQjAAQE&sclient=gws-wiz-serp), [urticária](https://www.google.com/search?q=urtic%C3%A1ria%2Bcausa&rlz=1C1GCEA_enBR852BR852&ei=rZXRY-roBZHM1sQPqqGguA4&ved=0ahUKEwiq84GRzOP8AhURppUCHaoQCOcQ4dUDCA8&uact=5&oq=urtic%C3%A1ria%2Bcausa&gs_lcp=Cgxnd3Mtd2l6LXNlcnAQAzIGCAAQBxAeMgYIABAHEB4yBggAEAcQHjIICAAQBxAeEA8yBggAEAcQHjIGCAAQBxAeMgQIABAeMgQIABAeMgQIABAeMgQIABAeOgoIABBHENYEELADOggIABAHEB4QCjoNCAAQgAQQDRCxAxCxAzoKCAAQgAQQDRCxAzoHCAAQgAQQDToNCAAQgAQQDRCxAxCDAUoECEEYAEoECEYYAFDACliFHmCvJWgBcAF4AIABvQKIAagNkgEHMC42LjEuMpgBAKABAcgBCMABAQ&sclient=gws-wiz-serp)).





## Ferramentas utilizadas 🧰
<p> <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a> 
    <a href="https://pandas.pydata.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/2ae2a900d2f041da66e950e4d48052658d850630/icons/pandas/pandas-original.svg" alt="pandas" width="40" height="40"/> </a>
    <a href="https://seaborn.pydata.org/" target="_blank" rel="noreferrer"> <img src="https://seaborn.pydata.org/_images/logo-mark-lightbg.svg" alt="seaborn" width="40" height="40"/> </a>
    </p>
