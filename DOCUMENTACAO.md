# Documentação — Landing Page: Instituto de Direito Aplicado

## Visão Geral

Arquivo único: `index.html`
Página de vendas (landing page) para o curso **"Servidores Públicos na Prática"**, ministrado por **Lourenço Grieco Neto** pelo Instituto de Direito Aplicado.

---

## Paleta de Cores (CSS Variables)

| Variável       | Valor     | Uso                          |
|----------------|-----------|------------------------------|
| `--orange`     | `#f4722b` | Cor principal, títulos, CTAs |
| `--navy`       | `#1d3557` | Cor secundária, bordas       |
| `--light-gray` | `#f1f5f9` | Fundo de seções alternadas   |

---

## Estrutura de Seções

### 1. Navbar (`<nav>`)
- Logo: "Instituto de Direito Aplicado" (link âncora `#`)
- Links de navegação: Sobre, Curso, Benefícios, FAQ
- Botão CTA: **"Comprar Agora"** → `#cta`
- Comportamento: `position: sticky; top: 0` (fixo ao rolar)
- Responsivo: links ocultados abaixo de 900px

---

### 2. Hero (`#hero`)
- Fundo: `--orange`
- Badge: "🎓 Aprenda Direito Aplicado na Prática"
- Título principal: **"Domine Servidores Públicos na Prática"**
- Subtítulo: referência ao professor Lourenço Grieco Neto
- Dois botões:
  - `btn-primary` → **"Comprar Curso (R$ 999)"** → `#cta`
  - `btn-secondary` → **"Conhecer o Curso"** → `#curso`

---

### 3. Quem Ensina (`#sobre`)
- Fundo: branco
- Grid de 2 colunas: foto (placeholder cinza) + informações do professor
- **Professor:** Lourenço Grieco Neto
- **Credenciais:**
  - Mestre em Direito Constitucional pela PUC-SP
  - Professor Titular — Faculdade de São Paulo
  - 10+ anos em Direito Público
  - Autor de obra jurídica sobre políticas públicas e inclusão
- Lista de credenciais com ícone `✓` (`.check-list`)

---

### 4. O Desafio do Advogado (`#desafio`)
- Fundo: `--light-gray`
- Grid de 2 colunas com cards de borda esquerda (`--navy`):
  - **O Problema** (ícone `✗` vermelho): falta de teses práticas e dificuldade de identificar oportunidades
  - **A Solução** (ícone `✓`): aprender teses que funcionam no judiciário

---

### 5. Curso (`#curso`)
- Fundo: branco
- Grid 2 colunas: capa decorativa (emoji 📚 com gradiente) + descrição do curso
- **Estatísticas do curso:**
  - Duração Total: 12+ horas
  - Aulas: 18 módulos
  - Acesso: Vitalício
- **Módulos listados (7 cards em grid 4 colunas):**

| # | Módulo | Descrição resumida |
|---|--------|-------------------|
| 1 | Fundamentos do Servidor | Estabilidade, direitos e garantias |
| 2 | Vencimentos, Gratificações e Adicionais | Diferenciais e integração no salário |
| 3 | Afastamentos e "Efetivo Exercício" | Tese de manutenção de benefícios |
| 4 | Tempo de Serviço e Aposentadoria | Contagem de tempo e acúmulo |
| 5 | Demissão e Direitos Garantidos | Garantias constitucionais e defesa |
| 6 | Danos Morais e Reparação | Quantificação e argumentação |
| 7 | Teses Específicas + Casos Práticos | Jurisprudência e decisões reais |

---

### 6. Benefícios (`#beneficios`)
- Fundo: gradiente laranja suave (`#fef3ee → #fde8df`)
- Grid de 5 itens (ícone + título + descrição):

| Ícone | Título | Descrição |
|-------|--------|-----------|
| 🎯 | Identifique Oportunidades | Reconhecer teses vencedoras |
| 📊 | Estruture Argumentação | Teses sólidas no judiciário |
| 💼 | Capacite Clientes | Confiança do cliente |
| 💰 | Aumente Rentabilidade | Nicho de alta demanda |
| ⚖️ | Decisões Judiciais | Jurisprudência atualizada |
| 🚀 | Escale seu Escritório | Serviços premium |

---

### 7. Depoimentos (`#depoimentos`)
- Fundo: branco
- Grid de 3 colunas com cards de borda esquerda (`--navy`)
- **Depoimentos:**
  - **Marina S.** (Advogada, São Paulo) — estruturou tese em caso de afastamento
  - **Carlos P.** (Sócio de Escritório, Minas Gerais) — mudança de abordagem com clientes
  - **Amanda L.** (Advogada Autônoma, Rio de Janeiro) — dois novos clientes por indicação

---

### 8. FAQ (`#faq`)
- Fundo: `--light-gray`
- 6 perguntas com acordeão (JS: `toggleFaq`)
- Comportamento: abre/fecha com transição CSS (`max-height`); apenas um item aberto por vez

| Pergunta | Resposta resumida |
|----------|------------------|
| Quanto tempo leva para completar? | 12+ horas; ritmo próprio; 30-60 dias |
| Preciso ter experiência em direito público? | Não; começa do zero |
| Como funciona o acesso? | Acesso exclusivo, vitalício, qualquer dispositivo |
| Qual é a política de reembolso? | 7 dias de garantia, 100% devolvido |
| Os exemplos são casos reais? | Sim, todos baseados em jurisprudência vigente |
| Posso usar para captar clientes? | Sim, esse é o objetivo |

---

### 9. CTA — Chamada para Ação (`#cta`)
- Fundo: `--orange`
- Título: **"Comece Agora"**
- Subtítulo: "Invista em você e domine um nicho rentável do direito"
- Preço em destaque: **R$ 999,00**
- Botão: **"Comprar Curso Completo"** (link `#`)
- Garantias: Acesso vitalício · Atualizações incluídas · 7 dias de garantia

---

### 10. Footer
- Fundo: `--navy`
- Texto: © 2024 Instituto de Direito Aplicado — Lourenço Grieco Neto
- Links: Política de Privacidade | Termos de Uso (ambos `href="#"` — não implementados)

---

## JavaScript

Função única `toggleFaq(btn)`:
- Fecha todos os `.faq-item.open`
- Abre o item clicado (se estava fechado)
- A animação é feita via CSS com `max-height` e `padding` em transição

---

## Responsividade

Breakpoint em `900px`:
- Navbar: padding reduzido; links ocultos
- Hero: padding reduzido; título reduzido para `2rem`
- Grids de 2 colunas → 1 coluna (instructor, desafio, curso)
- Módulos: 4 colunas → 2 colunas
- Benefícios: 5 colunas → 2 colunas
- Depoimentos: 3 colunas → 1 coluna

---

## Itens Pendentes / Placeholders

- Foto do professor: `div.instructor-photo` (retângulo cinza `#d1d5db`)
- Link "Comprar Curso Completo" no CTA: `href="#"` (não aponta para checkout)
- Links do footer (Privacidade, Termos): `href="#"` (páginas não criadas)
- Menu mobile: `.nav-links` oculto em mobile, sem hambúrguer implementado
