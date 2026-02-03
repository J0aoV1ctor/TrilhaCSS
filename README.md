# 📺 Clone de Layout do YouTube com CSS Grid

Este projeto demonstra como construir um **layout inspirado na página inicial do YouTube** utilizando **CSS Grid Layout**, com foco em organização, responsividade e boas práticas de front-end.

O objetivo é **entender e aplicar Grid Layout na prática**, criando uma estrutura moderna composta por **header fixo**, **sidebar lateral** e **grid responsivo de vídeos**.

---

## 🧠 Visão Geral do Layout

O layout é dividido em **três grandes áreas**:

1. **Header (topo)**
   Contém logo, barra de busca e ícones.

2. **Sidebar (menu lateral)**
   Menu fixo à esquerda com links de navegação.

3. **Conteúdo principal (grid de vídeos)**
   Área principal com cards de vídeos organizados automaticamente conforme o tamanho da tela.

Tudo isso é controlado com **CSS Grid**, sem frameworks externos.

---

## 🗂️ Estrutura de Pastas Sugerida

```text
📁 projeto-youtube-grid
├── index.html
├── style.css
└── README.md
```

Essa estrutura simples facilita o aprendizado e manutenção do código.

---

## 🧱 Estrutura HTML

A base do layout utiliza elementos semânticos do HTML5:

* `<header>` → topo da página
* `<aside>` → menu lateral
* `<main>` → conteúdo principal

### Exemplo simplificado:

```html
<body class="app">
  <header class="header">
    <div class="logo">YouTube</div>
    <input type="text" placeholder="Pesquisar">
    <div class="icons">⚙️</div>
  </header>

  <aside class="sidebar">
    <ul>
      <li>Início</li>
      <li>Explorar</li>
      <li>Inscrições</li>
    </ul>
  </aside>

  <main class="videos">
    <div class="video-card"></div>
    <div class="video-card"></div>
    <div class="video-card"></div>
  </main>
</body>
```

---

## 📐 Grid Principal (Layout Geral)

O layout principal usa **Grid Template Areas**, facilitando a leitura e manutenção:

```css
body.app {
  display: grid;
  grid-template-columns: 240px 1fr;
  grid-template-rows: 56px 1fr;
  grid-template-areas:
    "header header"
    "sidebar videos";
  height: 100vh;
}
```

### 🎯 O que isso significa?

* Sidebar fixa com `240px`
* Conteúdo ocupa o restante da tela
* Header ocupa toda a largura

---

## 🧩 Áreas do Layout

```css
.header {
  grid-area: header;
}

.sidebar {
  grid-area: sidebar;
}

.videos {
  grid-area: videos;
}
```

Cada seção é posicionada diretamente pelo Grid, sem `float` ou `position`.

---

## 🎥 Grid de Vídeos (Responsivo)

O grid de vídeos é totalmente fluido e se adapta automaticamente ao tamanho da tela:

```css
.videos {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
  gap: 24px;
}
```

### 🪄 Comportamento automático

| Tela           | Colunas |
| -------------- | ------- |
| Desktop grande | 4–5     |
| Notebook       | 3–4     |
| Tablet         | 2       |
| Mobile         | 1       |

Sem media queries extras.

---

## 📦 Card de Vídeo

Cada vídeo é representado por um card simples:

```css
.video-card {
  height: 230px;
  background: #e5e7eb;
  border-radius: 12px;
}
```

### Simulação de thumbnail:

```css
.video-card::before {
  content: "";
  height: 160px;
  background: #9ca3af;
  border-radius: 12px;
  display: block;
}
```

---

## 📱 Responsividade (Mobile)

Em telas menores, a sidebar é ocultada para priorizar o conteúdo:

```css
@media (max-width: 768px) {
  body.app {
    grid-template-columns: 1fr;
    grid-template-areas:
      "header"
      "videos";
  }

  .sidebar {
    display: none;
  }
}
```

---

## ✅ Boas Práticas Aplicadas

* ✔ HTML semântico
* ✔ CSS Grid moderno
* ✔ Layout responsivo
* ✔ Código limpo e escalável
* ✔ Fácil adaptação para React / Vue

---

## 🚀 Próximos Passos (Ideias)

* 🎨 Tema dark (igual YouTube)
* ⚛️ Transformar em componentes React
* 🔄 Consumir API de vídeos
* 🧩 Criar componente real de VideoCard
* 📱 Sidebar colapsável

---

## 🧑‍💻 Autor

Projeto criado para fins educacionais, focado em **aprendizado prático de CSS Grid Layout**.

Se quiser evoluir esse projeto, adaptar para framework ou deixar ainda mais fiel ao YouTube, é só continuar 🚀
