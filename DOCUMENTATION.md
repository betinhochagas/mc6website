# Documentação Técnica - Site Corporativo MC6

**Versão:** 2.1 (Hero Section Rework)
**Data:** 14 de Agosto de 2025

## 1. Visão Geral do Projeto

Este documento detalha a estrutura técnica e os componentes do site institucional da MC6 Corp. O projeto foi desenvolvido com o objetivo de criar uma presença digital moderna, tecnologicamente avançada e otimizada para a conversão de clientes B2B, refletindo a expertise da empresa em engenharia e monitoramento de redes.

O design adota uma estética "dark mode", associada ao universo da tecnologia, com animações e efeitos interativos que criam uma experiência de usuário imersiva e profissional.

---

## 2. Stack de Tecnologias (Frontend)

O site foi construído utilizando tecnologias web modernas, focadas em performance, flexibilidade e facilidade de manutenção.

- **HTML5:** Estrutura semântica para máxima acessibilidade e SEO.
- **Tailwind CSS v3:** Framework CSS utility-first para a criação rápida de um design customizado e responsivo.
- **JavaScript (ES6+):** Utilizado para interatividade, animações e manipulação do DOM.
- **AOS (Animate on Scroll):** Biblioteca para animações de elementos que surgem na tela durante a rolagem.
- **Font Awesome 6:** Biblioteca de ícones para elementos visuais.

---

## 3. Estrutura de Arquivos

```
/
|-- index.html              # O arquivo principal que contém todo o site.
|-- assets/
|   |-- clients/
|   |   |-- bk.webp
|   |   |-- ... (todos os outros logos de clientes)
|-- DOCUMENTATION.md        # Este arquivo.
|-- ROADMAP.md              # Arquivo com o roadmap de features.
```

---

## 4. Features e Efeitos Implementados

### 4.1. Design "Dark Mode"

O layout utiliza um tema escuro (`#0d1117`) com destaques em azul (`#1f6feb`) para criar uma estética sofisticada e tecnológica.

### 4.2. Hero Section Robusta

- **Layout Dividido:** A seção utiliza um layout de duas colunas para melhor organização visual, com texto à esquerda e uma imagem de destaque à direita.
- **Efeito de Digitação:** O título principal é renderizado dinamicamente via JavaScript para simular um efeito de digitação.
- **"Trust Badges" Animados:** Cards de métricas com ícones e um efeito de "scan" (linha de luz) para reforçar a credibilidade.
- **Imagem com Efeito "Glow":** A imagem principal possui uma animação de brilho pulsante para destacá-la.

### 4.3. Animações e Efeitos Visuais

- **Animações de Rolagem (AOS.js):** Elementos surgem na tela com animações suaves (`fade-up`, `zoom-in`).
- **Efeitos Parallax:** As seções "Diferenciais" e "Cases de Sucesso" utilizam `background-attachment: fixed;` para criar um efeito de profundidade.
- **Cards Interativos:** Cards de serviço com efeito de brilho no `hover`.
- **Header com Transição:** O cabeçalho transita de transparente para sólido com `backdrop-blur` durante a rolagem.

### 4.4. Acessibilidade

- Foram adicionados atributos `aria-label` em botões sem texto visível (ex: menu mobile) e tags `<label>` associadas a campos de formulário para garantir a compatibilidade com leitores de tela.

---

## 5. Como Customizar

### 5.1. Textos e Informações de Contato

Todos os textos, incluindo o endereço e informações de contato, podem ser editados diretamente no arquivo `index.html`.

### 5.2. Formulário de Contato

Os campos do formulário, incluindo as opções do menu de seleção (`<select>`), podem ser modificados na seção `<section id="contato">`.

### 5.3. Logos de Clientes

1.  Adicione o novo arquivo de imagem na pasta `assets/clients/`.
2.  Na seção `<section id="clientes">`, adicione uma nova tag `<img>` apontando para o arquivo.

### 5.4. Imagens de Fundo (Parallax)

As URLs das imagens de fundo são definidas no CSS, dentro da tag `<style>`, nas classes `.parallax-bg` e `.parallax-bg-diferenciais`.
