<div align="center">

<img src="https://github.com/digueraDEV.png" width="100" style="border-radius: 16px;" alt="Rodrigo avatar"/>

# ✦ diguera.dev

**Personal portfolio — Bento-style, dark theme, built with vanilla HTML/CSS/JS**

[![Live](https://img.shields.io/badge/live-diguera.dev-a855f7?style=flat-square&logo=vercel&logoColor=white)](https://diguera.dev)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)]()
[![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white)]()
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)]()
[![License](https://img.shields.io/badge/license-MIT-a855f7?style=flat-square)]()

</div>

---

## 📸 Preview

> *Landing section with typewriter effect + Bento dashboard grid*

```
┌─────────────────────────────────────────┐
│                                         │
│         RODRIGO.                        │
│   // Dev Fullstack_                     │
│                                         │
│   ↓ Rolar para explorar                 │
│                                         │
└─────────────────────────────────────────┘

┌──────────────┬──────────────┐
│  About Me    │   GitHub     │
│  + Tech      │   Insights   │
│  Stack       ├──────────────┤
│              │   LinkedIn   │
├──────────────┼──────────────┤
│  Currículo   │  Currículo   │
├──────┬───────┴──────────────┤
│  WA  │       E-mail         │
└──────┴──────────────────────┘
```

---

## ✨ Features

- **Bento Grid Layout** — cards responsivos inspirados no design system do macOS Sonoma
- **Typewriter Effect** — animação de digitação com múltiplas strings e cursor piscante
- **Scroll Reveal** — entradas animadas com `IntersectionObserver` (sem dependências externas)
- **Deep Link LinkedIn** — tenta abrir o app nativo via `iframe` sem navegar a página atual; fallback para web
- **Copy to Clipboard** — copia e-mail com toast animado e feedback visual no botão; fallback `execCommand` para WebViews antigos
- **WebView Detection** — detecta Instagram, TikTok, Facebook e outros in-app browsers e exibe um pill discreto no canto da tela sugerindo abrir no browser real
- **Zero-framework** — HTML puro + Tailwind CDN + Lucide Icons; sem build step, sem bundler
- **SEO Ready** — meta tags Open Graph e Twitter Card completas
- **Fully Responsive** — mobile-first, breakpoints em 480 px e 768 px

---

## 🛠️ Tech Stack

| Camada | Tecnologia |
|---|---|
| Markup | HTML5 semântico |
| Estilo | Tailwind CSS (CDN) + CSS custom properties |
| Ícones | Lucide Icons · Devicon |
| Fontes | Plus Jakarta Sans · JetBrains Mono (Google Fonts) |
| Scripts | Vanilla JavaScript (ES2020+) |
| Deploy | — *(Vercel / Netlify / GitHub Pages)* |

---

## 📁 Estrutura

```
diguera.dev/
├── index.html        # Arquivo único — todo o site está aqui
└── README.md
```

> O projeto é **single-file by design**: fácil de hospedar em qualquer CDN estático, sem etapa de build.

---

## 🚀 Como rodar localmente

```bash
# Clone o repositório
git clone https://github.com/digueraDEV/diguera.dev.git
cd diguera.dev

# Abra no browser (qualquer método abaixo)
open index.html                          # macOS
start index.html                         # Windows
xdg-open index.html                      # Linux

# Ou use o Live Server do VS Code (recomendado para hot-reload)
# Extensão: ritwickdey.liveserver
```

Não há dependências para instalar — tudo é carregado via CDN.

---

## ⚙️ Personalização

Antes de colocar em produção, atualize as seguintes linhas em `index.html`:

| O que alterar | Onde | Exemplo |
|---|---|---|
| Seu e-mail real | `copyEmail('seuemail@dominio.com', this)` | `copyEmail('rodrigo@diguera.dev', this)` |
| URL do currículo | `<a href="#">` no card Currículo | `<a href="/cv-rodrigo-2026.pdf">` |
| URL do perfil LinkedIn | `openLinkedIn` + `href` do card | Já configurado |
| Deep link LinkedIn | Variável `deepLink` em `openLinkedIn()` | Já configurado |
| URL canônica OG | `<meta property="og:url">` | `https://seudominio.dev` |

---

## 🔧 Decisões Técnicas

### Por que sem framework?
Para um portfólio single-page sem estado complexo, um framework adicionaria overhead de bundle sem benefício real. Vanilla JS + Tailwind CDN permite deploy imediato em qualquer host estático com **zero configuração**.

### Deep link LinkedIn sem navegar a página
O método comum (`window.location.href = 'linkedin://'`) causava o problema de *dupla navegação* (nova aba + página atual redirecionada). A solução adotada injeta um `<iframe>` invisível com o scheme `linkedin://`, que aciona o intent do sistema operacional sem alterar `window.location` — preservando o site aberto.

### WebView pill em vez de banner
Banners full-width são invasivos em telas pequenas. O pill no canto superior direito ocupa ≈ 130 px, tem `backdrop-filter: blur`, pode ser dispensado com um toque e não desloca nenhum elemento da página.

---

## 📄 Licença

Distribuído sob a licença **MIT**. Veja [`LICENSE`](LICENSE) para mais detalhes.

---

<div align="center">

**Feito com foco e café ☕ por [Rodrigo](https://github.com/digueraDEV)**

</div>
