# WR Concept — Salão de Beleza Premium

Site de página única do salão WR Concept (Chácara Inglesa, São Paulo): visagismo, coloração e luzes.
Projeto estático (HTML + CSS + JS puro), sem etapa de build.

## Estrutura

```
index.html              página principal
favicon.svg             ícone da aba
css/style.css           todos os estilos
js/main.js              lógica, animações (GSAP/ScrollTrigger) e cena 3D (Three.js)
images/                 fotos (wr-*.jpg), formas de pagamento e textura de ruído
vercel.json             configuração de cache/URLs para a Vercel
```

## Dependências externas (via CDN)

- Fontes: Google Fonts — Bodoni Moda e Jost
- GSAP 3.12.5 e ScrollTrigger 3.12.5 (cdnjs)
- Three.js r128 (cdnjs)

É preciso ter internet para carregar essas bibliotecas e fontes.

## Rodar localmente

Use um servidor local (abrir o index.html direto com file:// pode bloquear as texturas da cena 3D):

```
npx serve .
# ou
python3 -m http.server 8000
```

## Publicar

- **GitHub:** crie um repositório e envie todo o conteúdo desta pasta.
- **Vercel:** importe o repositório, Framework Preset = "Other", sem build command e sem output directory (raiz).

## Configurações editáveis

No topo de `js/main.js`, objeto `CONFIG`: WhatsApp, Instagram, Google Reviews, Facebook, TikTok e link do mapa.
Links vazios ficam desativados automaticamente.
