# Project Flexbox DIO

### Flexbox no CSS

Primeiro precisamos entender o conceito de box-model: Quando estamos criando o layout de um site o navegador representa cada elemento HTML como uma caixa retangular, isso é o box-model. E com CSS nós alteramos a aparência dessa caixa em largura, altura, cor de fundo, etc. Essa caixa é composta por 4 áreas, sendo elas o conteúdo, o padding, a borda e a margem.

###### Áreas do box-model

As margens (margin) são espaçamentos entre elementos;
As bordas (border) são linhas marcadas na borda desses elementos;
O padding é um espaçamento entre as bordas e o conteúdo, a diferença para as margens é que declarações de imagem de fundo funcionam nele;
O conteúdo (content) é o que o seu bloco representa, um texto, uma imagem, um vídeo, etc.

###### Estilizando elementos

Um breve resumo sobre display:flex, é uma espécie de caixa flexível que visa fornecer uma maneira mais eficiente de dispor, alinhar e distribuir espaços entre os itens em um contêiner, mesmo quando seu tamanho é desconhecido e/ou dinâmico. O layout do flexbox é independente de direção, ao contrário dos layouts regulares, o famigerado display:block, embora funcionem bem para as single pages, por exemplo, mas falta flexibilidade quando pensamos no quesito responsividade, que são aplicações adaptadas em diferentes tamanho de tela.

Como o flexbox é um módulo inteiro e não uma única propriedade, envolve muitas coisas, incluindo um conjunto de propriedades. Alguns deles devem ser definidos no container (elemento pai, conhecido como “flex container”), enquanto os outros devem ser definidos nos filhos (chamados “flex items”). Enquanto um display:block é baseado em direções de fluxo em bloco e em linha, o display:flex será baseado em "direções de fluxo flexível".

### Propriedades do Flexbox

O Flexbox torna a tag um elemento do tipo flex container e automaticamente todos seus filhos diretos também, passando a se comportasr como flex-items. Podemos usar Flexbox em qualquer tipo de tag.

###### flex-direction

Propriedade que estabelece o eixo principal do container definindo assim a direção dos flex items colocados no Flex-container. Os eixos vem como "row" por padrão começando da esquerda para a direita. Row-reverse é o oposto, da direita para a esquerda. O próximo é o eixo de coluna "column" por padrão é de cima pra baixo. O column-reverse é de baixo pra cima.

###### Flex-wrap

Define se os itens devem ou não quebrar a linha. Por padrão as linhas não quebram, portanto os itens filhos serão compactados além do limite do conteúdo e dessa forma, o conteúdo de dentro do contêiner pai começa a vazar.

###### Flex-flow

Atalho para as propriedades flex-direction e flex-wrap. Mas seu uso não é tão comum pois quando mudamos o flex-direction para column, mantemos o padrão do flex-wrap que é nowwrap.

###### Justify-content

Alinha os itens dentro do contêiner e distribui espaço entre eles. Se os elementos filhos ocupam 100% desse contêiner não tem como aplicá-la, pois seu objetivo é distribuir o espaçamento.

###### Align-items

Alinha os flex-itens de acordo com o eixo do contêiner. Tem diferença no eixo das colunas. Permite o alinhamento no eixo vertical. Diferente do justify-content ele não precisa ter conhecimento da altura desses itens.

###### Align-content

Responsável por tratar o alinhamento das linhas do contêiner em relação ao seu eixo vertical. E ele precisa respeitar algumas orientações como quebra de linha com modo wrap e a altura do contêiner tem que ser maior que a soma da altura das linhas desses itens. 

###### Flex-grow

Define a proporcionalidade de crescimento de itens. Respeita o tamanho dos seus flex-itens. Não vai funcionar com justify-content.

###### Flex-basis

Estabelece o tamanho inicial do item antes das distribuições de espaço restantes dentro dele usando como base o conteúdo interno disposto. Valores possíveis são em %, px, em, auto, 0, etc.

###### Flex-shrink

Estabelece a capacidade de redução ou compreensão do tamanho de um item. Ela lida com o tamanho mínimo a partir dele. Permite que os itens tenham tamanhos reduzidos em proporcional. O inverso de flex-grow.

###### Flex

Simplesmente a abreviação de grow, shrink e basis.

###### Order

Ficam agrupados um atrás do outro, ordena numeralmente os itens dentro do contêiner.

###### Align-self

Estabelece alinhamento individual de acordo com o item que queremos trabalhar. Seleciona itens aleatórios diferente das outras propriedades que trabalham com eixo e respeitando ordens

### Conclusão

Flexbox nasceu para facilitar o desenvolvimento responsivo, bem como a estilização de um layout de forma mais flexível. Com o surgimento de diferentes tamanhos de telas com acesso à internet, a demanda por estudos de melhoria para adaptação do mercado para esse novo horizonte cresceu também. Hoje em dia temos a opção de wrap, star, end, center, justify-content, e etc. que ajudaram muito na evolução e na acessibilidade de principais páginas e aplicações. 

### Referência bibliográfica

[Impulso React DIO](https://digitalinnovation.one/)

[CSS-tricks](https://css-tricks.com/snippets/css/a-guide-to-flexbox/#background)