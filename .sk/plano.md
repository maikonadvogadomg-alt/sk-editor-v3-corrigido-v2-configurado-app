# Plano do projeto: SK-Editor-v3-Corrigido-v2

_Gerado pelo Mini SK em 14/10/2026, 07:19:55_

## Resumo

- Arquivos: **170** (1.9 MB)
- Tipo: **monorepo** (vários projetos dentro de um) — 4 package.json
- Arquivos por tipo: TSX 88, TypeScript 29, JavaScript 11, JSON 11, Markdown 5, PNG 5, HTML 4, YAML 3, GRADLE 3, XML 2, TOML 2, Git 1, NPMRC 1, Java 1, PROPERTIES 1, SVG 1, Manifest 1, CSS 1
- Dependências diferentes: **121** (40 obrigatórias, 81 só para montar)
- Restos da Replit: **4 arquivo(s)**

## 📦 @workspace/api-server — `package.json`

- Arquivo principal: `electron/main.cjs`

**Comandos (scripts):**

| Comando | O que faz | Executa |
|---|---|---|
| `desktop` | — | `electron .` |
| `exe` | — | `electron-builder --win portable --publish never` |
| `dev` | Liga o app em modo de teste (atualiza sozinho) | `export NODE_ENV=development && pnpm run build && pnpm run start` |
| `build` | Gera a versão final (pasta dist) | `node ./build.mjs` |
| `start` | Liga a versão final | `node --enable-source-maps ./dist/index.mjs` |
| `typecheck` | Confere os tipos do TypeScript (não muda nada) | `tsc -p tsconfig.json --noEmit` |

**Dependências (o app precisa) — 15:**

| Pacote | Versão | Pra que serve | Tipo |
|---|---|---|---|
| `@types/multer` | ^2.1.0 | Tipos para o TypeScript — só para montar, pode ignorar | 📐 Tipos |
| `@workspace/api-zod` | workspace:* | Pacote INTERNO deste projeto (outra pasta do monorepo) | 🔗 Interno |
| `@workspace/db` | workspace:* | Pacote INTERNO deste projeto (outra pasta do monorepo) | 🔗 Interno |
| `cookie-parser` | ^1.4.7 | Lê cookies (login) | 🗄 Servidor |
| `cors` | ^2 | Deixa a tela falar com o servidor de outro endereço | 🗄 Servidor |
| `drizzle-orm` | catalog: (catalog) | Conversa com o banco de dados (Postgres) | 🛢 Banco |
| `express` | ^5 | Servidor (recebe os pedidos das telas: salvar, IA, banco) | 🗄 Servidor |
| `multer` | ^2.1.1 | Recebe arquivos enviados (upload) | 🗄 Servidor |
| `node-pty` | ^1.1.0 | (sem descrição — toque no nome para ver no npm) | ❔ |
| `node-pty-prebuilt-multiarch` | 0.10.1-pre.5 | (sem descrição — toque no nome para ver no npm) | ❔ |
| `pino` | ^9 | Escreve o log do servidor | 🗄 Servidor |
| `pino-http` | ^10 | Log de cada pedido ao servidor | 🗄 Servidor |
| `ws` | ^8.20.0 | Conexão em tempo real (WebSocket) | 🗄 Servidor |
| `@capacitor/core` | ^7.0.0 | Transforma o app em APK (Android) | 📱 APK |
| `@capacitor/android` | ^7.0.0 | Projeto Android do Capacitor | 📱 APK |

**Dependências de montagem (dev) — 11:**

| Pacote | Versão | Pra que serve | Tipo |
|---|---|---|---|
| `@types/cookie-parser` | ^1.4.10 | Tipos para o TypeScript — só para montar, pode ignorar | 📐 Tipos |
| `@types/cors` | ^2.8.19 | Tipos para o TypeScript — só para montar, pode ignorar | 📐 Tipos |
| `@types/express` | ^5.0.6 | Tipos do Express (só para montar) | 📐 Tipos |
| `@types/node` | catalog: (catalog) | Tipos para o TypeScript — só para montar, pode ignorar | 📐 Tipos |
| `esbuild` | ^0.27.3 | Empacotador rápido: junta o servidor num arquivo só | 🔧 Montagem |
| `esbuild-plugin-pino` | ^2.3.3 | Faz o esbuild funcionar com o Pino (log) | 🔧 Montagem |
| `pino-pretty` | ^13 | Deixa o log legível | 🗄 Servidor |
| `thread-stream` | 3.1.0 | (sem descrição — toque no nome para ver no npm) | ❔ |
| `@capacitor/cli` | ^7.0.0 | Comandos do Capacitor (só para montar) | 📱 APK |
| `electron` | ^33.2.0 | Executável de computador (janela própria) | 💻 EXE |
| `electron-builder` | ^25.1.8 | Gera o .exe do Electron | 💻 EXE |

## 📦 @workspace/api-server — `api-server (1)/package.json`


**Comandos (scripts):**

| Comando | O que faz | Executa |
|---|---|---|
| `dev` | Liga o app em modo de teste (atualiza sozinho) | `export NODE_ENV=development && pnpm run build && pnpm run start` |
| `build` | Gera a versão final (pasta dist) | `node ./build.mjs` |
| `start` | Liga a versão final | `node --enable-source-maps ./dist/index.mjs` |
| `typecheck` | Confere os tipos do TypeScript (não muda nada) | `tsc -p tsconfig.json --noEmit` |

**Dependências (o app precisa) — 13:**

| Pacote | Versão | Pra que serve | Tipo |
|---|---|---|---|
| `@types/multer` | ^2.1.0 | Tipos para o TypeScript — só para montar, pode ignorar | 📐 Tipos |
| `@workspace/api-zod` | workspace:* | Pacote INTERNO deste projeto (outra pasta do monorepo) | 🔗 Interno |
| `@workspace/db` | workspace:* | Pacote INTERNO deste projeto (outra pasta do monorepo) | 🔗 Interno |
| `cookie-parser` | ^1.4.7 | Lê cookies (login) | 🗄 Servidor |
| `cors` | ^2 | Deixa a tela falar com o servidor de outro endereço | 🗄 Servidor |
| `drizzle-orm` | catalog: (catalog) | Conversa com o banco de dados (Postgres) | 🛢 Banco |
| `express` | ^5 | Servidor (recebe os pedidos das telas: salvar, IA, banco) | 🗄 Servidor |
| `multer` | ^2.1.1 | Recebe arquivos enviados (upload) | 🗄 Servidor |
| `node-pty` | ^1.1.0 | (sem descrição — toque no nome para ver no npm) | ❔ |
| `node-pty-prebuilt-multiarch` | 0.10.1-pre.5 | (sem descrição — toque no nome para ver no npm) | ❔ |
| `pino` | ^9 | Escreve o log do servidor | 🗄 Servidor |
| `pino-http` | ^10 | Log de cada pedido ao servidor | 🗄 Servidor |
| `ws` | ^8.20.0 | Conexão em tempo real (WebSocket) | 🗄 Servidor |

**Dependências de montagem (dev) — 8:**

| Pacote | Versão | Pra que serve | Tipo |
|---|---|---|---|
| `@types/cookie-parser` | ^1.4.10 | Tipos para o TypeScript — só para montar, pode ignorar | 📐 Tipos |
| `@types/cors` | ^2.8.19 | Tipos para o TypeScript — só para montar, pode ignorar | 📐 Tipos |
| `@types/express` | ^5.0.6 | Tipos do Express (só para montar) | 📐 Tipos |
| `@types/node` | catalog: (catalog) | Tipos para o TypeScript — só para montar, pode ignorar | 📐 Tipos |
| `esbuild` | ^0.27.3 | Empacotador rápido: junta o servidor num arquivo só | 🔧 Montagem |
| `esbuild-plugin-pino` | ^2.3.3 | Faz o esbuild funcionar com o Pino (log) | 🔧 Montagem |
| `pino-pretty` | ^13 | Deixa o log legível | 🗄 Servidor |
| `thread-stream` | 3.1.0 | (sem descrição — toque no nome para ver no npm) | ❔ |

## 📦 @workspace/code-editor — `code-editor (1)/package.json`


**Comandos (scripts):**

| Comando | O que faz | Executa |
|---|---|---|
| `dev` | Liga o app em modo de teste (atualiza sozinho) | `vite --config vite.config.ts --host 0.0.0.0` |
| `build` | Gera a versão final (pasta dist) | `vite build --config vite.config.ts` |
| `serve` | Liga um servidor simples | `vite preview --config vite.config.ts --host 0.0.0.0` |
| `typecheck` | Confere os tipos do TypeScript (não muda nada) | `tsc -p tsconfig.json --noEmit` |
| `build:web` | Gera a versão final (pasta dist) | `vite build --config vite.config.apk.ts` |
| `cap:init` | Monta o APK com Capacitor | `npx cap init "SK Code Editor" com.skcodeeditor.app --web-dir dist` |
| `cap:add:android` | Monta o APK com Capacitor | `npx cap add android` |
| `cap:sync` | Monta o APK com Capacitor | `npx cap sync android` |
| `cap:open` | Monta o APK com Capacitor | `npx cap open android` |
| `build:apk` | Gera a versão final (pasta dist) | `npm run build:web && npx cap sync android` |

**Dependências (o app precisa) — 27:**

| Pacote | Versão | Pra que serve | Tipo |
|---|---|---|---|
| `@capacitor/core` | ^8.3.0 | Transforma o app em APK (Android) | 📱 APK |
| `@isomorphic-git/lightning-fs` | ^4.6.2 | (sem descrição — toque no nome para ver no npm) | ❔ |
| `@monaco-editor/react` | ^4.7.0 | Editor de código do VS Code dentro do app | 🖥 Tela |
| `@xterm/addon-fit` | ^0.11.0 | Ajusta o terminal ao tamanho | 🖥 Tela |
| `@xterm/addon-serialize` | 0.13.0 | (sem descrição — toque no nome para ver no npm) | ❔ |
| `@xterm/addon-web-links` | ^0.12.0 | (sem descrição — toque no nome para ver no npm) | ❔ |
| `@xterm/headless` | 5.5.0 | (sem descrição — toque no nome para ver no npm) | ❔ |
| `@xterm/xterm` | ^6.0.0 | Terminal na tela | 🖥 Tela |
| `chalk` | 4.1.2 | (sem descrição — toque no nome para ver no npm) | ❔ |
| `chokidar` | 3.6.0 | (sem descrição — toque no nome para ver no npm) | ❔ |
| `default-shell` | 2.2.0 | (sem descrição — toque no nome para ver no npm) | ❔ |
| `file-saver` | ^2.0.5 | Baixar arquivos | 🧰 Utilidade |
| `fossil-delta` | 1.0.2 | (sem descrição — toque no nome para ver no npm) | ❔ |
| `highlight.js` | ^11.11.1 | Cores em código | 🖥 Tela |
| `jszip` | ^3.10.1 | Cria e lê arquivos .zip | 🧰 Utilidade |
| `jsonwebtoken` | 9.0.3 | Token de login (JWT) | 🗄 Servidor |
| `node-fetch` | 3.3.2 | Faz pedidos à internet (servidor) | 🗄 Servidor |
| `node-pty` | 1.2.0-beta.10 | (sem descrição — toque no nome para ver no npm) | ❔ |
| `open` | 8.4.2 | (sem descrição — toque no nome para ver no npm) | ❔ |
| `os-locale` | 8.0.0 | (sem descrição — toque no nome para ver no npm) | ❔ |
| `qrcode-terminal` | 0.12.0 | (sem descrição — toque no nome para ver no npm) | ❔ |
| `react-markdown` | ^10.1.0 | Mostra texto Markdown formatado | 🖥 Tela |
| `rehype-highlight` | ^7.0.2 | (sem descrição — toque no nome para ver no npm) | ❔ |
| `remark-gfm` | ^4.0.1 | Tabelas e listas no Markdown | 🖥 Tela |
| `socket.io-client` | 4.8.3 | (sem descrição — toque no nome para ver no npm) | ❔ |
| `write-file-atomic` | 7.0.0 | (sem descrição — toque no nome para ver no npm) | ❔ |
| `yargs` | 17.7.2 | (sem descrição — toque no nome para ver no npm) | ❔ |

**Dependências de montagem (dev) — 73:**

| Pacote | Versão | Pra que serve | Tipo |
|---|---|---|---|
| `@capacitor/android` | ^8.3.0 | Projeto Android do Capacitor | 📱 APK |
| `@capacitor/cli` | ^8.3.0 | Comandos do Capacitor (só para montar) | 📱 APK |
| `@hookform/resolvers` | ^3.10.0 | Liga o formulário às regras do Zod | 🖥 Tela |
| `@radix-ui/react-accordion` | ^1.2.4 | Peça de interface pronta (botão, menu, janela) usada pelo shadcn/ui | 🖥 Tela |
| `@radix-ui/react-alert-dialog` | ^1.1.7 | Peça de interface pronta (botão, menu, janela) usada pelo shadcn/ui | 🖥 Tela |
| `@radix-ui/react-aspect-ratio` | ^1.1.3 | Peça de interface pronta (botão, menu, janela) usada pelo shadcn/ui | 🖥 Tela |
| `@radix-ui/react-avatar` | ^1.1.4 | Peça de interface pronta (botão, menu, janela) usada pelo shadcn/ui | 🖥 Tela |
| `@radix-ui/react-checkbox` | ^1.1.5 | Peça de interface pronta (botão, menu, janela) usada pelo shadcn/ui | 🖥 Tela |
| `@radix-ui/react-collapsible` | ^1.1.4 | Peça de interface pronta (botão, menu, janela) usada pelo shadcn/ui | 🖥 Tela |
| `@radix-ui/react-context-menu` | ^2.2.7 | Peça de interface pronta (botão, menu, janela) usada pelo shadcn/ui | 🖥 Tela |
| `@radix-ui/react-dialog` | ^1.1.7 | Peça de interface pronta (botão, menu, janela) usada pelo shadcn/ui | 🖥 Tela |
| `@radix-ui/react-dropdown-menu` | ^2.1.7 | Peça de interface pronta (botão, menu, janela) usada pelo shadcn/ui | 🖥 Tela |
| `@radix-ui/react-hover-card` | ^1.1.7 | Peça de interface pronta (botão, menu, janela) usada pelo shadcn/ui | 🖥 Tela |
| `@radix-ui/react-label` | ^2.1.3 | Peça de interface pronta (botão, menu, janela) usada pelo shadcn/ui | 🖥 Tela |
| `@radix-ui/react-menubar` | ^1.1.7 | Peça de interface pronta (botão, menu, janela) usada pelo shadcn/ui | 🖥 Tela |
| `@radix-ui/react-navigation-menu` | ^1.2.6 | Peça de interface pronta (botão, menu, janela) usada pelo shadcn/ui | 🖥 Tela |
| `@radix-ui/react-popover` | ^1.1.7 | Peça de interface pronta (botão, menu, janela) usada pelo shadcn/ui | 🖥 Tela |
| `@radix-ui/react-progress` | ^1.1.3 | Peça de interface pronta (botão, menu, janela) usada pelo shadcn/ui | 🖥 Tela |
| `@radix-ui/react-radio-group` | ^1.2.4 | Peça de interface pronta (botão, menu, janela) usada pelo shadcn/ui | 🖥 Tela |
| `@radix-ui/react-scroll-area` | ^1.2.4 | Peça de interface pronta (botão, menu, janela) usada pelo shadcn/ui | 🖥 Tela |
| `@radix-ui/react-select` | ^2.1.7 | Peça de interface pronta (botão, menu, janela) usada pelo shadcn/ui | 🖥 Tela |
| `@radix-ui/react-separator` | ^1.1.3 | Peça de interface pronta (botão, menu, janela) usada pelo shadcn/ui | 🖥 Tela |
| `@radix-ui/react-slider` | ^1.2.4 | Peça de interface pronta (botão, menu, janela) usada pelo shadcn/ui | 🖥 Tela |
| `@radix-ui/react-slot` | ^1.2.0 | Peça de interface pronta (botão, menu, janela) usada pelo shadcn/ui | 🖥 Tela |
| `@radix-ui/react-switch` | ^1.1.4 | Peça de interface pronta (botão, menu, janela) usada pelo shadcn/ui | 🖥 Tela |
| `@radix-ui/react-tabs` | ^1.1.4 | Peça de interface pronta (botão, menu, janela) usada pelo shadcn/ui | 🖥 Tela |
| `@radix-ui/react-toast` | ^1.2.7 | Peça de interface pronta (botão, menu, janela) usada pelo shadcn/ui | 🖥 Tela |
| `@radix-ui/react-toggle` | ^1.1.3 | Peça de interface pronta (botão, menu, janela) usada pelo shadcn/ui | 🖥 Tela |
| `@radix-ui/react-toggle-group` | ^1.1.3 | Peça de interface pronta (botão, menu, janela) usada pelo shadcn/ui | 🖥 Tela |
| `@radix-ui/react-tooltip` | ^1.2.0 | Peça de interface pronta (botão, menu, janela) usada pelo shadcn/ui | 🖥 Tela |
| `@tailwindcss/typography` | ^0.5.15 | Estilo bonito para textos longos | 🎨 Estilo |
| `@tailwindcss/vite` | catalog: (catalog) | Liga o Tailwind no Vite | 🎨 Estilo |
| `@tanstack/react-query` | catalog: (catalog) | Busca e guarda dados do servidor nas telas | 🖥 Tela |
| `@types/file-saver` | ^2.0.7 | Tipos para o TypeScript — só para montar, pode ignorar | 📐 Tipos |
| `@types/jsonwebtoken` | ^9.0.5 | Tipos para o TypeScript — só para montar, pode ignorar | 📐 Tipos |
| `@types/node` | ^20.0.0 | Tipos para o TypeScript — só para montar, pode ignorar | 📐 Tipos |
| `@types/node-fetch` | ^2.6.11 | Tipos para o TypeScript — só para montar, pode ignorar | 📐 Tipos |
| `@types/qrcode-terminal` | ^0.12.2 | Tipos para o TypeScript — só para montar, pode ignorar | 📐 Tipos |
| `@types/react` | catalog: (catalog) | Tipos para o TypeScript — só para montar, pode ignorar | 📐 Tipos |
| `@types/react-dom` | catalog: (catalog) | Tipos para o TypeScript — só para montar, pode ignorar | 📐 Tipos |
| `@types/socket.io-client` | ^3.0.0 | Tipos para o TypeScript — só para montar, pode ignorar | 📐 Tipos |
| `@types/write-file-atomic` | ^4.0.3 | Tipos para o TypeScript — só para montar, pode ignorar | 📐 Tipos |
| `@types/ws` | ^8.5.10 | Tipos para o TypeScript — só para montar, pode ignorar | 📐 Tipos |
| `@types/yargs` | ^17.0.32 | Tipos para o TypeScript — só para montar, pode ignorar | 📐 Tipos |
| `@vitejs/plugin-react` | catalog: (catalog) | Faz o Vite entender React | 🔧 Montagem |
| `@workspace/api-client-react` | workspace:* | Pacote INTERNO deste projeto (outra pasta do monorepo) | 🔗 Interno |
| `class-variance-authority` | catalog: (catalog) | Variações de botões/estilos (shadcn/ui) | 🎨 Estilo |
| `clsx` | catalog: (catalog) | Monta listas de classes CSS | 🎨 Estilo |
| `cmdk` | ^1.1.1 | Caixa de comandos/busca rápida | 🖥 Tela |
| `date-fns` | ^3.6.0 | Datas (formatar, somar dias, prazos) | 🧰 Utilidade |
| `embla-carousel-react` | ^8.6.0 | Carrossel de imagens/cartões | 🖥 Tela |
| `framer-motion` | catalog: (catalog) | Animações nas telas | 🖥 Tela |
| `input-otp` | ^1.4.2 | Campo de código (tipo SMS) | 🖥 Tela |
| `lucide-react` | catalog: (catalog) | Ícones (desenhos dos botões) | 🖥 Tela |
| `next-themes` | ^0.4.6 | Tema claro/escuro | 🖥 Tela |
| `react` | catalog: (catalog) | Biblioteca que monta as telas do app | 🖥 Tela |
| `react-day-picker` | ^9.11.1 | Calendário para escolher datas | 🖥 Tela |
| `react-dom` | catalog: (catalog) | Coloca as telas do React no navegador | 🖥 Tela |
| `react-hook-form` | ^7.55.0 | Formulários (campos, validação) | 🖥 Tela |
| `react-icons` | ^5.6.0 | Ícones | 🖥 Tela |
| `react-resizable-panels` | ^2.1.9 | Painéis que mudam de tamanho | 🖥 Tela |
| `recharts` | ^2.15.2 | Gráficos | 🖥 Tela |
| `sonner` | ^2.0.7 | Avisos que aparecem no canto da tela | 🖥 Tela |
| `tailwind-merge` | catalog: (catalog) | Junta classes do Tailwind sem conflito | 🎨 Estilo |
| `tailwindcss` | catalog: (catalog) | Estilos prontos por classes (cores, espaços, tamanhos) | 🎨 Estilo |
| `ts-node` | ^10.9.2 | (sem descrição — toque no nome para ver no npm) | ❔ |
| `tw-animate-css` | ^1.4.0 | Animações prontas para Tailwind | 🎨 Estilo |
| `typescript` | ^5.3.0 | JavaScript com tipos — só para montar, não vai pro app final | 🔧 Montagem |
| `vaul` | ^1.1.2 | Gaveta que sobe de baixo (celular) | 🖥 Tela |
| `vite` | catalog: (catalog) | Monta (builda) o app e roda o modo de teste rápido | 🔧 Montagem |
| `vitest` | ^3.0.0 | Testes automáticos | 🧪 Teste |
| `wouter` | ^3.3.5 | Troca de páginas dentro do app (rotas) — leve | 🖥 Tela |
| `zod` | catalog: (catalog) | Confere se os dados estão no formato certo | 🧰 Utilidade |

## 📦 sk-code-editor-desktop — `code-editor (1)/desktop/package.json`

- Arquivo principal: `server.js`

**Comandos (scripts):**

| Comando | O que faz | Executa |
|---|---|---|
| `start` | Liga a versão final | `node server.js` |
| `build:win` | Gera a versão final (pasta dist) | `pkg server.js --target node18-win-x64   --output ../dist-desktop/SKCodeEditor.exe` |
| `build:linux` | Gera a versão final (pasta dist) | `pkg server.js --target node18-linux-x64 --output ../dist-desktop/SKCodeEditor-linux` |
| `build:mac` | Gera a versão final (pasta dist) | `pkg server.js --target node18-macos-x64 --output ../dist-desktop/SKCodeEditor-mac` |

## ⛔ Restos da Replit (tirar ou trocar)

- PLANO.md — 2 menção(ões)
- src/components/BuildPanel.tsx — 2 menção(ões)
- src/components/Manual.tsx — 14 menção(ões)
- src/components/WebContainerTerminal.tsx — 1 menção(ões)

## Arquivos importantes (31) — mandar estes para a IA

- `.github/workflows/apk-capacitor.yml`
- `.github/workflows/apk.yml`
- `.github/workflows/desktop-exe.yml`
- `api-server (1)/build.mjs`
- `api-server (1)/package.json`
- `api-server (1)/src/index.ts`
- `api-server (1)/src/routes/aiProcess.ts`
- `api-server (1)/src/routes/ghProxy.ts`
- `api-server (1)/src/routes/health.ts`
- `api-server (1)/src/routes/index.ts`
- `api-server (1)/src/routes/siteExtract.ts`
- `api-server (1)/tsconfig.json`
- `build.js`
- `build.mjs`
- `capacitor.config.json`
- `code-editor (1)/capacitor.config.ts`
- `code-editor (1)/components.json`
- `code-editor (1)/desktop/app/manifest.json`
- `code-editor (1)/desktop/package.json`
- `code-editor (1)/desktop/server.js`
- `code-editor (1)/package.json`
- `code-editor (1)/tsconfig.json`
- `code-editor (1)/vite.config.ts`
- `electron/main.cjs`
- `electron/preload.cjs`
- `package.json`
- `server.cjs`
- `src/App.tsx`
- `src/main.tsx`
- `tsconfig.json`
- `vite.config.ts`

## Estrutura completa (170 arquivos)

```
├── .github/
│   └── workflows/
│       ├── apk-capacitor.yml
│       ├── apk.yml
│       └── desktop-exe.yml
├── .sk/
│   └── plano.md
├── android/
│   ├── app/
│   │   ├── src/
│   │   │   └── main/
│   │   │       ├── assets/
│   │   │       │   └── __ponte.js
│   │   │       ├── java/
│   │   │       │   └── app/
│   │   │       │       └── minisk/
│   │   │       │           └── shell/
│   │   │       │               └── MainActivity.java
│   │   │       ├── res/
│   │   │       │   ├── mipmap-xxxhdpi/
│   │   │       │   │   └── ic_launcher.png
│   │   │       │   └── xml/
│   │   │       │       └── rede.xml
│   │   │       └── AndroidManifest.xml
│   │   └── build.gradle
│   ├── build.gradle
│   ├── gradle.properties
│   └── settings.gradle
├── api-server (1)/
│   ├── .replit-artifact/
│   │   └── artifact.toml
│   ├── src/
│   │   ├── lib/
│   │   │   ├── logger.ts
│   │   │   └── terminal.ts
│   │   ├── routes/
│   │   │   ├── aiProcess.ts
│   │   │   ├── ghProxy.ts
│   │   │   ├── health.ts
│   │   │   ├── index.ts
│   │   │   └── siteExtract.ts
│   │   ├── app.ts
│   │   └── index.ts
│   ├── build.mjs
│   ├── package.json
│   └── tsconfig.json
├── code-editor (1)/
│   ├── .replit-artifact/
│   │   └── artifact.toml
│   ├── desktop/
│   │   ├── app/
│   │   │   ├── extrator.html
│   │   │   ├── favicon.svg
│   │   │   ├── index.html
│   │   │   ├── manifest.json
│   │   │   └── sw.js
│   │   ├── package.json
│   │   ├── server_main.js
│   │   └── server.js
│   ├── capacitor.config.ts
│   ├── components.json
│   ├── index.html
│   ├── MANUAL-APK.md
│   ├── package.json
│   ├── tsconfig.json
│   ├── vite.config.apk.ts
│   ├── vite.config.standalone.ts
│   └── vite.config.ts
├── electron/
│   ├── main.cjs
│   └── preload.cjs
├── public/
│   ├── icon-192.png
│   ├── icon-512.png
│   ├── icon.ico.png
│   ├── icon.png
│   └── manifest.webmanifest
├── src/
│   ├── components/
│   │   ├── ui/
│   │   │   ├── accordion.tsx
│   │   │   ├── alert-dialog.tsx
│   │   │   ├── alert.tsx
│   │   │   ├── aspect-ratio.tsx
│   │   │   ├── avatar.tsx
│   │   │   ├── badge.tsx
│   │   │   ├── breadcrumb.tsx
│   │   │   ├── button-group.tsx
│   │   │   ├── button.tsx
│   │   │   ├── calendar.tsx
│   │   │   ├── card.tsx
│   │   │   ├── carousel.tsx
│   │   │   ├── chart.tsx
│   │   │   ├── checkbox.tsx
│   │   │   ├── collapsible.tsx
│   │   │   ├── command.tsx
│   │   │   ├── context-menu.tsx
│   │   │   ├── dialog.tsx
│   │   │   ├── drawer.tsx
│   │   │   ├── dropdown-menu.tsx
│   │   │   ├── empty.tsx
│   │   │   ├── field.tsx
│   │   │   ├── form.tsx
│   │   │   ├── hover-card.tsx
│   │   │   ├── input-group.tsx
│   │   │   ├── input-otp.tsx
│   │   │   ├── input.tsx
│   │   │   ├── item.tsx
│   │   │   ├── kbd.tsx
│   │   │   ├── label.tsx
│   │   │   ├── menubar.tsx
│   │   │   ├── navigation-menu.tsx
│   │   │   ├── pagination.tsx
│   │   │   ├── popover.tsx
│   │   │   ├── progress.tsx
│   │   │   ├── radio-group.tsx
│   │   │   ├── resizable.tsx
│   │   │   ├── scroll-area.tsx
│   │   │   ├── select.tsx
│   │   │   ├── separator.tsx
│   │   │   ├── sheet.tsx
│   │   │   ├── sidebar.tsx
│   │   │   ├── skeleton.tsx
│   │   │   ├── slider.tsx
│   │   │   ├── sonner.tsx
│   │   │   ├── spinner.tsx
│   │   │   ├── switch.tsx
│   │   │   ├── table.tsx
│   │   │   ├── tabs.tsx
│   │   │   ├── textarea.tsx
│   │   │   ├── toast.tsx
│   │   │   ├── toaster.tsx
│   │   │   ├── toggle-group.tsx
│   │   │   ├── toggle.tsx
│   │   │   └── tooltip.tsx
│   │   ├── AIChat.tsx
│   │   ├── AssistenteJuridico.tsx
│   │   ├── BuildPanel.tsx
│   │   ├── CampoLivre.tsx
│   │   ├── CodeEditor.tsx
│   │   ├── CombinarApps.tsx
│   │   ├── DatabasePanel.tsx
│   │   ├── DeployPanel.tsx
│   │   ├── DriveBackupPanel.tsx
│   │   ├── EditorLayout.tsx
│   │   ├── ElectronTerminal.tsx
│   │   ├── FileScanner.tsx
│   │   ├── FileTree.tsx
│   │   ├── GitHubPanel.tsx
│   │   ├── HTMLPlayground.tsx
│   │   ├── Manual.tsx
│   │   ├── PackageSearch.tsx
│   │   ├── Preview.tsx
│   │   ├── QuickPrompt.tsx
│   │   ├── RealTerminal.tsx
│   │   ├── SiteExtractor.tsx
│   │   ├── SKTerminal.tsx
│   │   ├── StreamTerminal.tsx
│   │   ├── SystemStatusPanel.tsx
│   │   ├── TemplateSelector.tsx
│   │   ├── Terminal.tsx
│   │   ├── VoiceCard.tsx
│   │   ├── VoiceMode.tsx
│   │   ├── WebContainerTerminal.tsx
│   │   └── XTermConnector.tsx
│   ├── hooks/
│   │   ├── use-mobile.tsx
│   │   └── use-toast.ts
│   ├── lib/
│   │   ├── ai-service.ts
│   │   ├── github-service.ts
│   │   ├── idb-storage.ts
│   │   ├── projects.ts
│   │   ├── store.ts
│   │   ├── templates.ts
│   │   ├── tts-service.ts
│   │   ├── utils.ts
│   │   ├── virtual-fs.ts
│   │   └── zip-service.ts
│   ├── App.tsx
│   ├── index.css
│   └── main.tsx
├── workflow.ylm/
│   └── workflow.js
├── .gitignore
├── .npmrc
├── apk.config.json
├── build.js
├── build.mjs
├── capacitor.config.json
├── COMO-RODAR.md
├── devServerRegistry.ts
├── index.html
├── logger.ts
├── package.json
├── persistFiles.ts
├── PLANO.md
├── README-SK-EDITOR-V3.md
├── server.cjs
├── storage.ts
├── tsconfig.json
└── vite.config.ts
```
