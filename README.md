# Fujiex — Landing page

Página de venda da produção de dados de treino visual para IA.
No ar em https://lp.fujiextech.com

## Estrutura

- `index.html` — home: hero, posicionamento, números, 6 categorias, formulário, rodapé
- `about.html` — About us: missão e os quatro mecanismos (método, registro, incentivo, geografia)
- `css/site.css` — folha compartilhada pelas duas páginas
- `img/hero-opcoes/hero-f-azul.png` — ilustração da hero
- `img/about-team.jpg` — ilustração do About
- `img/portfolio/` — peças reais, 6 categorias
- `img/favicon-*.png` — favicon (a torre em neon sobre azul)

## Convenções

- Paleta: fundo `#162CB6` · neon `#39FF14` · texto sobre azul `#A8FF8F`. Trocar só no
  bloco PALETA do `:root` em `css/site.css`.
- Toda imagem sobre azul tem o fundo recolorido para `#162CB6` exato, senão a emenda
  com a seção fica visível.
- Fundo de seção mora sempre numa `<section>` de largura total; `.c` só limita o conteúdo.
- `.up` (animação de entrada) nunca no mesmo elemento que tenha `opacity`, hover ou
  transform próprios — a regra base ou a animação anulam uma à outra.

## Formulário

Envia via FormSubmit para `hello@fujiextech.com`. O endpoint está em `FORM_ENDPOINT`,
no topo do script de cada página. Não funciona aberto como `file://`: precisa de HTTP.

Deploy: Vercel (estático, sem build). Push na `main` republica.
