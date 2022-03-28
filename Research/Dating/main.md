## dating recommendation

* Ссылка на постоянный созвон: [zoom](https://us02web.zoom.us/j/84017944503?pwd=Y3paWTUzbXkrQWU2RGkyb21nQk1wdz09)

## Статус 28.03.2022

Мотивирующая картинка
##
![63cb813ed6b4ca81fc2fb2aad827ce3a.png](Images/63cb813ed6b4ca81fc2fb2aad827ce3a.png)
Решили что будем учить рекомендательную модель, которая будет прогнозировать насколько одному эмбеддингу понравится другой. Прогнозировать будем на основании трёх видов даннх (картинка, граф, текст, атрибуты). При этом модель нужно учить отдельно для newcommer'ов, отдельно для опытных пользователей т.к. у первых еще нет сетевого эмбеддинга.

## Для общего развития
Стенфордский курс по SNA [notion](https://www.notion.so/yads/Sberloga-with-Graphs-12fafe3224e1483eb435a16aa990e1a1)


Как учить GAT можно найти тут: [colab](https://github.com/gordicaleksa/pytorch-GAT/blob/main/The%20Annotated%20GAT%20(Cora).ipynb), но если лень разбираться, то он есть в [stellar graph](https://stellargraph.readthedocs.io/en/stable/)


## Обзор литературы
Берем хороший обзор по SNA link prediction, например A Survey of Link Recommendation for Social Networks: Methods, Theoretical Foundations, and Future Research Directions [acm](https://dl.acm.org/doi/10.1145/3131782), [pdf](https://dl.acm.org/doi/pdf/10.1145/3131782) и смотрим [кто его процитировал в google scholar](https://scholar.google.com/scholar?hl=ru&as_sdt=2005&sciodt=0%2C5&as_ylo=2018&cites=13239567524783213560&scipsc=1&q=graph+attention+networks&btnG=&oq=graph+attention+)

Среди релевантных сразу находим статью из [Q1](https://www.scimagojr.com/journalsearch.php?q=17362&tip=sid&clean=0) журнала 2022 года: "[What You Like, What I Am: Online Dating Recommendation via Matching Individual Preferences with Features](https://ieeexplore.ieee.org/abstract/document/9706322)" [pdf](https://dl.dropboxusercontent.com/s/i5bowxdgt3h08wc/What_You_Like_What_I_Am_Online_Dating_Recommendation_via_Matching_Individual_Preferences_with_Features.pdf)

Также стоит посмотреть:
"[Reciprocal and heterogeneous link prediction in social networks](https://dl.acm.org/doi/10.1007/978-3-642-30220-6_17)" PAKDD'12 - старенькая, лучше сразу смотреть кто цитировал

# К след . разу:
1. Выгрузить данные из Dating бота в формате
    * Nodes
        * id
        * gender
        * reg date
        * …
     * Edges
         * id
         * node id A
         * node id B
         * timestamp
         * type
2. Загрузить данные в [NetworkX](https://networkx.org/documentation/stable/reference/readwrite/index.html) и прогнать их через простенькие link prediction модели:
    * Простые модели прогнозирвания, такие как preferential attachment, Adaic, Jaccard можно посмотреть тут: [colab](https://drive.google.com/file/d/1IVfBKPJo2rPHXgNim73WyYrj_ACtubcU/view?usp=sharing)
    * Чуть более умные модели на основании случайных блужданий и skipgram тут: [colab](https://drive.google.com/file/d/1PYNFGH5kHZwrX_hCykIyJpD6tyqZWioN/view?usp=sharing)
3. Сделать обзор литературы по гайду выше в формате <статья><ключевая идея><что понравилось><что не понравилось>

## Потом
* Сделать описание сети (@ki расскажет как)
* Начать разбираться с GAT