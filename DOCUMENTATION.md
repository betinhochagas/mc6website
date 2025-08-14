Documentação Técnica - Site Corporativo MC6
Versão: 3.0 (Implementação de Tema Claro/Escuro)
Data: 14 de Agosto de 2025

1. Visão Geral do Projeto
Este documento detalha a estrutura técnica e os componentes do site institucional da MC6 Corp. O projeto foi desenvolvido com o objetivo de criar uma presença digital moderna, tecnologicamente avançada e otimizada para a conversão de clientes B2B.

O design adota uma estética "dark mode" como padrão, mas agora inclui um sistema de tema claro/escuro completo, permitindo que o usuário escolha sua preferência. Ambos os temas mantêm as animações e efeitos interativos que criam uma experiência de usuário imersiva e profissional.

2. Stack de Tecnologias (Frontend)
HTML5: Estrutura semântica para máxima acessibilidade e SEO.

CSS3 (com Variáveis/Custom Properties): A arquitetura de temas é construída sobre variáveis CSS, permitindo uma troca de paleta de cores eficiente e de fácil manutenção.

Tailwind CSS v3: Framework CSS utility-first para a criação rápida de um design customizado e responsivo.

JavaScript (ES6+): Utilizado para interatividade, animações, manipulação do DOM e gerenciamento do estado do tema.

AOS (Animate on Scroll): Biblioteca para animações de elementos que surgem na tela durante a rolagem.

Font Awesome 6: Biblioteca de ícones para elementos visuais.

3. Estrutura de Arquivos
/
|-- index.html              # O arquivo principal que contém todo o site.
|-- assets/
|   |-- clients/
|   |   |-- ... (logos de clientes em formato .webp)
|-- DOCUMENTATION.md        # Este arquivo.
|-- ROADMAP.md              # Arquivo com o roadmap de features.

4. Features e Efeitos Implementados
4.1. Sistema de Tema (Claro/Escuro)
Implementação com Variáveis CSS: O núcleo do sistema de temas reside na definição de variáveis CSS (--bg-primary, --text-primary, etc.) no seletor :root (para o tema escuro padrão) e sua redefinição na classe .theme-light.

Controle via JavaScript: Um script gerencia a adição/remoção da classe .theme-light na tag <body>, controla o ícone do botão de alternância e salva a preferência do usuário no localStorage.

Preferência do Sistema: Na primeira visita, o site detecta e aplica o tema preferido do sistema operacional do usuário (claro ou escuro).

4.2. Hero Section Robusta
Layout Dividido: Layout de duas colunas com texto à esquerda e imagem à direita.

Efeito de Digitação: O título principal é renderizado dinamicamente via JavaScript.

"Trust Badges" Animados: Cards de métricas com ícones e um efeito de "scan".

Imagem com Efeito "Glow": A imagem principal possui uma animação de brilho pulsante que se adapta ao tema.

4.3. Animações e Efeitos Visuais
Animações de Rolagem (AOS.js): Elementos surgem na tela com animações suaves.

Efeito Parallax Responsivo: A seção "Diferenciais" utiliza background-attachment: fixed; em desktops. Uma media query desativa este efeito em telas com menos de 768px de largura, trocando para background-attachment: scroll; para garantir a correta visualização e performance em dispositivos móveis.

Cards Interativos: Cards de serviço com efeito de brilho e sombra no hover.

Header com Transição: O cabeçalho transita de transparente para sólido com backdrop-blur durante a rolagem.

4.4. Acessibilidade
Atributos aria-label em botões sem texto visível.

Estrutura de formulário com tags <label> associadas (mesmo que sr-only).

5. Como Customizar
5.1. Cores dos Temas
Para alterar as cores, edite as variáveis CSS no topo da tag <style> no index.html:

Tema Escuro: Modifique as variáveis dentro do seletor :root { ... }.

Tema Claro: Modifique as variáveis dentro do seletor .theme-light { ... }.

5.2. Textos e Informações de Contato
Todos os textos podem ser editados diretamente no index.html.

5.3. Logos de Clientes
Adicione o novo arquivo de imagem (preferencialmente .webp) na pasta assets/clients/.

Na seção <section id="clientes">, duplique um dos <div> com a classe client-logo-bg e atualize o src da imagem.

5.4. Imagens de Fundo (Parallax)
A URL da imagem de fundo é definida no CSS, na classe .parallax-bg.
