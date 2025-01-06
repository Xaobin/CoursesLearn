# Curso de FlexBox (capturado em video)
=======================================

<a href="https://github-com.translate.goog/Xaobin/CoursesLearn/blob/main/All/Flex/Flexbox.md?_x_tr_sl=pt&_x_tr_tl=en&_x_tr_hl=pt-BR&_x_tr_pto=wapp">Link for translate page (google)</a>
<br>
<br>
A imagem a seguir mostra a arquitetura interna do FlexBox, X axis, Y axis. É o primeiro passo para aprender a usar esta tecnologia!.
<br>
<img weigth="500" heigth="400" src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Flex/imgs/Flex01.png?raw=true">
<br>
<br>
A diferença básica entre Flexbox e CSS Grid
<br>
<img weigth="450" heigth="250" src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Flex/imgs/Flex02.png?raw=true">
<br>
<br>
Um container básico onde os elementos serão inseridos, usado apenas para aprendizado.
<br>
<img weigth="250" heigth="250" src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Flex/imgs/Flex03.png?raw=true">
<br>
<br>
A propriedade CSS flex-direction define como os itens flexíveis são colocados no contêiner flexível, definindo o eixo principal e a direção (normal ou invertido).
<br>
<img weight="490" height="295" src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Flex/imgs/Flex04.png?raw=true">
<br>
<br>
<b>Flex direction - collumn</b>
<br>
<img weight="490" height="295" src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Flex/imgs/Flex05.png?raw=true">
<br>
<br>
Um preview inicial do curso - usando @media - e o que ocorre na redução de tela
<br>
<img weight="490" height="295" src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Flex/imgs/Flex06.png?raw=true">
<br>
<br>
Elementos que serão aprendidos, quando a tela reduzir...
<br>
<img weight="490" height="295" src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Flex/imgs/Flex07.png?raw=true">
<br>
<br>
<hr>
<b>FLEX-WRAP</b>
É uma propriedade na qual permite que os Flex-items quebrem a linha caso não tenha espeço suficiente no flex-container<br>
Lembra do Word-wrap do VS code? então...<br>
Neste caso os itens estão extrapolando o container, qual é a solução?
Está contecendo o overflow.
<br>
<img weight="490" height="295" src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Flex/imgs/Flex08.png?raw=true">
<br>
Usaremos o word-wrap para corrigir, mais precisamente o (wrap) - pois os elementos estão dispostos numa única linha (nowrap). A propriedade <em>wrap-reverse</em> faz o mesmo, porém inverte a ordem.
<br>
<img weight="490" height="295" src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Flex/imgs/Flex09.png?raw=true">
<br>
<hr>
<b>Flex-Flow</b>.<br>
Flex-wrap e Flex-direction são duas das propriedades mais importantes, elas definem o comportamento visualo que será apresentado!<br>
Forma abreviada para trabalhar com as duas propriedades (direction e wrap) ao mesmo tempo.<br>
Através de flex-flow é possível ter controle dos ítens, controlando a direção.<br>
sintaxe:<br>
flex-flow: |flex-direction| |flex-wrap|<br>
<img weight="490" height="295" src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Flex/imgs/FlexFlow.png?raw=true">
<img weight="490" height="295" src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Flex/imgs/Flex11.png?raw=true">
<br>
<hr>
<b>Justify-Content</b>. <br>
Controla o alinhamento dos flex-items no main-axis.<br>
Valor padrão: <br>
justify-content: flex-start (não precisa usar pois é padrão)
<br>
<b>Propriedades</b>:
<br>
<b>flex-start</b> - seria o left <br>
<b>flex-end</b> - seria o right<br>
<b>center</b> - centraliza<br>
<b>space-around</b> espaço a redor<br>
<b>space-between</b> espaço entre, similar ao anterior, as extremidades não recebem a quota de espaço inicio e fim<br>
<img weight="490" height="295" src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Flex/imgs/FlexJustifyContent.png?raw=true">
<hr>
<b>Align-items</b> <br>
A propriedade align-items especifica o alinhamento padrão para itens dentro de um flexbox ou contêiner de grade<br>
<img weight="490" height="295" src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Flex/imgs/Flex12.png?raw=true"><br>
<b>Valores do align-items:</b><br>
<b>flex-start</b> - semelhante ao do justify-content: flex-start mas em outro eixo<br>
center: dispõe no centro (VERTICAL) do container<br>
<b>flex-end</b> - dispõe no fim do conteiner<br>
<b>baseline</b> - alinhados na linha de base (linha imaginária debaixo de cada letra/número em horizontal), se um flex-item estiver maior que outro, mantará a base da linha<br>
<img weight="490" height="295" src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Flex/imgs/Flex13.png?raw=true"><br>
Excelentes Exemplos:<br>
<a href="https://www.w3schools.com/cssref/playdemo.php?filename=playcss_align-items&preval=center">W3Schools - align-items</a><br>
<br>
<hr>
<b>Align-content</b> <br>
Propriedade parecida com o align-item mas só fará sentido se o container tiver mais de uma linha. Dispõe o alinhamento dos flex-items em diferentes linhas, uso do cross-axis<br>
<img weight="490" height="295" src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Flex/imgs/Flex14.png?raw=true"><br>
Também pode ser usado as mesmas propriedades do anterior: flex-end, space-between, space-around.<br>
<br>
<br>
<hr>
<b>Order</b> <br>
É possível alterar a ordem na qual os elementos são apresentados, sem apresentar a ordem no HTML - ESSA é a grande sacada!<br>
Antigamente era impossível ou complicadíssimo apresentar de se fazer.<br>
<img weight="490" height="295" src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Flex/imgs/Flex15.png?raw=true"><br>
Observe como, com esta linha de comando, a ordem é alterada a partir do elemento 2<br>
Valor padrão: 0, apenas anúmeros inteiros(pos. e neg.)<br>
<img weight="490" height="295" src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Flex/imgs/Flex16.png?raw=true"><br>
Menos um<br>
Mais um exemplo<br>
<img weight="490" height="295" src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Flex/imgs/Flex17.png?raw=true"><br>
Utilizando se um menu aparecesse primeiro<br>
<img weight="490" height="295" src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Flex/imgs/Flex18.png?raw=true"><br>
<br>
<hr>
<b>Align-self</b> <br>
Alinhamentos individuais de Flex-itens. Faria o mesmo que align-items, utiliza flex-items<br>
Permite o controle de flex-items individualmente<br>
<img weight="490" height="295" src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Flex/imgs/Flex19.png?raw=true"><br>
<br>
<hr>
<h4>Diferenças</h4><br>
<b>align-items</b>: Controla o alinhamento de todos os itens no eixo cruzado.<br>
<b>align-self</b>: controla o alinhamento de um item flexível individual no eixo cruzado.<br> 
<b>align-content</b>: Controla o espaço entre as linhas flexíveis no eixo cruzado<br>
<b>Align-content</b> gerencia o espaço entre as linhas quando os itens são quebrados. <b>Align-items</b> alinha os itens entre si quando os tamanhos dos itens são diferentes. Quando o tamanho dos itens é igual e há apenas uma linha, eles se comportam de forma semelhante<br>
<hr>
<b>Flex-basis</b> <br>
Flex-basis Serve para especificar qual é o tamanho do espaço inicial do flex-items antes do eventual espaço livre ou faltante no container ser divido ou distribuído.<br>
É a maneira correta de se definir tamanho para item em flex-box, seja altura ou altura, a depender de flex-direction.<br>
A propriedade flex-basis especifica o comprimento inicial de um item flexível.<br>
valor padrão:auto<br>
<img weight="490" height="295" src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Flex/imgs/Flex20.png?raw=true"><br>
<br>
A propriedade <b>FLEX</b> é um atalho para usar esta propriedade e mais outras, ou seja, <b>Flex </b> trabalha com <b>basis, row e shrink</b><br>
Mais exemplo:<br>
<img weight="490" height="295" src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Flex/imgs/Flex21.png?raw=true"><br>
<hr>
<b>O processo do flexbox Para calcular a direção de um item:</b>
<ol>
<li> Verifica o flex-basis, altura/largura inicial</li>
<li> O container tem espaço faltando (flex row e shrink são úteis)</li>
<li> Calcula a cota para cada item crescer ou diminuir</li>
</ol>
Utilizando o FLEX: observe a propriedade flex: os items vão crescer numa cota de 1, diminuir numa cota de 1, com tamanho inicial 100px<br>
<img weight="490" height="295" src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Flex/imgs/Flex22.png?raw=true"><br>
Valor padrão de flex => flex: 0 1 auto; (row 0, shrink 1, basis auto)<br>
<br>
<hr>
<b>Centralização Vertical</b><br>
<br>
<img weight="490" height="295" src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Flex/imgs/Flex23.png?raw=true"><br>
<br>
<img weight="490" height="295" src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Flex/imgs/Flex24.png?raw=true"><br>
<br>
<hr>
<b>Multicolunas altura igual</b><br>
Como fazer em flexbox, foi usado elementos card, muito comum em sites<br>
O elemento de maior altura irá esticar por toda a extensão vertical do flex-container<br>
imagem<br>
<img weight="490" height="295" src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Flex/imgs/Flex25.png?raw=true"><br>
<hr>
<b>Rodapé fixo</b><br>
Antes do flexbox, era algo feito com muita dificuldade, o rodapé fixo<br>
Fazendo: O body é o elemento flex, Tem o Header e Footer<br>
Flex é uma shorthand css para (row, shrink, basis)<br>
Então ficaria desta forma:<br>
<img weight="490" height="295" src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Flex/imgs/Flex26.png?raw=true"><br>
Tendo muito ou pouco conteúdo, o rodapé sempre estará abaixo<br>
<br>
<hr>
<b>Layout Santo Graal</b><br>
Primeiro exemplo do mundo real para o Flexbox<br>
Flexbox é indicado para porções menores de layout, no entanto será demonstrado todo o potencial do flexbox no layout santo graal<br>
Pode ser feito para layouts sem problema algum<br>
Santo graal - porque tinha uma época que era bem buscado por desenvolvedores - era tão difícil de achar - como se buscasse o santo graal, por isto veio este nome<br>
<b> Características </b><br>
1) header, 3 colunas, footer<br>
2) colunas de tamanho igual<br>
3) Rodapé fixo<br>
4) Conteúdo primeiro no Html<br>
5) Marcação mínima<br>
Link para explicação:<br>
<a href="https://en-m-wikipedia-org.translate.goog/wiki/Holy_grail_(web_design)?_x_tr_sl=en&_x_tr_tl=pt&_x_tr_hl=pt&_x_tr_pto=tc">Layout Santo Graal</a><br>
Os prints a seguir demonstram os procedimentos para se chegar ao resultado esperado, utilizando-se inclusive de @media, quando o tamanho da tela é reduzido<br>
<img weight="490" height="295" src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Flex/imgs/Flex27.png?raw=true"><br>
<img weight="490" height="295" src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Flex/imgs/Flex28.png?raw=true"><br>
<img weight="490" height="295" src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Flex/imgs/Flex29.png?raw=true"><br>
<img weight="490" height="295" src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Flex/imgs/Flex30.png?raw=true"><br>
<img weight="490" height="295" src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Flex/imgs/Flex31.png?raw=true"><br>
<img weight="490" height="295" src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Flex/imgs/Flex32.png?raw=true"><br>
<img weight="490" height="295" src="https://github.com/Xaobin/CoursesLearn/blob/main/All/Flex/imgs/Flex33.png?raw=true"><br>
<br>
<br>
<hr>
<b>Menu responsivo</b><br>
<br>
Tentativa de fazer o menu responsivo do vídeo:<br>
<a href="https://github.com/Xaobin/CoursesLearn/blob/main/All/Flex/MenuResponsivo.html?raw=true">Menu Responsivo</a><br>
Nível Avançado<br>
Como fazer:<br>
<a href="https://webdesign.tutsplus.com/how-to-build-a-responsive-navigation-bar-with-flexbox--cms-33535t">Link Webdesign - menu responsivo</a><br>
Pesquisa duckduckgo: menu Responsivo em Flexbox<br>
<a href="https://duckduckgo.com/?t=h_&q=responsive+menu+with+flexbox&ia=web">Responsive menu with CSS Flexbox</a><br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
