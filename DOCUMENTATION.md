# Documentação Técnica - Site Corporativo MC6

**Versão:** 2.0 (Dark Mode Tech)
**Data:** 13 de Agosto de 2025

## 1. Visão Geral do Projeto

Este documento detalha a estrutura técnica e os componentes do site institucional da MC6 Corp. O projeto foi desenvolvido com o objetivo de criar uma presença digital moderna, tecnologicamente avançada e otimizada para a conversão de clientes B2B, refletindo a expertise da empresa em engenharia e monitoramento de redes.

O design adota uma estética "dark mode", associada ao universo da tecnologia, com animações e efeitos interativos que criam uma experiência de usuário imersiva e profissional.

---

## 2. Stack de Tecnologias (Frontend)

O site foi construído utilizando tecnologias web modernas, focadas em performance, flexibilidade e facilidade de manutenção.

- **HTML5:** Estrutura semântica para máxima acessibilidade e SEO.
- **Tailwind CSS v3:** Framework CSS utility-first para a criação rápida de um design customizado e responsivo. Todo o estilo é aplicado diretamente nas classes HTML.
- **JavaScript (ES6+):** Utilizado para interatividade, animações e manipulação do DOM. O código está contido em uma tag `<script>` no final do `index.html`.
- **AOS (Animate on Scroll):** Biblioteca para animações de elementos que surgem na tela durante a rolagem.
- **Font Awesome 6:** Biblioteca de ícones para elementos visuais.

---

## 3. Estrutura de Arquivos

A estrutura do projeto é intencionalmente simples para facilitar a manutenção.

```
/
|-- index.html              # O arquivo principal que contém todo o site.
|-- assets/
|   |-- clients/
|   |   |-- bk.webp
|   |   |-- cliente-trezo.webp
|   |   |-- ... (todos os outros logos de clientes)
|   |-- (outros assets como imagens de cases, etc.)
```

- **`index.html`**: Contém todo o código HTML, CSS customizado (dentro de `<style>`) e JavaScript (dentro de `<script>`).
- **`assets/clients/`**: Diretório onde os logos dos clientes devem ser armazenados.

---

## 4. Features e Efeitos Implementados

### 4.1. Design "Dark Mode"

O layout utiliza um tema escuro (`#0d1117`) para criar uma estética sofisticada e tecnológica. As cores de destaque são tons de azul (`#1f6feb`), remetendo a luzes de LED e interfaces de software.

### 4.2. Efeito de Digitação (Hero Section)

O título principal é renderizado dinamicamente via JavaScript para simular um efeito de digitação, com um cursor piscando. A lógica está na função `typeWriter()` no script principal.

### 4.3. Animações de Rolagem (AOS.js)

Elementos como seções, cards e textos utilizam a biblioteca `AOS.js` para aparecerem na tela com animações suaves (`fade-up`, `zoom-in`, etc.), tornando a navegação mais fluida.

### 4.4. Efeitos Parallax

- **Seção "Diferenciais":** Utiliza a propriedade `background-attachment: fixed;` para criar um efeito de parallax, onde o conteúdo rola sobre um fundo estático.
- **Seção "Cases de Sucesso":** Aplica o mesmo efeito com uma imagem de fundo diferente, criando profundidade e dinamismo.

### 4.5. Cards de Serviço Interativos

Os cards na seção de serviços possuem um efeito de brilho que os percorre no `hover` e uma borda que se ilumina, incentivando a interação do usuário.

### 4.6. Header com Transição

O cabeçalho começa transparente sobre a Hero Section e, com a rolagem da página, suavemente se torna sólido e com um efeito de `backdrop-blur` para manter a legibilidade.

---

## 5. Como Customizar

### 5.1. Textos

Todos os textos (títulos, parágrafos, itens de menu) podem ser editados diretamente no arquivo `index.html`.

### 5.2. Logos de Clientes

Para adicionar ou alterar os logos dos clientes:

1.  Adicione o novo arquivo de imagem (preferencialmente `.webp` ou `.png`) na pasta `assets/clients/`.
2.  Na seção `<section id="clientes">`, edite ou adicione uma tag `<img>` apontando para o novo arquivo. Ex: `<img src="assets/clients/novo-cliente.webp" ...>`.

### 5.3. Imagens de Fundo (Parallax)

As imagens de fundo das seções parallax são definidas no CSS, dentro da tag `<style>`. Para alterá-las, modifique as URLs nas classes `.parallax-bg` e `.parallax-bg-diferenciais`.

### 5.4. Informações de Contato

Os dados de contato (telefone, e-mail, WhatsApp) estão na seção `<section id="contato">`. Edite o texto diretamente no HTML.
