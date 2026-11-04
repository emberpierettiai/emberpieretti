# emberpieretti.com — Projetos em andamento

Site pessoal de Emberson Pieretti: uma página só, com um carrossel de cartões em leque (um cartão por projeto).

## O que está no ar
- Domínio: https://emberpieretti.com (www redireciona para o principal)
- Projeto no Netlify: `emberpieretti-projetos` (site id `3b65df2c-116c-480e-b990-06136fcfb53b`)
- Hoje o deploy é manual (arrastar a pasta na aba Deploys). O objetivo é ligar este repositório ao Netlify para cada alteração ir ao ar sozinha.
- DNS no GoDaddy: registro A `@` → `75.2.60.5` e CNAME `www` → `emberpieretti-projetos.netlify.app`. Não precisa mexer.

## Estrutura
```
index.html      a página inteira (HTML, CSS e JS no mesmo arquivo)
img/            prints dos projetos usados nos cartões (640 x 1120 px)
netlify.toml    diz ao Netlify que não há build e que a pasta raiz é publicada
```

## Como funciona
- React 18.3.1 (UMD, cdnjs) e GSAP 3.15.0 (jsDelivr), carregados por CDN. Não tem npm nem build.
- Fontes: Bricolage Grotesque e Instrument Sans (Google Fonts).
- Os projetos ficam na lista `PROJECTS`, dentro do `index.html`. Cada item tem título e descrição em PT e EN, status (`live`, `build` ou `next`), link e imagem.
  - `src: 'img/arquivo.jpg'` usa uma imagem da pasta `img`.
  - Sem `src`, o cartão usa uma ilustração desenhada por código (função `paint`).
- Com mais de 7 cartões aparecem as setas e os pontos para girar o leque. Hoje são 9: 7 projetos e 2 cartões de exemplo (`ex3`, `ex4`).
- Botão PT/EN no topo; o idioma inicial segue o navegador.
