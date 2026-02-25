# Global Landing

Site institucional da **Global Landing** — agência de criação de sites e landing pages profissionais para empresas brasileiras. Projeto estático (HTML, CSS e JavaScript), focado em SEO, conversão e entrega em 14 dias.

---

## O que é este projeto

- **Homepage**: hero, portfólio, processo (4 etapas), serviços/preços, tech stack, métricas, FAQ e formulário de contato.
- **Serviços** (`servicos.html`): três níveis de preço + Schema.org.
- **Portfólio** (`portfolio.html`): filtros por segmento e links para cases.
- **Cases** (`projeto-*.html`): 8 páginas de projetos (advocacia, clínica, restaurante, imóveis, estética, fitness, educação, tecnologia).
- **Segmentos** (`sites-para-*.html`): 8 páginas de nicho (advocacia, clínicas, restaurantes, imóveis, estética, fitness, educação, tecnologia).
- **Blog** (`blog/`): índice + 10 artigos em HTML.
- **SEO**: meta tags, canonical, Open Graph, Twitter Card, Schema.org (Organization, WebSite, Service). `sitemap.xml` e `robots.txt` para produção.

---

## Tecnologias

- HTML5, CSS3 (variáveis, flex/grid), JavaScript (vanilla).
- Fontes: Google Fonts (Cormorant Garamond, Space Mono, DM Sans).
- Deploy: qualquer host estático (Netlify, Vercel, GitHub Pages, Apache/Nginx).

---

## Como rodar localmente

1. Clone ou baixe o repositório.
2. Abra a pasta no computador e sirva os arquivos com um servidor estático, por exemplo:
   - **VS Code**: extensão “Live Server” → botão “Go Live”.
   - **Node**: `npx serve .` na raiz do projeto.
   - **Python**: `python -m http.server 8000` na raiz.
3. Acesse `http://localhost:3000` (ou a porta que o servidor indicar) e abra `index.html`.

Não há `package.json` nem etapa de build; o site é 100% estático.

---

## Antes de colocar no ar (checklist)

Substitua os placeholders abaixo para o site funcionar por completo:

| Onde | O que fazer |
|------|-------------|
| **Formulário de contato** | Crie um formulário em [Formspree](https://formspree.io), copie o ID (ex: `xeqwqkzn`) e no `index.html` troque `YOUR_FORMSPREE_FORM_ID` em `action="https://formspree.io/f/YOUR_FORMSPREE_FORM_ID"` pelo seu ID. |
| **Google Analytics (GA4)** | No `index.html`, substitua `G-XXXXXXXXXX` pelo seu ID de medição GA4 (ex: `G-ABC123XYZ`). |
| **Meta Pixel (Facebook/Instagram)** | No `index.html`, substitua `XXXXXXXXXXXXXXX` pelo ID do seu Pixel. |
| **WhatsApp** | No `index.html` e no footer, troque `https://wa.me/5524981313689` pelo número real (ex: `5511987654321`). |
| **Imagem OG** | Adicione em `assets/` uma imagem `og-image.jpg` com **1200×630 px** para redes sociais. Veja `assets/README.md`. |
| **URL base** | Se o domínio for diferente de `https://globallanding.com.br`, atualize canonical, `og:url`, `sitemap.xml` e `robots.txt` com a URL correta. |

---

## Estrutura de pastas (resumo)

```
globallanding/
├── index.html              # Home
├── servicos.html           # Serviços e preços
├── portfolio.html          # Listagem de projetos
├── projeto-*.html          # 8 páginas de case
├── sites-para-*.html       # 8 páginas por segmento
├── blog/
│   ├── index.html         # Índice do blog
│   └── *.html             # 10 artigos
├── assets/
│   ├── logo.svg           # Logo (Schema.org, etc.)
│   ├── og-image.jpg       # (você adiciona) Imagem para redes sociais
│   └── README.md
├── sitemap.xml
├── robots.txt
└── README.md               # Este arquivo
```

---

## URLs e sitemap

- Os links internos usam `.html` (ex: `portfolio.html`, `servicos.html`).
- O `sitemap.xml` usa URLs sem extensão (ex: `/portfolio`). Em muitos hosts (Netlify, Vercel) dá para configurar rewrites para que `/portfolio` sirva `portfolio.html`. Se não configurar, as páginas continuam acessíveis pelo `.html`.

---

## Licença e uso

Projeto de uso da Global Landing. Ajuste textos, imagens e links conforme sua marca e política de uso.
