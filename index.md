# Analise de Inclusão em Aplicações Web
## Um guia pratico dos padrões de navegabilidade e acessibilidade

Este conjunto de documentos é uma versão baseada em texto de parte do conteúdo abordado no projeto ...

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

### Diretrizes de acessibilidade de conteúdo da Web

Ao longo deste guia, faremos referência às Diretrizes de acessibilidade de conteúdo da Web (WCAG) 2.0 , um conjunto de diretrizes e práticas recomendadas reunidas por especialistas em acessibilidade para abordar o que "acessibilidade" significa de maneira metódica.

As WCAG estão organizadas em torno de quatro princípios frequentemente chamados pelo acrónimo POUR :

- Perceptível : Os usuários podem perceber o conteúdo? Isso nos ajuda a ter em mente que só porque algo é perceptível com um sentido, como a visão, isso não significa que todos os usuários possam percebê-lo.

- Operável : os usuários podem usar componentes de interface do usuário e navegar pelo conteúdo? Por exemplo, algo que requer uma interação de foco não pode ser operado por alguém que não pode usar um mouse ou tela sensível ao toque.

- Compreensível : os usuários podem entender o conteúdo? Os usuários podem entender a interface e ela é consistente o suficiente para evitar confusão?

- Robusto : O conteúdo pode ser consumido por uma ampla variedade de agentes de usuário (navegadores)? Funciona com tecnologia assistiva?

Embora as WCAG forneçam uma visão geral abrangente do que significa que o conteúdo seja acessível, também pode ser um pouco esmagador. Para ajudar a mitigar isso, o grupo WebAIM (Web Accessibility in Mind) destilou as diretrizes WCAG em uma lista de verificação fácil de seguir, direcionada especificamente para conteúdo da web.

A lista de verificação do WebAIM pode fornecer um resumo curto e de alto nível do que você precisa implementar, além de vincular à especificação WCAG subjacente se você precisar de uma definição expandida.

Com essa ferramenta em mãos, você pode traçar uma direção para seu trabalho de acessibilidade e ter certeza de que, desde que seu projeto atenda aos critérios descritos, seus usuários terão uma experiência positiva ao acessar seu conteúdo.





```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/alycesuza/Analise-de-Inclusao-em-aplicacoes-web/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
