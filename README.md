📘 Discord Landing Page – Replica (Mobile First)

Réplica da página inicial do Discord desenvolvida utilizando HTML5 e CSS3, aplicando a metodologia Mobile First e princípios de responsividade moderna.

O objetivo do projeto é praticar:

Estruturação semântica com HTML

Layout responsivo com CSS

Flexbox

Media Queries

Organização visual baseada em design system

🚀 Demonstração

Projeto desenvolvido para fins educacionais, simulando a home pública do Discord.

🛠 Tecnologias Utilizadas

HTML5

CSS3

Flexbox

Media Queries (Mobile First)

Gradients CSS

Menu hambúrguer com checkbox hack

📱 Conceito Mobile First

O projeto foi estruturado começando pelo layout para dispositivos móveis e evoluindo progressivamente para telas maiores:

/* Base: Mobile */
.hero {
  padding: 60px 20px;
}

/* Tablet */
@media (min-width: 768px) { }

/* Desktop */
@media (min-width: 1024px) { }
Estratégia aplicada:

Layout base otimizado para celulares

Escalonamento progressivo

Ajuste de tipografia proporcional

Mudança de layout de colunas via Flexbox

📂 Estrutura de Arquivos
discord-replica/
│
├── index.html
├── style.css
└── README.md
🎨 Principais Componentes
Header

Logo textual

Menu responsivo

Botão de login

Menu hambúrguer funcional (sem JavaScript)

Hero Section

Título de destaque

Texto explicativo

Botões principais com variação de estilo

Background com gradiente

Feature Sections

Blocos alternando fundo branco e cinza claro

Estrutura centralizada

Texto hierarquizado

📐 Responsividade
Breakpoint	Comportamento
< 768px	Layout em coluna
≥ 768px	Menu horizontal + botões lado a lado
≥ 1024px	Aumento de escala tipográfica e espaçamento
📎 Melhorias Futuras

Implementar imagens ilustrativas

Adicionar animações CSS

Criar footer completo

Implementar dropdown no menu

Utilizar Grid Layout

Tornar acessível (ARIA + melhores contrastes)

🎯 Objetivo Educacional

Este projeto não possui fins comerciais.
Foi desenvolvido exclusivamente para prática de front-end, responsividade e replicação visual de interfaces modernas.
