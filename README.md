<div align="center">

# 🌿 GoNature 2.0

**Trilhas, corridas e campings: descubra, registre e compartilhe aventuras ao ar livre.**

Novo design **Dia & Noite**: o tema claro tem a luz da manhã na mata, o escuro tem a floresta à noite.
Mesma estrutura, mesmos tokens, só a luz muda.

![Vue 3](https://img.shields.io/badge/Vue-3-2f6b48?logo=vuedotjs&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-8-2f6b48?logo=vite&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-6-2f6b48?logo=typescript&logoColor=white)
![Tema](https://img.shields.io/badge/tema-Dia%20%26%20Noite-8b5e3c)

<img src="../REDESIGN/media/gonature-2.0-web.gif" alt="Tour pelo GoNature 2.0 na web: feed, busca, mapa, chat, perfil e troca de tema Dia/Noite" width="100%">

▶️ **Vídeos em alta qualidade:** [Web (MP4, 45 s)](../REDESIGN/media/gonature-2.0-web.mp4) · [Mobile — protótipo (MP4, 50 s)](../REDESIGN/media/gonature-2.0-mobile.mp4)

</div>

---

## ✨ O que há de novo no 2.0

| | |
|---|---|
| 🌗 **Dia & Noite** | Paleta tirada da natureza: linho, folha e casca de dia; mata escura, musgo e areia à noite. Um botão de **sol/lua** troca o tema com animação, e as cores atravessam suavemente em 400 ms. |
| 🧭 **Navegação lateral nova** | Ícones em quadradinhos que acendem em verde na página ativa, botão **Nova aventura** sempre à mão e menu recolhível para 72 px. |
| 🔎 **Uma busca só** | Um campo procura **pessoas, aventuras e lugares** ao mesmo tempo, com resultados agrupados. |
| 📰 **Feed social** | Cards com foto em destaque, etiqueta do tipo, avaliação, comentários e **Ver no mapa**. Filtros Todos · Trilha · Corrida · Camping. |
| 🗺️ **Mapa em tela cheia** | Painel flutuante com busca de lugar e "Perto de você", trilha desenhada na cor do tema, satélite/ruas e "Minha localização". |
| 💬 **Chat** | Lista e conversa num só card, abas segmentadas, balões com cantos suaves e fundo personalizado com véu de 70%. |
| 👤 **Perfil e Configurações** | Cabeçalho horizontal com números clicáveis, grade "Meus catálogos", configurações em grupos com interruptores. |
| 🎞️ **Movimento** | Uma curva só para tudo (`cubic-bezier(.22, 1, .36, 1)`), mola nos toques e entrada suave das telas. Respeita `prefers-reduced-motion`. |

---

## 🌞🌙 Dia & Noite

| Dia | Noite |
|:---:|:---:|
| <img src="../REDESIGN/media/feed-light.jpg" alt="Feed no tema Dia"> | <img src="../REDESIGN/media/feed-dark.jpg" alt="Feed no tema Noite"> |
| **Feed** — filtros por tipo e sugestões de quem seguir | |
| <img src="../REDESIGN/media/map-light.jpg" alt="Mapa no tema Dia"> | <img src="../REDESIGN/media/map-dark.jpg" alt="Mapa no tema Noite"> |
| **Mapa** — painel "Perto de você" e trilha selecionada | |
| <img src="../REDESIGN/media/chat-light.jpg" alt="Chat no tema Dia"> | <img src="../REDESIGN/media/chat-dark.jpg" alt="Chat no tema Noite"> |
| **Chat** — conversas diretas e grupos | |
| <img src="../REDESIGN/media/profile-light.jpg" alt="Perfil no tema Dia"> | <img src="../REDESIGN/media/profile-dark.jpg" alt="Perfil no tema Noite"> |
| **Perfil** — números, pedidos para seguir e catálogos | |
| <img src="../REDESIGN/media/settings-light.jpg" alt="Configurações no tema Dia"> | <img src="../REDESIGN/media/settings-dark.jpg" alt="Configurações no tema Noite"> |
| **Configurações** — sol/lua, seguir o sistema, fundo do chat e privacidade | |

---

## 📱 Mobile (Android) — protótipo

> O design do app Android já está definido e navegável como protótipo. A implementação no app
> ([gonature-mobile](https://github.com/alissonkl20/gonature-mobile)) é a próxima etapa.

<div align="center">
<img src="../REDESIGN/media/gonature-2.0-mobile.gif" alt="Protótipo mobile do GoNature 2.0 nos temas Dia e Noite" width="640">
</div>

| Feed | Nova aventura | Configurações |
|:---:|:---:|:---:|
| <img src="../REDESIGN/media/mobile-feed.jpg" alt="Feed mobile, Dia e Noite"> | <img src="../REDESIGN/media/mobile-create.jpg" alt="Formulário de nova aventura no mobile"> | <img src="../REDESIGN/media/mobile-settings.jpg" alt="Configurações no mobile"> |

No mobile: o **sol/lua** fica no topo do feed, o botão **+** da barra inferior abre uma gaveta para escolher Trilha, Corrida ou Camping, e a barra de abas abre o nome da aba ativa com animação.

---

## 🎨 Sistema de design

### Cores (tokens em `src/assets/styles/colors.css`)

| Token | Dia | Noite | Uso |
|---|---|---|---|
| `--n-scaffold` | `#F4F0E6` | `#0D1310` | Fundo da página |
| `--n-card` | `#FFFCF5` | `#151D18` | Cards e painéis |
| `--n-surface-2` | `#ECE5D6` | `#1E2922` | Campos, chips, áreas secundárias |
| `--n-primary` | `#2F6B48` | `#86C59A` | Ação principal, item ativo |
| `--n-primary-soft` | `#DFEBDC` | `#1E3427` | Fundo de item ativo |
| `--n-accent` | `#8B5E3C` | `#CFA77F` | Casca / areia: detalhes |
| `--n-ink` | `#1C261E` | `#ECEEE6` | Texto |
| `--n-muted` | `#5E5648` | `#A2AD9F` | Texto secundário |
| `--n-star` | `#C08A2A` | `#E3B341` | Avaliações |

### Tipografia, espaço e movimento

- **Fraunces** para títulos e nomes de lugares; **Inter** para toda a interface.
- Escala: caption 11 · small 13 · body 15 · heading 18 · title 24 · display 32.
- Grade de **4 px**; cantos `8 · 14 · 20 · 28 · pill`.
- Movimento: `fast 120 ms` (toque), `base 200 ms` (cor/borda), `slow 320 ms` (telas), `theme 400 ms` (Dia ↔ Noite).

### Princípios

1. **Calmo** — muito respiro, poucas cores por tela; a foto da natureza é a estrela.
2. **Óbvio** — cada ação tem ícone e texto; o que é tocável parece tocável.
3. **Fluido** — tudo se move com a mesma curva; nada pisca nem salta.
4. **Consistente** — web e Android compartilham tokens, ícones, nomes e ordem de navegação.
5. **Acessível** — alvos de toque ≥ 44 px, foco visível com anel de 4 px, estado ativo nunca só por cor.

---

## 🧩 Repositórios

| Repo | O quê |
|------|--------|
| [gonature-backend](https://github.com/alissonkl20/gonature-backend) | Django |
| [gonature](https://github.com/alissonkl20/gonature) | SDK Python |
| **gonature-web** (este) | Vue 3 |
| [gonature-mobile](https://github.com/alissonkl20/gonature-mobile) | React Native |

O cliente HTTP TypeScript (`@gonature/api`) fica em `packages/api/` neste repo.

## 🚀 Setup

```bash
cp .env.example .env
npm install
npm run dev
```

Backend: `http://127.0.0.1:8000` (repo **gonature-backend**).
Produção: Vercel, com `VITE_API_BASE=https://api.alissonkisp.tech`.

### Estrutura do front

- Tema e CSS global em `src/assets/styles/` (sem `<style>` nos `.vue`).
- Views finas, lógica em `src/composables/`, componentes em `src/components/<feature>/`.
- Tema Dia/Noite: `useThemeStore` + `useThemeToggle` (salvo nas configurações do perfil).

> As capturas e vídeos de `../REDESIGN/media/` foram gravados com dados de exemplo.
