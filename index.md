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

![image](https://user-images.githubusercontent.com/88754556/175757189-eb2b7d0d-c1b9-45f9-832c-c756bb2f7319.png)

Este formulário tem vários problemas de acessibilidade.

- O texto é de baixo contraste, o que é difícil para usuários com baixa visão lerem.
- Ter rótulos à esquerda e campos à direita torna difícil para muitas pessoas associá-los e quase impossível para alguém que precise ampliar para usar a página; imagine olhar para isso em um telefone e ter que percorrer para descobrir o que se passa com o quê.
- O "Lembrar detalhes?" o rótulo não está associado à caixa de seleção, portanto, você deve tocar ou clicar apenas no pequeno quadrado em vez de apenas clicar no rótulo; além disso, alguém usando um leitor de tela teria problemas para descobrir a associação.

Agora vamos agitar nossa varinha de acessibilidade e ver o formulário com esses problemas corrigidos. Vamos tornar o texto mais escuro, modificar o design para que os rótulos fiquem próximos às coisas que estão rotulando e corrigir o rótulo a ser associado à caixa de seleção para que você possa alterná-lo clicando no rótulo também.

![image](https://user-images.githubusercontent.com/88754556/175757216-dd1e4ee2-d8dd-4990-b944-7740bac826ae.png)

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

Em segundo lugar, os elementos semânticos vêm com sua própria acessibilidade de teclado integrada, sem necessidade de trabalho extra de sua parte. O elemento <button> , por exemplo, permite que os usuários “cliquem” no elemento com a tecla Enter/Return e foquem nele com a tecla Tab. Este não é o caso com  ``` <div>  ``` . Ao usar elementos semânticos, você ativa a funcionalidade acessível complementar.

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
  
**Para se aprofundar no assunto**: [https://developer.mozilla.org/pt-BR/docs/Learn/Accessibility/HTML]
  
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

