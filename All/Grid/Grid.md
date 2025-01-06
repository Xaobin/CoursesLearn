# GRID

<h4>Tutorial of Grid [PT-BR]</h4>
<a href="https://github-com.translate.goog/Xaobin/CoursesLearn/blob/main/All/Grid/Grid.md?_x_tr_sl=pt&_x_tr_tl=en&_x_tr_hl=pt-BR&_x_tr_pto=wapp">Link to translate page (Google)</a>
<br>
<br>
CSS Grid trouxe várias possibilidades para o desenvolvimento de layouts modernos. Veja como alinhar conteúdos com CSS Grid.<br>
<br>
Outras 4 propriedades bastante importantes ao se trabalhar com CSS Grid são:<br>
<br>
    - align-items
    - justify-items
    - align-self
    - justify-self
<br>
Essas são propriedades CSS que permitem alinhar conteúdo dentro de células da grid, o que pode ser bastante útil no desenvolvimento de qualquer layout com CSS.<br>
<br>
O Grid por padrão oculpa por total o tamanho onde se encontra
<br>
<a href="https://www.w3schools.com/css/css_grid.asp">CSS grid</a><br>
<a href="https://www.youtube.com/playlist?list=PLYgzkrmJnLwpeeGgdADYq3cE2yUwLLTOv">Curso em vídeo</a><br>
<a href="https://css-tricks.com/snippets/css/complete-guide-grid/">Guia completo de Grid</a><br>
<br>
<hr>
<b>Grid-template-columns</b><br>
O grid-template-columns propriedade especifica o número (e as larguras) das colunas em uma grade layout. <br>
<a href="https://www.w3schools.com/cssref/pr_grid-template-columns.php">W3chools grid-template-column</a><br>
<br>
Exemplo no codepen:<br>
<a href="https://codepen.io/Sameer-Begh/pen/bGmYZaY">CodePen Home
Grid-template-columns (CSS-only)</a><br>
-----------<br>
<br>
<hr>
<b>Grid-column-gap</b><br>
A propriedade grid-column-gap define o tamanho do intervalo entre as colunas..<br>
<a href="https://www.w3docs.com/learn-css%20/grid-column-gap.html">W3Docs - grid-column-gap</a><br>
Exemplo Codepen<br>
<a href="https://codepen.io/hubspot/pen/yLRwmvx">Grid-Column_Gap</a><br>
-----------<br>
<br>
<hr>
<b>Grid-template-rows</b><br>
O grid-template-rows propriedade especifica o número (e as alturas) das linhas em um layout de grade.<br>
<a href="https://www.w3schools.com/cssref/pr_grid-template-rows.php">W3schools - grid-template-rows</a><br><br>
<a href="https://codepen.io/origamid/pen/gRKpow/">Exemplo Codepen - grid-template-rows</a><br><br>
<br>
<hr>
<b>Grid explícita e grid implícita</b>: Na explícita, especificamos a configuração da grid, na grid implícita as células da grid serão preenchidas automaticamente<br>
-----------<br>
Quando usamos grid-template-columns e grid-template-rows criamos uma grade explícita . No entanto, se tentarmos colocar um item fora dessa grade, o navegador criará uma linha ou linhas de grade implícita para conter esse item.<br>
<br>
Por padrão, as trilhas de grade implícitas criadas pelas linhas implícitas serão dimensionadas automaticamente. No entanto, você pode dimensionar as faixas com o grid-auto-columns e grid-auto-rows propriedades. Dimensionei minhas trilhas automáticas em 100px para corresponder ao restante das trilhas de coluna em minha grade
<img src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Grid/imgs/GridImpExp.png?raw=true" weight="390" height="195"><br>
<a href="https://gridbyexample.com/examples/code/example10">Codepen - grid implícita/explícita </a><br>
<hr>
<b>Grid-auto-rows e grid-auto-columns</b><br>
O grid-auto-rows propriedade define um tamanho para as linhas em um contêiner de grade. <br>
A propriedade CSS grid-auto-rows faz parte da especificação CSS Grid Layout, especificando o tamanho das linhas da grade que foram criadas sem ter um tamanho <b>explícito</b>. Em outras palavras, esta propriedade define o tamanho das linhas <b>implícitas</b> e quaisquer outras linhas que não tenham sido explicitamente dimensionadas na propriedade grid-template-rows<br>
<a href="https://www.w3schools.com/cssref/pr_grid-auto-rows.php">W3schools - grid-auto-rows</a><br>
<a href="https://codepen.io/stephenyrkoo/pen/BwBKaz">Codepen - grid-auto-rows e grid-auto-columns</a><br>
<a href="https://css-tricks.com/almanac/properties/g/grid-auto-rows/">Grid-auto-rows (CSS-tricks)</a><br>
<code>
.grid-container {
  display: grid;
  grid-template-areas: "media detail detail"
                       "media detail detail";
  grid-template-rows: 200px;
  grid-auto-rows: 150px;
}
</code>
-----------<br>
<br>
<hr>
<b>Grid-row-gap</b><br>
A propriedade grid-row-gap define o tamanho do intervalo entre as linhas dos elementos da grade. A largura do intervalo pode ser especificada, separando as linhas usando um valor para grid-row-gap.<br>
<a href="https://www.w3docs.com/learn-css/grid-row-gap.html">W3Docs - grid-row-gap</a><br>
<a href="https://codepen.io/imbeshat7/pen/GRGxmKv">Codepen - grid-row-gap</a><br>
-----------<br>
<br>
<hr>
<b>Grid-gap</b><br>
forma reduzida de usar o grid-row-gap, tanto em linhas como em colunas. Produz espaçamento entre elementos<br>
<a href="https://www.w3docs.com/learn-css%20/grid-gap.html">W3Docs - grid-gap</a><br>
<a href="https://codepen.io/aneesh-palamthodi/pen/dyxabZK">Codepen - grid-gap</a><br>
-----------<br>
<br>
<hr>
<b>Unidade FR</b><br>
Esta unidade foi necessária criar para não ocorrer problemas, significa fração<br>
exemplo: grid-template-columns: repeat(3, 1fr); <br>
<a href="https://css-tricks.com/introduction-fr-css-unit/">Unidade FR, explicação - css-tricks</a><br>
-----------<br>
<br>
<hr>
<b>Alinhamento de conteúdo</b><br>
Parecido com flexbox, tem a propriedade align-items, com as propriedades stretch, center, start, end<br>
Também a propriedade justify-items<br>
<a href="https://css-tricks.com/almanac/properties/j/justify-items/">Justify-items css-tricks</a><br>
<a href=""></a><br>
-----------<br>
<br>
<hr>
<b>Align-sef</b><br>
Similar ao align-items, funciona para um item<br>
<a href="https://www.w3schools.com/cssref/css3_pr_align-self.php">W3Schools align-self</a><br>
<a href="https://codepen.io/rachelandrew/pen/KdKLLX">Codepen exemplo</a><br>
Melhor exemplo:<br>
<a href="https://codepen.io/amelieyeh/pen/KXmRxO">Codepen -exemplo 2</a><br>
-----------<br>
<br>
<hr>
<b>Ocupando espaços no CSS grid (grid-column)</b><br>
Adentrando na parte mais interessante. Grid-column é um abreviador para grid-column-start e grid-column-end. A propriedade grid-column especifica o tamanho e a localização de um item de grade em um layout de grade e é uma propriedade abreviada para as seguintes propriedades:(grid-column-start+grid-column-end)
<br>
<a href="https://www.w3schools.com/cssref/pr_grid-column.php">W3Schools - grid-column</a><br>
Aqui está o exemplo mais fácil de entender<br>
<a href="https://css-tricks.com/almanac/properties/g/grid-column/">Grid-column CSS-tricks</a><br>
Aqui está a imagem desenhada que explica a column do grid:<br>
<img src="https://i0.wp.com/css-tricks.com/wp-content/uploads/2022/10/s_5E600D44A3602E06FB6B7B59AD446BE1961B4B0D409EEEA69A28E839C5C65BD4_1662830734930_first-example.jpg?resize=805%2C288&ssl=1" weight="350" height="150"><br>
Exemplo Real, com grid, wrapper, onde a imagem se parece com um menu:<br>
<img src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Grid/imgs/GridAula08-0215.png?raw=true" weight="490" height="295"><br>
Continuando o exemplo:<br>
<img src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Grid/imgs/GridAula08-0250.png?raw=true" weight="490" height="295"><br>
Ainda falta a responsividade, para isto será usado o media query, como ficaria se, em certo tamanho de tela mobile, os elementos ficassem um abaixo de outro:<br>
<img src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Grid/imgs/GridAula09-0204.png?raw=true" weight="350" height="180"><br>
<br>
<br>
<hr>
<b>Sobreposição de conteúdo CSS</b><br>
No item interior foi visto posicionamento de colunas, esta parte trata do posicionamento de linhas, propriedades: grid-row-start e grid-row-end<br>
Exemplo básico:<br>
<img src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Grid/imgs/GridAula10-0110.png?raw=true" weight="490" height="295"><br>
Simplificador da Sintaxe: <b>Grid-row</b><br>
É possíve usar grid-row e grid-columns juntos<br>
Com essas duas propriedades o poder do CSS Grid aumenta drasticamente, desta forma, as possibilidades de fazer coisas viram infinitas<br>
Mais um exemplos:<br>
<img src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Grid/imgs/GridAula10-0357.png?raw=true" weight="490" height="295"><br>
<br>
Também nesta seção, vale destacar o <b>z-index</b> - propriedade que posiciona o elemento por cima de outro<br>
-----------<br>
<a href="https://codepen.io/luanalvesdev/pen/gOZeWwW">Codepen - Exemplo do Grid-row</a><br>
<a href="https://www.w3docs.com/learn-css/grid-row.html">W3Docs - grid-row</a><br>
-----------<br>
<br>
<hr>
<b>Áreas de grid</b><br>
Para fazer uma área de grid, é preciso especificar uma <b>grid-area</b> para cada elemento onde se quer fazer uma composição baseada nas áreas do grid<br>
<a href="https://codepen.io/origamid/pen/eRKwaN/">Codepen - Grid-area</a><br>
<a href="https://www.w3docs.com/learn-css/grid-area.html">W3Docs - grid-area</a><br>
<br>
A propriedade grid-area é usada para especificar o tamanho e a localização do item da grade dentro da linha da grade. É uma propriedade abreviada para as seguintes propriedades:<br>
  -  grid-row-start , especificando a linha na qual o item deve começar.
  -  grid-column-start , especificando a coluna na qual o item deve começar.
  -  grid-row-end , especificando a linha na qual o item deve terminar.
  -  grid-column-end , especificando a coluna na qual o item deve terminar.
A propriedade grid-area também especifica um nome para um item de grade. Em seguida, os itens de grade nomeados podem ser referenciados pela propriedade grid-template-areas do contêiner de grade. <br>
<b>Grid-template-areas</b><br>
A propriedade grid-template-areas é usada para se referir ao nome ao configurar o layout da grade. Você pode nomear itens de grade com a propriedade grid-area . Cada área é definida por apóstrofos. Essas áreas podem ser referenciadas a partir de propriedades de posicionamento de grade como grid-row-start , final da linha da grade , final da coluna da grade , grid-column-start, bem como suas propriedades abreviadas, como grid-row , área de grade e coluna de grade . <br>
<a href="https://www.w3docs.com/learn-css/grid-template-areas.html">W3Docs- grid-template-areas</a><br>
Exemplo básico - usando grid-area + Grid-template-areas<br>
<img src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Grid/imgs/GridAula11-0449.png?raw=true" weight="490" height="295"><br>
Com Responsividade, usando media query, a partir do breakpoint especificado!<br>
<img src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Grid/imgs/GridAula11-0702.png?raw=true" weight="490" height="295"><br>
-----------<br>
<br>
<hr>
<b>CSS auto-fill e auto-fit</b><br>
Exemplo<br>
<img src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Grid/imgs/GridAula12-0200.png?raw=true" weight="490" height="295"><br>
<a href="https://css-tricks.com/auto-sizing-columns-css-grid-auto-fill-vs-auto-fit/">Auto-Sizing Columns in CSS Grid: `auto-fill` vs `auto-fit`</a><br>
<a href="https://duckduckgo.com/?t=h_&q=css+auto-fill+auto-fit&ia=web">Duckduckgo - Auto-fill e auto-fit</a><br>
<br>
<hr>
<b>Nomes de linha em CSS grid</b><br>
Também conhecido como track names, usa-se o colchete dentro do grid-template-areas e mais os nomes das divs separados por vírgula para o grid-column, na propriedade grid-column adiciona-se os items em colchete ([item] / [item]). A palavra site pode ser especificada sozinha, sendo um termo reservado, junto de [site-start] ...[site-end], ... grid-column:site;<br>
<a href="https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_grid_layout/Grid_layout_using_named_grid_lines">Layout using named grid lines</a><br>
Exemplo<br>
<img src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Grid/imgs/GridAula13-0248.png?raw=true" weight="490" height="295"><br>
Também pode ser uado o [content-start], retirando o sufixo start - grid-column-start:content<br>
<code>
header,
footer {
	grid-column:site;
}
main {
	grid-column:content;
}
aside {
	grid-column:site-start / content-start;
	grid-row: content-top / content-bottom;
}
@media (min-width:500px){
	.wrapper {
		display:grid;
		grid-template-columns: [site-start] 1fr [content-start] repeat(4,1fr) [site-end];
		grid-template-rows:[site-top] 200px [content-top] 200px [content-bottom] 200px [site-bottom];
		grid-gap:.5rem;
	}

}
</code>
<br>
Exemplo<br>
<img src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Grid/imgs/GridAula14-0329.png?raw=true" weight="490" height="295"><br>
<hr>
<b>Grid Layout na prática - 3 Layouts</b><br>
Exemplos no codepen<br>
<a href="https://codepen.io/desenvolvweb/pen/zYadPPY">Layout 1</a><br>
<a href="https://codepen.io/desenvolvweb/pen/bGKrYxx">Layout 2</a><br>
<a href="https://codepen.io/desenvolvweb/pen/YzvxERx">Layout 3</a><br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
