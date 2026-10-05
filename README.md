# atacadistafut.com — Landing page Atacadista Fut
**Site publicado:** https://devagenciaontrack-sys.github.io/atacadistafut/

Landing page independente da **Atacadista Fut**, focada em lojistas e revendedores.
Posicionamento: “A gente não vende pra torcedor.” · Ideia central: “Atacado para quem vende.”

Site estático (HTML + CSS + JS, sem build). Publicado via GitHub Pages.

## Estrutura

| Arquivo | Conteúdo |
|---|---|
| `index.html` | Página: header, hero com vídeo, Para quem é, Aplicativo, Como funciona, CTA final com QR Code, FAQ e rodapé |
| `style.css` | Identidade: azul profundo `#102A43`, azul comercial `#1664D8`, amarelo `#FFC928`, branco gelo `#F6F8FB`, grafite `#18212F`. Fontes Archivo Black / Archivo (títulos) e Inter (corpo) |
| `main.js` | Vídeo sob demanda e eventos de rastreamento |
| `politica-de-privacidade.html`, `termos-de-uso.html` | Páginas provisórias (aguardando texto oficial) |

## Regras atendidas

- **Um único link para o app** em todos os CTAs: `https://foxappy.com/link?store=atkfut` (sem botões separados de App Store / Google Play).
- **Vídeo** `https://youtube.com/shorts/EGvx4QLrc-0` na primeira dobra, formato vertical, **sem autoplay**: o player do YouTube só carrega quando a pessoa toca no vídeo (página mais leve).
- **Mobile-first**: no celular a ordem é headline → vídeo → CTA, e há um CTA fixo “ACESSAR ATACADO” no rodapé da tela.
- **QR Code** apontando para o link do app apenas no desktop.
- Nenhum depoimento, número, preço, frete, pedido mínimo, estoque, prazo, desconto ou selo foi inventado.
- Rodapé com a empresa responsável por esta marca: PAIXAO BRASILEIRA INTERMEDIACOES LTDA — CNPJ 65.444.402/0001-20.

## Rastreamento

Os eventos são enviados ao `dataLayer` (Google Tag Manager) e, se estiverem instalados na página, também para `gtag`, Meta Pixel (`fbq`) e TikTok Pixel (`ttq`).

| Evento | Quando dispara |
|---|---|
| `atacadista_app_click` | Clique em qualquer CTA do app (parâmetro `location`: header, hero, cta_final, sticky_mobile) |
| `atacadista_video_play` | Clique para assistir ao vídeo |
| `atacadista_instagram_click` | Clique no Instagram do rodapé |
| `atacadista_qrcode_view` | QR Code visível na tela (somente desktop) |

Para ativar: inserir o snippet do GTM (ou dos pixels) no `<head>` do `index.html`.

## Pendências do cliente

- [ ] Link do Instagram — `[INSERIR_INSTAGRAM_ATACADISTA]` (marcado com TODO no rodapé do `index.html`)
- [ ] Texto oficial da Política de Privacidade e dos Termos de Uso
- [ ] Logo oficial (hoje é um logotipo em texto)
- [ ] Domínio `atacadistafut.com`: apontar o DNS para o GitHub Pages e configurar o domínio em *Settings → Pages*
- [ ] Código do GTM / pixels
