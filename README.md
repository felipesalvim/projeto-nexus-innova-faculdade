# Website Institucional - Nexus Innova

<p align="center">
<img src="images/captura-site.png" alt="Banner do Projeto Nexus Innova" width="1000"/>
</p>

## 📋 Índice

- [🎯 Sobre o Projeto](#-sobre-o-projeto)
- [🚀 Tecnologias Utilizadas](#-tecnologias-utilizadas)
- [📁 Estrutura do Projeto](#-estrutura-do-projeto)
- [⚡ Funcionalidades](#-funcionalidades)
- [🏗️ Arquitetura e Padrões](#️-arquitetura-e-padrões)
- [🛠️ Instalação e Configuração](#️-instalação-e-configuração)
- [💻 Uso](#-uso)
- [🔍 SEO e Analytics](#-seo-e-analytics)
- [♿ Acessibilidade](#-acessibilidade)
- [🔒 Segurança](#-segurança)
- [🤝 Contribuindo](#-contribuindo)
- [📄 Licença](#-licença)
- [📞 Contato](#-contato)

## 🎯 Sobre o Projeto

O **"Nexus Innova"** é um website institucional desenvolvido como parte de um projeto de extensão acadêmico da **Faculdade CDL**. Nascido no ambiente acadêmico, o projeto atua como um laboratório prático, unindo a teoria à prática de mercado para simular uma empresa de tecnologia real.

Foi construído com **HTML5**, **CSS3** e **JavaScript puro (Vanilla JS)**, seguindo princípios modernos de desenvolvimento web, com foco em performance, acessibilidade e experiência do usuário.

### Objetivos

- Apresentar os "serviços" do projeto de forma clara e profissional.
- Criar um "portfólio interativo" de projetos desenvolvidos.
- Estabelecer um "canal de comunicação" eficiente com potenciais clientes e parceiros.
- Compartilhar conhecimento através de um "blog técnico".
- Gerar leads qualificados através de "materiais educativos (e-books)" e "quiz interativo".

## 🚀 Tecnologias Utilizadas

### Frontend

- **HTML5**: Estrutura "semântica" e acessível.
- **CSS3**: Estilização moderna com "variáveis CSS", "Grid" e "Flexbox".
- **JavaScript (ES6+)**: Lógica de aplicação "sem frameworks" para injeção de componentes (header/footer) e interatividade.
- **AOS (Animate On Scroll)**: Animações suaves durante o scroll.
- **Font Awesome**: Biblioteca de ícones.

### Backend

- **PHP 7.4+**: Processamento de formulários (especificamente para a página de detalhes do projeto).
- **MySQL**: Armazenamento de dados de contato oriundos dos projetos.

### Analytics & Marketing

- **Google Tag Manager (GTM)**: Gerenciamento centralizado de tags de marketing e análise.
- **Google Analytics (GA4)**: Monitoramento de tráfego e comportamento do usuário.

## 📁 Estrutura do Projeto

A arquitetura do projeto evoluiu para um modelo híbrido. A página inicial, blog e portfólio utilizam o `data.js` para renderização dinâmica, enquanto as páginas de serviço são **estáticas** (`.html` individuais) para melhor performance, SEO individualizado e foco na conversão de e-books.

nexus-innova/ │ ├── index.html # Página principal (Home) ├── blog.html # Listagem de posts do blog │ ├── bi-ux.html # Página estática do serviço de BI e UX ├── full-stack.html # Página estática do serviço de Full Stack ├── qa.html # Página estática do serviço de QA ├── suporte-sites.html # Página estática do serviço de Suporte a Sites ├── suporte-juridico.html # Página estática do serviço Jurídico ├── automacao.html # Página estática do serviço de Automação │ ├── style.css # Estilos globais ├── script.js # Lógica principal (injeção de header/footer, chatbot, quiz, etc.) ├── data.js # Dados centralizados (para blog, equipe, chatbot, etc.) ├── salvar_contato.php # Backend para processamento de formulários de projeto │ ├── blog/ │ └── post.html # Template de post individual (dinâmico) │ ├── projetos/ │ └── projeto.html # Template de projeto individual (dinâmico) │ ├── images/ # Imagens globais (logos, hero, favicons) │ └── membros/ # Fotos da equipe │ ├── blog/images/ # Imagens dos posts do blog │ ├── projetos/images/ # Imagens dos projetos │ ├── covers/ # Imagens das capas dos e-books │ └── documentos/ ├── ebook-bi-ux.pdf # Exemplo de E-book └── videos/ # Vídeos locais (atualmente comentados no código)

## ⚡ Funcionalidades

1.  **"Navegação Responsiva"**
    - Menu hambúrguer para dispositivos móveis.
    - Header fixo com efeito de transparência ao rolar.

2.  **"Páginas de Serviço Estáticas (Foco em Conversão)"**
    - Seis páginas de serviço individuais (`bi-ux.html`, `full-stack.html`, etc.) para melhor indexação (SEO).
    - Layout otimizado para conversão com destaque para download de **e-books**.
    - Seção de vídeo preparada (código comentado) para futura ativação com suporte a vídeos verticais (formato mobile/reels).

3.  **"Sistema de Blog (Dinâmico)"**
    - Renderização de posts a partir do `data.js`.
    - Listagem de posts com busca em tempo real.
    - Posts individuais com SEO otimizado e dados estruturados (JSON-LD).

4.  **"Portfólio de Projetos (Dinâmico)"**
    - Renderização de projetos a partir do `data.js`.
    - Detalhamento completo com seções "Desafio", "Solução" e "Resultados".
    - Formulário de contato "Interessado neste projeto?" com validação e backend em PHP.

5.  **"Quiz Interativo de Contato"**
    - Sistema de qualificação de leads por etapas na seção de contato.
    - Redirecionamento automático para WhatsApp com mensagens contextualizadas.

6.  **"Chatbot Flutuante e WhatsApp"**
    - Assistente virtual com fluxo conversacional definido no `data.js`.
    - Botão flutuante de WhatsApp acessível em todas as páginas.

7.  **"Componentes de Segurança e Performance"**
    - Formulários com validação *client-side* (JavaScript).
    - Proteção contra "SQL Injection" no *backend* (PHP).
    - Carregamento otimizado de imagens e scripts.

## 🏗️ Arquitetura e Padrões

### Princípios de Design

- **"DRY (Don't Repeat Yourself)"**
    - Componentes reutilizáveis (Header, Footer, Botão WhatsApp) são injetados em todas as páginas via `script.js`.
    - Dados para seções dinâmicas (blog, equipe, chatbot, projetos) são centralizados em `data.js`.
- **"Separation of Concerns"**
    - **HTML** para estrutura semântica.
    - **CSS** para apresentação visual.
    - **JavaScript** para comportamento e interatividade.
    - **PHP** para lógica de servidor.
- **"Mobile-First"**
    - Design responsivo com *breakpoints* estratégicos.
    - Imagens otimizadas com `loading="lazy"`.

## 🛠️ Instalação e Configuração

### Pré-requisitos

- Servidor web (Apache, Nginx, ou um plugin como "Live Server" do VS Code para desenvolvimento local).
- PHP 7.4 ou superior (Necessário *apenas* para o formulário da página de projeto).
- MySQL 5.7 ou superior (Necessário *apenas* para o formulário da página de projeto).

### Configuração do Banco de Dados (Opcional)

Este passo é necessário apenas para o formulário "Interessado neste projeto?" nas páginas de detalhes do projeto.

1.  Crie o banco de dados:
    ```sql
    CREATE DATABASE nexus_innova_db CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
    ```
2.  Crie a tabela de contatos:
    ```sql
    USE nexus_innova_db;

    CREATE TABLE contatos_projetos (
        id INT AUTO_INCREMENT PRIMARY KEY,
        nome VARCHAR(255) NOT NULL,
        telefone VARCHAR(20),
        email VARCHAR(255) NOT NULL,
        projeto_id VARCHAR(100) NOT NULL,
        data_contato TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
        INDEX idx_email (email),
        INDEX idx_projeto (projeto_id)
    ) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci;
    ```
3.  Configure as credenciais em `salvar_contato.php`:
    ```php
    $servername = "localhost";
    $username = "seu_usuario";
    $password = "sua_senha";
    $dbname = "nexus_innova_db";
    ```

## 💻 Uso

### Adicionando Novo Post ou Projeto (Dinâmico)

Edite o arquivo `data.js` e adicione novos objetos aos arrays `blogPosts` ou `highlightedProjects`. O sistema renderizará automaticamente o conteúdo na Home, Blog e páginas de detalhes.

### Editando uma Página de Serviço (Estático)

Para editar uma página de serviço (ex: `bi-ux.html`), **edite o arquivo HTML correspondente diretamente**. O conteúdo (texto, links de e-book, vídeos) é gerenciado dentro do próprio arquivo HTML para facilitar a manutenção de SEO específico e conversão.

## 🔍 SEO e Analytics

- **"Meta Tags Otimizadas"**: Título, descrição, Open Graph e Twitter Cards configurados individualmente para cada página estática.
- **"Analytics"**: Integração completa com Google Tag Manager (GTM) e Google Analytics 4 (GA4) para monitoramento de tráfego.

## 🔒 Segurança

- **"Backend (PHP)"**: Uso de "Prepared Statements" (`bind_param`) em `salvar_contato.php` para proteção total contra SQL Injection.
- **"Frontend"**: Validação de formulários no lado do cliente para feedback imediato ao usuário.

## 🤝 Contribuindo

Contribuições são bem-vindas!

1.  **"Fork"** o projeto
2.  Crie uma **"Branch"** para sua feature (`git checkout -b feature/NovaFuncionalidade`)
3.  **"Commit"** suas mudanças (`git commit -m 'Adiciona nova funcionalidade'`)
4.  **"Push"** para a branch (`git push origin feature/NovaFuncionalidade`)
5.  Abra um **"Pull Request"**

## 📄 Licença

Este projeto é parte integrante do projeto de extensão **"Nexus Innova"** da Faculdade CDL.

## 📞 Contato

**Nexus Innova**

- **Repositório Github:** [https://github.com/felipesalvim/projeto-nexus-innova](https://github.com/felipesalvim/projeto-nexus-innova)
- **Website:** [https://www.nexusinnova.com.br](https://www.nexusinnova.com.br)
- **Email:** contato@nexusinnova.com.br
- **Instagram:** @nexus_innova

-----

*Desenvolvido com 💚 pela equipe Nexus Innova*
