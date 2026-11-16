# MY3E Via Theme

Tema **Material 3 Expressive** para a página inicial do [Via Browser](https://viayoo.com/) (Android): saudação por horário, busca com seletor de buscador (Brave Search como padrão), favoritos em formas expressivas e um fundo com formas animadas e linhas em zigzag e onda.

Este é o irmão para celular do [MY3E Firefox Theme](https://github.com/VitzzALT/MY3EFirefoxTheme), com o mesmo visual, mas com uma paleta fixa.

## Requisitos

Foi feito e usado com o **Via + [BetterVia](https://github.com/Xposed-Modules-Repo/com.jiguro.bettervia)**, um módulo LSPosed/LSPatch que adiciona recursos ao Via. Os arquivos daqui são só CSS e HTML. Eu não testei sem o BetterVia, então não sei se o tema funciona do mesmo jeito no Via puro.

## O que tem aqui

| Arquivo | Para quê |
| --- | --- |
| `homepage.css` | Todo o visual: cores, formas, animações, busca e favoritos |
| `logo-snippet.html` | Cria a saudação, o título, a onda, o fundo e o seletor de buscador |

## Instalação

O Via refaz o HTML da homepage sozinho quando você mexe nos favoritos. Por isso o tema fica nos campos de configuração, e não em um arquivo `homepage.html`.

1. **Custom CSS:** nas configurações do Via, apague o CSS padrão e cole o conteúdo de `homepage.css`.
2. **Logo (HTML):** no campo do logo da homepage, cole o conteúdo de `logo-snippet.html`.
3. Abra uma nova aba para ver o resultado.

## Personalização

- **Buscadores:** no `logo-snippet.html`, edite a lista `g`. O primeiro da lista é o padrão. Para a barra de endereço do Via, o buscador padrão é uma configuração separada do navegador (pode ser um buscador personalizado com `%s` no lugar da pesquisa).
- **Cores:** ficam nas variáveis no início do `homepage.css`. Ao contrário da versão do Firefox, aqui a paleta é fixa (roxa) e **não** acompanha a cor do sistema.
- **Título da aba:** a linha `document.title=...` no fim do `logo-snippet.html` define o texto que aparece na barra.

## Limitações

- Ícones de favoritos com fundo branco (como o do Brave) aparecem com esse fundo. O CSS só consegue reduzir o brilho e colocar o ícone dentro de um bloco colorido.
- Não testei em outras telas além de 1080x2400.

## Versão para computador

Quer esse visual no Firefox do PC, com cor dinâmica e tema da interface do navegador? Veja o [MY3E Firefox Theme](https://github.com/VitzzALT/MY3EFirefoxTheme).

## Créditos

- Design baseado no [Material 3 Expressive](https://m3.material.io/blog/building-with-m3-expressive), do Google.
- O BetterVia é um projeto separado e **proprietário**, de JiGuro. Este repositório não inclui nem redistribui o módulo, só linka para ele, e não tem vínculo com os autores.
- Desenvolvido com a ajuda do [Claude](https://claude.ai), assistente de IA da [Anthropic](https://www.anthropic.com).
