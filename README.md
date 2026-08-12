# Fujiex — Landing page

No ar em https://fujiextech.com · Homologação em https://staging.fujiextech.com

## Dois ambientes

| Branch | Ambiente | URL |
|---|---|---|
| `staging` | homologação, para os sócios revisarem | staging.fujiextech.com |
| `main` | produção | fujiextech.com |

**Nunca editar os arquivos deste repositório à mão.** A fonte da verdade é a pasta
`site/` do workspace. Publicar sempre pelo script:

```
./publicar.sh stage "o que mudou"    # sobe pra homologação
./publicar.sh prod  "o que mudou"    # sobe pra produção
```

O script sincroniza `site/` para cá, reescreve os links internos, copia só as imagens
efetivamente referenciadas e aborta se algum asset estiver faltando.

## Estrutura

- `index.html` — home: hero, posicionamento, números, 6 categorias, formulário, rodapé
- `about.html` — About us: missão e os quatro mecanismos
- `css/site.css` — folha compartilhada pelas duas páginas
- `img/` — ilustrações, portfólio por categoria, favicon e cartão de link

## Convenções

- Paleta: fundo `#162CB6` · neon `#39FF14` · texto sobre azul `#A8FF8F`.
  Trocar só no bloco PALETA do `:root` em `css/site.css`.
- Imagem que encosta no azul tem o fundo recolorido para `#162CB6` exato, senão a
  emenda com a seção fica visível.
- Fundo de seção mora sempre numa `<section>` de largura total; `.c` só limita o
  conteúdo. Fundo aplicado junto com `.c` deixa faixas laterais transparentes.
- `.up` (animação de entrada) nunca no mesmo elemento que tenha `opacity`, hover ou
  transform próprios: um anula o outro.
- Sem travessão em nenhum texto.

## Formulário

Envia via FormSubmit para `hello@fujiextech.com`. Endpoint em `FORM_ENDPOINT`, no topo
do script de cada página. Não funciona em `file://`, precisa de HTTP.

## Plano da Vercel

O repositório precisa continuar **público**: o plano Hobby não aceita repositório
privado pertencente a organização.
