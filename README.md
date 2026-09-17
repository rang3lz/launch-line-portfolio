# Launch Line — Site (portfólio)

Site institucional de página única para a **Launch Line** (IA, Automação, Marketing, Estratégia, Negócios), fundada por **Arthur Leon** (Fundador) e **Daniel Rangel** (Co-fundador).

- **Site publicado (GitHub Pages):** https://rang3lz.github.io/launch-line-portfolio/
- **Artifact editável (Claude):** https://claude.ai/artifact/8uCZ3J8AhMc2bSyfKmAyTD
- **Repositório:** https://github.com/rang3lz/launch-line-portfolio

> Existe também um repositório separado, `rang3lz/launch-line`, com uma versão anterior e mais elaborada do site (símbolo 3D em Three.js, animações GSAP). Este repositório (`launch-line-portfolio`) é um projeto independente e mais simples — não sobrescreve nem depende daquele.

## O que tem no site

Página única (`index.html`) com as seções, nesta ordem:

1. **Header fixo** — logo, navegação (Serviços / Processo / Sobre / Contato) e botão "Agendar conversa".
2. **Hero** — vídeo em loop (`images/hero.mp4`, "feixe de luz atravessando a logo"), com `images/hero.png` como imagem de capa (poster) enquanto o vídeo carrega.
3. **Fundadores** (`#sobre`) — Arthur Leon (Fundador) e Daniel Rangel (Co-fundador), cada um com foto e bio curta.
4. **Serviços** (`#servicos`) — 5 frentes: Inteligência Artificial, Automação, Marketing, Estratégia, Negócios.
5. **Processo** (`#processo`) — 4 etapas: Diagnóstico → Plano → Implementação → Acompanhamento.
6. **Contato / CTA** (`#contato`) — botão para WhatsApp e link de e-mail.
7. **Footer** — logo, marca, e-mail e WhatsApp.

## Estrutura de arquivos

```
index.html              # toda a marcação, estilo (<style> inline) e o script de animação de entrada
images/
  hero.mp4               # vídeo do hero (feixe de luz sobre a logo)
  hero.png               # poster/capa do vídeo do hero (arte original "Launch Line")
  logo.png               # logo recortada da arte original, usada no header e rodapé
  founder-arthur.png      # foto do Arthur Leon
  founder-daniel.png      # foto do Daniel Rangel
```

Não há build step: é HTML + CSS + JS puro em um único arquivo, mais os assets em `images/`. Basta abrir `index.html` num navegador para rodar localmente.

## Decisões de design

- **Identidade visual**: preto/grafite com detalhes cromados (prata), seguindo a arte e a logo originais da Launch Line — tema único e escuro, sem alternância clara/escura.
- **Tipografia**: `Michroma` (títulos e destaques, efeito metálico) + `Inter` (texto corrido), carregadas via Google Fonts.
- **Animações de entrada**: hero com fade + zoom sutil ao carregar, barra de navegação desliza de cima, wordmark com brilho metálico contínuo, e cada seção aparece com *fade-up* ao rolar a página (via `IntersectionObserver`), com cascata nos cards de Serviços e Processo. Tudo respeita a preferência do sistema "reduzir movimento".
- **Conteúdo**: por pedido explícito, os textos de serviços e bios são genéricos/institucionais — **nenhum case, número ou depoimento foi inventado**. Quando houver projetos reais, é só substituir os textos correspondentes.

## Como editar depois

**Opção 1 — pela interface do GitHub (mais simples):**
Acesse o arquivo em https://github.com/rang3lz/launch-line-portfolio/blob/main/index.html, clique no ícone de lápis, edite e clique em "Commit changes". O GitHub Pages publica a mudança automaticamente em cerca de 1 minuto.

**Opção 2 — pedindo para o Claude:**
Volte nesta conversa (ou abra uma nova apontando para este repositório/artifact) e descreva a mudança desejada. As edições são aplicadas tanto no Artifact quanto neste repositório.

**Opção 3 — localmente:**
Não havia `git` instalado na máquina usada para publicar este projeto (só o `gh` CLI, usado via chamadas diretas à API do GitHub). Para editar por fora do navegador, instale o [Git for Windows](https://git-scm.com/download/win) e clone com:

```
gh repo clone rang3lz/launch-line-portfolio
```

## Pontos de contato configurados

- **WhatsApp:** +55 31 97118-6432 (botões "Agendar conversa" / "Agendar no WhatsApp")
- **E-mail:** contato@launchline.com

## Pendências / próximos passos sugeridos

- Trocar a seção de Serviços por cases reais quando houver (nomes, desafio/solução/resultado, com métricas verdadeiras).
- Avaliar domínio próprio (ex.: `launchline.com.br`) apontando para o GitHub Pages, em vez do endereço `.github.io`.
- Adicionar redes sociais no rodapé, se desejado.
