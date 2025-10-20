# Luciana Soares Nutricionista – Deploy na Render

Este projeto é um app Next.js (App Router) com Tailwind e Radix UI. Abaixo estão os passos para rodar localmente e publicar na Render.

## Rodar localmente

1. Node 18+ instalado.
2. Instalar dependências:
   - Windows PowerShell:
     ```powershell
     npm install
     ```
3. Rodar em modo dev:
   ```powershell
   npm run dev
   ```
   Acesse http://localhost:3000.

4. Build de produção (opcional):
   ```powershell
   npm run build; npm start
   ```

## Configuração de imagens remotas
Permitidas em `next.config.ts`: `images.unsplash.com` e `picsum.photos`.

## Publicar na Render (Web Service)

Opção A – Usando render.yaml (recomendado):
- Faça push deste repositório para o GitHub/GitLab.
- Na Render, clique New + > Blueprint > selecione o repositório.
- Render detectará `render.yaml` e criará o serviço.

Opção B – Criando manualmente:
- New + > Web Service > conecte o repositório.
- Runtime: Node
- Build Command: `npm install && npm run build`
- Start Command: `npm run start`
- Environment: `NODE_ENV=production`
- Region/Plan conforme desejado.

Após o deploy, a Render executa `npm run build` e inicializa com `npm run start`.

## Variáveis de ambiente
Se futuramente usar chaves (ex.: Google AI), adicione-as nas Environment Variables do serviço na Render.

---

Se quiser, posso conectar o repositório e finalizar o deploy com você.