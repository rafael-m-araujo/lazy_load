# 📝 Prática de Performance: Lazy Load com Intersection Observer

Este é um projeto prático desenvolvido com o objetivo de estudar e fixar conceitos de **performance web**, **manipulação de DOM** e o uso da API nativa **Intersection Observer**. O projeto foi criado a partir de um desafio de curso para aplicar os conhecimentos na prática.

A técnica de **Lazy Loading** (carregamento tardio) implementada aqui evita que o navegador baixe imagens pesadas logo no primeiro carregamento da página, economizando dados do usuário e acelerando a velocidade do site.

## 🎯 Objetivos do Aprendizado

Durante o desenvolvimento deste projeto, pratiquei:
* 🧠 **Uso do Intersection Observer:** Substituição dos antigos eventos de `scroll` (que prejudicam o desempenho) por uma API moderna e nativa para detectar elementos na tela.
* ⚡ **Efeito Blur-up (Placeholder):** Exibição de uma miniatura ultra leve de 10px de largura com desfoque (*blur*) enquanto a imagem de alta resolução não é carregada.
* 🏷️ **Atributos Data-\*:** Uso do atributo customizado `data-src` no HTML para gerenciar URLs dinamicamente via JavaScript.
* 📱 **Responsividade com CSS:** Correção de problemas comuns de layout fixo, tornando os containers e imagens adaptáveis para qualquer tamanho de tela.

## 🛠️ Tecnologias e Conceitos Aplicados

* **HTML5:** Estrutura e uso de atributos `data-src`.
* **CSS3:** Flexibilidade com `max-width`, controle de altura mínima (`min-height`) para evitar quebras de layout e transição de efeitos visuais (`filter: blur`).
* **JavaScript Puro (Vanilla):** Lógica de intersecção, manipulação do dataset e otimização de observadores (`unobserve`).

## ⚙️ Como funciona a lógica na prática?

1. **Estado Inicial (HTML):** A imagem carrega uma versão minúscula (`w=10`) no `src` e fica com um efeito de desfoque no CSS. A URL da imagem em alta resolução fica "escondida" no `data-src`.
2. **O Monitoramento (JS):** O `IntersectionObserver` monitora a rolagem. Quando a imagem chega a 200px de distância da tela (`rootMargin`), o JavaScript entra em ação.
3. **A Troca (JS):** O script joga o valor do `data-src` para o `src`.
4. **O Resultado (CSS):** Assim que o link muda, o efeito de desfoque é removido suavemente através de uma transição CSS, revelando a imagem nítida.

## 📂 Estrutura de Arquivos

```text
├── css/
│   └── styles.css      # Estilos e efeitos de transição (blur)
├── js/
│   └── scripts.js     # Lógica do Intersection Observer
└── index.html         # Estrutura com as imagens e atributos data
```

---
⭐ *Projeto focado estritamente em estudos e evolução de habilidades em Front-End.*
