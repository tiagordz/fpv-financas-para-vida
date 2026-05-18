<div align="center">

# 💚 FPV — Finanças Para Vida

**Seu assistente financeiro pessoal com IA Generativa**

[![React](https://img.shields.io/badge/React_18-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)](https://supabase.com/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)](https://vitejs.dev/)

[🚀 Acessar o App](https://fpv-financas-para-vida.lovable.app) · [📖 Documentação](#-tecnologias) · [✨ Features](#-funcionalidades)

![dark mode](https://img.shields.io/badge/tema-dark%20%7C%20light-black?style=flat-square)
![mobile first](https://img.shields.io/badge/layout-mobile--first-blue?style=flat-square)
![status](https://img.shields.io/badge/status-em%20desenvolvimento-green?style=flat-square)

</div>

---

## 📌 Sobre o Projeto

O **FPV Finanças Para Vida** é uma aplicação web mobile-first que centraliza o controle financeiro pessoal em um único lugar. Com ele, você registra receitas e despesas, define metas de economia, acompanha objetivos financeiros e ainda conta com um **assistente virtual com IA** para tirar dúvidas e até registrar lançamentos por conversa.

Desenvolvido com foco em usabilidade mobile e design moderno, o FPV oferece dark mode padrão e uma experiência fluida de navegação por bottom tabs como um app nativo.

---

## ✨ Funcionalidades

### 🔐 Autenticação
- Cadastro e login com email e senha
- Login social com Google
- Verificação de email obrigatória
- Indicador de força de senha em tempo real

### 💰 Controle Financeiro
- **Lançamentos**: CRUD completo de receitas e despesas com categorias, descrição e data
- **Dashboard**: Resumo mensal (receitas, despesas, saldo), gráficos de evolução e últimas movimentações
- **Transações**: Listagem completa do mês com filtros e ordenação
- **Relatórios**: Análise por categoria com gráficos avançados de distribuição

### 🎯 Metas e Objetivos
- **Meta Global**: Limite mensal de gastos com barra de progresso e alertas (🟢 🟡 🔴)
- **Metas por Categoria**: Limites específicos por tipo de despesa (Alimentação, Lazer, etc.)
- **Meta de Economia**: Valor mensal a guardar com acompanhamento de progresso
- **Objetivos Específicos**: Metas personalizadas com valor total e valor guardado (ex: "Viagem", "Carro novo")

### 🔮 Planejamento Futuro
- Visualização de transações agendadas com data futura
- Agrupamento por mês com resumo de receitas e despesas previstas

### 📰 Notícias e Câmbio
- Resumos semanais do mercado financeiro gerados por IA (Gemini)
- Cotação USD/BRL em tempo real via Banco Central (PTAX/Olinda)
- Variação percentual com indicadores visuais de alta e queda

### 🤖 Assistente Virtual (ChatBot com IA)
- Chat com streaming em tempo real
- Consultor financeiro: responde dúvidas sobre investimentos, planejamento e finanças pessoais
- **Registro por conversa**: o assistente consegue lançar movimentações na sua conta via chat
- Suporte a Markdown e tool calling
- Powered by **Gemini AI**

### 🧮 Utilitários
- Calculadora integrada ao app
- Toggle dark / light mode
- Toast notifications para feedback de ações

---

## 🛠️ Tecnologias

| Categoria | Tecnologia |
|---|---|
| Frontend | React 18, TypeScript, Vite 5 |
| Estilização | Tailwind CSS, shadcn/ui |
| Estado e Cache | TanStack Query |
| Backend / BaaS | Lovable Cloud (Supabase) |
| Banco de Dados | PostgreSQL (via Supabase) |
| Autenticação | Supabase Auth (email + Google OAuth) |
| IA Generativa | Google Gemini |
| Edge Functions | Supabase Edge Functions (Deno) |

---

## 🗄️ Banco de Dados

Todas as tabelas possuem **RLS (Row Level Security)** ativo — cada usuário acessa apenas seus próprios dados.

| Tabela | Função |
|---|---|
| `profiles` | Dados do usuário (nome, email) |
| `movimentacoes` | Lançamentos financeiros |
| `metas_mensais` | Metas globais e por categoria |
| `objetivos_economia` | Objetivos de poupança específicos |
| `preferencias_notificacao` | Configurações de notificações |

---

## ⚡ Edge Functions

| Função | Propósito |
|---|---|
| `financial-chat` | Assistente virtual com IA (streaming) |
| `financial-news` | Geração de resumos de notícias financeiras |
| `currency-rate` | Cotação USD/BRL em tempo real |

---

## 🏗️ Arquitetura

```
fpv-financas-para-vida/
│
├── src/
│   ├── components/         # Componentes reutilizáveis (UI, gráficos, chatbot)
│   ├── pages/              # Telas principais (Dashboard, Transações, Metas...)
│   ├── hooks/              # Custom hooks (TanStack Query, autenticação)
│   ├── integrations/       # Cliente Supabase e tipos gerados
│   └── lib/                # Utilitários e helpers
│
├── supabase/
│   ├── functions/          # Edge Functions (financial-chat, financial-news, currency-rate)
│   └── migrations/         # Migrations do banco de dados
│
└── public/                 # Assets estáticos
```

---

## 🚀 Roadmap

- [x] Autenticação completa (email + Google)
- [x] CRUD de movimentações financeiras
- [x] Dashboard com gráficos e resumo mensal
- [x] Sistema de metas e objetivos
- [x] Planejamento financeiro futuro
- [x] Assistente virtual com IA + registro por conversa
- [x] Notícias financeiras geradas por IA
- [x] Cotação USD/BRL em tempo real
- [ ] Notificações de lembrete semanal por email
- [ ] Cotações EUR/BRL e BTC/BRL
- [ ] App mobile nativo (React Native / Expo)

---

## 📱 Preview

> Acesse o app em: **[fpv-financas-para-vida.lovable.app](https://fpv-financas-para-vida.lovable.app)**

O app foi desenvolvido com layout **mobile-first** e funciona perfeitamente no navegador do celular — sem precisar instalar nada.

---

## 👤 Tiago A R Resende

Feito com 💚 usando **vibe-coding** e muita vontade de aprender.

> *"Finanças para vida — não só para sobreviver, mas para construir o futuro que você quer."*

---

<div align="center">

Se esse projeto te ajudou de alguma forma, deixa uma ⭐ no repositório!

</div>
