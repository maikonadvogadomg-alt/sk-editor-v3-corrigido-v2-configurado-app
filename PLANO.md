# 📋 Plano do projeto: SK-Editor-v3-Corrigido-v2

_Gerado em 14/10/2026, 07:21:21 — sem IA, lendo os arquivos._

## 📊 Visão geral
| Item | Valor |
|---|---|
| Arquivos | 160 |
| Linhas | 40.795 |
| Telas/páginas | 4 |
| Rotas do backend | 40 |
| Chamadas do app | 28 |
| Tabelas do banco | 4 |
| Variáveis de ambiente | 33 |

**Linguagens:** TypeScript (React) (88), TypeScript (29), JSON (11), JavaScript (10), Outros (5), HTML (4), Markdown (4), Imagem (4), YAML (3), Imagem SVG (1), CSS (1)

## 🧩 Apps dentro deste projeto
- api-server (1) (@workspace/api-server)
- code-editor (1)/desktop (sk-code-editor-desktop)
- code-editor (1) (@workspace/code-editor)

## 💡 O que fazer (em ordem)
1. 🧹 Tirar a Replit de 16 arquivo(s) (🏗️ Preparar → Fazer tudo)
2. 🖥️ O projeto tem backend próprio: para funcionar fora da Replit ele precisa ficar ligado num servidor (Render, Railway, Vercel) ou virar funções
3. 🔐 Criar um .env.example com: AI_API_KEY, ALLOWED_ORIGINS, ANTHROPIC_API_KEY, BASE_PATH, BASE_URL, DATABASE_URL, GEMINI_API_KEY, GROQ_API_KEY, JWT_EXPIRES_IN, JWT_SECRET, LOG_LEVEL, MONGODB_URI… (os valores você coloca no servidor, nunca no código)
4. 🗄️ Precisa de banco de dados (4 tabela(s)) — Neon ou Supabase servem, grátis
5. 📝 Criar um README.md explicando como rodar

## 🚀 Por onde começa
- `api-server (1)/src/app.ts`
- `api-server (1)/src/index.ts`
- `api-server (1)/src/routes/index.ts`
- `code-editor (1)/desktop/app/index.html`
- `code-editor (1)/desktop/server.js`
- `code-editor (1)/index.html`
- `index.html`
- `src/App.tsx`
- `src/main.tsx`

## ⌨️ Comandos (package.json)
| Pasta | Comando | O que roda |
|---|---|---|
| api-server (1) | `npm run dev` | `export NODE_ENV=development && pnpm run build && pnpm run start` |
| api-server (1) | `npm run build` | `node ./build.mjs` |
| api-server (1) | `npm run start` | `node --enable-source-maps ./dist/index.mjs` |
| api-server (1) | `npm run typecheck` | `tsc -p tsconfig.json --noEmit` |
| code-editor (1)/desktop | `npm run start` | `node server.js` |
| code-editor (1)/desktop | `npm run build:win` | `pkg server.js --target node18-win-x64   --output ../dist-desktop/SKCodeEditor.exe` |
| code-editor (1)/desktop | `npm run build:linux` | `pkg server.js --target node18-linux-x64 --output ../dist-desktop/SKCodeEditor-linux` |
| code-editor (1)/desktop | `npm run build:mac` | `pkg server.js --target node18-macos-x64 --output ../dist-desktop/SKCodeEditor-mac` |
| code-editor (1) | `npm run dev` | `vite --config vite.config.ts --host 0.0.0.0` |
| code-editor (1) | `npm run build` | `vite build --config vite.config.ts` |
| code-editor (1) | `npm run serve` | `vite preview --config vite.config.ts --host 0.0.0.0` |
| code-editor (1) | `npm run typecheck` | `tsc -p tsconfig.json --noEmit` |
| code-editor (1) | `npm run build:web` | `vite build --config vite.config.apk.ts` |
| code-editor (1) | `npm run cap:init` | `npx cap init "SK Code Editor" com.skcodeeditor.app --web-dir dist` |
| code-editor (1) | `npm run cap:add:android` | `npx cap add android` |
| code-editor (1) | `npm run cap:sync` | `npx cap sync android` |
| code-editor (1) | `npm run cap:open` | `npx cap open android` |
| code-editor (1) | `npm run build:apk` | `npm run build:web && npx cap sync android` |
| . | `npm run desktop` | `electron .` |
| . | `npm run exe` | `electron-builder --win portable --publish never` |
| . | `npm run dev` | `export NODE_ENV=development && pnpm run build && pnpm run start` |
| . | `npm run build` | `node ./build.mjs` |
| . | `npm run start` | `node --enable-source-maps ./dist/index.mjs` |
| . | `npm run typecheck` | `tsc -p tsconfig.json --noEmit` |

## 📱 Telas e páginas
| Endereço | Arquivo |
|---|---|
| `code-editor (1)/desktop/app/extrator.html` | code-editor (1)/desktop/app/extrator.html |
| `code-editor (1)/desktop/app/index.html` | code-editor (1)/desktop/app/index.html |
| `code-editor (1)/index.html` | code-editor (1)/index.html |
| `index.html` | index.html |

## 🖥️ Rotas do backend
| Método | Rota | Arquivo |
|---|---|---|
| USE | `/api` | api-server (1)/src/app.ts |
| POST | `/ai/process` | api-server (1)/src/routes/aiProcess.ts |
| POST | `/code-assistant` | api-server (1)/src/routes/aiProcess.ts |
| GET | `/gh-proxy/zipball` | api-server (1)/src/routes/ghProxy.ts |
| GET | `/gh-proxy/repo` | api-server (1)/src/routes/ghProxy.ts |
| GET | `/healthz` | api-server (1)/src/routes/health.ts |
| GET | `/config` | api-server (1)/src/routes/index.ts |
| POST | `/site-extract` | api-server (1)/src/routes/siteExtract.ts |
| GET | `/site-extract/proxy` | api-server (1)/src/routes/siteExtract.ts |
| GET | `/api/processos` | src/components/AIChat.tsx |
| GET | `/api/items` | src/lib/templates.ts |
| GET | `/api/items/:id` | src/lib/templates.ts |
| POST | `/api/items` | src/lib/templates.ts |
| GET | `/api/health` | src/lib/templates.ts |
| USE | `/api/auth` | src/lib/templates.ts |
| USE | `/api/usuarios` | src/lib/templates.ts |
| POST | `/register` | src/lib/templates.ts |
| POST | `/login` | src/lib/templates.ts |
| GET | `/perfil` | src/lib/templates.ts |
| GET | `/api/provedores` | src/lib/templates.ts |
| POST | `/api/chat` | src/lib/templates.ts |
| GET | `/health` | src/lib/templates.ts |
| POST | `/auth/login` | src/lib/templates.ts |
| POST | `/auth/registro` | src/lib/templates.ts |
| GET | `/clientes` | src/lib/templates.ts |
| GET | `/clientes/:id` | src/lib/templates.ts |
| POST | `/clientes` | src/lib/templates.ts |
| PUT | `/clientes/:id` | src/lib/templates.ts |
| GET | `/processos` | src/lib/templates.ts |
| GET | `/processos/:id` | src/lib/templates.ts |
| POST | `/processos` | src/lib/templates.ts |
| GET | `/audiencias` | src/lib/templates.ts |
| POST | `/audiencias` | src/lib/templates.ts |
| GET | `/prazos/proximos` | src/lib/templates.ts |
| GET | `/dashboard` | src/lib/templates.ts |
| GET | `/api/registros` | src/lib/templates.ts |
| GET | `/api/registros/:id` | src/lib/templates.ts |
| POST | `/api/registros` | src/lib/templates.ts |
| PUT | `/api/registros/:id` | src/lib/templates.ts |
| DELETE | `/api/registros/:id` | src/lib/templates.ts |

## 📡 O que o app pede ao servidor
| Método | Endereço | Onde |
|---|---|---|
| POST | `/chat/completions` | api-server (1)/src/routes/aiProcess.ts |
| GET | `/repos/${owner}/${repo}` | api-server (1)/src/routes/ghProxy.ts |
| POST | `/voice/speak` | src/components/AIChat.tsx |
| GET | `/api/search?q=${encodeURIComponent(q)}` | src/components/AIChat.tsx |
| POST | `/api/ai/chat` | src/components/AssistenteJuridico.tsx |
| POST | `/api/ai/forward` | src/components/CampoLivre.tsx |
| POST | `/api/criar-checkout` | src/components/DeployPanel.tsx |
| GET | `/drive/list` | src/components/DriveBackupPanel.tsx |
| POST | `/drive/upload` | src/components/DriveBackupPanel.tsx |
| DELETE | `/drive/delete/${fileId}` | src/components/DriveBackupPanel.tsx |
| POST | `/api/workspace/write` | src/components/EditorLayout.tsx |
| POST | `/api/workspace/sync` | src/components/EditorLayout.tsx |
| POST | `/api/db/query` | src/components/EditorLayout.tsx |
| POST | `/api/exec-stream` | src/components/ElectronTerminal.tsx |
| POST | `/api/exec-stop` | src/components/ElectronTerminal.tsx |
| POST | `/api/pages/deploy` | src/components/GitHubPanel.tsx |
| GET | `/api/twa-files?url=${encodeURIComponent(url)}` | src/components/Manual.tsx |
| GET | `/api/pwa-check?url=${encodeURIComponent(url)}` | src/components/Manual.tsx |
| POST | `/api/workspace/install` | src/components/PackageSearch.tsx |
| GET | `/api/config` | src/components/RealTerminal.tsx |
| POST | `/api/projects/default/exec-stream` | src/components/StreamTerminal.tsx |
| POST | `/api/projects/default/exec-stdin` | src/components/StreamTerminal.tsx |
| GET | `/api/healthz` | src/components/SystemStatusPanel.tsx |
| GET | `/api/ai/chat` | src/components/SystemStatusPanel.tsx |
| POST | `/api/voice/speak` | src/components/VoiceMode.tsx |
| GET | `/api/provedores` | src/lib/templates.ts |
| POST | `/api/chat` | src/lib/templates.ts |
| GET | `/api/registros?busca=` | src/lib/templates.ts |

## 🔌 O que falta no backend
✅ Tudo que o app chama tem rota no projeto (ou o app não usa servidor).

## 💤 Rotas que o app não usa
- POST `/ai/process` — api-server (1)/src/routes/aiProcess.ts
- POST `/code-assistant` — api-server (1)/src/routes/aiProcess.ts
- GET `/gh-proxy/zipball` — api-server (1)/src/routes/ghProxy.ts
- GET `/gh-proxy/repo` — api-server (1)/src/routes/ghProxy.ts
- POST `/site-extract` — api-server (1)/src/routes/siteExtract.ts
- GET `/site-extract/proxy` — api-server (1)/src/routes/siteExtract.ts
- GET `/api/processos` — src/components/AIChat.tsx
- GET `/api/items` — src/lib/templates.ts
- GET `/api/items/:id` — src/lib/templates.ts
- POST `/api/items` — src/lib/templates.ts
- GET `/api/health` — src/lib/templates.ts
- POST `/register` — src/lib/templates.ts
- POST `/login` — src/lib/templates.ts
- GET `/perfil` — src/lib/templates.ts
- GET `/health` — src/lib/templates.ts
- POST `/auth/login` — src/lib/templates.ts
- POST `/auth/registro` — src/lib/templates.ts
- GET `/clientes` — src/lib/templates.ts
- GET `/clientes/:id` — src/lib/templates.ts
- POST `/clientes` — src/lib/templates.ts
- PUT `/clientes/:id` — src/lib/templates.ts
- GET `/processos` — src/lib/templates.ts
- GET `/processos/:id` — src/lib/templates.ts
- POST `/processos` — src/lib/templates.ts
- GET `/audiencias` — src/lib/templates.ts
- POST `/audiencias` — src/lib/templates.ts
- GET `/prazos/proximos` — src/lib/templates.ts
- GET `/dashboard` — src/lib/templates.ts
- GET `/api/registros/:id` — src/lib/templates.ts
- PUT `/api/registros/:id` — src/lib/templates.ts
- DELETE `/api/registros/:id` — src/lib/templates.ts

## 🗄️ Banco de dados
- **processos** — src/components/AIChat.tsx
- **usuarios** — src/components/DatabasePanel.tsx
- **User** — src/components/Terminal.tsx
- **Post** — src/components/Terminal.tsx

## 🔐 Variáveis de ambiente (configurar no servidor)
- `AI_API_KEY`
- `ALLOWED_ORIGINS`
- `ANTHROPIC_API_KEY`
- `BASE_PATH`
- `BASE_URL`
- `DATABASE_URL`
- `GEMINI_API_KEY`
- `GROQ_API_KEY`
- `JWT_EXPIRES_IN`
- `JWT_SECRET`
- `LOG_LEVEL`
- `MONGODB_URI`
- `NODE_ENV`
- `OPENAI_API_KEY`
- `OPENROUTER_API_KEY`
- `PERPLEXITY_API_KEY`
- `PORT`
- `STORAGE_PATH`
- `STRIPE_SECRET_KEY`
- `SUPABASE_ANON_KEY`
- `SUPABASE_KEY`
- `SUPABASE_URL`
- `TELEGRAM_TOKEN`
- `VITE_FIREBASE_API_KEY`
- `VITE_FIREBASE_APP_ID`
- `VITE_FIREBASE_AUTH_DOMAIN`
- `VITE_FIREBASE_MESSAGING_SENDER_ID`
- `VITE_FIREBASE_PROJECT_ID`
- `VITE_FIREBASE_STORAGE_BUCKET`
- `VITE_SUPABASE_ANON_KEY`
- `VITE_SUPABASE_URL`
- `XAI_API_KEY`
- `YOUTUBE_URL`

_Só os nomes. Os valores (chaves, senhas) nunca vão no código nem no GitHub._

## 🤖 IA usada
- api.openai.com
- api.anthropic.com
- generativelanguage.googleapis.com
- api.groq.com
- openrouter.ai
- console.groq.com
- platform.openai.com
- console.anthropic.com

## 🌐 Serviços de fora que ele acessa
- adoptium.net
- aistudio.google.com
- api.allorigins.win
- api.anthropic.com
- api.codetabs.com
- api.exemplo.com
- api.github.com
- api.groq.com
- api.mistral.ai
- api.openai.com
- api.perplexity.ai
- api.together.xyz
- api.x.ai
- app.netlify.com
- cdn.jsdelivr.net
- console.anthropic.com
- console.groq.com
- console.neon.tech
- console.x.ai
- corsproxy.io
- developer.android.com
- digitalocean.com
- duckduckgo.com
- exemplo.com
- expo.dev
- generativelanguage.googleapis.com
- git-scm.com
- github.com
- github.dev
- gitpod.io
- hostinger.com.br
- instagram.com
- meu-app.replit.app
- namecheap.com
- neon.tech
- netlify.com
- nodejs.org
- openrouter.ai
- pages.cloudflare.com
- platform.openai.com
- play.google.com
- pwabuilder.com
- pypi.org
- railway.app
- registro.br
- registry.npmjs.org
- render.com
- replit.com
- resend.com
- seu-app.replit.app
- seu-nome-abc123.netlify.app
- seu-projeto.vercel.app
- seusite.com
- sk-code-editor.app
- sk-editor.app
- stackblitz.com
- stripe.com
- supabase.com
- vercel.com
- vscode.dev
- wa.me
- www.google.com
- www.netlify.com
- www.perplexity.ai
- www.pwabuilder.com
- www.youtube.com
- xxx.supabase.co
- xxxx.supabase.co
- youtube.com

## 📦 Peças principais (dependências)
`@capacitor/android` · `@capacitor/core` · `@isomorphic-git/lightning-fs` · `@monaco-editor/react` · `@types/multer` · `@workspace/api-zod` · `@workspace/db` · `@xterm/addon-fit` · `@xterm/addon-serialize` · `@xterm/addon-web-links` · `@xterm/headless` · `@xterm/xterm` · `chalk` · `chokidar` · `cookie-parser` · `cors` · `default-shell` · `drizzle-orm` · `express` · `file-saver` · `fossil-delta` · `highlight.js` · `jsonwebtoken` · `jszip` · `multer` · `node-fetch` · `node-pty` · `node-pty-prebuilt-multiarch` · `open` · `os-locale` · `pino` · `pino-http` · `qrcode-terminal` · `react-markdown` · `rehype-highlight` · `remark-gfm` · `socket.io-client` · `write-file-atomic` · `ws` · `yargs`

## 🧹 Arquivos com coisa da Replit
- src/components/AIChat.tsx
- src/components/AssistenteJuridico.tsx
- src/components/BuildPanel.tsx
- src/components/CampoLivre.tsx
- src/components/CombinarApps.tsx
- src/components/DatabasePanel.tsx
- src/components/EditorLayout.tsx
- src/components/ElectronTerminal.tsx
- src/components/GitHubPanel.tsx
- src/components/Manual.tsx
- src/components/RealTerminal.tsx
- src/components/SKTerminal.tsx
- src/components/Terminal.tsx
- src/components/ui/badge.tsx
- src/components/ui/button.tsx
- src/components/WebContainerTerminal.tsx

## 🔁 Roteiro para recriar fora da Replit
1. Importar o projeto no Mini SK e tocar em 🏗️ Preparar → ✅ Fazer tudo (tira a Replit, cria os arquivos que faltam).
2. Backend: escolher onde ele vai ficar ligado (Render/Railway grátis) — ou pedir à IA para transformar as rotas em funções do Netlify/Vercel, usando a tabela "O que falta no backend".
3. Banco: criar no Neon ou Supabase e colocar o endereço na variável de ambiente do servidor.
4. Variáveis: cadastrar 33 variável(is) no servidor (lista acima).
5. Testar a prévia; se der erro, 🤖 Mandar os erros para a IA.
6. App: 📲 Instalável (PWA), 📦 APK ou 🖥️ Desktop (.exe) pelo 🏗️ Preparar.

## 🌳 Árvore de arquivos
```
├─ 📁 .github/
│  └─ 📁 workflows/
│     ├─ apk-capacitor.yml
│     ├─ apk.yml
│     └─ desktop-exe.yml
├─ 📁 api-server (1)/
│  ├─ 📁 .replit-artifact/
│  │  └─ artifact.toml
│  ├─ 📁 src/
│  │  ├─ 📁 lib/
│  │  │  ├─ logger.ts
│  │  │  └─ terminal.ts
│  │  ├─ 📁 routes/
│  │  │  ├─ aiProcess.ts
│  │  │  ├─ ghProxy.ts
│  │  │  ├─ health.ts
│  │  │  ├─ index.ts
│  │  │  └─ siteExtract.ts
│  │  ├─ app.ts
│  │  └─ index.ts
│  ├─ build.mjs
│  ├─ package.json
│  └─ tsconfig.json
├─ 📁 code-editor (1)/
│  ├─ 📁 .replit-artifact/
│  │  └─ artifact.toml
│  ├─ 📁 desktop/
│  │  ├─ 📁 app/
│  │  │  ├─ extrator.html
│  │  │  ├─ favicon.svg
│  │  │  ├─ index.html
│  │  │  ├─ manifest.json
│  │  │  └─ sw.js
│  │  ├─ package.json
│  │  ├─ server_main.js
│  │  └─ server.js
│  ├─ capacitor.config.ts
│  ├─ components.json
│  ├─ index.html
│  ├─ MANUAL-APK.md
│  ├─ package.json
│  ├─ tsconfig.json
│  ├─ vite.config.apk.ts
│  ├─ vite.config.standalone.ts
│  └─ vite.config.ts
├─ 📁 electron/
│  ├─ main.cjs
│  └─ preload.cjs
├─ 📁 public/
│  ├─ icon-192.png
│  ├─ icon-512.png
│  ├─ icon.ico.png
│  ├─ icon.png
│  └─ manifest.webmanifest
├─ 📁 src/
│  ├─ 📁 components/
│  │  ├─ 📁 ui/
│  │  │  ├─ accordion.tsx
│  │  │  ├─ alert-dialog.tsx
│  │  │  ├─ alert.tsx
│  │  │  ├─ aspect-ratio.tsx
│  │  │  ├─ avatar.tsx
│  │  │  ├─ badge.tsx
│  │  │  ├─ breadcrumb.tsx
│  │  │  ├─ button-group.tsx
│  │  │  ├─ button.tsx
│  │  │  ├─ calendar.tsx
│  │  │  ├─ card.tsx
│  │  │  ├─ carousel.tsx
│  │  │  ├─ chart.tsx
│  │  │  ├─ checkbox.tsx
│  │  │  ├─ collapsible.tsx
│  │  │  ├─ command.tsx
│  │  │  ├─ context-menu.tsx
│  │  │  ├─ dialog.tsx
│  │  │  ├─ drawer.tsx
│  │  │  ├─ dropdown-menu.tsx
│  │  │  ├─ empty.tsx
│  │  │  ├─ field.tsx
│  │  │  ├─ form.tsx
│  │  │  ├─ hover-card.tsx
│  │  │  ├─ input-group.tsx
│  │  │  ├─ input-otp.tsx
│  │  │  ├─ input.tsx
│  │  │  ├─ item.tsx
│  │  │  ├─ kbd.tsx
│  │  │  ├─ label.tsx
│  │  │  ├─ menubar.tsx
│  │  │  ├─ navigation-menu.tsx
│  │  │  ├─ pagination.tsx
│  │  │  ├─ popover.tsx
│  │  │  ├─ progress.tsx
│  │  │  ├─ radio-group.tsx
│  │  │  ├─ resizable.tsx
│  │  │  ├─ scroll-area.tsx
│  │  │  ├─ select.tsx
│  │  │  ├─ separator.tsx
│  │  │  ├─ sheet.tsx
│  │  │  ├─ sidebar.tsx
│  │  │  ├─ skeleton.tsx
│  │  │  ├─ slider.tsx
│  │  │  ├─ sonner.tsx
│  │  │  ├─ spinner.tsx
│  │  │  ├─ switch.tsx
│  │  │  ├─ table.tsx
│  │  │  ├─ tabs.tsx
│  │  │  ├─ textarea.tsx
│  │  │  ├─ toast.tsx
│  │  │  ├─ toaster.tsx
│  │  │  ├─ toggle-group.tsx
│  │  │  ├─ toggle.tsx
│  │  │  └─ tooltip.tsx
│  │  ├─ AIChat.tsx
│  │  ├─ AssistenteJuridico.tsx
│  │  ├─ BuildPanel.tsx
│  │  ├─ CampoLivre.tsx
│  │  ├─ CodeEditor.tsx
│  │  ├─ CombinarApps.tsx
│  │  ├─ DatabasePanel.tsx
│  │  ├─ DeployPanel.tsx
│  │  ├─ DriveBackupPanel.tsx
│  │  ├─ EditorLayout.tsx
│  │  ├─ ElectronTerminal.tsx
│  │  ├─ FileScanner.tsx
│  │  ├─ FileTree.tsx
│  │  ├─ GitHubPanel.tsx
│  │  ├─ HTMLPlayground.tsx
│  │  ├─ Manual.tsx
│  │  ├─ PackageSearch.tsx
│  │  ├─ Preview.tsx
│  │  ├─ QuickPrompt.tsx
│  │  ├─ RealTerminal.tsx
│  │  ├─ SiteExtractor.tsx
│  │  ├─ SKTerminal.tsx
│  │  ├─ StreamTerminal.tsx
│  │  ├─ SystemStatusPanel.tsx
│  │  ├─ TemplateSelector.tsx
│  │  ├─ Terminal.tsx
│  │  ├─ VoiceCard.tsx
│  │  ├─ VoiceMode.tsx
│  │  ├─ WebContainerTerminal.tsx
│  │  └─ XTermConnector.tsx
│  ├─ 📁 hooks/
│  │  ├─ use-mobile.tsx
│  │  └─ use-toast.ts
│  ├─ 📁 lib/
│  │  ├─ ai-service.ts
│  │  ├─ github-service.ts
│  │  ├─ idb-storage.ts
│  │  ├─ projects.ts
│  │  ├─ store.ts
│  │  ├─ templates.ts
│  │  ├─ tts-service.ts
│  │  ├─ utils.ts
│  │  ├─ virtual-fs.ts
│  │  └─ zip-service.ts
│  ├─ App.tsx
│  ├─ index.css
│  └─ main.tsx
├─ 📁 workflow.ylm/
│  └─ workflow.js
├─ .gitignore
├─ .npmrc
├─ apk.config.json
├─ build.js
├─ build.mjs
├─ capacitor.config.json
├─ COMO-RODAR.md
├─ devServerRegistry.ts
├─ index.html
├─ logger.ts
├─ package.json
├─ persistFiles.ts
├─ PLANO.md
├─ README-SK-EDITOR-V3.md
├─ server.cjs
├─ storage.ts
├─ tsconfig.json
└─ vite.config.ts
```
