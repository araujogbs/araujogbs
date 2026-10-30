<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=ff91a4&height=120&section=header"/>

# 👋 Olá, eu sou o Gabriel Araújo!

**Desenvolvedor Full Stack** em São Paulo. Crio aplicações web, mobile e APIs REST com **TypeScript, React, React Native, Node.js e C# (.NET)**, do banco de dados ao deploy.

Hoje sou **Analista de Suporte Nível 2 na Joinner Sistemas**, referência técnica da operação e elo direto com o time de Engenharia de Software: investigo a causa-raiz de incidentes em produção, escrevo SQL em PostgreSQL para auditoria e correção de dados, e automatizo o que se repete (como um [bot em Python, com OCR](https://github.com/araujogbs/bot-suporte-ERP), que indexa erros de ERP e foi adotado por toda a equipe).

<p align="left">
  <a href="https://www.linkedin.com/in/gabriel-ara%C3%BAjo-a5a439277/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge" alt="LinkedIn" /></a>
  <a href="mailto:Gabriel.AraujoC@outlook.com"><img src="https://img.shields.io/badge/E--mail-Gabriel.AraujoC%40outlook.com-ff91a4?style=for-the-badge&labelColor=0D1117" alt="E-mail" /></a>
</p>

---

## 🚀 Projetos em destaque

### 💄 [Lari Novais Beauty](https://larinovaisbeauty.com.br) — site e sistema de agendamento de uma maquiadora profissional

Projeto real, feito para uma cliente e **em produção** em [larinovaisbeauty.com.br](https://larinovaisbeauty.com.br): **site e painel em React + TypeScript** e **API em ASP.NET Core (.NET 10) + PostgreSQL**. A cliente escolhe os serviços de cada pessoa, o dia e o horário, e já vê a taxa de deslocamento calculada pelo CEP; a maquiadora aprova ou recusa cada pedido no painel (instalável no iPhone, com notificação push), envia a confirmação com o PIX do sinal pelo WhatsApp, e o atendimento vai sozinho para o Google Agenda dela.

- Horários sem conflito garantidos por *exclusion constraint* no PostgreSQL, mesmo com pedidos simultâneos
- Fluxo de aprovação com estados, sinal via PIX (QR Code) e tarefas em segundo plano que expiram pedidos sem resposta e mantêm bloqueios fixos de agenda
- Integrações com Google Calendar (conta de serviço), Web Push (VAPID) e cálculo de rota por CEP
- JWT, senha em hash, rate limiting, upload validado, CSP e segredos fora do Git
- Site pré-renderizado, fotos WebP responsivas e tema celeste com modo noturno; testes com Vitest e Testing Library
- Deploy: API em Docker + Caddy (HTTPS) numa VPS Linux, com backup diário; site na Cloudflare com publicação a cada push

<p>
  <img src="https://raw.githubusercontent.com/araujogbs/lari-novais-beauty-site/master/docs/site-home.jpg" width="48.6%" alt="Site: página inicial" />
  <img src="https://raw.githubusercontent.com/araujogbs/lari-novais-beauty-site/master/docs/site-celular.jpg" width="13.4%" alt="Site no celular" />
  <img src="assets/lari-agendamento-1.jpg" width="16.7%" alt="Agendamento: serviços, dia e horário" />
  <img src="assets/lari-agendamento-2.jpg" width="18.3%" alt="Agendamento: dados e resumo" />
</p>
<p>
  <img src="assets/lari-painel.jpg" width="55%" alt="Painel da maquiadora: pedidos em análise e agenda do dia" />
</p>

[Site no ar](https://larinovaisbeauty.com.br) · [Código do site](https://github.com/araujogbs/lari-novais-beauty-site) · [API](https://github.com/araujogbs/lari-novais-beauty-agendamento)

### 🤖 [Bot de suporte ERP](https://github.com/araujogbs/bot-suporte-ERP) — memória compartilhada do time de suporte *(em uso)*

Iniciativa minha no suporte da Joinner: um bot de **Discord em Python** que lê com **OCR** cada print de erro postado pelo time, guarda a solução junto do erro e acha em qual relatório do ERP está uma informação. A **equipe inteira usa** no dia a dia, sem instalar nada.

- Busca por texto ou **pelo próprio print** (OCR com Tesseract): mostra os casos parecidos com data, link da conversa e a solução registrada
- Base com **mais de 13,5 mil prints** indexados, que cresce com o uso ( ou reação ✅ no print)
- Catálogo de **459 telas e 1.337 relatórios e exportações** (SPICA 7 e 8) com busca E/OU, plural e "você quis dizer…?"
- Envia o print do menu do sistema com a tela **circulada em vermelho**, localizada por OCR
- SQLite, indexação do histórico retomável e OCR fora do loop do bot; dados de clientes e token fora do Git

### 🎓 [Lessionato](https://github.com/araujogbs/lessionato-edtech-platform) — plataforma de cursos livres *(estudo de caso)*

Entregue de ponta a ponta para a **Gemba Consultoria** com **React, TypeScript, Node.js, Express e MongoDB**. O aluno compra o curso por PIX, o acesso é liberado sozinho quando o banco confirma, e no fim ele faz a prova e emite um certificado que qualquer pessoa pode validar. O código foi vendido junto com o produto; o repositório documenta a arquitetura e as decisões técnicas.

- Pagamento via **PIX com mTLS** (API da Gerencianet/EFI), webhook de liquidação e confirmação em tempo real na tela
- Certificados em PDF gerados no servidor (`pdf-lib`), com código de autenticidade, QR Code e validação pública
- Prova final com nota mínima, cupons de desconto com limite e validade, e prazo de 7 dias do CDC antes do certificado
- JWT com token de renovação, senhas com bcrypt e recuperação de senha por e-mail com token de uso único
- Deploy em VPS Linux com Nginx

<p>
  <img src="https://raw.githubusercontent.com/araujogbs/lessionato-edtech-platform/main/docs/home.jpg" width="460" alt="Lessionato: página inicial" />
</p>

---

## 💻 Tech Stack

### **Frontend & Mobile**
![React](https://img.shields.io/badge/-React-0D1117?style=for-the-badge&logo=react&logoColor=61DAFB&labelColor=0D1117)
![React Native](https://img.shields.io/badge/-React%20Native-0D1117?style=for-the-badge&logo=react&logoColor=61DAFB&labelColor=0D1117)
![Expo](https://img.shields.io/badge/-Expo-0D1117?style=for-the-badge&logo=expo&logoColor=ffffff&labelColor=0D1117)
![TypeScript](https://img.shields.io/badge/-TypeScript-0D1117?style=for-the-badge&logo=typescript&logoColor=3178C6&labelColor=0D1117)
![JavaScript](https://img.shields.io/badge/-JavaScript-0D1117?style=for-the-badge&logo=javascript&logoColor=F7DF1E&labelColor=0D1117)
![Vite](https://img.shields.io/badge/-Vite-0D1117?style=for-the-badge&logo=vite&logoColor=646CFF&labelColor=0D1117)
![Vitest](https://img.shields.io/badge/-Vitest-0D1117?style=for-the-badge&logo=vitest&logoColor=6E9F18&labelColor=0D1117)
![CSS](https://img.shields.io/badge/-CSS-0D1117?style=for-the-badge&logo=css&logoColor=663399&labelColor=0D1117)

### **Backend**
![C# / .NET](https://img.shields.io/badge/-C%23%20%7C%20.NET%20%7C%20ASP.NET%20Core-0D1117?style=for-the-badge&logo=dotnet&logoColor=512BD4&labelColor=0D1117)
![EF Core](https://img.shields.io/badge/-Entity%20Framework%20Core-0D1117?style=for-the-badge&logo=dotnet&logoColor=512BD4&labelColor=0D1117)
![Node.js](https://img.shields.io/badge/-Node.js-0D1117?style=for-the-badge&logo=node.js&logoColor=5FA04E&labelColor=0D1117)
![Express](https://img.shields.io/badge/-Express-0D1117?style=for-the-badge&logo=express&logoColor=ffffff&labelColor=0D1117)
![Python](https://img.shields.io/badge/-Python-0D1117?style=for-the-badge&logo=python&logoColor=3776AB&labelColor=0D1117)
![discord.py](https://img.shields.io/badge/-discord.py-0D1117?style=for-the-badge&logo=discord&logoColor=5865F2&labelColor=0D1117)
![Tesseract OCR](https://img.shields.io/badge/-Tesseract%20OCR-0D1117?style=for-the-badge&logo=googlelens&logoColor=4285F4&labelColor=0D1117)
![JWT](https://img.shields.io/badge/-JWT-0D1117?style=for-the-badge&logo=jsonwebtokens&logoColor=ffffff&labelColor=0D1117)

### **Bancos de Dados**
![PostgreSQL](https://img.shields.io/badge/-PostgreSQL-0D1117?style=for-the-badge&logo=postgresql&logoColor=4169E1&labelColor=0D1117)
![MySQL](https://img.shields.io/badge/-MySQL-0D1117?style=for-the-badge&logo=mysql&logoColor=4479A1&labelColor=0D1117)
![SQLite](https://img.shields.io/badge/-SQLite-0D1117?style=for-the-badge&logo=sqlite&logoColor=74C0FC&labelColor=0D1117)
![MongoDB](https://img.shields.io/badge/-MongoDB-0D1117?style=for-the-badge&logo=mongodb&logoColor=47A248&labelColor=0D1117)

### **Infraestrutura & Ferramentas**
![Linux](https://img.shields.io/badge/-Linux-0D1117?style=for-the-badge&logo=linux&logoColor=FCC624&labelColor=0D1117)
![Nginx](https://img.shields.io/badge/-Nginx-0D1117?style=for-the-badge&logo=nginx&logoColor=009639&labelColor=0D1117)
![PM2](https://img.shields.io/badge/-PM2-0D1117?style=for-the-badge&logo=pm2&logoColor=ffffff&labelColor=0D1117)
![Let's Encrypt](https://img.shields.io/badge/-SSL%2FTLS-0D1117?style=for-the-badge&logo=letsencrypt&logoColor=ffffff&labelColor=0D1117)
![Docker](https://img.shields.io/badge/-Docker-0D1117?style=for-the-badge&logo=docker&logoColor=2496ED&labelColor=0D1117)
![Caddy](https://img.shields.io/badge/-Caddy-0D1117?style=for-the-badge&logo=caddy&logoColor=1F88C0&labelColor=0D1117)
![Cloudflare](https://img.shields.io/badge/-Cloudflare-0D1117?style=for-the-badge&logo=cloudflare&logoColor=F38020&labelColor=0D1117)
![Git](https://img.shields.io/badge/-Git-0D1117?style=for-the-badge&logo=git&logoColor=F05032&labelColor=0D1117)

---

## 📊 Estatísticas do GitHub

<div align="center">
  <img width="58%" src="https://streak-stats.demolab.com/?user=araujogbs&background=0D1117&ring=FF91A4&fire=FF91A4&currStreakLabel=FF91A4&sideLabels=C9D1D9&dates=8B949E&currStreakNum=C9D1D9&sideNums=C9D1D9&stroke=30363D&hide_border=true&locale=pt_BR&disable_animations=true" alt="Sequência de contribuições de Gabriel Araújo" />
  <img width="40%" src="https://github-profile-summary-cards.vercel.app/api/cards/most-commit-language?username=araujogbs&theme=github_dark" alt="Linguagens mais usadas" />
</div>

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=ff91a4&height=100&section=footer"/>
