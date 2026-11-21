# MY3E Via Theme

Tema **Material 3 Expressive** para a página inicial do [Via Browser](https://viayoo.com/) (Android): saudação por horário, busca com seletor de buscador (Brave Search como padrão), favoritos em formas expressivas e um fundo com formas animadas e linhas em zigzag e onda.

Este é o irmão para celular do [MY3E Firefox Theme](https://github.com/VitzzALT/MY3EFirefoxTheme), com o mesmo visual, mas com uma paleta fixa.

## Requisitos

Funciona no **Via** sem módulos. O tema usa dois campos das configurações do próprio navegador, e o `logo-snippet.html` foi testado no Via puro, sem o [BetterVia](https://github.com/Xposed-Modules-Repo/com.jiguro.bettervia):

- **Custom CSS:** Configurações → Customization → Advanced → Custom CSS
- **Logo (HTML):** Configurações → Customization → Logo

O `logo-snippet.html` foi testado tanto no Via puro quanto com o [BetterVia](https://github.com/Xposed-Modules-Repo/com.jiguro.bettervia). O `logo-snippet-bettervia.html` é a versão original, feita para o BetterVia, e mantém a barra de pesquisa nativa do Via (com sugestões).

## O que tem aqui

| Arquivo | Para quê |
| --- | --- |
| `homepage.css` | Todo o visual: cores, formas, animações, busca e favoritos |
| `logo-snippet.html` | Versão para o Via normal: saudação, título, onda, fundo e barra de pesquisa própria com seletor de buscador |
| `logo-snippet-bettervia.html` | Versão original, para o BetterVia: mantém a barra de pesquisa nativa do Via (com sugestões) |
| `extras/homepage.html` | Página completa para o Theme Editor do BetterVia (já inclui o snippet antigo). Mais frágil: o Via refaz o arquivo ao editar favoritos, e o caminho do CSS vale só para o Via da Play Store |

## Instalação

O Via refaz o HTML da homepage sozinho quando você mexe nos favoritos. Por isso o tema fica nos campos de configuração, e não em um arquivo `homepage.html`.

1. **Custom CSS:** nas configurações do Via, apague o CSS padrão e cole o conteúdo de `homepage.css`.
2. **Logo (HTML):** no campo **Logo**, cole o `logo-snippet.html`. Se você usa o BetterVia e quer manter a barra de pesquisa nativa, use o `logo-snippet-bettervia.html`.
3. Abra uma nova aba para ver o resultado.

## Personalização
- **Buscadores:** no `logo-snippet.html`, edite a lista `g`. O primeiro da lista é o padrão. A página usa uma barra de pesquisa própria, então o buscador escolhido no seletor vale só para pesquisas feitas por ela. A barra de endereço do Via continua usando o buscador padrão configurado no navegador (pode ser um personalizado com `%s` no lugar da pesquisa).
- **Cores:** ficam nas variáveis no início do `homepage.css`. Ao contrário da versão do Firefox, aqui a paleta é fixa (roxa) e **não** acompanha a cor do sistema.
- **Título da aba:** a linha `document.title=...` no fim do `logo-snippet.html` define o texto que aparece na barra.

## Limitações
- A barra de pesquisa da página inicial substitui a do Via, então ela não mostra as sugestões de pesquisa nativas. Quem quiser mantê-las pode usar o `logo-snippet-bettervia.html`.
- Testado em telas de 1080x2400 (Galaxy M55 5G) e 720x1480 (Galaxy J8).

## Versão para computador

Quer esse visual no Firefox do PC, com cor dinâmica e tema da interface do navegador? Veja o [MY3E Firefox Theme](https://github.com/VitzzALT/MY3EFirefoxTheme).

## Créditos

- Design baseado no [Material 3 Expressive](https://m3.material.io/blog/building-with-m3-expressive), do Google.
- O BetterVia é um projeto separado e **proprietário**, de JiGuro. Este repositório não inclui nem redistribui o módulo, só linka para ele, e não tem vínculo com os autores.
- Desenvolvido com a ajuda do [Claude](https://claude.ai), assistente de IA da [Anthropic](https://www.anthropic.com).
