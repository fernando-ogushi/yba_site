# YBÁ - Projeto PWA + Serverless (Vercel)

Este repositório contém um site PWA (frontend) + funções serverless para integração com a CO2 Offset API e Zoho CRM, pronto para deploy na Vercel.

## Estrutura
- `index.html`, `about.html`, `projects.html`, `contact.html`, `dashboard.html` — páginas públicas do site.
- `public/manifest.json`, `public/service-worker.js`, `public/icon-192.png`, `public/icon-512.png`
- `assets/styles.css` — estilos simples e responsivos.
- `api/carbon.js` — função serverless para obter créditos de carbono.
- `api/crm-lead.js` — função serverless para criar leads no Zoho CRM.
- `api/crm-leads.js` — (demo) função para listar leads (pode ser ajustada).
- `vercel.json` — configuração para builds (opcional).

## Deploy rápido (arrastar e soltar)
1. Acesse https://vercel.com e faça login.
2. Clique em **New Project** → **Import** → **Drag & Drop** e selecione o conteúdo desta pasta.
3. Adicione as variáveis de ambiente no Vercel (Project → Settings → Environment Variables):
   - `CO2_API_KEY`
   - `ZOHO_CLIENT_ID`
   - `ZOHO_CLIENT_SECRET`
   - `ZOHO_REFRESH_TOKEN`
4. Deploy — Vercel publicará o site e exponha as funções em:
   - `GET /api/carbon`
   - `POST /api/crm-lead`

## Observações
- Ajuste endpoints conforme a documentação das APIs reais.
- Nunca comite tokens em repositórios públicos — use variáveis de ambiente do Vercel.

