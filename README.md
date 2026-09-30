# Trabalho-FrontEnd

## Stats Preview Card

- **Aluno:** Luiz Henrique Alves Ferreira
- **RA:** 60025993
- **Professor:** Allan da Silva
- **Curso:** Análise e Desenvolvimento de Sistemas - 2S
- **Matéria:** Design Front End

---

## Qual era o trabalho

O professor mandou três layouts e a gente tinha que escolher um para copiar usando só HTML e CSS, ficando o mais parecido possível com a imagem dele. Eu escolhi o card de estatísticas. É aquele bloco escuro com um título, um textinho, três números grandes (10k+, 314 e 12M+) e uma foto de equipe com um filtro roxo do lado.

## Como eu fiz

Primeiro fiz só o HTML, sem me preocupar com cor nem fonte. Coloquei tudo dentro de uma `section` chamada `card` e dividi em duas partes: de um lado o texto com os números e do outro a foto.

Tentei usar as tags certas para cada coisa:

- `main` para o conteúdo principal
- `section` para o card
- `header` para o título e o parágrafo
- `ul` e `li` para os três números, porque são uma lista de itens parecidos
- `img` com texto alternativo, dentro de um `picture`

A palavra "insights" ficou dentro de um `span` só para eu conseguir pintar ela de roxo claro sem mexer no resto do título.

## O CSS

No começo do arquivo eu guardei as cores e as fontes em variáveis. Assim, se eu quiser trocar o roxo, mudo em um lugar só e vale para o projeto inteiro. Os valores vieram do `style-guide.md` do desafio.

As fontes são a Inter (títulos e números) e a Lexend Deca (o resto). As duas são do Google Fonts.

A parte mais legal foi o filtro roxo da foto. Em vez de editar a imagem, coloquei uma camada roxa por cima usando `::after` e o `mix-blend-mode: multiply` com 75% de opacidade. Ela mistura a cor com a foto e o resultado fica igual ao do design.

Nos nomes das classes usei um jeito parecido com o BEM, tipo `card__title` e `stats__value`. Ajuda a saber de qual parte do card cada classe é.

## Celular e computador

Fiz o CSS pensando primeiro no celular. Lá o card vira uma coluna: foto em cima, texto embaixo, tudo centralizado e os números um embaixo do outro.

Quando a tela passa de 900px, uma `media query` muda o layout: texto na esquerda, foto na direita e os números lado a lado. Também usei o `picture` para o navegador escolher a foto certa, a mobile nas telas pequenas e a desktop nas grandes.

Não coloquei altura fixa no card para o conteúdo não ser cortado. No desktop só defini uma altura mínima.

## O que eu pratiquei

- montar a estrutura de uma página com HTML semântico
- Flexbox para organizar o card e os números
- variáveis no CSS
- `media query` e imagens que mudam conforme a tela
- `::after` e `mix-blend-mode` para o filtro da foto
- subir um projeto no GitHub com README

## Como ficou a pasta

```
stats-preview-card/
├── index.html
├── css/
│   └── style.css
├── images/
│   ├── image-header-desktop.jpg
│   ├── image-header-mobile.jpg
│   └── favicon-32x32.png
└── README.md
```
