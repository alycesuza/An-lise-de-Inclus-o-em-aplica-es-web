# Analise de Inclusão em Aplicações Web
## Um guia pratico dos padrões de navegabilidade e acessibilidade

Este conjunto de documentos é uma versão baseada em texto de parte do conteúdo abordado no projeto A
,
Compreender a acessibilidade, seu escopo e seu impacto pode torná-lo um desenvolvedor web melhor. Este guia destina-se a ajudá-lo a entender como tornar seus sites acessíveis e utilizáveis por todos.

"Acessibilidade" pode ser difícil de soletrar, mas não precisa ser difícil de realizar. Neste guia, você verá como obter algumas vitórias fáceis para ajudar a melhorar a acessibilidade com o mínimo de esforço, como você pode usar o que está embutido no HTML para criar interfaces mais acessíveis e robustas e como aproveitar algumas técnicas avançadas para criar experiências acessíveis polidas .

Você também descobrirá que muitas dessas técnicas o ajudarão a criar interfaces mais agradáveis ​​e fáceis de usar para todos os usuários, não apenas para aqueles com deficiências.

Claro, muitos desenvolvedores têm apenas uma compreensão nebulosa do que significa acessibilidade - algo a ver com contratos governamentais, listas de verificação e leitores de tela, certo? - e há muitos equívocos por aí. Por exemplo, muitos desenvolvedores acham que abordar a acessibilidade os forçará a escolher entre criar uma experiência agradável e atraente ou uma experiência desajeitada e feia, mas acessível.

Isso, é claro, não é o caso, então vamos esclarecer isso antes de entrarmos em qualquer outra coisa. O que queremos dizer com acessibilidade e o que estamos aqui para aprender?


### O que é acessibilidade?
De um modo geral, quando dizemos que um site é acessível, queremos dizer que o conteúdo do site está disponível e sua funcionalidade pode ser operada, literalmente, por qualquer pessoa . Como desenvolvedores, é fácil supor que todos os usuários podem ver e usar um teclado, mouse ou tela sensível ao toque e podem interagir com o conteúdo de sua página da mesma maneira que você. Isso pode levar a uma experiência que funciona bem para algumas pessoas, mas cria problemas que variam de simples aborrecimentos a interrupções para outras.

Acessibilidade, então, refere-se à experiência de usuários que podem estar fora do alcance restrito do usuário "típico", que pode acessar ou interagir com coisas de maneira diferente do que você espera. Especificamente, trata-se de usuários que estão passando por algum tipo de deficiência ou deficiência - e tenha em mente que essa experiência pode ser não física ou temporária.

Por exemplo, embora tenhamos a tendência de centrar nossa discussão sobre acessibilidade em usuários com deficiências físicas, todos podemos nos relacionar com a experiência de usar uma interface que não é acessível a nós por outros motivos. Você já teve problemas ao usar um site para computador em um celular, ou viu a mensagem "Este conteúdo não está disponível em sua área" ou não conseguiu encontrar um menu familiar em um tablet? Essas são todas as questões de acessibilidade.

À medida que você aprende mais, descobrirá que abordar os problemas de acessibilidade nesse sentido mais amplo e geral quase sempre melhora a experiência do usuário para todos. Vejamos um exemplo:

![image](https://user-images.githubusercontent.com/88754556/175758991-558800ed-a6af-45ea-a633-e08bd955c9b9.png)

Este site tem varios problemas de acessibilidade.

- O texto é de baixo contraste, o que é difícil para usuários com baixa visão lerem.
- Fonte pequena (instrutor Boot Santos) e cor quase não visível
- Imagem de fundo que distrai, 
- Deve-se melhorar a saturação e brilho do site
- Há imagens com baixa resolução
- A imagem de fundo ser animada, e desfocada, o que dificulta a leitura.

Agora vamos agitar nossa varinha de acessibilidade e propor mudanças para mitigar estes problemas:

![image](https://user-images.githubusercontent.com/88754556/175759821-91f014dc-62fd-4a46-9380-d26b3e18a4d6.png)
![image](https://user-images.githubusercontent.com/88754556/175759831-b5c7725a-377a-45fc-a0c1-34aae2542117.png)

Acrescentar barra de atalhos com os ícones de :Botões , especificando devidos atalhos, aumento e diminuição de letra e contraste da página.
Ao clicar em contraste, a parte menu do site tem variação de cor de preto para branco, além disso pode-se também optar por aumento das letras dos ícones, como demonstrado na imagem abaixo:  

![image](https://user-images.githubusercontent.com/88754556/175759848-46e03d8d-4d75-448b-9ee3-ac96ef7fed3f.png)

Foi acrescentado uma barra de rolagem em tons mais nítidos:

![image](https://user-images.githubusercontent.com/88754556/175759882-d7db2c09-1bac-4b40-a17b-59cb0e8a30c8.png)

E tirado a transição de fundo para uma imagem estática:

![image](https://user-images.githubusercontent.com/88754556/175759892-67aeb202-b2fc-4a1d-9d47-332d452a85c1.png)

Qual você prefere usar? Se você disse "a versão acessível", está no caminho certo para entender a premissa principal deste guia. Muitas vezes, algo que é um bloqueador completo para alguns usuários também é um ponto problemático para muitos outros, portanto, ao corrigir o problema de acessibilidade, você melhora a experiência para todos.

### A acessibilidade começa com o seu HTML

HTML — assim como sua linguagem de estilo complementar, CSS — é flexível. Se você quiser construir um certo tipo de página, provavelmente há várias maneiras de escrever com HTML e estilizá-la com CSS. No entanto, nem todos os elementos HTML são iguais quando se trata de acessibilidade.

Ao escrever páginas da web, a melhor maneira de torná-las acessíveis é usar HTML semântico . HTML semântico é um código HTML que diz o que faz – em outras palavras, a própria tag transmite o propósito do elemento. Elementos semanticamente ricos incluem :

```
<button> , <form> , <header> , <footer> , <nav> e os títulos <h1> , <h2> , etc.
 ```
 
Considere o exemplo abaixo. Aqui, temos dois elementos de botão que, pelo menos ao olho humano, parecem iguais:
  
![image](https://user-images.githubusercontent.com/88754556/175757659-7f8fea69-37ef-4a78-b3af-ce1df17d6bdd.png)

  Mas, se você revelar o HTML subjacente, verá que o primeiro elemento é um elemento  ``` <button>  ``` , enquanto o segundo é um elemento  ``` <div>  ```  . A primeira é semântica, enquanto a segunda não é.

Outro exemplo: Abaixo, temos duas listas. No entanto, a primeira utiliza a tag semântica  ``` <ol>  ``` (lista ordenada), enquanto a segunda é formatada com tags genéricas:
  
 ![image](https://user-images.githubusercontent.com/88754556/175757756-1cb737fe-207c-4699-b47e-be452fba7efc.png)

Embora a diferença entre tags semânticas e não semânticas possa não parecer importante para usuários com visão, ela é significativamente importante para aqueles que usam leitores de tela por vários motivos:

Primeiro, o HTML semântico informa aos usuários de leitores de tela exatamente o que eles estão visualizando. O elemento semântico  ``` <button>  ``` informa ao leitor de tela que este elemento deve ser clicado para realizar alguma ação, e o elemento  ``` <ol>  ``` diz que os elementos que ele contém fazem parte de uma lista numerada. Como   ``` <div>  ``` não é semanticamente rico, ele não transmite essa informação — tudo o que o usuário sabe é que o elemento em questão é alguma coisa genérica de nível de bloco....

Em segundo lugar, os elementos semânticos vêm com sua própria acessibilidade de teclado integrada, sem necessidade de trabalho extra de sua parte. O elemento ``` <button> ``` , por exemplo, permite que os usuários “cliquem” no elemento com a tecla Enter/Return e foquem nele com a tecla Tab. Este não é o caso com  ``` <div>  ``` . Ao usar elementos semânticos, você ativa a funcionalidade acessível complementar.

Por fim, muitos leitores de tela ajudam os usuários a navegar em uma página, permitindo que eles pulem entre as tags com o mesmo nome (ou seja, H2s) ou agreguem todas as mesmas tags para uma maneira mais fácil de verificar o conteúdo de uma página. Portanto, está claro por que usar principalmente tags  ``` <div>  ``` negaria esse recurso.

Para resumir, evite criar elementos de interação específicos com a tag genérica <div> e seu irmão embutido,  ``` <span>  ``` , se possível. Embora essas tags geralmente sejam úteis para layouts, sempre escolha o elemento HTML semântico nativo quando possível para melhor acessibilidade.
  
  - Texto alternativo da imagem : O objetivo do texto alternativo era adicionar contexto para aqueles que usam leitores de tela e para aqueles que não podem ver suas imagens por qualquer motivo (por exemplo, baixa visão, uma conexão ruim ou um link de origem quebrado). Quando um leitor de tela encontra um texto alternativo, ele simplesmente o lê para o usuário. Os navegadores também podem ser configurados para exibir texto alternativo na tela no lugar da imagem.
 
  ```
  <img src="cute-dog.jpg" alt="a small, brown sitting in a field of dandelions with a chew toy in its mouth">
  ```

  - Conteudo textual adequado :
  
  Uma das melhores formas de ajudar um leitor de tela a interpretar sua página é criar uma boa e consistente estrutura de títulos, parágrafos, listas, etc. Um exemplo de boa semântica vai ser parecido com o a seguir, respeitando sua semantica adequada, assim se você tentar navegar dentro do documento, vai perceber que é bem fácil:
  
```markdown
 
 <h1>Meu título</h1>

<p>Essa é a primeira sessão do meu documento.</p>

<p>Eu vou adicionar outro parágrafo aqui também.</p>

<ol>
  <li>Aqui é</li>
  <li>uma lista para</li>
  <li>você ler</li>
</ol>

<h2>Meu sub-título</h2>

<p>Essa é a primeira sub sessão do meu documento. Eu adoro quando as pessoas conseguem encontrar meu conteúdo!</p>

<h2>Meu segundo sub-título</h2>

<p>Essa é a primeira sub sessão do meu documento. Eu acho que essa é mais interessante que a última.</p>
```
  
**Para se aprofundar no assunto**: <a href="[url](https://developer.mozilla.org/pt-BR/docs/Learn/Accessibility/HTML)">
  
### Usando linguagem clara
  
A linguagem que você usa também pode afetar a acessibilidade. No geral, você deve utilizar uma linguagem clara, que não é exageradamente complexa, e que não use jargões ou gírias desnecessárias. Isso não traz somente benefícios para pessoas com deficiência cognitiva, mas também beneficia pessoas que não estão lendo em sua primeira língua, jovens leitores... todo mundo, de fato! Tirando isso, você deve tentar evitar uma linguagem ou caracteres que não podem ser lidos ou entendidos bem por um leitor de tela. Por exemplo:

- Não utilize traços se você pode evitá-los. Ao invés de escrever 5-7, escreva 5 a 7.
- Expanda as abreviações — ao invés de escrever Jan, escreva Janeiro.
- Expanda os acrônimos, pelo menos uma ou duaz vezes. Ao invés de escrever direto HTML, escreva Hypertext Markup Language, ou HTML.
  
### Diretrizes de acessibilidade de conteúdo da Web

Ao longo deste guia, faremos referência às Diretrizes de acessibilidade de conteúdo da Web (WCAG) 2.0 , um conjunto de diretrizes e práticas recomendadas reunidas por especialistas em acessibilidade para abordar o que "acessibilidade" significa de maneira metódica.

As  WCAG estão organizadas em torno de quatro princípios frequentemente chamados pelo acrónimo POUR ( Perceivable, Operable, Understandable e Robust) :

- Perceptível : Os usuários podem perceber o conteúdo? Isso nos ajuda a ter em mente que só porque algo é perceptível com um sentido, como a visão, isso não significa que todos os usuários possam percebê-lo.

- Operável : os usuários podem usar componentes de interface do usuário e navegar pelo conteúdo? Por exemplo, algo que requer uma interação de foco não pode ser operado por alguém que não pode usar um mouse ou tela sensível ao toque.

- Compreensível : os usuários podem entender o conteúdo? Os usuários podem entender a interface e ela é consistente o suficiente para evitar confusão?

- Robusto : O conteúdo pode ser consumido por uma ampla variedade de agentes de usuário (navegadores)? Funciona com tecnologia assistiva?

Em extenso temos as doze diretrizes WCAG 2.0:
1. Perceptível
1.1 Forneça alternativas de texto para qualquer conteúdo não textual para que possa ser alterado para outras formas que as pessoas precisem, como letras grandes, Braille, fala, símbolos ou linguagem mais simples.
1.2 Fornecer alternativas para mídia baseada em tempo.
1.3 Criar conteúdo que possa ser apresentado de diferentes formas (por exemplo, layout mais simples) sem perder informações ou estrutura.
1.4 Torne mais fácil para os usuários ver e ouvir o conteúdo, incluindo a separação do primeiro plano do plano de fundo.

2. Operável
2.1 Disponibilizar todas as funcionalidades a partir de um teclado.
2.2 Forneça aos usuários tempo suficiente para ler e usar o conteúdo.
2.3 Não crie conteúdo de uma forma que possa causar convulsões.
2.4 Forneça maneiras de ajudar os usuários a navegar, encontrar conteúdo e determinar onde estão.

3. Compreensível
3.1 Torne o conteúdo do texto legível e compreensível.
3.2 Fazer com que as páginas da Web apareçam e funcionem de maneira previsível.
3.3 Ajude os usuários a evitar e corrigir erros.

4. Robusto
4.1 Maximize a compatibilidade com agentes de usuário atuais e futuros, incluindo tecnologias assistivas.

As WCAG 2.1 também apresentam a seguinte diretriz adicional:
2.5 Acessível por ponteiro: Facilite para os usuários a operação da funcionalidade por meio de várias entradas além do teclado.

### Critérios de Sucesso

Para alcançar a conformidade com as WCAG, o W3C dividiu os critérios de sucesso em três diferentes níveis de implementação. Esses níveis são conhecidos como Nível A, AA e AAA, respectivamente.

No padrão WCAG original, o W3C descreveu as diferenças entre os níveis assim:

Prioridade 1: Um desenvolvedor de conteúdo da Web deve atender a esse ponto de verificação. Caso contrário, um ou mais grupos acharão impossível acessar as informações do documento. Satisfazer esse ponto de verificação é um requisito básico para que alguns grupos possam usar documentos da Web.
Prioridade 2: Um desenvolvedor de conteúdo da Web deve atender a esse ponto de verificação. Caso contrário, um ou mais grupos terão dificuldade em acessar as informações do documento. A satisfação desse ponto de verificação removerá barreiras significativas ao acesso a documentos da Web.
Prioridade 3: Um desenvolvedor de conteúdo da Web pode abordar esse ponto de verificação. Caso contrário, um ou mais grupos terão alguma dificuldade em acessar as informações do documento. A satisfação desse ponto de verificação melhorará o acesso aos documentos da Web.
Se o primeiro ponto fosse alcançado, atingiria o Nível A. Se o primeiro e o segundo pontos fossem alcançados, atingiria o Nível AA e, se todos os três fossem alcançados, atingiria o Nível AAA.

Na Austrália, espera-se que as principais organizações atendam ao nível de conformidade AA. Isso significa que sua organização deve ter como objetivo atender:

Conformidade WCAG 2.0 Nível AA; ou conformidade WCAG 2.1 Nível AA.

### Leitura recomendada 

- Diretrizes de Acessibilidade para Conteúdo Web (WCAG): 
 
 <a href="[url](https://www.w3c.br/traducoes/wcag/wcag21-pt-BR/)">
 <a href="[url](https://www.w3.org/standards/webdesign/accessibility)">
 <a href="[url](https://www.w3.org/WAI/)">
 <a href="[url](https://www.w3.org/TR/wai-aria-1.1/)">
 <a href="[url](https://www.w3.org/TR/UNDERSTANDING-WCAG20/visual-audio-contrast-contrast.html?utm_campaign=chrome_series_wcag1.4.3_050417&utm_source=chromedev&utm_medium=yt-desc)">
 <a href="[url](https://www.w3.org/TR/UNDERSTANDING-WCAG20/visual-audio-contrast7.html?utm_campaign=chrome_series_wcag1.4.6_050417&utm_source=chromedev&utm_medium=yt-desc)">
 
- Conteúdo em vídeo:
  
 <a href="[url](https://www.youtube.com/watch?v=wkvslBGkhZY&list=PLNYkxOF6rcIBiiuN53rzwEidPcLZRtiOW)">
 <a href="[url](https://www.youtube.com/playlist?list=PLNYkxOF6rcIDJlkmUY8qoSV7PKSoBEEvp)">
 <a href="[url](https://www.youtube.com/playlist?list=PLNYkxOF6rcICWx0C9LVWWVqvHlYJyqw7g)">
 <a href="[url](https://www.youtube.com/channel/UCU6ljj3m1fglIPjSjs2DpRA/featured)">
 <a href="[url](https://www.youtube.com/playlist?list=PLkyTB2cNy_166ByzQBRK26mAilyBEX4Zo)">
 <a href="[url](https://www.youtube.com/playlist?list=PLd9b-GuOJ3nFHykZgRBZ7_bzwfZ526rxm)">
 <a href="[url](https://www.youtube.com/playlist?list=PLj7tC-O0sEHfLuY6o_hVbCe5Fm-cHbP1t)">
 
 Outros:
 
  <a href="[url](https://chrome.google.com/webstore/detail/color-contrast-analyzer/dagdlcijhfbmgkjokkjicnnfimlebcll?hl=en?utm_campaign=chrome_series_contrastanalyzer_050417&utm_source=chromedev&utm_medium=yt-desc)">
  <a href="[url](https://contrast-ratio.com/?utm_campaign=chrome_series_contrastratio_050417&utm_source=chromedev&utm_medium=yt-desc)">
  <a href="[url](https://developers.google.com/web/fundamentals/accessibility)">
  <a href="[url](https://www.useragentman.com/blog/2019/03/17/creating-accessible-html5-modal-dialogs-for-desktop-and-mobile/)">
  <a href="[url](https://support.google.com/accessibility/android/answer/6006564?hl=en)">
  <a href="[url](https://ebay.gitbook.io/mindpatterns/)">
  <a href="[url](https://github.com/WICG/inert)">
  <a href="[url](https://webaim.org/techniques/keyboard/)">
  <a href="[url](https://webaim.org/articles/nvda/)">
  <a href="[url](https://html.spec.whatwg.org/multipage/interaction.html#activation)">
  <a href="[url](https://developer.mozilla.org/en-US/docs/Web/Accessibility)">
  <a href="[url](https://developer.mozilla.org/en-US/docs/Learn/Accessibility)">
  <a href="[url](https://www.apple.com/accessibility/vision/)">
  <a href="[url](https://heydonworks.com/article/responses-to-the-screen-reader-strategy-survey/)">



