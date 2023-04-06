# data-science-series-temporais

![Badge em Desenvolvimento](http://img.shields.io/static/v1?label=STATUS&message=FINALIZADO&color=GREEN&style=for-the-badge)

![Badge code size](https://img.shields.io/github/languages/code-size/fab-souza/data-science-series-temporais)


| :placard: Vitrine.Dev |    |
| -------------  | --- |
| :sparkles: Nome        | **Data Science: análise de séries temporais**
| :label: Tecnologias | python
| :rocket: URL         | [Notebook no Kaggle](https://www.kaggle.com/code/fabianadesouza/data-science-series-temporais)
| :fire: Desafio     | Conteúdo do curso [Data Science: análise de séries temporais](https://www.alura.com.br/curso-online-data-science-series-temporais)

![](https://user-images.githubusercontent.com/67301805/212129044-2344ace3-b75c-42ac-b14e-32a228d09ac1.jpg#vitrinedev)

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

Para aprofundar essa análise, usei o método *.diff()* nas vendas mensais do R03, que calcula a diferença entre os registros do dataframe, retirando a necessidade de fazer um *for* ou de criar algo ‘na unha’ para executar este cálculo. Fazer esta operação significa decompor os dados, que é uma forma de verificar quanto foi o aumento das vendas do medicamento. Ao plotar o gráfico, observa-se que não houve um aumento constante das vendas, na maior parte dele, os registros oscilam próximos as escalas 100 e -100, porém ao longo do tempo, os picos de vendas ficam próximos a 100 e ultrapassa essa marca mais vezes do que na queda de vendas, até chegar ao final de 2018, em que houve o ápice das vendas e depois a redução desses números.

![grafico 2 editado](https://user-images.githubusercontent.com/67301805/214289241-c022a9d2-c551-4bbe-97e5-935f4e1aa53f.jpg)

Fiz o mesmo processo para o medicamento N02BA, porém ao contrário do que aconteceu com o R03, a venda deste produto vai decaindo ao longo da análise.

![graficoN02BA](https://user-images.githubusercontent.com/67301805/214647248-dc2689e9-b992-4977-9761-e6d364b4aa7e.png)

Passando para o medicamento R06, ele apresenta uma sazonalidade, pois suas vendas são baixas no começo e final de ano, mas são altas a partir do mês de maio, aproximadamente. 

![graficoR06](https://user-images.githubusercontent.com/67301805/214676634-acf701fb-7602-441c-b6f0-82f74dcd322c.png)

Ao pesquisar o que são medicamentos Anti-histamínicos de uso sistêmico, eles são indicados para tratamento de: rinite alérgica, asma e urticária (Fonte: [UFJF](https://www.ufjf.br/farmacologia/files/2015/03/Anti-histam%C3%ADnicos.pdf)). 
Porém não consegui identificar o que pode causar as vendas sazonais, já que essas doenças podem ser causadas por inalação de substâncias, pelos de animais, mofo, uso de outros medicamentos, entre outros fatores ([rinite alérgica](https://www.google.com/search?q=rinite%2Bal%C3%A9rgica%2Bcausa&rlz=1C1GCEA_enBR852BR852&ei=i5XRY6zRBs_S1sQPmva36A8&ved=0ahUKEwjswueAzOP8AhVPqZUCHRr7Df0Q4dUDCA8&uact=5&oq=rinite%2Bal%C3%A9rgica%2Bcausa&gs_lcp=Cgxnd3Mtd2l6LXNlcnAQAzIECAAQHjIECAAQHjIECAAQHjIECAAQHjIECAAQHjIECAAQHjIECAAQHjIECAAQHjIECAAQHjIECAAQHjoLCC4QgAQQsQMQgwE6BQgAEIAEOgsIABCABBCxAxCDAToICAAQgAQQsQM6BAgAEEM6DgguEIAEELEDEMcBENEDOggILhCABBCxAzoHCC4QsQMQQzoKCAAQsQMQgwEQQzoHCAAQsQMQQzoKCAAQgAQQsQMQCjoHCAAQgAQQCjoPCAAQgAQQDRCxAxCxAxAKOgwIABCABBANELEDEAo6CQgAEIAEEA0QCkoECEEYAEoECEYYAFAAWOxrYL9vaABwAXgAgAG2AYgBlRaSAQQwLjIxmAEAoAEBwAEB&sclient=gws-wiz-serp), [asma](https://www.google.com/search?q=asma%2Bcausa&rlz=1C1GCEA_enBR852BR852&ei=25XRY5vjGvjV1sQPi5WS4Ac&ved=0ahUKEwjbvI6nzOP8AhX4qpUCHYuKBHwQ4dUDCA8&uact=5&oq=asma%2Bcausa&gs_lcp=Cgxnd3Mtd2l6LXNlcnAQAzIGCAAQBxAeMgYIABAHEB4yBggAEAcQHjIJCAAQBxAeEPEEMgQIABAeMgQIABAeMgQIABAeMgQIABAeMgQIABAeMgQIABAeOgoIABBHENYEELADSgQIQRgASgQIRhgAUPgLWJQQYPcRaAJwAHgAgAGEAYgBgwSSAQMwLjSYAQCgAQHIAQjAAQE&sclient=gws-wiz-serp), [urticária](https://www.google.com/search?q=urtic%C3%A1ria%2Bcausa&rlz=1C1GCEA_enBR852BR852&ei=rZXRY-roBZHM1sQPqqGguA4&ved=0ahUKEwiq84GRzOP8AhURppUCHaoQCOcQ4dUDCA8&uact=5&oq=urtic%C3%A1ria%2Bcausa&gs_lcp=Cgxnd3Mtd2l6LXNlcnAQAzIGCAAQBxAeMgYIABAHEB4yBggAEAcQHjIICAAQBxAeEA8yBggAEAcQHjIGCAAQBxAeMgQIABAeMgQIABAeMgQIABAeMgQIABAeOgoIABBHENYEELADOggIABAHEB4QCjoNCAAQgAQQDRCxAxCxAzoKCAAQgAQQDRCxAzoHCAAQgAQQDToNCAAQgAQQDRCxAxCDAUoECEEYAEoECEYYAFDACliFHmCvJWgBcAF4AIABvQKIAagNkgEHMC42LjEuMpgBAKABAcgBCMABAQ&sclient=gws-wiz-serp)).

---

Passando para o dataset da panificadora, que são sobre vendas delivery que a empresa recebeu entre julho de 2019 até junho de 2020. Após tratar os dados, criei um novo dataframe contendo a data, hora, dia da semana e o valor do pedido, porque, primeiramente, queria analisar como estavam as vendas, se estavam crescendo, diminuindo ou se oscilavam em um intervalo. Porém, me deparei com um gráfico cheio de ruídos e com um outlier que bagunçou a escala do gráfico.

![grafico panificadora](https://user-images.githubusercontent.com/67301805/214970812-adc95694-c860-4023-bd3f-7d22453c5c76.png)

Para reduzir os ruídos, apliquei a média móvel duas vezes, primeiro para 7 dias, depois para 21 dias e obtive o seguinte gráfico: 

![grafico com as duas medias moveis](https://user-images.githubusercontent.com/67301805/214977859-6b1323fd-7a56-4901-a365-38a01e22a02b.png)

Ambos referem-se às vendas que foram entregues, há uma queda dos pedidos até o começo de outubro, depois eles sobem um pouco e oscilam em uma faixa de preço, até que em fevereiro de 2020 os pedidos voltam a subir até o início do mês seguinte e voltam a cair. Porém no segundo gráfico, com a redução do ruído houve perda de informação, essa troca melhorou a visualização dos pedidos, mas deve ser utilizado com cautela, pois dependendo do negócio ou do valor escolhido para a média móvel, o resultado ficará tão alterado que pode dar margem para interpretação incorreta.


## Conclusão 🏁

Eu gostei de aprender este conteúdo, porque a análise dos gráficos nos permite tomar melhores decisões administrativas. Por exemplo os medicamentos R03, as vendas cresceram até 2019, mas começaram a declinar. Neste caso, posso criar hipóteses do tipo:
- estes produtos estavam na fase de Crescimento, atingiu a Maturidade, até que entrou na última fase do ciclo de vida do produto, o Declínio;
- ou, em 2019, entrou no mercado um produto concorrente, que causou a queda nas vendas.

Já sobre os medicamentos N02BA, eu levantaria as hipóteses:

- de que o produto está na fase de Declínio e pode começar a dar prejuízo para o fabricante;
- a região pode estar passando por um período de crise;
- ou foi inaugurado um concorrente nas proximidades e que vende seus produtos mais baratos.

Se eu estivesse acompanhando as vendas dos medicamentos desde seu lançamento, seria interessante identificar cada fase e indicar a relação entre as vendas e o lucro. Pois entre as fases Crescimento e Maturidade, é quando o produto gera maior lucro, como apresenta o próximo gráfico, e o valor arrecadado pode ser utilizado para desenvolver novos produtos, ou lançar uma extensão do produto, como acontece na indústria de videogames. Determinado tempo após o lançamento do jogo é lançado um DLC, que faz com que as pessoas continuem jogando e pode incentivar novos clientes a adquirirem o jogo com a extensão.  

![image](https://user-images.githubusercontent.com/67301805/216786107-31eba537-ce8f-4859-9e69-4afe52c1c58e.png)

Fonte: [Agendor](https://www.agendor.com.br/blog/significado-ciclo-de-vida-do-produto/)

Sei que na indústria farmacêutica não é bem assim que funcionam suas vendas, que não tem como lançar uma extensão do remédio de gripe, por exemplo. Sei que é mais custoso e burocrático liberar a venda de um novo fármaco, começando pela pesquisa e até chegar nos testes em humanos, demanda muito tempo. No entanto, os dados referem-se às vendas de uma farmácia e não do setor farmacêutico, em escala global. Os três medicamentos analisados (R03, N02BA e R06) apresentaram queda em 2019, o que pode ser um indicativo de que a farmácia não esteja passando por um bom momento, que talvez não seja um problema dos medicamentos, e sim, da empresa.

---

Muito obrigada por chegar até aqui e até a próxima 🤗


## Ferramentas utilizadas 🧰
<p> <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a> 
    <a href="https://pandas.pydata.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/2ae2a900d2f041da66e950e4d48052658d850630/icons/pandas/pandas-original.svg" alt="pandas" width="40" height="40"/> </a>
    <a href="https://seaborn.pydata.org/" target="_blank" rel="noreferrer"> <img src="https://seaborn.pydata.org/_images/logo-mark-lightbg.svg" alt="seaborn" width="40" height="40"/> </a>
    </p>
