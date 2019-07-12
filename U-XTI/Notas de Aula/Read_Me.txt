IDE - Dream Weaver (Pago)

***AULA 1 e 2 - INTRODUÇÃO AO CSS***
Torna sua vida no mundo web muito mais colorida haha
Cascading Style Sheet (CSS) é um mecanismo simples para adicionar estilos nos documentos web. O CSS é mais uma tecnoligia que é normatizada pela W3C. O HTML e o SCC é a base de todos os projetos desenvolvidos para a web.

O HTML deve ser utilizado apenas para estruturar a página. O CSS será responsável pela criação do estilo das páginas. Já existe o CSS3, mas ele ainda não é sportados por todos os brousers.

O site http://www.cssmania.com/ possui estilos CSS para diversas situações.

No site W3Schools pode-se encontrar muitas referências ao CSS.

*** Paleta de cores RGB e Hexadecimal:
	https://www.w3schools.com/colors/colors_picker.asp

================================================================================================================
***AULA 2 - SINTAXE STYLE SHEET***
As TAG's possuem o atributo tyle que recebem declarações CSS para personalizar seu conteúdo. Existem uma TAG que não foi vista no curso de HTML que se chama <style></style>. Esta TAG fica dentro da TAG <head></head> e é utilizada para centralizar todos os estilos da página dentro desta TAG <style>. Essa abordagem não é interessante, pois se o arquivo html ficar muito extenso, pode ficar difícil dar manutenção no código.

Para começar a introduzir estilos CSS nas páginas html ´enecessário utilizar seletores.
Seletores são elementos/alvos que receberão as declarações CSS e a declaração vai sempre entre chaves. Os seletores vão dentro da TAG <style> e a TAG style vai dentro da TAG <head></head> na sua estrutura HTML. Veja um exemplo:
<head>
     <style type="text/css" media="all">
    		p {
    			color: #006699;
    			font-size:12px
    		}
    </style>
</head>

O atributo 'type' que valida a aplicação dos estilos. O atributo 'media' indica qual o dispositivo que irá receber este CSS. Os valores que podem ser passados para este atributo são:

screen: para monitores
tty: para teletipo
tv: para dispositivos de televisão
projection: utilizado para projetores
handheld: utilizados para dispositivos móveis
print: Para visualização em modo de impressão
aural: para sintetizadores de voz
all: É o CSS que será aplicado para todos os dispositivos acima.

Quando o estilo não puder ser aplicado o código html recebe  estilo padrão do navegador

Esta declaração significa que toda TAG <p> receberá esta formatação. O elemento p é chamado de seletor e ele determina onde será aplicada a regra CSS. Pode-se ter diversas declarações dentro de uma regra. A regra CSS e a unidade básica de uma folha de estilos. Se mais de uma TAG for receber a mesma configuração de estilo, pode-se criar apenas um bloco de estilo, relacionado a mais de um seletor, basta separar os seletores por vírgula, exemplo:

<style type="text/css">
		p, h1, h3 {
			color: 006699;
			font-size:12px
		}
</style>

Caso seja necessário personalizar a TAG h1 novamente e somente ela, basta criar um seletor para ela separadamente. Para passar valores com palavras compostas, informe o valor entre aspas duplas, exemplo:
h1{
	font-familt: "comic sans"
}

É possivel fazer comentários dentro da TAG <style> para isso o comentário vem entre /**/
Exemplo: /*trecho comentado*/

O arquivo "aula1-2.html" possui exemplos de uso de seletores.

================================================================================================================
***AULA 3 - FOLHAS DE ESTILO***

As folhas de estilo podem ser escritas no próprio documento html (dentro da TAG <style>), dentro da própria TAG html (estilo inline), ou pode-se criar um documento específico para conter o estilo (estilo esterno).

A folha de estilo externo se trada de um arquivo que não foi escrita dentro do documento html. Este arquivo deve ser gravado com a extensão ".css".

Deve-se criar um diretório nomeado 'css' e dentro dele devem ser colocadas todas as folhas de estilo utilizadas pelo sistema. Neste arquivo não é necessário utilizar a TAG <style> basta adicionar as regras.

Existem duas formas de vincular o arquio de estilos ao código html.

A primeira forma é utilizando "folhas de estilo linkadas". A TAG <link> dentro da TAG <head></head> e informar o tipo de link através do atributo 'rel="stylesheet"', informar o tipo de folha de estilo através do atributo 'type="text/css"' e informar o caminho do arquivo .css usando o atributo 'href="caminho/nome.css"' e qual o tipo de mídia a qual o seu CSS será aplicado pelo atribudo 'media'.
Exemplo:
<link rel="stylesheet" type="text/css" href="diretorio/nome_arquivo.css" media="all" />

A segunda forma é utilizar "folhas de estilos importadas". Utilizando a TAG <style type="estilos.css"><style/>. Dentro do corpo da TAG deve ser informada qual folha de estilos será importada, da seguinte forma: @import url("esilos.css") screen, projection;
Se o tipo de mídia não for informado, o estilo será aplicado a todas as mídias por padrão.
Exemplo:

<style type="text/css">
	@import url("css/estilos.css") screen, projection;
</style>

Pode-se colocar essa segunda forma de importar folhas de estilo dentro de um arquivo.css que funciona da mesma forma, a diferença é que não é nece´ssário usar a TAG <style></style>.

Os arquivos aula3.1.html e aula3.2.html possuem exemplos.

================================================================================================================
***AULA 4 e 5 - SELETORES SIMPLES***

Existem três tipos de seletores: Simples, Compostos, e Pseudo-coletores. Nesta aula focaremos nos seletores simples.

Seletores simples são aqueles constituidos de apenas um elemento e pode, ou não, estar associado com uma classe, id ou pseudo-classe.

Exemplo de seletor simples com o elemento h1:
h1 {color: blue; font-size: 12px;}.

Existem 5 tipos de seletores simples.

Seletor universal:
	É o seletor que será aplicado a todos os elementos do documento .html, todas as instâncias do documento são alvos do seletor universal. O seletor universal é representado pelo asterísco (*). As regras definidas dentro do escopo deste seletor será aplicada a todos os elementos do documento, a não ser que se tenha uma regra mais específica.
	O seletor universal é mais utilizado para remover os valores padrão aplicados na página pelo próprio brouser, como margem. O seletor simples é a formatação que possui menor prioridade.

	Exemplo de seletor simples:
	*{margin: 0;}

Seletor elemento:
	É o tipo de estilo que será aplicado a um elemento(TAG) html.

Seletor classe:
	Para utilizar um seletor classe, é necessário atribuir uma classe a uma TAG por meio do atributo 'class' que recebe como valor um nome de sua escolha que identificará aquele seletor. Uma vez que este passo foi feito, basta criar um bloco no arquivo .css como  nome da classe precedido de um ponto. Por convenção as classes tem nome em minúsculo.

	Exemplo:
	No arq html:
		<h1 class="titulo">
	No arq .css:
		.titulo{font-size: 25px;}

	É possível ter mais de uma classe aplicada ao mesmo elemento. Para isso, basta adicionar o nome da outra classe como valor do atributo 'class' separando os nomes com um espaço simples e criar um bloco no arquivo .css como  nome da classe precedido de um ponto.
	Exemplo:
	<h1 class="titulo tamanho">

Seletor id:
	O seletor id é aplicado nos atributos que possuem o atributo 'id' informado. Como o id é um identificador único da TAG, nenhum outro elemento da página poderá ter este mesmo id. Para aplicar uma formatação css em um seletor id, deve se criar um bloco de código no arquivo .css com o nome do id precedido do símbolo '#'.
	Exemplo:
	No arq html:
		id="post01"
	No arq css:
		#post01{font-size: 25px;}
	
Seletor atributo:
	É um seletor que casa com determinado atributo de um dos elementos (TAG) do texto html. Para isto utilize o atributo 'title' e passe como valor um nome identificador para este seletor.
	Exemplo:

	html:
		<strong title="casa">casa</strong>
	css:
		strong[title="casa"]{
		color: #00ff00;
		font-size: 40px;
	}

	Se o valor do atributo 'title' for tiver mais de uma palavra separadas por espaço, no arquivo css, usa-se o ~ imediatamente antes do simbolo = para que a formatação ainda possa ser aplicada.
	Exemplo:

	html:
		<strong title="casa 01">casa</strong>
	css:
		strong[title~="casa"]{
		color: #00ff00;
		font-size: 40px;
	}

	Se o valor do atributo 'title' for tiver mais de uma palavra separadas pelo sinal de menos, no arquivo css, usa-se o | imediatamente antes do simbolo = para que a formatação ainda possa ser aplicada.

	html:
		<strong title="casa-01">casa</strong>
	css:
		strong[title|="casa"]{
		color: #00ff00;
		font-size: 40px;
	}

Estes são todos os seletores simples.

================================================================================================================
***AULA 6 - SELETORES COMPOSTOS***

O seletor composto é composto de diversos outros seletores.

Seletor Descendente:
	É aquele que é aplicado a um elemento do documento que descende de outro elemento.
	Por exemplo, no body do arquivo aula5.html, temos o elemento <strong> que está dentro do elemento <p> que por sua vez esta dentro do elemento <div>.
	
	Caso se queira alcançar o elemento <strong> dentro do elemento <div> basta criar um seletor com a sintaxe css da seguinte forma:
	div strong {
		/*estilos*/
	}

	Perceba que no caso de um seletor descendente não é necessário declarar todo o "caminho" até o elemento que se quer formatar, pois omitimos a o elemento <p> na declaração acima. Também poderiamos tê-lo informado, da seguinte forma...

	div p strong {
		/*estilos*/
	}
	... tornando a declaração completa.

Seletor Filho:
	O seletor filho é um seletor que aplica uma formatação css no elemento que está imediatamente 1 nivel dentro do elemento mais externo. Utilizamos o sinal maior (>) para explicitar a formatação.
	Exemplo:

	div > strong {
		text-decoration: underline;
		font-size: 20px;
	}

Seletor Irmão-Adjacente:
	Este seletor aplica no elemento (TAGs) irmão que está adjacente a um elemento de referência, ou seja, TAGs, não necessáriamente iguais, que estão sequencialmente presentes no documento.html, como uma sequencia de paragrafos TAGs <p></p>. Caso você queira aplicar um estilo à TAG <p> após o primeiro <p> faça:
	p + p{
		color: blue;
	}

	Este estilo será aplicado ao irmão da primeira TAG <p>.

	Se a próxima TAG fosse uma TAG <h2> bastava fazer:
	p + h2{
		color: green;
	}

================================================================================================================
***AULA 6 - PSEUDO CLASSES E PSEUDO ELEMENTOS***

O funcionamento dos seletores se baseiam na posição dos elementos na árvore do documento html, então dependendo de onde a TAG estiver podemos alcançá-lo como os seletores como visto nas aulas anteriores. Mas existem casos em que não seria possível alcançar estes elementos. Desta forma as pseudo classes e os pseudos elementos foram criados para complementar os seletores, com a finalidade de estilizar informações que estão inacessíveis na árvore do documento html e de conteúdos que sequer estejam na marcação html.

A pseudo classe pode ocupar qualquer posição no seletor, e o pseudo elemento deve ser colocado após o ultimo seletor simples.

Continuar no momento 2:00min da aula 7...