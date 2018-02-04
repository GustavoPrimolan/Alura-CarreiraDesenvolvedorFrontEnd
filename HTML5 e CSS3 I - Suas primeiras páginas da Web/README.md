<h1>Imagens do Projeto</h1>
<img src="ImagemProjeto01.PNG"/>
<img src="ImagemProjeto02.PNG"/>
<img src="ImagemProjeto03.PNG"/>
------------------------------------------------------------------------------------------
<h1>Se��o 01 - Introdu��o ao HTML</h1>

A Internet est� cada vez mais presente no nosso dia-a-dia, n�o s� porque temos cada vez mais acesso, mas tamb�m mais conte�do online. Temos desde sites pessoais e portfolios at� grandes portais. Temos blogs e redes sociais.

Conforme a Internet foi crescendo, ficou mais robusta, isto �, as tecnologias que a sustentam s�o cada vez mais poderosas e vers�teis.

Para a cria��o de conte�do para a Internet, HTML, CSS e JavaScript s�o as tecnologias dominantes atualmente. Se voc� quer colocar um site online, muito provavelmente ter� que saber mexer com essas tecnologias.

Neste curso, vamos ver diversas coisas que conseguimos fazer apenas com HTML e CSS. E como toda tecnologia pode ser bem ou mal utilizada, veremos quais cuidados devemos tomar ao desenvolver p�ginas para a Internet, quais boas pr�ticas podemos seguir e como elas impactam para nossos usu�rios finais.

Para estudar essas tecnologias, vamos trabalhar em um projeto de um site pessoal.

HTML
Quando pensamos em fazer uma p�gina, pensamos em fazer isso pois queremos expor algum conte�do para nossos visitantes. No nosso caso, em que estamos desenvolvendo um site pessoal, queremos divulgar nosso trabalho para o mundo, nossos conhecimentos e qualidades.

Para isso, podemos fazer uma p�gina como a da figura abaixo, com um texto descrevendo nosso trabalho, nossa foto e alguns links para nosso visitante explorar o site.

P�gina que vamos desenvolver

Todo esse conte�do e visual precisa ser descrito de alguma forma para o navegador conseguir mostr�-lo para o usu�rio. � a� que entram em cena o HTML e o CSS.

Vamos come�ar analisando o conte�do: temos um t�tulo (sobre mim), dois par�grafos de texto, um subt�tulo, mais texto... Num editor de texto, conseguimos selecionar o t�tulo e aplicar um tamanho de fonte maior, uma cor diferente, centralizar etc. Quando voc� fizer isso, seu editor de texto provavelmente gravar� suas escolhas junto do texto:

Sobre mim = fonte 24pt, branco, centralizado

Moro em S�o Paulo... = fonte 12pt, preto, justificado

Trabalho usando a web... = fonte 12pt, preto, justificado

Como trabalho = fonte 18pt, preto, � esquerda
No caso do nosso navegador, precisamos fazer isso tamb�m: indicar que um determinado trecho do texto tem uma fonte diferente, uma cor diferente... Mas mais ainda: podemos indicar que esse primeiro trecho (sobre mim) � um t�tulo da p�gina. Assim, podemos evitar o retrabalho de definir todo o estilo de novo para o pr�ximo t�tulo: basta configurarmos, posteriormente, o estilo dos t�tulos. O mesmo vale para os par�grafos de texto, subt�tulos etc.

Sobre mim = t�tulo

Moro em S�o Paulo... = par�grafo

Trabalho usando a web... = par�grafo

Como trabalho = subt�tulo
Tags
O HTML serve justamente para indicar o que significa cada trecho de texto que digitamos. Para o nosso exemplo, poder�amos colocar essas informa��es no texto da seguinte forma:
<code>
<h1>Sobre mim</h1>

<p>Moro em S�o Paulo...</p>

<p>Trabalho usando a web...</p>

<h2>Como trabalho</h2>
</code>
Repare nas marca��es que colocamos: <h1>, <h2> e <p>. Essas marca��es s�o o que chamamos de tags do HTML, e s�o o bloco de constru��o fundamental da linguagem.

Repare que usamos tamb�m </h1>, </h2> e </p>. Quando colocamos essas marca��es, estamos indicando o final de uma tag ou, como dizemos, fechamos a tag que estava aberta.

Com isso, j� conseguimos representar o conte�do b�sico da p�gina. Mas repare que algumas partes do texto s�o mais importantes, t�m destaque. Novamente, para indicar que uma parte do texto tem uma caracter�stica especial, vamos colocar uma tag ao redor dela:

<p>Moro em S�o Paulo mas atendo clientes do mundo todo. Sou conhecido por
fazer produtos de <em>qualidade</em>, <em>durabilidade</em> e que <em>agregam
valor</em> para meus clientes.</p>
Repare que, para dar uma �nfase ao texto, usamos a tag <em>. Em outro trecho, onde temos um texto com um destaque mais forte, podemos usar a tag <strong>:

<p>... Crio sites para todos, seguindo as principais diretivas de
<strong>acessibilidade</strong>, <strong>responsividade</strong> e <strong>web
sem�ntica</strong>, sem descuidar da qualidade de c�digo.</p>
Em ambos os casos, veja que colocamos tags dentro de tags. Esse � um recurso que vamos explorar bastante ao longo do curso para poder detalhar bem as informa��es da nossa p�gina.

Estrutura b�sica
Apesar de j� podermos salvar esse c�digo num arquivo com a extens�o .html e abri-lo num navegador, possivelmente teremos problemas, como na imagem abaixo.

P�gina bagun�ada no navegador

Isso acontece porque, apesar de termos escrito c�digo HTML correto, o navegador n�o tem todas as informa��es necess�rias para mostrar nossa p�gina corretamente.

A informa��o faltante mais vis�vel aos nossos olhos � a codifica��o dos caracteres. Repare que toda letra que deveria aparecer acentuada est� com problema. Isso acontece porque, atualmente, existem v�rias formas de representar caracteres acentuados em c�digo bin�rio, que � como o computador guarda nosso arquivo no disco. Precisamos, ent�o, indicar qual a codifica��o que estamos usando em nossa p�gina.

Da mesma forma que usamos tags para indicar o significado de cada trecho de texto, vamos usar uma tag para indicar a codifica��o da p�gina: a tag <meta>.

<meta charset="utf-8">
No exemplo acima, estamos indicando que nossa p�gina usa a codifica��o de caracteres UTF-8. Essa � uma codifica��o bastante popular e completa, e recomendamos que voc� sempre use ela.

Uma outra informa��o faltando, mais sutil, � o t�tulo da p�gina. N�o o t�tulo "Sobre mim", que j� est� l�, mas um t�tulo na janela do navegador, para que nosso visitante saiba qual p�gina est� aberta naquela janela do navegador.

P�gina sem t�tulo e sem �cone

Novamente, vamos usar uma tag para passar essa informa��o para o navegador: a tag <title>.

<title>Biografia - Jo�o da Silva</title>
Uma outra informa��o legal de passarmos para o navegador, para ajudar ainda mais nosso visitante, � mostrar um �cone correspondente � nossa p�gina, para facilitar a identifica��o da janela.

�cone e t�tulo na janela do navegador

Para fazer isso, podemos colocar um arquivo chamado favicon.png na mesma pasta do nosso arquivo .html. E, para garantir que o navegador vai mostr�-la, podemos colocar mais uma tag na nossa p�gina: a tag <link>.

<link rel="icon" href="favicon.png">
Repare que a tag <link> � um pouco mais complexa que as outras que j� usamos. Ela tem dois atributos: rel e href. O atributo rel diz que tipo de conte�do que queremos referenciar com ela (um �cone, no nosso caso). J� o atributo href diz onde esse conte�do se encontra. Usaremos novamente essa tag mais para a frente.

Com isso, nosso HTML j� fica mais ou menos assim:

<meta charset="utf-8">
<title>Biografia - Jo�o da Silva</title>
<link rel="icon" href="favicon.png">
<h1>Sobre mim</h1>
<p>Moro em S�o Paulo...</p>
<p>Trabalho usando a web...</p>
<h2>Como trabalho</h2>
Meio bagun�ado, n�o? As informa��es que s�o necess�rias para o navegador est�o misturadas com as informa��es que queremos mostrar para o visitante do site. Para organizar melhor essas informa��es, existem duas tags fundamentais da linguagem HTML: <head> e <body>.

A tag <head> serve para agrupar informa��es para o navegador entender melhor nossa p�gina, como o t�tulo da p�gina, o �cone e a codifica��o. Em outras palavras, as meta-informa��es da p�gina devem ficar dentro dessa tag.

J� a tag <body> serve para agrupar as informa��es que queremos mostrar para os usu�rios, ou seja, o conte�do que quer�amos mostrar originalmente.

Usando essas duas tags, podemos reorganizar nosso c�digo da seguinte forma:

<head>
    <meta charset="utf-8">
    <title>Biografia - Jo�o da Silva</title>
    <link rel="icon" href="favicon.png">
</head>
<body>
    <h1>Sobre mim</h1>
    <p>Moro em S�o Paulo...</p>
    <p>Trabalho usando a web...</p>
    <h2>Como trabalho</h2>
</body>
Repare um detalhe no c�digo escrito acima: as tags que est�o dentro das tags <head> e <body> foram escritas com alguns espa�os � frente. Escrever c�digo assim � uma boa pr�tica, conhecida como indenta��o. Ela nos ajuda a enxergar melhor a estrutura da nossa p�gina e vai ser bem importante conforme nossa p�gina vai ficando mais complexa.

O c�digo fica melhor organizado usando as tags <head> e <body>, mas ainda falta uma tag essencial para embrulhar toda a nossa p�gina e indicar para o navegador que estamos escrevendo c�digo HTML em nosso arquivo: a tag <html>. Colocando-a no nosso c�digo, chegamos ao seguinte resultado:

<html>
    <head>
        <meta charset="utf-8">
        <title>Biografia - Jo�o da Silva</title>
        <link rel="icon" href="favicon.png">
    </head>
    <body>
        <h1>Sobre mim</h1>
        <p>Moro em S�o Paulo...</p>
        <p>Trabalho usando a web...</p>
        <h2>Como trabalho</h2>
    </body>
</html>
Pronto, agora o navegador sabe que estamos usando HTML. Mas estamos esquecendo de um detalhe: o HTML � uma linguagem j� com uma certa idade, que passou por reformula��es para se aperfei�oar e ficar mais poderosa. Assim, n�o basta dizer para o navegador que estamos usando HTML; precisamos dizer qual vers�o do HTML estamos usando. � a� que entra uma instru��o especial para o navegador, que parece uma tag mas n�o �: o DOCTYPE.

Como o nome diz, essa instru��o serve para dizer para o navegador (ou qualquer programa que queira ler nosso arquivo) qual tipo de documento ele est� lendo. Ou seja, essa instru��o n�o � exclusiva da linguagem HTML, mas vem de uma linguagem mais gen�rica chamada SGML (do ingl�s Standard Generalized Markup Language). Sendo assim, nessa instru��o vamos dizer para o navegador que estamos usando HTML e qual vers�o do HTML estamos usando. Mas qual vers�o estamos usando?

Neste curso, vamos estudar a vers�o mais recente do HTML, que � a vers�o 5. Mais para a frente, vamos estudar as diferen�as dessa vers�o para as anteriores e por que devemos us�-la atualmente.

Precisamos, ent�o, colocar a instru��o DOCTYPE correspondente ao HTML 5 no nosso c�digo HTML. Ent�o colocamos no in�cio do documento o seguinte c�digo:

<!DOCTYPE html>
E pronto! Agora o navegador consegue entender corretamente nosso c�digo HTML. Repare que n�o h� nada nesse c�digo que diga que � a vers�o 5 do HTML que estamos usando; isso � proposital. A organiza��o que define como deve ser a linguagem HTML - a W3C - quis facilitar a nossa vida e decidiu criar o DOCTYPE acima, que diz para o navegador que estamos usando a �ltima vers�o do HTML dispon�vel. Assim, quando surgir uma nova vers�o do HTML, nossa p�gina n�o precisa ser alterada.

Resumindo, nosso c�digo, no final, vai ficar assim:

<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title>Biografia - Jo�o da Silva</title>
        <link rel="icon" href="favicon.png">
    </head>
    <body>
        <h1>Sobre mim</h1>
        <p>Moro em S�o Paulo...</p>
        <p>Trabalho usando a web...</p>
        <h2>Como trabalho</h2>
    </body>
</html>
Essa estrutura, com DOCTYPE e tag <html> com <head> e <body>, deve ser seguida por todo documento HTML para que os navegadores interpretem-no corretamente.

Estilo
Com o c�digo HTML, conseguimos definir o qu� vamos mostrar, mas n�o como vamos mostrar. Esse � um papel que cabe ao CSS, tecnologia que vamos abordar no pr�ximo cap�tulo.

<h2>Realce de texto</h2>
Na p�gina que estamos desenvolvendo, temos bastante texto escrito. Com tanto texto, talvez o usu�rio fique meio perdido, por isso � importante real�ar alguns termos que merecem mais destaque.

No primeiro par�grafo, por exemplo, temos o seguinte texto:

Moro em S�o Paulo mas atendo clientes do mundo todo. Sou conhecido por fazer produtos de qualidade, durabilidade e que agregam valor para meus clientes.

Aqui, seria interessante dar destaque para os termos "qualidade", "durabilidade" e "agregam valor", deixando-os em it�lico, por exemplo. Para fazer isso, usamos a tag <em>:

Sou conhecido por fazer produtos de <em>qualidade</em>
Neste outro par�grafo

Satisfazer meus clientes � prioridade. Para isso, garanto um processo de desenvolvimento altamente interativo, baseado em feedback cont�nuo. N�o trabalho com escopo fechado: o cliente � que decide quando o produto est� pronto.

� importante ressaltar aqui a parte "N�o trabalho com escopo fechado", com ainda mais destaque que os termos anteriores, deixando-os em negrito. Para isso, podemos usar a tag <strong>:

<p><strong>N�o trabalho com escopo fechado</strong>: o cliente � que decide quando o produto est� pronto</p>
Aplique essas duas tags em seu c�digo, neste e em outros lugares que achar relevante.


<h2>P�gina do blog</h2>
O site do Jo�o da Silva ser� composto de diversas p�ginas, como visto em aula. Vamos come�ar tamb�m a p�gina do blog. Crie o arquivo blog.html. Nele, deve haver o seguinte texto:

Blog

O essencial de design responsivo

Design responsivo tem ganho cada vez mais aten��o como t�cnica de desenvolvimento de p�ginas web para dispositivos m�veis. Mas como come�ar?

Por que fazer p�ginas acess�veis?

Tem se falado cada vez sobre acessibilidade na web. H� diversas t�cnicas e diretivas a serem seguidas, inclusive da pr�pria W3C. Mas vale a pena investir nisso?

JavaScript n�o obstrusivo

JavaScript � uma linguagem essencial hoje em dia para criar p�ginas ricas, interativas e din�micas. Por�m, h� alguns cuidados que devem ser tomados ao colocarmos c�digo JavaScript em nossas p�ginas.

Formate o texto usando HTML.

-------------------------------------------------------------------------------------------------
<h1>Se��o 02 - Come�ando com CSS</h1>

Na aula anterior, vimos como criar o conte�do de uma p�gina usando a linguagem HTML. Por�m, nossa p�gina ainda est� muito b�sica. Isso porque o navegador j� sabe o qu� queremos mostrar, mas n�o sabe como queremos mostrar, ent�o mostra apenas o conte�do, sem estilo algum.

Precisamos, ent�o, ensin�-lo como queremos mostrar os elementos da nossa p�gina. Imagine que queremos definir o tamanho da letra (fonte) como 16 pixels. O navegador nos permite especificar isso da seguinte forma:

font-size: 16px;
Essa forma de declarar como queremos mostrar um elemento � o que chamamos de linguagem CSS. Nessa linguagem, conseguimos configurar diversos aspectos da exibi��o dos elementos da nossa p�gina.

Repare no formato da declara��o: dizemos qual propriedade queremos mudar (font-size) e colocamos dois-pontos para separ�-la do valor que lhe queremos dar, no nosso caso o tamanho da fonte (16 pixels). Por fim, colocamos um ponto-e-v�rgula no final, para indicar que nossa declara��o terminou.

Associando estilos a elementos
Na declara��o que fizemos, dissemos que quer�amos mudar o tamanho da fonte. Mas de qual elemento? Precisamos sempre associar estilo a elemento. Uma forma de fazer isso � usar o atributo style das tags do HTML. Por exemplo, podemos mudar a fonte do elemento <h2> da nossa p�gina:

<h2 style="font-size: 16px;">Como trabalho</h2>
Apesar de funcionar, n�o � muito pr�tico: se quisermos deixar todos os subt�tulos da p�gina com a mesma apar�ncia, teremos que repetir esse c�digo em todas as tags <h2>. Ent�o, melhor que isso, podemos usar a tag <style>, colocando o estilo desejado dentro dela:

<style>
    font-size: 16px;
</style>
E onde colocamos a tag <style>? No lugar onde v�o as tags com as informa��es para o navegador: dentro da tag <head>.

Est� faltando algo na declara��o acima, n�o? Anteriormente, dissemos que todo estilo deveria ser associado a um elemento da p�gina. A qual elemento a declara��o acima est� associada? Precisamos fazer associa��o selecionando um elemento da p�gina para essa regra. � a� que entram os seletores da linguagem CSS.

<style>
    h2 {
        font-size: 16px;
    }
</style>
No exemplo acima, estamos selecionando os elementos <h2> da p�gina e aplicando o estilo que quer�amos, o tamanho de fonte. Repare que precisamos abrir chaves logo ap�s o seletor e fechar chaves ao final do estilo. Podemos colocar mais regras dentro das chaves, se quisermos. Por exemplo, podemos alterar a fonte usada no subtitulo para "Arial":

<style>
    h2 {
        font-family: "Arial";
        font-size: 16px;
   }
</style>
Colocando o CSS no seu devido lugar
Com a tag <style>, conseguimos n�o s� evitar repeti��o como tamb�m deixar nosso c�digo mais organizado: tudo que � relativo � apar�ncia da p�gina fica agrupado num s� lugar, facilitando a manuten��o da p�gina.

Mas ainda temos um problema: nosso site n�o vai ter uma p�gina s�. Essas outras p�ginas muito provavelmente ter�o uma cara parecida com a p�gina que estamos desenvolvendo agora. Ent�o o CSS tamb�m ser� bem parecido, com bastante coisa repetida. Pior: se quisermos alterar alguma caracter�stica visual do site inteiro, teremos que fazer a altera��o em todas as p�ginas do site. Muito trabalho com muita chance de erro!

Como podemos evitar essa repeti��o? Colocando o CSS num arquivo separado! Podemos, ent�o, criar um arquivo chamado site.css com o conte�do que t�nhamos colocado na tag <style>:

h2 {
    font-family: "Arial";
    font-size: 16px;
}
Agora, no arquivo HTML, precisamos dizer para o navegador que esse arquivo CSS precisa ser carregado. Para isso, usamos a tag <link>. Lembra dela?

<link rel="stylesheet" href="site.css">
Assim como a tag <link> que criamos para escolher o �cone, essa tag tamb�m vai dentro da tag <head>. E agora, quando o navegador encontrar essa tag, ele vai baixar o arquivo site.css e, por causa do atributo rel="stylesheet", ele sabe que esse arquivo tem o estilo da p�gina.

Um pouco de cor
Agora que sabemos onde escrever o CSS, podemos come�ar a especificar o estilo que queremos que nossa p�gina tenha, para chegarmos no resultado mostrado na imagem abaixo.

Resultado desejado

Vamos come�ar ajustando as cores. O t�tulo tem um fundo roxo. Como alterar a cor de fundo? Como queremos mexer na cor de fundo do t�tulo, a propriedade que vamos alterar chama-se background-color. Faz sentido, n�o? A maior parte das propriedades que podemos alterar no CSS tem um nome bem explicativo. Veremos mais exemplos adiante.

Nosso t�tulo est� dentro de uma tag <h1>. Ent�o precisamos selecion�-lo para alterar a cor de fundo. Teremos algo assim no CSS, ent�o:

h1 {
    background-color: ????;
}
A quest�o que resta �: como dizer que queremos a cor roxa? Ali�s, qual tom de roxo queremos? Existem v�rios "roxos". E tamb�m existem v�rias formas de identificar uma cor no CSS. A mais popular � especificar uma mistura das cores prim�rias vermelho, verde e azul para chegar � cor que queremos, dizendo o "quanto" queremos de cada cor numa escala de 0 a 255. Por exemplo, nosso roxo tem 133 de vermelho, 25 de verde e 68 de azul.

<img src="cores-rgb.png"/>

Alguns exemplos de misturas de cores

Sabendo disso, basta escrever essa mistura no CSS. Existem duas formas para isso. A mais popular e compacta � usar a nota��o hexadecimal para representar essas quantidades. Nessa nota��o, "0" continua sendo "0", mas "10" vira "A", "15" vira a letra "F" e "16" vira "10". Seguindo nessa l�gica, "133" vira "85", "25" vira "19" e "68" vira "44". Juntando as cores na ordem vermelho, verde e azul chegamos no formato usado no CSS:

h1 {
    background-color: #851944;
}
Repare que colocamos um cerquilha (#) na frente dos n�meros. Ele faz parte desse formato de cor do CSS e serve para deixar claro para quem ler o c�digo que aquela sequ�ncia de n�meros e letras � uma cor.

Outra forma de especificar essa mistura � usando a forma abaixo:

h1 {
    background-color: rgb(133, 25, 68);
}
Precisamos mudar tamb�m a cor da letra do nosso t�tulo para branco. Para isso, usamos a propriedade color. Nosso CSS fica, ent�o:

h1 {
    background-color: rgb(133, 25, 68);
    color: rgb(255, 255, 255);
}
Ou ent�o, se voc� preferir a nota��o hexadecimal:

h1 {
    background-color: #851944;
    color: #FFFFFF;
}
Algumas cores n�o precisam de tanta precis�o assim (de 0 a 255) para serem especificadas; dezesseis n�veis de cor (de 0 a 15) j� bastariam, economizando um pouco de c�digo para n�s. Pois bem: temos uma nota��o hexadecimal compacta no CSS tamb�m! Podemos escrever a cor branca usando essa sintaxe:

h1 {
    background-color: #851944;
    color: #FFF;
}
A cor roxa, por ser mais espec�fica, precisa ser especificada na nota��o hexadecimal normal. Por�m, se a cor fosse #882244, poder�amos escrev�-la como #824.

Uma �ltima cor que precisamos ajustar � a cor de fundo da p�gina. � uma cor quase branca: #F2FFFC. Como fazer para mudar a cor da p�gina toda? Mudando a cor da tag que cont�m a p�gina toda, que � a tag <body>:

body {
    background-color: #F2FFFC;
}
Ajustando o texto
Uma outra coisa que precisamos ajustar no cabe�alho � o alinhamento do texto. Queremos deixar o t�tulo principal centralizado na tela. Para isso, usamos a propriedade text-align com o valor center:

h1 {
    background-color: #851944;
    color: #FFF;
    text-align: center;
}
Precisamos ajustar o alinhamento dos par�grafos de texto, tamb�m, deixando as linhas todas com a mesma largura. Podemos, ent�o, selecionar os par�grafos e usar novamente a propriedade text-align, dessa vez com o valor justify:

p {
    text-align: justify;
}
Outra coisa que precisamos ajustar no nosso texto � o tipo da fonte usada na p�gina. Dependendo do navegador e do sistema que voc� est� usar, voc� ver� o texto numa fonte diferente.

Fonte no Firefox

Fonte no Chrome

Se voc� olhar com aten��o a imagem que estamos usando como refer�ncia para estilizar nossa p�gina, ver� que estamos usando duas fontes diferentes: uma para o t�tulo e os subt�tulos (Arial) e outra para o texto (Times New Roman). Para mudar as fontes para esses elementos da p�gina, podemos usar a propriedade font-family, passando o nome da fonte que queremos usar para aquele elemento:

h1 {
    background-color: #851944;
    color: #FFF;
    text-align: center;
    font-family: "Arial";
}

h2 {
    font-family: "Arial";
}

p {
    text-align: justify;
    font-family: "Times New Roman";
}
Podemos melhorar um pouco o c�digo CSS, tirando a repeti��o do nome da fonte. Para isso, podemos selecionar o t�tulo e os subt�tulos ao mesmo tempo. Conseguimos fazer isso separando os nomes das tags por v�rgula no nosso seletor:

h1, h2 {
    font-family: "Arial";
}
Fazendo isso, podemos retirar a declara��o de dentro do seletor h1, e tanto os <h1> como os <h2> da p�gina ser�o exibidos com a fonte Arial.

S� precisamos tomar cuidado com uma coisa: nossa p�gina ser� exibida nos mais diversos navegadores e sistemas. Ser� que todos eles t�m essas fontes que escolhemos? Provavelmente n�o. E, se o navegador n�o encontra a fonte que pedimos, ele vai exibir nossa p�gina com as fontes que ele quiser, possivelmente deixando nossa p�gina bem estranha.

Felizmente, podemos controlar um pouco qual ser� a fonte usada caso a fonte que escolhemos n�o seja encontrada, bastando especificar uma fonte alternativa. Por exemplo:

p {
    font-family: "Times New Roman", "Baskerville";
}
Com essa declara��o, dizemos para o navegador usar a fonte Baskerville se a fonte Times New Roman n�o estiver dispon�vel. Agora, ser� que especificar outra fonte � suficiente? E se a fonte Baskerville n�o estiver dispon�vel tamb�m? Podemos explorar mais e mais possibilidades, ou ent�o abrir m�o do controle total da fonte: em vez de escolher a fonte espec�fica, escolher apenas o tipo da fonte que queremos usar. As fontes Times New Roman e Baskerville, por exemplo, s�o fontes serifadas. Por outro lado, as fontes Arial e Verdana s�o fontes sem serifa. A diferen�a pode ser vista na imagem abaixo: as fontes serifadas possuem tra�os em algumas pontas.

<img src="serifa-com-sem.png"/>

Fonte com serifa e sem serifa

Ent�o podemos dizer para o navegador: se a fonte Times New Roman n�o estiver dispon�vel, use uma fonte qualquer, desde que ela seja serifada; fazemos isso passando o valor serif para o font-family. Podemos fazer algo semelhante para os t�tulos e subt�tulos, mas dizendo que queremos uma fonte sem serifa com o valor sans-serif.

h1, h2 {
    font-family: "Arial", sans-serif;
}

p {
    font-family: "Times New Roman", serif;
}
Pr�ximos passos
Com o que j� vimos, nossa p�gina deve ficar assim:

P�gina com algumas cores e fontes

Nosso texto come�a a ter um pouco mais da apar�ncia que queremos no final. No entanto, o espa�amento entre os elementos da p�gina ainda n�o est� legal. Al�m disso, antes de podermos nos preocupar com a foto e a barra lateral, faltam alguns elementos no pr�prio texto. No pr�ximo cap�tulo cuidaremos desses detalhes.

<h2>Google Fonts</h2>

Se nos basearmos apenas nas fontes que o usu�rio ter� instaladas em sua m�quina, teremos poucas op��es para enriquecer nosso design. Felizmente, � poss�vel usar uma fonte que n�o est� na m�quina do usu�rio! Podemos pedir para o navegador baixar a fonte necess�ria para nossa p�gina com algumas linhas de CSS.

A Google disponibiliza um servi�o gratuito chamado Google Fonts que tem diversas fontes para baixarmos e usarmos em nossos sites. Esse servi�o disponibiliza n�o apenas o arquivo da fonte em si como tamb�m o CSS necess�rio para o navegador baixar a fonte!

Vamos, ent�o, enriquecer nosso design! No arquivo CSS, use a fonte "Open Sans Condensed" para os t�tulos (h1 e h2) e a fonte "Crimson Text" para o texto. J� no cabe�alho do arquivo HTML utilize o c�digo abaixo:

<!-- carrega a fonte Crimson Text nas vers�es normal, it�lico e negrito -->
<link rel="stylesheet" href="http://fonts.googleapis.com/css?family=Crimson+Text:400,400italic,600">

<!-- carrega a fonte Open Sans Condensed na vers�o negrito, -->
<!-- que � a �nica necess�ria para os cabe�alhos            -->
<link rel="stylesheet" href="http://fonts.googleapis.com/css?family=Open+Sans+Condensed:700">
Em seguida, no arquivo site.css, podemos us�-las em seus respectivos lugares.


-----------------------------------------------------------------------------------------
<h1>Se��o 03 - Aprofundando no HTML</h1>

Nas aulas anteriores, vimos um pouco de HTML e CSS e, com o que vimos, j� conseguimos fazer uma p�gina web simples, mas us�vel. Agora vamos al�m: faremos algo us�vel e bonito, seguindo boas pr�ticas de c�digo.

A p�gina que fizemos ainda n�o est� completa nem do ponto de vista visual (CSS) nem do ponto de vista de conte�do (HTML). No HTML, faltam algumas imagens, o menu lateral e o rodap� da p�gina, al�m de alguns links para auxiliar nossos visitantes na explora��o do site.

Resultado desejado

Vamos ver cada um deles com mais detalhes.

Links
No nosso texto, citamos a realiza��o de trabalhos para grandes empresas. Seria legal levar o nosso visitante a conhecer de perto esses trabalhos! Para isso, poder�amos transformar os nomes das empresas para as quais trabalhamos nesse trecho de texto:

J� desenvolvi projetos para grandes empresas como BMW, UOL e IBM...

em regi�es clic�veis, em links.

Imagem dos links

Quando ele clicar no texto "BMW", queremos que o navegador abra a p�gina da BMW (http://www.bmw.com/). Para tornar a regi�o clic�vel, usamos a tag <a> e, para dizer para onde esse link levar� nosso visitante quando clicado, usamos o atributo href dessa tag:

<p>... grandes empresas como <a href="http://www.bmw.com/">BMW</a>...</p>
Mais para baixo no texto, temos outro trecho onde pode ser interessante colocar um link

Para isso, j� dei diversas palestras e mantenho um blog.

Podemos levar o visitante para assistir as palestras na p�gina de portfolio ou ler alguns artigos no nosso blog. Ent�o, no nosso HTML, fazemos

<p>... Para isso, j� dei <a href="portfolio.html">diversas palestras</a> e mantenho um <a href="blog.html">blog</a>.</p>
Repare que colocamos apenas os nomes dos arquivos nos atributos href mas, normalmente, o endere�o que o navegador acessa � algo como http://meusite.com/bio.html. Ent�o, se estamos num endere�o como esse, para qual endere�o o navegador vai quando clicamos nesse link do portfolio? Ele vai para http://meusite.com/portfolio.html, ou seja, se voc� n�o passa o endere�o completo, o navegador troca s� o final dele. Isso � o que chamamos de link relativo: relativo ao endere�o que voc� est� visitando no momento.

No entanto, nada impede que coloquemos o endere�o completo no link:

<p>... Para isso, j� dei <a href="http://meusite.com/portfolio.html">diversas palestras</a> e mantenho um <a href="http://meusite.com/blog.html">blog</a>.</p>
Esse tipo de link � o que chamamos de link absoluto. Quando queremos endere�ar outro site, precisamos usar esse tipo de link. Agora, quando queremos endere�ar nosso pr�prio site, podemos usar links absolutos ou relativos. Mas qual devemos usar?

Imagine que voc� hospedou seu site com o endere�o joaodasilva.com. Depois, para facilitar a vida dos seus visitantes, voc� resolveu mudar para joao.com. Se voc� usou links absolutos no seu site, o que acontecer� com eles? V�o apontar para um endere�o que n�o existe mais! Usando links relativos, n�o temos esse problema. Ent�o, quando queremos referenciar nosso pr�prio site, o ideal � usar links relativos.

Na verdade, qualquer link que n�o comece com http � considerado um link relativo. Ou seja, os seguintes links s�o relativos:

portfolio.html
/posts/html5-e-css3.html
//facebook.com
Para entender como o navegador interpreta cada um deles, considere que voc� est� atualmente na URL http://meusite.com/paginas/bio.html. Os links levar�o para os seguintes endere�os, respectivamente:

http://meusite.com/paginas/portfolio.html
http://meusite.com/posts/html5-e-css3.html
http://facebook.com
Ou seja: o primeiro link troca somente a �ltima parte do endere�o. O segundo, come�ando com uma barra, troca tudo que vem depois do meusite.com, que � o dom�nio do site. E o �ltimo tipo de link, come�ando com duas barras, troca tudo que vem depois das duas barras. Ou seja, estiv�ssemos no endere�o https://meusite.com/portfolio.html, o �ltimo link nos levaria para https://facebook.com.

Imagens
Queremos colocar nossa foto na nossa p�gina para dar um ar mais pessoal, criar uma rela��o mais direta com nossos visitantes. Para colocar imagens na p�gina, usamos a tag <img>. Nessa tag, precisamos indicar qual imagem queremos que o navegador carregue. Para isso, a tag <img> tem o atributo src. Ent�o, se queremos carregar o arquivo eu.jpg, colocamos no HTML

<img src="eu.jpg">
Imagem no navegador

Assim como nos links, o endere�o dentro do src pode ser relativo ou absoluto.

Quando usamos imagens e outros recursos visuais na nossa p�gina, precisamos lembrar de um caso de uso bastante importante: nem todos os nossos visitantes conseguem enxergar a nossa p�gina. No Brasil, cerca de 3.5% da popula��o tem problemas graves de vis�o ou cegueira. Por�m, mesmo com defici�ncia visual, essa parcela da popula��o acessa � Internet. Para conseguirem fazer isso, utilizam programas chamados de leitores de tela, que s�o capazes de ler o conte�do de uma p�gina e oferecer uma navega��o pela p�gina usando o teclado.

Agora, quando usamos uma imagem ou outro recurso visual, como o usu�rio com defici�ncia visual ter� acesso a ele? No caso de uma imagem, como esse usu�rio vai conseguir saber que ela existe e qual o conte�do dela? Precisamos oferecer uma descri��o da imagem para esses usu�rios; fazemos isso por meio do atributo alt da tag <img>:

<img src="eu.jpg" alt="Foto do Jo�o da Silva">
Tornar nossa p�gina acess�vel deve ser uma preocupa��o constante, afinal n�o podemos excluir tanta gente do acesso ao nosso site. E j� � uma preocupa��o constante do W3C, o �rg�o que cuida dos padr�es da Web. Tanto � que o W3C definiu que o atributo alt � obrigat�rio nas tags <img>.

Ainda n�o podemos esquecer que n�o s� as pessoas com defici�ncia visual n�o enxergam nosso site. Ferramentas de busca tamb�m n�o enxergam e, ao fornecer a elas uma p�gina acess�vel, facilitamos o trabalho de extra��o e cataloga��o de conte�do que elas realizam para fornecerem seus resultados. Na imagem abaixo, por exemplo, podemos ver que, ao buscarmos por "alura" no Google, al�m da p�gina inicial, ele nos mostra p�ginas internas do site. O Google consegue nos dar essas p�ginas internas pois nosso conte�do est� bem marcado.

Alura no Google

Recomenda��es
Para dar mais credibilidade ao nosso trabalho, � legal colocarmos recomenda��es de outros profissionais que trabalharam conosco e aprovam nosso servi�o. Ent�o vamos citar algumas recomenda��es que fizeram do nosso trabalho:

Jo�o domina as tecnologias como ningu�m -- Manoel Santos, Petrobr�s

Podemos colocar esse texto em nossa p�gina dentro de uma tag <p> como fizemos com o resto do texto:

<h2>Experi�ncia</h2>
<p>Jo�o domina as tecnologias como ningu�m -- Manoel Santos, Petrobr�s</p>
<p>J� <a href="portfolio.html">desenvolvi projetos...</a>...</p>
Mas vamos retomar um pouco que acabamos de ver com as imagens: isso � acess�vel? � um texto como qualquer outro, ent�o o computador consegue ler isso. Mas queremos que seja realmente um texto como qualquer outro? N�o, esse n�o � um texto como qualquer outro, afinal estamos citando algu�m. Da mesma forma que colocamos o t�tulo da p�gina em uma tag <h1> para indicar que ele era, de fato, o t�tulo, precisamos colocar a cita��o dentro de uma tag que indique que ela � realmente uma cita��o! � a� que entra a tag <blockquote>:

<blockquote>Jo�o domina as tecnologias como ningu�m -- Manoel Santos, Petrobr�s</blockquote>
Mas essa frase n�o deixa de ser um par�grafo de texto, ent�o podemos manter a tag <p> dentro da tag <blockquote>:

<blockquote><p>Jo�o domina as tecnologias como ningu�m -- Manoel Santos, Petrobr�s</p></blockquote>
Se voc� escrever isso no seu HTML, vai notar que o navegador j� coloca um estilo diferente nessa tag, justamente porque ele identificou que � uma cita��o.

Cita��o com estilo diferente

Ainda podemos melhorar um pouco. O nome do autor da frase, por enquanto, est� misturado com a pr�pria frase. Podemos separar o nome da frase colocando-os em tags diferentes:

<blockquote>
    <p>Jo�o domina as tecnologias como ningu�m</p>
    <p>Manoel Santos, Petrobr�s</p>
</blockquote>
Mas, de novo, o texto "Manoel Santos, Petrobr�s" n�o � um texto qualquer; � o nome do autor da cita��o. Ent�o, novamente, podemos usar uma tag mais espec�fica, que transmita essa informa��o. A tag que indica autores de cita��es � a tag <cite>:

<blockquote>
    <p>Jo�o domina as tecnologias como ningu�m</p>
    <cite>Manoel Santos, Petrobr�s</cite>
</blockquote>
No caso da tag <cite>, n�o precisamos colocar a tag <p> dentro. Na verdade, n�o faz sentido coloc�-la: o nome do autor da frase n�o chega a formar um par�grafo de texto.

HTML e sem�ntica
Essa discuss�o que acabamos de fazer na verdade vale para todo tipo de conte�do que queremos representar na p�gina. Devemos descrever bem o conte�do para que leitores de tela e buscadores consigam processar melhor esse conte�do e, assim, tornar a informa��o mais acess�vel aos nossos visitantes.

Em outras palavras, devemos tentar deixar o nosso c�digo HTML sem�ntico, usando, para isso, as tags mais adequadas a cada tipo de conte�do.

Vejamos outros exemplos. Na nossa p�gina, teremos uma regi�o com links na lateral direita da tela. Essa regi�o ter� um estilo pr�prio, diferente do resto do texto. Ent�o � interessante isol�-la do resto do texto usando, para isso, uma tag. � bem comum fazermos isso usando a tag <div>:

<h2>Comunidade</h2>
<p>Procuro repassar meu conhecimento...</p>
<img src="eu.jpg" alt="Foto de Jo�o da Silva">
<div>
    <a href="home.html">Home</a>
    <a href="portfolio.html">Portfolio</a>
    <a href="bio.html">Sobre mim</a>
</div>
A tag <div> serve justamente para isso: criar regi�es, divis�es na p�gina. Mas podemos ser mais espec�ficos quanto ao tipo de regi�o que queremos criar! Nesse caso, estamos especificando um conjunto de links para que o usu�rio possa navegar pelo site. Na vers�o mais recente do HTML surgiu a tag <nav>, que tem justamente esse prop�sito: indicar regi�es da p�gina que cont�m links de navega��o pelo site.

<h2>Comunidade</h2>
<p>Procuro repassar meu conhecimento...</p>
<img src="eu.jpg" alt="Foto de Jo�o da Silva">
<nav>
    <a href="home.html">Home</a>
    <a href="portfolio.html">Portfolio</a>
    <a href="bio.html">Sobre mim</a>
</nav>
Visualmente, n�o teremos nenhuma diferen�a, mas agora os leitores de tela podem oferecer um atalho que leve o usu�rio mais rapidamente ao menu de navega��o do site e os buscadores podem oferecer esses links no resultado da busca. Um HTML sem�ntico melhora a acessibilidade do site para todos.

Um HTML sem�ntico � t�o importante que, em sua �ltima atualiza��o, a linguagem HTML incluiu diversas novas tags cujo �nico prop�sito � permitir uma marca��o mais sem�ntica para nossas p�ginas! Al�m da tag <nav> que acabamos de usar, temos diversas outras:

<main>: conte�do principal da p�gina
<header>: cabe�alho da p�gina ou de uma regi�o dela
<footer>: mesma ideia da tag <header> para o rodap�
<aside>: conte�do auxiliar ao conte�do principal, como links relacionados ao conte�do
<article>: conte�do que, por si s�, j� tem um sentido completo, como um post de um blog ou uma not�cia
<section>: parte/se��o de uma p�gina ou texto
H� ainda muitas outras, que estudaremos aos poucos. Por hora, podemos usar algumas das tags para deixar nosso c�digo mais sem�ntico. O texto da biografia, por exemplo, pode ser embrulhado numa tag <main>. O <nav> da lateral pode ser embrulhado numa tag <aside> junto com o t�tulo e os outros links que ainda precisamos colocar para essa parte. Podemos colocar um rodap� na p�gina com uma mensagem de copyright com a tag <footer>. Nosso c�digo ficaria assim:

<!DOCTYPE html>
<html>
<head>
     <!-- aqui continua igual -->
</head>
<body>
    <main>
        <h1>Sobre mim</h1>
        <!-- texto que j� escrevemos -->
    </main>
    <img src="eu.jpg" alt="Foto de Jo�o da Silva">
    <aside>
        <h1>Jo�o da Silva</h1>
        <nav>
            <a href="index.html">Home</a>
            <a href="portfolio.html">Portfolio</a>
            <a href="bio.html">Sobre mim</a>
            <a href="#">Blog</a>
            <a href="contato.html">Contato</a>
        </nav>
        <!-- links das redes sociais -->
    </aside>
    <footer>
        � Jo�o da Silva 2014
    </footer>
</body>
</html>
Mais para a frente colocaremos os links das redes sociais mas, por hora, podemos fazer mais uma melhoria do ponto de vista sem�ntico nos links do <nav>: podemos indicar que eles formam uma lista de links. Para isso, usamos as tags <ul> e <li>:

<nav>
    <ul>
        <li><a href="index.html">Home</a></li>
        <li><a href="portfolio.html">Portfolio</a></li>
        <li><a href="bio.html">Sobre mim</a></li>
        <li><a href="blog.html">Blog</a></li>
        <li><a href="contato.html">Contato</a></li>
    </ul>
</nav>
A tag <ul> n�o � a �nica tag que existe para fazer listas. Existem tamb�m as tags <ol> e <dl>, que veremos mais para a frente.

Entidades HTML
No footer, queremos colocar o s�mbolo e a mensagem de copyright. Podemos colocar sem problema algum o s�mbolo � direto no arquivo HTML mas, dependendo do teclado que voc� usa, pode ser dif�cil digit�-lo. Al�m disso, em algumas codifica��es de arquivo poss�veis, o s�mbolo pode simplesmente n�o existir (no nosso exemplo, estamos usando o UTF-8, ent�o n�o corremos esse risco).

Para solucionar esses casos, a linguagem HTML nos permite especificar caracteres especiais por meio das entidades. Ent�o, em vez de digitar �, podemos digitar &copy; e o navegador entender� que queremos colocar esse s�mbolo na p�gina.

H� diversas entidades que podemos usar no nosso c�digo. Abaixo uma lista com alguns exemplos:

&euro;: �
&yen;: �
&pound;: �
&reg;: �
&hearts;: ?
Tamb�m temos algumas entidades �teis para poder mostrar c�digo HTML sem que o navegador o entenda como tags. Para podermos colocar o texto "<h1> serve para t�tulos" na p�gina, por exemplo, precisamos escrever no HTML:

<p>&lt;h1&gt; serve para t�tulos</p>
As entidades &lt; e &gt; representam, respectivamente o s�mbolo de menor que (<) e maior que (>).

Arrumando o CSS
Com as altera��es que fizemos na p�gina, o visual vai ficar meio estranho. Em particular, o conte�do da nossa barra lateral ganhou um fundo roxo, igual ao t�tulo da p�gina.

Site com o t�tulo da barra lateral estilizado incorretamente

Faz um certo sentido isso ter acontecido, afinal, no nosso CSS, temos a seguinte declara��o:

h1 {
    text-align: center;
    background-color: #851944;
    color: #FFF;
}
Estamos selecionando todos os <h1> da p�gina, inclusive o da barra lateral! Podemos arrumar isso de duas formas: ou n�o usamos a tag <h1> na barra lateral ou selecionamos o <h1> que queremos de algum outro jeito.

Faz sentido o <h1> da barra lateral ser, de fato, um <h1>, afinal ele � o t�tulo principal da barra lateral. Ent�o vamos ver um outro jeito de selecionar o t�tulo do texto principal.

Se olharmos com aten��o, veremos que o <h1> com fundo roxo � o �nico <h1> dentro da tag <main>. Podemos usar essa informa��o para selecion�-lo. Ou seja, podemos dizer que queremos s� os <h1> dentro de <main>. Podemos dizer isso no CSS com o seletor main h1:

main h1 {
    text-align: center;
    background-color: #851944;
    color: #FFF;
}
Quando colocamos nomes de tags separados por espa�os no seletor CSS, queremos dizer que um elemento deve estar dentro de outro.

Usando esse truque, j� conseguimos arrumar o estilo que ficou quebrado. Ainda h� bastante coisa para arrumar no visual, mas veremos como nos pr�ximos cap�tulos.

<h2>Mais sem�ntica nos posts do blog</h2>

Na p�gina blog.html, usamos a tag <p> para demarcar a regi�o das tags do post:

<p>Tags: <a href="#">design responsivo</a>, <a href="#">mobile</a>, <a href="#">css</a></p>
Essa � a melhor tag para demarcar esse conte�do? Tamb�m n�o demarcamos em nenhum momento cada um dos posts, isto �, nada separa um post do outro.

Podemos melhorar a sem�ntica dos posts envolvendo cada um deles numa tag <article>, que representa um elemento que, por si s�, j� tem sentido completo, ou seja, cada um deles representa um bloco �nico de conte�do, de artigo de post, por isso o uso da tag article.

Dentro do post, as tags s�o uma informa��o complementar diretamente relacionada ao post, s�o palavras chaves daquele post. Sendo assim, podemos indicar essa rela��o usando, no lugar da tag <p>, a tag <footer>.

Por fim, uma informa��o interessante em um post � sua data de publica��o. Podemos marcar semanticamente datas no nosso c�digo HTML com a tag <time> e seu atributo datetime, que especifica a data num formato mais f�cil do computador processar/entender:

<time datetime="2014-07-13">13 de julho de 2014</time>
Adicione uma data de publica��o para cada post usando essa tag e use as tags <article> e <footer> para melhorar a sem�ntica dessa p�gina, empregando atrav�s das tags corretas o significado que mais faz sentido para cada uma das partes do site.

VER OPINI�O DO INSTRUTOR
Opini�o do Instrutor

O c�digo final da p�gina blog.html deve ficar assim:

<!DOCTYPE html>
<html>
    <head>
        <title>Blog - Jo�o da Silva</title>
        <meta charset="utf-8">
        <link rel="icon" href="favicon.png">
        <link rel="stylesheet" href="site.css">
        <link rel="stylesheet" href="http://fonts.googleapis.com/css?family=Crimson+Text:400,400italic,600">
        <link rel="stylesheet" href="http://fonts.googleapis.com/css?family=Open+Sans+Condensed:700">
    </head>
    <body>
        <h1>Blog</h1>

        <article>
            <h2>O essencial de design responsivo</h2>
            <time datetime="2014-07-01">01 de julho de 2014</time>

            <p>Design responsivo tem ganho cada vez mais aten��o como t�cnica de desenvolvimento de p�ginas web para dispositivos m�veis. Mas como come�ar?</p>

            <a href="#">Leia mais</a>
            <footer>Tags: <a href="#">design responsivo</a>, <a href="#">mobile</a>, <a href="#">css</a></footer>
        </article>

        <article>
            <h2>Por que fazer p�ginas acess�veis?</h2>
            <time datetime="2014-06-15">15 de junho de 2014</time>

            <p>Tem se falado cada vez sobre acessibilidade na web. H� diversas t�cnicas e diretivas a serem seguidas, inclusive da pr�pria W3C. Mas vale a pena investir nisso?</p>

            <a href="#">Leia mais</a>
            <footer>Tags: <a href="#">acessibilidade</a>, <a href="#">boas pr�ticas</a></footer>
        </article>

        <article>
            <h2>JavaScript n�o obstrusivo</h2>
            <time datetime="2014-05-28">28 de maio de 2014</time>

            <p>JavaScript � uma linguagem essencial hoje em dia para criar p�ginas ricas, interativas e din�micas. Por�m, h� alguns cuidados que devem ser tomados ao colocarmos c�digo JavaScript em nossas p�ginas.</p>

            <a href="#">Leia mais</a>
            <footer>Tags: <a href="#">javascript</a>, <a href="#">boas pr�ticas</a></footer>
        </article>
    </body>
</html>


<h2>Cores para os links</h2>

O navegador coloca uma cor padr�o para os links da p�gina. Vamos alter�-la.

No conte�do principal, a cor deve ser #851944. Na barra lateral, deve ser id�ntica � cor do texto dessa barra, que j� foi configurada no exerc�cio anterior. Aproveite para tamb�m mudar a fonte dos links para usar a fonte "Open Sans Condensed".

Dica: para n�o ter que repetir a cor do texto do <aside> para os links dentro dele, voc� pode usar o valor inherit para a cor. Esse valor faz com que a propriedade assuma o valor que foi definido em seu pai (ou ancestral, de um modo geral) em vez de assumir um outro valor. Por exemplo, se tivermos o seguinte HTML:

<ul>
    <li>
        <a href="#">Link 1</a>
    </li>
</ul>
Para colorir os links dentro da lista podemos fazer o seguinte CSS:

ul {
    color: pink;
}

ul li a {
    color: inherit;
}
O link a, neste caso, vai obrigatoriamente pegar a cor do pai dele, o <li>, que j� pega normalmente a cor do pai dele, o <ul>, que � rosa.


-------------------------------------------------------------------------------------------------------
<h1>Se��o 04 - O navegador trabalhando a nosso favor</h1>
<h2>Primeiros Passos com o Console do Navegador</h2>

Quando estamos desenvolvendo uma p�gina, muito frequentemente fazemos uma altera��o no c�digo para tentar chegar a um design final ou simplesmente testar como fica, tentar melhorar o layout ou ver se nosso c�digo funciona. Em todos esses casos, precisamos alterar um arquivo, salv�-lo e, depois, recarregar a p�gina no navegador. Esse � um ciclo que se repete bastante e que pode ser desgastante, sobretudo quando algum ou alguns dos passos n�o s�o instant�neos, como quando estamos mexendo em arquivos de outra m�quina.

Desenvolver uma p�gina tamb�m pode ser bem desgastante quando o comportamento apresentado no navegador n�o corresponde �s nossas expectativas e n�o conseguimos entender o porqu�. Um elemento n�o aparece na posi��o desejada ou aparece com as dimens�es erradas. �s vezes gastamos horas at� encontrar o motivo.

Felizmente, os navegadores mais modernos v�m com ferramentas para nos auxiliar nessas situa��es. Podemos acess�-las apertando a tecla F12, normalmente. Dentre elas, temos visualiza��o e edi��o de HTML, CSS e JavaScript, an�lise do desempenho de rede e inspe��o do estado do navegador.

Ferramentas para desenvolvedores no Firefox
Ferramentas para desenvolvedores no Chrome
Ferramentas para desenvolvedores no Internet Explorer
Explorar todas essas ferramentas foge do escopo do curso mas, agora, saber lidar com o Inspetor vai nos ajudar bastante!

Ao abrir a aba do Inspetor, vemos uma regi�o com o c�digo HTML da p�gina aberta no momento e, � direita, temos um painel com c�digo CSS. No painel do HTML, podemos explorar a estrutura da p�gina: o navegador nos mostra quais tags est�o dentro de quais. Podemos esconder ou mostrar o conte�do de uma tag para melhor visualiza��o.

Painel com algumas tags fechadas e outras abertas

Agora, experimente clicar numa tag da p�gina; voc� ver� o painel � direita mudar. Nele, o navegador mostra as regras do CSS que o navegador est� aplicando naquele elemento que voc� clicou.

Painel com uma cita��o selecionada e CSS correspondente mostrado � direita

No painel com o HTML da p�gina, o navegador n�o mostra exatamente o c�digo que digitamos, mas sim como ele interpreta o que digitamos. Se esquecermos de fechar uma tag <p>, por exemplo, veremos que o navegador � capaz de "adivinhar" onde ela seria fechada.

O navegador fecha a tag P e mostra isso no inspetor

Por outro lado, se esquecemos de fechar uma tag <em> dentro de um par�grafo, vemos que o navegador fica perdido, e tenta fech�-la e abri-la em diversos lugares.

O navegador fecha e abre a tag EM repetidas vezes

Usando essa ferramenta, somos capazes de identificar erros de digita��o mais facilmente, tanto no HTML como no CSS! Se, por exemplo, errarmos a digita��o da propriedade width dentro do seletor blockquote, veremos que o navegador, al�m de n�o aplicar a largura, vai omitir ou riscar a declara��o no painel do CSS.

Propriedade width ignorada no Firefox

Propriedade width ignorada no Chrome

Alterando a p�gina pelo pr�prio navegador
O Inspetor do navegador permite n�o apenas visualizar o c�digo mas tamb�m alter�-lo. Experimente selecionar a tag <body> e clicar no valor da propriedade background-color. Quando voc� fizer isso, o navegador permitir� que voc� altere o valor da propriedade. Digite uma nova cor para o fundo da p�gina, por exemplo #FFA; voc� ver� a p�gina mudar de cor instantaneamente.

Alterando a propriedade background-color no inspetor

Depois de digitar o novo valor, voc� pode apertar a tecla Enter para o navegador memorizar sua altera��o. Assim, voc� passar� � edi��o da pr�xima linha do CSS. Note que o navegador n�o vai alterar seu arquivo original, vai apenas guardar suas altera��es temporariamente. Se voc� recarregar a p�gina (apertando F5, por exemplo), as altera��es feitas no Inspetor n�o estar�o mais l�. Assim, essa ferramenta � muito pr�tica para realizar pequenos testes no CSS.

Na edi��o do CSS, voc� n�o est� limitado a alterar as propriedades j� declaradas; voc� pode fazer novas declara��es. Basta clicar no valor da �ltima propriedade declarada e apertar Enter: o navegador abrir� uma nova linha onde voc� poder� digitar uma nova propriedade.

Inserindo a propriedade color no body

Tamb�m n�o estamos limitados � edi��o de CSS. Podemos alterar o c�digo HTML tamb�m! Experimente dar um clique duplo na tag <h1>; voc� poder� trocar o tipo de tag para <h2>, por exemplo.

T�tulo principal alterado para H2

Voc� tamb�m pode remover uma tag da p�gina completamente. Para isso, basta clicar nela com o bot�o direito e selecionar a op��o "Deletar N�".

Apagando o t�tulo principal da p�gina

A edi��o do c�digo HTML � tempor�ria como a do CSS; se recarregarmos a p�gina, veremos o c�digo como deixamos no arquivo.

O Inspetor � uma ferramenta bem poderosa do navegador. Vale lembrar que � apenas uma das ferramentas que o navegador oferece para facilitar nossas vidas como desenvolvedores.


-------------------------------------------------------------------------------------------------
<h1>Aprimorando o layout</h1>
<h2>Melhorando o Layout</h2>

A estrutura da p�gina j� est� praticamente completa, mas o visual ainda est� longe do que queremos.

Layout desejado

Espa�amentos
Um primeiro aspecto do qual precisamos cuidar s�o os espa�os em branco na p�gina. Alguns lugares que deveriam ter espa�o n�o t�m e vice-versa.

Espa�os indevidos

Felizmente, conseguimos controlar esses espa�os com CSS. Mas repare, temos dois tipos de espa�os: dentro e fora dos elementos!

Espa�o dentro e fora do elemento

O espa�o dentro dos elementos � conhecido como padding. Ent�o, se queremos aumentar o tamanho da caixa roxa do t�tulo ou, em outras palavras, se queremos mais espa�o entre o texto do t�tulo e as bordas da caixa, vamos usar a propriedade padding:

h1 {
    padding: 24px;
}
Repare no efeito causado pelo padding: antes, a caixa roxa tinha praticamente o mesmo tamanho do texto; agora, ela ficou maior, com 24 pixels a mais em cima e abaixo do t�tulo.

T�tulo sem padding

T�tulo com padding

Com isso, j� podemos arrumar tamb�m as cita��es:

blockquote {
    padding: 16px;
}
Podemos arrumar um outro detalhe das cita��es, tamb�m. No layout desejado, temos uma borda mais escura ao redor da caixa.

Borda escura ao redor da cita��o

Podemos colocar bordas nos elementos com a propriedade border. Mas repare que podemos fazer bordas de v�rios jeitos: podemos fazer bordas claras e escuras (cor), podemos fazer bordas finas ou grossas (espessura) e podemos fazer bordas de estilos diferentes (tracejadas, pontilhadas etc.). A figura abaixo d� alguns exemplos de bordas poss�veis no navegador.

Estilos de borda poss�veis

Ent�o, na propriedade border, precisamos passar esses 3 valores que identificamos, na ordem: espessura, estilo e cor. No nosso caso, queremos uma borda com 10 pixels de espessura, s�lida (uma linha cont�nua) e da cor #C2CCCA, um cinza levemente azulado. No c�digo CSS:

blockquote {
    padding: 16px;
    border: 10px solid #C2CCCA;
}
Repare que essas 3 propriedades da borda s�o separadas por espa�o e precisam estar nessa ordem.

Por fim, repare que a cita��o est� um pouco mais para a direita que o texto normal, isto �, h� um espa�o entre ela e a borda da p�gina. Tamb�m h� um espa�o entre a pr�pria p�gina e as bordas da janela do navegador. Esse espa�o entre elementos � o que chamamos no CSS de margin! Ent�o, se quisermos deixar a cita��o alinhada com o texto, como na figura abaixo, podemos usar essa propriedade.

blockquote {
    padding: 16px;
    margin: 0;
    border: 10px solid #C2CCCA;
}
Cita��o alinhada com o texto

Essas tr�s propriedades que acabamos de conhecer -- padding, border e margin -- nos permitem controlar como as caixinhas que os elementos formam se comportam. Elas n�o s�o as �nicas: podemos controlar tamb�m a largura com a propriedade width e a altura com a propriedade height. Podemos, por exemplo, definir uma largura menor para as nossas cita��es:

blockquote {
    padding: 16px;
    margin: 0;
    border: 10px solid #C2CCCA;
    width: 250px;
}
Todas essas regras juntas formam o que chamamos box model ou, em portugu�s, "modelo de caixa", do CSS.

<img src="box-model.png"/>

Box model

Um fato interessante para notar nesse desenho � que a largura e a altura s�o referentes ao conte�do apenas. Ou seja, no nosso exemplo do blockquote, apesar de termos definido a largura como 250 pixels, por ter 16 pixels de padding e 10 pixels de borda, ter�, na verdade, 302 pixels.

Cita��o com 250 pixels de largura ocupando, na verdade, 302 pixels

Ent�o, se voc� quiser que a caixa tenha realmente 250 pixels de largura, o que voc� faz? Uma solu��o � fazer a conta de quanto tem que ser o valor da propriedade width para chegar nesse resultado, neste caso 198 pixels. Ruim, n�o?

Felizmente, podemos dizer para o navegador mudar esse box model por meio da propriedade box-sizing. Por exemplo, se queremos que a largura seja medida pelas bordas:

blockquote {
    padding: 16px;
    margin: 0;
    border: 10px solid #C2CCCA;
    width: 250px;
    box-sizing: border-box;
}
Fazendo isso, nossa cita��o ter� 250 pixels de largura de verdade. Vale notar que essa propriedade s� come�ou a ser suportada recentemente pelos navegadores, ent�o voc� pode ter alguns problemas ao tentar us�-la. Discutimos sobre as propriedades mais recentes do CSS no curso avan�ado de HTML e CSS.

Agora, repare como o CSS � poderoso: conseguimos controlar praticamente todos os aspectos da exibi��o da nossa p�gina, inclusive alguns mais abstratos, como o box model.


Quando as bordas t�m cores diferentes, o navegador realiza a mudan�a de cor na diagonal em que as bordas se encontram.

Se deixamos uma borda com a cor transparent, ela � desenhada com a cor de fundo do elemento. Ou, em outras palavras, a borda ocupa espa�o, mas fica invis�vel.


A propriedade margin controla o espa�o entre elementos.

A propriedade padding controla o espa�o entre o conte�do de um elemento e sua borda.

As propriedades width e height controlam apenas o tamanho de um elemento, e n�o afetam o espa�amento entre esse elemento e seus vizinhos. J� a propriedade box-sizing controla apenas como a largura e a altura de um elemento deve ser calculada.

Por fim, a propriedade line-height controla apenas a altura entre as linhas de texto da p�gina, n�o afetando a dist�ncia entre elementos.


--------------------------------------------------------------------------------------------------------
<h1>Se��o 06 - Construindo uma base s�lida</h1>

Antes de come�armos a fazer os ajustes nos outros espa�amentos, repare em uma coisa: definimos os tamanhos das fontes dos t�tulos e subt�tulos? H� espa�o entre os par�grafos de texto e entre o t�tulo e as bordas da janela; fomos n�s que colocamos esses espa�os?

Desde a primeira aula, quando fizemos apenas o HTML, a p�gina j� tinha alguns estilos, mesmo sem termos escrito nenhum CSS.

Layout ao final da primeira aula

Ou seja, o navegador j� d� um estilo padr�o para nossas p�ginas. E qual o problema disso? O problema � que nem sempre queremos esse estilo padr�o. E mais: como � um estilo do navegador, cada navegador pode fazer o seu pr�prio estilo, como vimos anteriormente com as fontes.

Fonte no Firefox

Fonte no Chrome

Nosso site precisa funcionar bem em todos os navegadores, ent�o usar como base para o nosso CSS o estilo padr�o do navegador n�o � uma boa ideia.

Por�m, nada impede de sobrescrevermos o estilo padr�o do navegador, como j� fizemos com as fontes! No caso dos espa�amentos, vimos que podemos mexer no espa�o entre eles com a propriedade margin e no espa�o dentro deles com a propriedade padding. Ent�o, se quisermos tirar o espa�o que o navegador coloca entre nossos par�grafos, podemos escrever no nosso CSS:

p {
    margin: 0;
}
Podemos, tamb�m, querer tirar os tamanhos de fonte que o navegador coloca para os t�tulos e subt�tulos:

h1, h2 {
    font-size: 100%; /* 100% = tamanho original da fonte do navegador */
}
Esses s�o apenas alguns exemplos. Na pr�tica, precisamos sobrescrever v�rias regras que o navegador coloca por padr�o, mesmo nos navegadores mais modernos, o que d� um bom trabalho. Para poder reaproveitar esse trabalho entre os nossos projetos, podemos at� colocar essa sobrescrita num arquivo CSS separado, s� para ele. Felizmente, v�rios desenvolvedores j� tiveram essa ideia e disponibilizaram seus arquivos para que pud�ssemos usar nos nossos pr�prios projetos.

Esse tipo de arquivo at� ganhou um nome: reset. Atualmente, existem alguns dispon�veis, com algumas diferen�as entre eles. Alguns dos mais populares s�o:

Eric Meyer: arquivo bem pequeno; deixa todos os elementos com mesma apar�ncia e tamanho de fonte; usa a fonte padr�o do navegador
Normalize: arquivo um pouco maior, mas com ajustes mais finos; j� define fontes e tamanhos padr�o para alguns elementos; corrige diversas inconsist�ncias entre navegadores
YUI (Yahoo!): arquivo bem pequeno, com um efeito bem parecido com o do Eric Meyer, mas com alguns ajustes mais espec�ficos
No nosso projeto, vamos usar o reset do Eric Meyer, mas voc� pode usar qual voc� achar melhor. O importante � usar um para ter uma base s�lida para desenvolver seu layout, independente de navegador.

Como o reset � s� mais um arquivo CSS no projeto, para us�-lo, basta baixar o arquivo e import�-lo como j� fizemos com o nosso pr�prio CSS:

<link rel="stylesheet" href="reset.css">
Podemos, sim, ter v�rios arquivos CSS para uma �nica p�gina HTML. Mas onde colocamos essa tag? No <head>? Antes ou depois do nosso CSS? Veja s�: no reset, teremos uma regra do tipo

h1, h2, h3, h4, h5, h6 {
    font-size: 100%;
}
J� no nosso arquivo, vamos querer fazer algo do tipo

h1 {
    font-size: 30px;
}
Qual dessas duas regras o navegador deve usar? A ordem em que colocamos as tags <link> � importante. O navegador l� as regras sequencialmente e, se houver conflito entre regras, pega a �ltima declara��o. Ou seja, no exemplo acima, o navegador vai usar o tamanho de fonte 30px.

Ent�o, se queremos usar o reset como base para o nosso CSS, devemos import�-lo antes do nosso CSS na p�gina:

<head>
    <link rel="stylesheet" href="reset.css">
    <link rel="stylesheet" href="bio.css">
</head>
Um pouco mais sobre conflitos no CSS
Acabamos de ver que, quando duas declara��es conflitam no CSS, o navegador usa aquela que for declarada por �ltimo. Agora, o que ser� que acontece na seguinte situa��o?

h1 {
    font-size: 100%;
    color: red;
}

h1 {
    font-size: 30px;
    font-weight: bold;
}
Para entender como o navegador entende as declara��es acima, precisamos entender que o conflito acontece no elemento onde o estilo vai ser aplicado. No exemplo acima, o estilo vai ser aplicado nos <h1>. Ent�o o navegador vai fazer o seguinte:

Aplicar o font-size: 100%
Aplicar o color: red
Aplicar o font-size: 30px, sobrescrevendo o font-size: 100% anterior
Aplicar o font-weight: bold
Ou seja, o navegador vai simplesmente aplicando todas as regras que ele encontrar para um elemento. Se ele j� mexeu numa propriedade (como o font-size no exemplo), n�o tem problema: ele mexe de novo.

A figura muda um pouco quando somos mais espec�ficos na hora de selecionar um elemento. Imagine que agora temos o seguinte cen�rio: no HTML temos

<main>
    <h1>T�tulo principal</h1>
</main>
E, no CSS, temos

main h1 {
    font-size: 30px;
    color: red;
}

h1 {
    font-size: 20px;
    font-weight: bold;
}
Quando selecionamos elementos por hierarquia, estamos sendo mais espec�ficos do que quando selecionamos apenas pela tag. Nesse caso, o navegador come�a a aplica��o dos estilos partindo das regras declaradas em seletores menos espec�ficos. Ou seja:

Aplica o font-size: 20px do seletor h1
Aplica o font-weight: bold do seletor h1
Aplica o font-size: 30px do seletor main h1, sobrescrevendo o font-size: 20px
Aplica o color: red do seletor main h1
Ent�o n�o apenas a ordem no CSS importa, mas tamb�m a especificidade dos seletores que usamos. Existem v�rias regras para definir a especificidade de um seletor e n�o vale a pena entrar em detalhes aqui. O importante � saber que, quando selecionamos um elemento, ser muito ou pouco espec�fico pode atrapalhar no desenvolvimento do projeto: podemos ser espec�ficos demais e n�o conseguirmos reaproveitar c�digo ou podemos ser espec�ficos de menos e acabar aplicando estilos em lugares que n�o gostar�amos.

Devemos usar um reset nos nossos projetos para eliminar diferen�as de layout entre navegadores e bugs espec�ficos de alguns navegadores. Com isso, ganhamos uma base s�lida para desenvolvermos nosso site. Ou seja, todas as alternativas listam benef�cios de se usar um reset.


<h2>Outros resets</h2>
No momento, estamos usando o reset do Eric Meyer, mas existem v�rias alternativas. Uma tamb�m bastante famosa � o Normalize, criado por Nicolas Gallagher e Jonathan Neal.

Baixe o Normalize clicando aqui e teste-o nas suas p�ginas. Que diferen�as voc� nota entre ele e o reset do Eric Meyer?

Uma das diferen�as mais not�veis entre o Normalize e o reset do Eric Meyer � que o Normalize n�o apenas remove o estilo padr�o do navegador como tamb�m define alguns estilos �teis, como tamanhos de fontes para cabe�alhos e estilos de fontes para elementos <em> e <strong>.

Note que esses padr�es n�o s�o mais dependentes de navegador: o Normalize que os define. Assim, qualquer navegador deve mostrar nossa p�gina do mesmo jeito.

O Normalize tamb�m cuida de alguns detalhes mais avan�ados que o reset que estamos usando n�o cuida. Isso tem seu pre�o: o Normalize tem 7 KB, enquanto o reset do Eric Meyer tem apenas 1 KB. Assim, cada um tem suas vantagens e desvantagens.

---------------------------------------------------------------------------------------------------
<h1>Se��o 07 - Um pouquinho de posicionamento</h1>

Na barra lateral, ainda est�o faltando os �cones que servir�o de links para os nossos perfis nas redes sociais.

�cones na barra lateral

Podemos representar esses �cones como uma lista de links dentro do nosso <aside>. Dentro de cada tag <a>, podemos colocar, em vez de texto, a imagem com o logotipo da rede social:

<ul>
    <li>
        <a href="https://github.com/joaodasilva">
            <img src="github.png" alt="Github">
        </a>
    </li>
    <li>
        <a href="https://twitter.com/joaodasilva">
            <img src="twitter.png" alt="Twitter">
        </a>
    </li>
    <li>
        <a href="https://br.linkedin.com/pub/jo�o-da-silva/32/4/508">
            <img src="linkedin.png" alt="LinkedIn">
        </a>
    </li>
</ul>
Isso j� nos d� um resultado pr�ximo do esperado: as imagens aparecem, s�o clic�veis mas ainda est�o uma em cima da outra. Por que isso acontece e como resolver isso?

Imagens das redes sociais na vertical

Se olharmos nosso layout atual e compararmos com o nosso HTML, veremos que, de modo geral, as tags que criamos � <p>, <header>, <aside>, <footer> � ficam uma embaixo da outra. Ou seja, esse � o comportamento padr�o do navegador: empilhar as tags como caixas, uma em cima da outra.

Tags empilhadas no layout

Mas nem toda tag tem esse comportamento. Repare, por exemplo, nas tags <a>, <strong> e <em>. Elas ficam no meio do texto, n�o empilhadas.

Tags no meio do texto no layout

Ent�o, na verdade, temos esses dois comportamentos poss�veis: empilhar ou ficar no meio do texto. Ou, em outras palavras, temos tags que s�o block, que empilham, e tags que s�o inline, que ficam no meio do texto.

No caso da nossa lista de �cones, as tags <li> t�m o comportamento de empilhar, s�o block, por isso os �cones aparecem um abaixo do outro. Se as removermos, deixando apenas os links com as imagens, conseguiremos o resultado desejado. Mas ser� que faz sentido mexer no HTML por uma quest�o visual? Faz sentido alterar a sem�ntica da nossa p�gina por isso?

Como � uma quest�o visual, devemos resolver usando a linguagem respons�vel por esse aspecto da nossa p�gina: a linguagem CSS. No CSS, conseguimos controlar esse aspecto de um elemento por meio da propriedade display. Se quisermos fazer com que os <strong> tenham comportamento block, podemos escrever no CSS:

strong {
    display: block;
}
Resultado do display: block na tag strong: quebra linha

No nosso caso, como queremos deixar os �cones das redes sociais em linha, como se fossem texto, podemos mudar o comportamento padr�o do <li>, tornando-o inline:

li {
    display: inline;
}
Com isso, conseguimos o efeito desejado. Ou quase; aparecem uns sublinhados estranhos do lado das imagens:

�cones em linha, mas com sublinhados estranhos

Se olharmos como o navegador "enxerga" nossos elementos, veremos que h� algo estranho: os itens da lista est�o menores que as imagens dentro deles:

Inspetor mostrando tamanho dos li's

O problema � que n�o podemos mudar a altura de um elemento inline, e � isso que a imagem tenta fazer com o <li>. O elemento inline sempre ter� a altura da fonte. Ou seja, se quisermos que a imagem fique dentro do <li>, precisamos definir um font-size para ele igual � altura da imagem. Isso n�o � muito pr�tico e, ainda por cima, n�o resolve o problema do sublinhado.

O que precis�vamos, nesse caso, � que o <li> tivesse a altura e a largura correta automaticamente sem perder o comportamento do inline, de ficar em linha. Para resolver esse cen�rio, temos o inline-block, mais um valor da propriedade display. Usando-o nos <li>, conseguimos o resultado que quer�amos.

Resultado final conforme desejado

Acabamos alterando o layout do menu logo acima das redes sociais, tamb�m. Resolveremos esse problema na pr�xima aula.


<h2>inline versus inline-block</h2>

Qual a diferen�a entre elementos inline e inline-block?
O valor inline-block para a propriedade display surgiu para podermos definir altura e largura em elementos inline. Fora isso, ambos os elementos podem ter um padding definido, ambos ficam em linha e ambos s�o suportados por todos os navegadores modernos

-------------------------------------------------------------------------------------------------------------
<h1>Se��o 08 - Mais seletores</h1>

Na aula passada, vimos como deixar os �cones das redes sociais lado a lado usando a propriedade display:

li {
    display: inline-block;
}
Mas acabamos alterando tamb�m o estilo do menu logo acima desses �cones:

Menu e �cones na horizontal

Por que isso aconteceu e como resolver? Vamos analisar o seletor: li. Quais elementos da p�gina estamos selecionando? Todos os <li>, estejam eles no <aside>, no <header>, no <footer> ou em qualquer outro lugar da p�gina.

LIs selecionados

Mesmo se tentarmos usar o seletor de descendente � o espa�o � n�o conseguiremos selecionar apenas os <li> das redes sociais. O c�digo abaixo seleciona todos os <li> dentro de <aside>, estando eles dentro do <nav> ou n�o.

aside li {
    display: inline-block;
}
Precisamos, ent�o, de uma forma mais poderosa de selecionar elementos, que n�o seja apenas pelas tags HTML. Se pudermos, de alguma forma, dar um nome para a lista dos �cones das redes sociais, conseguimos fazer algo do tipo:

icones-sociais li {
    display: inline-block;
}
Assim, selecionamos os <li> somente dentro dessa lista. Para isso, temos o atributo id do HTML:

<ul id="icones-sociais">
    <!-- LIs continuam id�nticos aqui dentro -->
</ul>
Qualquer elemento pode ter um id e, com ele, podemos selecion�-lo facilmente no CSS: basta usar, no lugar da tag, o pr�prio id, precedido por cerquilha (#):

#icones-sociais {
    /* estilo exclusivo da lista de �cones */
}
Ent�o, para pegar os <li> dentro dessa lista espec�fica, basta combinar o seletor de id com o seletor de descend�ncia:

#icones-sociais li {
    display: inline-block;
}
Fazendo essas altera��es, conseguimos deixar apenas os �cones das redes sociais na horizontal.

Menu na vertical e �cones na horizontal

Pensando no futuro
O seletor de id j� resolve nosso problema agora. Mas imagine que precisamos colocar os �cones das redes sociais no rodap�, tamb�m. Podemos repetir o HTML?

<aside>
    <nav>
        <!-- links -->
    </nav>
    <ul id="icones-sociais">
        <!-- icones -->
    </ul>
</aside>
<footer>
    &copy; Jo�o da Silva 2014
    <ul id="icones-sociais">
        <!-- icones -->
    </ul>
</footer>
Como o id � um identificador, um nome para um elemento, ele n�o pode se repetir na p�gina. Quer dizer, se repetirmos um id na p�gina, o CSS e o JavaScript podem deixar de funcionar corretamente. Poder�amos dar um outro nome id para os �cones do rodap�, mas isso nos obrigaria a colocar esse outro nome no CSS tamb�m, o que geraria mais c�digo desnecessariamente.

Quando criamos uma p�gina, frequentemente temos um componente visual que se repete, como as cita��es no nosso caso.

Cita��es com mesma apar�ncia

No caso das cita��es, podemos agrup�-las todas pois todas usam a tag <blockquote>. Agora, no caso dos �cones das redes sociais, usamos a tag <ul>, que tamb�m � usada em outros contextos. Precisamos, ent�o, de uma forma de agrupar componentes da p�gina sem ser pela tag. � a� que entra o atributo class do HTML.

Enquanto o id n�o pode ser repetido, o class � feito para ser repetido. Podemos sem nenhum problema us�-lo para agrupar os �cones das redes sociais no <aside> e no <footer>:

<aside>
    <nav>
        <!-- links -->
    </nav>
    <ul class="icones-sociais">
        <!-- icones -->
    </ul>
</aside>
<footer>
    &copy; Jo�o da Silva 2014
    <ul class="icones-sociais">
        <!-- icones -->
    </ul>
</footer>
No CSS, podemos selecionar elementos pelo atributo class usando a classe precedida por um ponto (.):

.icones-sociais li {
    display: inline-block;
}
� dif�cil dizermos que um determinado componente visual nunca ser� repetido. Por isso, mesmo quando queremos identificar um componente �nico na p�gina para estiliz�-lo, � recomend�vel usar classes para essa estiliza��o.


--------------------------------------------------------------------------------------------------
<h1>Se��o 09 - Nem tudo � o que parece</h1>

Como j� discutimos antes, quando desenvolvemos uma p�gina, precisamos levar sempre em conta n�o s� a apar�ncia dos elementos da p�gina, mas tamb�m o que eles significam, ou seja, a sem�ntica deles.

Quando come�amos a lev�-la em conta, percebemos que nem sempre o mapeamento entre a apar�ncia de um elemento e o HTML � direto. Considere, por exemplo, o t�tulo da p�gina. Atualmente, ele est� assim: com letras mai�sculas e min�sculas.

Imagem do t�tulo da p�gina: sobre mim

Por�m, se olharmos no layout original, aquele que queremos implementar, o t�tulo � feito apenas de letras mai�sculas:

Imagem do t�tulo com letras mai�sculas

A primeira solu��o que podemos pensar � mudar o HTML para deixar o texto com letras mai�sculas:

<h1>SOBRE MIM</h1>
Para quem entende portugu�s, o significado n�o muda, pois ainda � poss�vel identificar as palavras "sobre" e "mim". Mas, para algu�m que n�o entende portugu�s, o que � isso? Quando usamos apenas letras mai�sculas, n�o estamos escrevendo uma palavra, mas sim uma sigla. Ent�o, quem n�o entende portugu�s vai achar que isso � uma sigla.

Dentre aqueles que n�o entendem portugu�s, podemos citar, al�m das pessoas que n�o falam portugu�s, as m�quinas. Isto �, programas como os leitores de tela e as ferramentas de busca n�o entendem o que nosso texto quer dizer. Isso significa, ent�o, que os programas leitores de tela e as ferramentas de busca n�o entendem o que nossa p�gina significa; para eles, tudo s�o apenas s�mbolos.

Ent�o como podemos fazer para manter o significado original, de palavra, e deixar o visual com letras mai�sculas? A pr�pria pergunta j� traz a resposta: o HTML � onde definimos o significado e o CSS � onde definimos a apar�ncia. Ent�o, no HTML, mantemos o texto com palavras:

<h1>Sobre mim</h1>
E, no CSS, mudamos a apar�ncia do texto usando a propriedade text-transform, dizendo que queremos que esse texto seja exibido com letras mai�sculas:

h1 {
    text-transform: uppercase;
}
Nem toda imagem � uma imagem
Anteriormente, colocamos os �cones das redes sociais na barra lateral usando uma lista para represent�-las. Conseguimos o resultado esperado, mas ser� que a sem�ntica est� correta?

Quando pensamos em colocar imagens na p�gina, a primeira ideia que vem � mente � colocar uma tag <img>. Por�m, precisamos pensar, como sempre, na s�mantica. Por que essas imagens est�o l�? Elas est�o l� para representar uma informa��o visual? Ou est�o l� apenas para representar visualmente o nome de uma rede social? Se est�o l� apenas porque representam visualmente o nome da rede social correspondente, dever�amos deixar o lado visual para o CSS, e deixar no HTML o nome da rede social, que � o que queremos passar de significado. Ou seja, nosso HTML ficaria assim:

<ul class="icones-sociais">
    <li>
        <a href="https://github.com/joaodasilva">
            Github
        </a>
    </li>
    <li>
        <a href="https://twitter.com/joaodasilva">
            Twitter
        </a>
    </li>
    <li>
        <a href="https://br.linkedin.com/pub/jo�o-da-silva/32/4/508">
            LinkedIn
        </a>
    </li>
</ul>
Agora, precisamos fazer a imagem aparecer via CSS e, al�m disso, fazer o texto sumir. Colocar a imagem via CSS � poss�vel gra�as � propriedade background-image.

.icones-sociais a {
    background-image: url(github.png);
}
Fazendo isso, veremos a imagem do Github atr�s do texto dos links.

Logo do Github cortado atr�s dos textos dos links

Repare que o logo do Github est� cortado. Precisamos, ent�o, definir um tamanho para o link, de modo que a imagem inteira apare�a no fundo do elemento. Para isso, usamos as propriedades width e height. Por�m, para que essas propriedades funcionem com nossos links, � necess�rio que eles tenham um display que seja inline-block ou block. Vamos usar o valor block, mas poderia ser inline-block tamb�m.

.icones-sociais a {
    background-image: url(github.png);
    width: 40px;
    height: 40px;
    display: block;
}
Com isso, j� conseguimos ver a imagem inteira, mas o texto continua em cima dela.

Logo do Github completo, mas atr�s do texto

Como remover o texto? No CSS, existe a propriedade text-indent, que permite regular o recuo da primeira linha de um par�grafo.

Efeito da propriedade text-indent

Quando colocamos um tamanho maior que zero para essa propriedade, a primeira linha come�a um pouco depois das linhas seguintes. Se colocamos um tamanho menor que zero, a primeira linha come�a um pouco antes.

text-indent positivo e negativo

Se aumentamos muito o valor do text-indent, o texto pode come�ar fora da p�gina.

text-indent muito grande joga o texto para fora da p�gina

Mas, se o texto tiver mais de uma palavra, apenas a primeira palavra ficar� para fora da p�gina. Ent�o podemos tentar com um tamanho bem menor que zero. No nosso caso, nosso CSS vai ficar parecido com:

.icones-redes-sociais a {
    background-image: url(github.png);
    width: 40px;
    height: 40px;
    display: block;
    text-indent: -99999px;
}
Com isso, conseguimos o efeito desejado.

Logotipo do Github sem o texto por cima

Conseguimos, assim, substituir um texto do HTML por uma imagem carregada via CSS. Essa � uma pr�tica comum, t�o comum que at� tem um nome popular: image replacement.

S� falta arrumar um problema: todos os links est�o com a imagem do Github. Isso acontece porque, no CSS, estamos selecionando todos os links de uma vez. Para selecionar cada link de uma vez, podemos colocar uma classe para cada um:

<ul class="icones-sociais">
    <li>
        <a href="https://github.com/joaodasilva" class="github">
            Github
        </a>
    </li>
    <li>
        <a href="https://twitter.com/joaodasilva" class="twitter">
            Twitter
        </a>
    </li>
    <li>
        <a href="https://br.linkedin.com/pub/jo�o-da-silva/32/4/508" class="linkedin">
            LinkedIn
        </a>
    </li>
</ul>
No CSS, podemos manter boa parte das regras no seletor .icones-sociais a. Apenas a imagem de fundo muda, ent�o apenas essa declara��o precisa ficar na classe espec�fica do link:

.icones-sociais a {
    width: 40px;
    height: 40px;
    display: block;
    text-indent: -99999px;
}

.github {
    background-image: url(github.png);
}

.twitter {
     background-image: url(twitter.png);
}

.linkedin {
    background-image: url(linkedin.png);
}


<h2>Outras formas de image replacement<h2>
Fizemos o image replacement usando, entre outras, a propriedade text-indent com um valor negativo bem grande. Contudo, essa � apenas uma forma poss�vel de aplicar essa t�cnica.

Experimente, por exemplo, trocar a declara��o text-indent: -9999px por font-size: 0. Funciona tamb�m, n�o?

Ent�o qual desses m�todos usar? Discuta vantagens e desvantagens que voc� enxerga em cada m�todo.

A propriedade text-indent tem um comportamento que depende da l�ngua usada na p�gina. Em algumas l�nguas, como o �rabe, escrevemos da direita para a esquerda. Ent�o, se nossa p�gina est� escrita nessa dire��o, o text-indent tem seu comportamento invertido: um valor positivo joga o texto para a esquerda e, por outro lado, um valor negativo joga o texto para a direita. Assim, se usamos um text-indent bem negativo e sua p�gina est� escrita nessa dire��o, o texto do elemento com image replacement ficar� bastante para a direita e, portanto, far� aparecer no navegador uma barra de rolagem horizontal.

Um outro problema com o valor muito grande e negativo da propriedade text-indent � que esse valor muito grande pode fazer com que o navegador gaste muita mem�ria para exibir a p�gina, pois agora ele precisa levar em considera��o um elemento muito grande nos c�lculos para a exibi��o da p�gina.

Por outro lado, usar o font-size com valor zero n�o � bem interpretado por todos os navegadores. Alguns simplesmente ignoram uma declara��o desse tipo; outros, mesmo com o tamanho zerado, mostram o texto numa fonte pequena. Ou seja, h� um problema de compatibilidade com essa t�cnica, que a propriedade text-indent n�o tem.


------------------------------------------------------------------------------------------------------
<h1>Se��o 10 - Posicionamento mais a fundo</h1>

Nossa p�gina est� quase pronta. Resta apenas colocar a barra lateral, a foto e as cita��es nos seus devidos lugares.

P�gina no estado atual

Resultado desejado

Vamos come�ar pelas cita��es. Repare que, no final, cada uma deve ficar de um lado do texto. Vimos que a propriedade display permite colocar um elemento ao lado do outro. Por�m, ela n�o permite mudar a ordem de exibi��o dos elementos: o que vem primeiro no HTML, vem primeiro no visual.

Para conseguirmos o resultado desejado, precisamos "quebrar" essa rela��o de ordem entre o HTML e o visual final, que podemos chamar de fluxo do documento.

Uma das propriedades que nos permite fazer essa "quebra" � a propriedade float. H� dois valores poss�veis para ela (al�m do none, que � o padr�o): left e right. Quando colocamos float: left na cita��o, a caixa da cita��o permanece no mesmo lugar, mas o texto, que estava abaixo, passa a ficar ao lado da cita��o, como se tiv�ssemos definido tanto a cita��o como o texto como elementos inline.

Cita��o com float: left

Mas repare que n�o � exatamente o mesmo comportamento de um elemento inline: o subt�tulo seguinte, depois do par�grafo, tamb�m vai parar do lado da cita��o! O que aconteceu, na verdade, � que o resto do conte�do da p�gina "subiu", e a cita��o ficou flutuando do lado esquerdo do conte�do.

Se usarmos o valor right, veremos que a cita��o permanece na mesma altura do fluxo, mas do lado direito do conte�do.

Cita��o com float: right

� importante notar que os elementos flutuados permanecem na mesma altura de antes. Isso nos permite prever qual comportamento teremos ao usar a propriedade.

Elemento flutuado permanece na mesma altura do fluxo de antes

Para conseguir o resultado desejado no layout final, com cada cita��o de um lado, precisamos ser capazes de selecionar apenas uma delas individualmente. Para isso, podemos usar um id para cada uma delas mas, como vimos nas aulas anteriores, o ideal � sempre usar classes. Ent�o podemos colocar mais uma classe nas cita��es:

<h2>Como trabalho</h2>
<blockquote class="citacao-bio-fiat">
    <p>Jo�o � o melhor...</p>
    <cite>Jos� Souza, Fiat</cite>
</blockquote>
<!-- ... -->
<h2>Experi�ncia</h2>
<blockquote class="citacao-bio-petrobras">
    <p>Jo�o domina as tecnologias...</p>
    <cite>Manoel Santos, Petrobr�s</cite>
</blockquote>
Agora, nas classes rec�m-criadas, colocamos a declara��o da propriedade float:

.citacao-bio-fiat {
    float: right;
}

.citacao-bio-petrobras {
    float: left;
}
E temos quase o resultado esperado.

Cita��es flutuando � esquerda e � direita

Repare que os subt�tulos tamb�m acabam ficando do lado das cita��es; n�o queremos isso. Felizmente, podemos controlar o fluxo do documento com rela��o aos floats da p�gina. Para isso, usamos a propriedade clear, que permite dizer que n�o queremos floats do lado de um determinado elemento. Por exemplo, se n�o queremos floats � esquerda dos nossos subt�tulos, podemos fazer:

h2 {
    clear: left;
}
Comunidade com clear:left

Repare que o subt�tulo "Comunidade" � "empurrado" para baixo, para n�o ficar ao lado da cita��o com float: left. Mas o subt�tulo "Experi�ncia" continua ao lado da cita��o com float: right. Ent�o, na verdade, queremos que n�o haja floats em nenhum dos lados dos <h2>. Para isso, usamos o valor both na propriedade clear:

h2 {
    clear: both;
}
Assim, chegamos no resultado esperado, bastando apenas alguns pequenos ajustes nas margens das cita��es para que elas fiquem alinhadas com o texto.

Subt�tulos com clear:both

Floats e mais floats
Podemos aproveitar a ideia de floats para posicionar a foto e a barra lateral tamb�m. Para entender como isso � poss�vel, precisamos entender o que acontece quando temos v�rios floats seguidos no HTML.

Como o float faz com que o elemento saia do fluxo, o resto do conte�do da p�gina sobe. Assim, se outro float vem logo em seguida no fluxo, esse outro float acabar� na mesma altura do primeiro float, independente do lado em que ele vai ficar.

Floats seguidos sendo aplicados pelo navegador

Agora, e se esse segundo float tem a propriedade clear definida justamente com o lado em que o primeiro float est�?

.primeiro {
    float: left;
}

.segundo {
    float: left;
    clear: left;
}
Neste caso, o segundo float ser� "empurrado" para baixo, da mesma forma que qualquer outro conte�do. Por�m, o conte�do sem float continuar� ao lado dos dois floats.

Floats com clear no segundo e conte�do ao lado

Se olharmos para o resultado do cen�rio descrito acima, veremos que ele � bem parecido com o resultado que desejamos, apenas espelhado. Ent�o podemos tentar aplicar essa l�gica no nosso layout, definindo tamb�m as larguras para o conte�do, de forma que a parte do texto fique com 80% da largura da tela e a foto e a barra lateral com 20%.

main {
    width: 80%;
}

img,
aside {
    width: 20%;
    float: right;
}

aside {
    clear: right;
}
Por�m, se fizermos isso, o resultado n�o ser� o esperado: a foto e a barra lateral ficam na mesma altura do rodap�. Al�m disso, a barra lateral fica mais larga que a foto.

Resultado do float: right na imagem e no aside

Esse segundo problema ocorre devido ao box model padr�o do navegador. Como a barra lateral tem padding e o padding n�o entra no c�lculo da largura do elemento por padr�o, ela acaba ficando mais larga. Para resolver esse problema, basta dizermos ao navegador que queremos que ele calcule a largura do elemento levando o padding em conta (e a borda, que colocaremos mais adiante) usando a propriedade box-sizing com o valor border-box:

aside {
    box-sizing: border-box;
}
Isso resolve o problema da largura, mas n�o o fato de a imagem e a barra lateral estarem na altura do rodap�. Por�m, na verdade, isso deveria acontecer, pois os elementos flutuados permanecem na altura em que estavam e a imagem, de fato, estava abaixo do texto, como est� agora.

Como fazer, ent�o, para que ela fique no topo da p�gina? A solu��o � lembrar que floats seguidos formam uma linha. Se o <main> tamb�m for um float, a imagem ficar� em linha com ele. Ou seja, basta adicionar a declara��o:

main {
    float: left;
}
Ao fazermos isso, a imagem e a barra lateral ficar�o no lugar certo, ao lado do cabe�alho. Mas, estranhamente, o rodap� da p�gina tamb�m sobe. Por que?

Resultado ap�s aplicar float: left no main

Cuidado com tantos floats!
Precisamos lembrar que, sempre que transformamos um elemento em float, ele sai do fluxo da p�gina, o que faz com que o resto do conte�do suba. Neste caso, o rodap� subiu para ocupar o espa�o entre os floats que criamos.

Para resolver esse problema, basta lembrarmos da propriedade clear. N�o queremos nenhum float em nenhum dos lados do nosso rodap�, ent�o podemos declarar:

footer {
    clear: both;
}
Com isso, chegamos num resultado bem mais pr�ximo do desejado.

Resultado ap�s aplicar o clear:both no rodap�

Frequentemente, quando usamos floats para posicionar os elementos do nosso layout, precisamos "limpar" a sequ�ncia de floats, como no nosso caso agora. Assim, � comum encontrarmos declara��es clear: both nesse tipo de layout. Essa � uma solu��o t�o comum que at� ganhou um nome popular: clearfix. Frequentemente, projetos incluem em seus arquivos CSS uma classe cujo �nico prop�sito � fazer essa "limpeza" de floats:

.clearfix {
    clear: both;
}
Se tiv�ssemos essa classe no nosso arquivo CSS, bastaria aplic�-la no nosso rodap�:

<footer class="clearfix">
    &copy; Jo�o da Silva 2014
</footer>
Aumentando a imagem
Falta apenas fazer com que a imagem fique maior do que a barra lateral, sobrepondo um pouco do <main> tamb�m. Para conseguir esse resultado, precisamos entender mais uma propriedade, que veremos na pr�xima aula.

----------------------------------------------------------------------------------------------
<h1>Se��o 11 - Elementos onde queremos</h1>

Nossa p�gina j� est� quase com o layout que queremos. Falta apenas deixar a foto do Jo�o da Silva maior, cobrindo ligeiramente o resto da p�gina.

Se aumentarmos a foto, nosso layout quebra completamente: a foto e a barra lateral descem para baixo do conte�do principal. Isso porque estamos usando a propriedade float para posicionar esses dois elementos. Essa propriedade nos permite posicionar elementos, por�m de uma forma limitada, respeitando o fluxo do documento.

Layout quebrado por causa da foto um pouco maior

Para posicionarmos elementos com controle total, precisamos da propriedade position e suas parceiras top, left, bottom e right. O comportamento dessas quatro �ltimas propriedades muda bastante de acordo com o valor passado � propriedade position. Vamos estudar cada um desses valores em detalhe.

Posicionamento relativo
Quando passamos o valor relative para a propriedade position, conseguimos mudar a posi��o do elemento de acordo com a posi��o original dele. Por exemplo, podemos deslocar a foto de sua posi��o original para tentar aument�-la depois.

Foto ligeiramente deslocada para baixo e para a esquerda

Para conseguir esse efeito, usamos o position: relative em conjunto com top e right, inserindo espa�o no topo e na direita:

img {
    position: relative;
    top: 30px;
    right: 30px;
}
Repare que o resto da p�gina continua intacto! Apenas a foto � deslocada, cobrindo um pouco da barra lateral e do cabe�alho.

Agora podemos tentar aument�-la. Colocamos uma largura de 300 pixels, por exemplo e... o resultado n�o � o esperado: a foto e a barra lateral descem.

Foto aumentada, fazendo o conte�do descer

Por que isso acontece? Precisamos lembrar que a foto e a barra lateral est�o posicionados com o uso da propriedade float. Quando aumentamos a foto, ela deixa de caber do lado do nosso conte�do principal (tag <main>).

O position: relative tem v�rios usos interessantes. Mas nossa ideia de usar o position: relative e, depois, aumentar a imagem n�o vai funcionar porque nossa foto n�o pode influenciar os outros elementos.

Posicionamento absoluto
Quando falamos de posicionar elementos na p�gina independentemente do resto do conte�do, estamos falando de usar o valor absolute da propriedade position. Com ele, podemos colocar um elemento onde quisermos na p�gina. Podemos pegar nossa foto grande, que n�o est� cabendo ao lado do cabe�alho, e transformar seu posicionamento em absoluto:

img {
    width: 300px;
    position: absolute;
}
Isso vai nos dar um resultado um tanto interessante. Primeiro, veremos que a barra lateral aparentemente desaparece. Segundo, veremos que a foto permanece ao lado do cabe�alho, s� que um pouco para fora da p�gina.

Foto com position:absolute

Podemos mover a foto para uma outra posi��o qualquer da p�gina como, por exemplo, o canto superior esquerdo. Para isso, dizemos que queremos zero de dist�ncia entre o topo da p�gina e a foto e entre a borda esquerda da p�gina e a foto:

img {
    width: 300px;
    position: absolute;
    top: 0;
    left: 0;
}
A foto vai para o canto esquerdo da tela e vemos que a barra lateral n�o desapareceu, apenas estava escondida atr�s da foto.

Foto no canto superior esquerdo da p�gina com position:absolute

Como queremos que a foto fique no canto superior direito, vamos usar right: 0 no lugar de left: 0. Mas ainda precisamos fazer com que a barra lateral apare�a! Podemos fazer isso de algumas maneiras como, por exemplo, usando o position: relative. Deslocamos a barra lateral para baixo, 300 pixels da altura da foto mais os 10 pixels de borda que ela tem.

img {
    width: 300px;
    position: absolute;
    top: 0;
    right: 0;
}

aside {
    position: relative;
    top: 310px;
}
E, assim, chegamos no resultado final desejado.

P�gina como desej�vamos no come�o do curso

Posicionamento fixo
Podemos ir um pouco al�m do resultado desejado e come�ar a pensar na interatividade da p�gina. O que acontece, por exemplo, quando nosso usu�rio faz a rolagem da p�gina? Ou quando coloca o mouse em cima de um link? Vemos algumas dessas quest�es no curso avan�ado de HTML.

Por�m, um detalhe relativamente simples de ser feito e que tem um resultado interessante � deixar o rodap� da p�gina sempre vis�vel, independentemente da posi��o da rolagem da p�gina no navegador.

Rodap� sempre vis�vel

Para conseguir esse resultado, usaremos mais um valor da propriedade position: o valor fixed. Ele nos permite deixar um elemento no lugar que quisermos da janela usando, tamb�m, as propriedades top, left, bottom e right para determinar a dist�ncia do elemento para esses quatro cantos da janela.

Aplicando a ideia ao nosso <footer>, teremos:

footer {
    position: fixed;
    bottom: 0;
    left: 0;
}
O resultado inicial ser� um pouco estranho. O rodap� deixar� de ocupar toda a parte de baixo da tela.

Rodap� pequeno no canto esquerdo da tela

Podemos resolver isso determinando que a largura seja 100%. Como o rodap� tem um espa�amento interno (padding), precisamos usar o width junto com o box-sizing, para que a largura seja medida pelas bordas do rodap�, e n�o pelo espa�o interno apenas.

footer {
    position: fixed;
    bottom: 0;
    left: 0;
    width: 100%;
    box-sizing: border-box;
}
Feito isso, teremos o resultado visual esperado, mas n�o conseguiremos ver o final da p�gina. O rodap� ficar� em cima do final da p�gina.

Rodap� em cima do final da p�gina

Para resolver esse problema, podemos colocar um espa�o extra no final do conte�do principal (tag <main>), dentro dele. Usamos, ent�o, a propriedade padding-bottom:

main {
    padding-bottom: 80px;
}
-----------------------------------------------------------------------------------------------------
<h1>Desafios finais</h1>

Durante o curso, desenvolvemos duas p�ginas: bio.html e blog.html. Com elas, exploramos as linguagens HTML e CSS. Agora que temos esse conhecimento em m�os, podemos nos preocupar com alguns detalhes al�m da tecnologia e aproveitar para amadurecer nossos conhecimentos.

Organiza��o do projeto
Um primeiro detalhe com o qual podemos nos preocupar � a organiza��o do c�digo no projeto. At� agora, est�vamos colocando todos os arquivos juntos no mesmo diret�rio. Ainda n�o temos muitos arquivos, mas j� come�a a ficar meio complicado de encontrar o que queremos. Num projeto maior, isso pode ser bem complicado!

A ideia, ent�o, � separar os arquivos em diret�rios de acordo com o tipo deles. Ou seja, um diret�rio para imagens, um para arquivos CSS... Os arquivos HTML podem ficar no diret�rio principal, j� que s�o a base do projeto.

Organiza��o do CSS
Outra coisa que podemos notar � que nosso c�digo CSS est� ficando grande. Conforme o projeto vai crescendo, fica cada vez mais complicado manter todo o estilo num �nico arquivo.

Para facilitar a manuten��o desse c�digo, podemos quebr�-lo em v�rios arquivos de acordo com os crit�rios que acharmos mais interessantes. Um crit�rio bastante comum � a p�gina � qual aquele c�digo se aplica. Ou seja, criamos um arquivo CSS para cada p�gina. Nesse crit�rio, � importante observar que parte do c�digo � aplicado a todas as p�ginas (pense no cabe�alho ou na barra de navega��o, por exemplo)! Assim, acabamos com a divis�o: um arquivo para o estilo gen�rico de todas as p�ginas e um arquivo espec�fico para cada p�gina.

Consolidando o conhecimento
Para consolidar o que vimos durante o curso, deixaremos para voc� o desafio de criar mais uma p�gina para o site do Jo�o da Silva: o portf�lio. Essa p�gina ter� a lista dos projetos feitos por ele e quais responsabilidades ele teve em cada um. Veremos mais detalhes nos exerc�cios.