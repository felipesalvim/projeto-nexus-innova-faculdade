Excelente pergunta. Analisei a estrutura de arquivos da sua imagem (`image_09658c.png`) com cuidado.

Antes de te entregar o README final, vamos fazer a **limpeza** que você sugeriu. Sim, existem arquivos que **devem** ser excluídos, principalmente por questões de segurança.

### 🗑️ O que você deve EXCLUIR (Limpeza)

Esses arquivos foram scripts utilitários que criamos apenas para "consertar" o banco de dados ou criar o primeiro usuário. Mantê-los no servidor é um **risco de segurança gravíssimo**, pois qualquer pessoa que acessar a URL poderia resetar a senha do administrador.

1.  ❌ **`criar_admin.php`**: Exclua imediatamente. O usuário já está criado.
2.  ❌ **`reset_senha.php`**: Exclua imediatamente. A senha já foi corrigida.

### ⚠️ O que você PODE excluir (Opcional)

1.  ⚠️ **`projetos/projeto.html`**:
      * Este arquivo era o template estático antigo. Agora, o sistema usa o **`projeto_detalhe.php`** (que está na raiz) para gerar as páginas de projeto dinamicamente.
      * **Recomendação:** Pode excluir o arquivo `projeto.html`, mas **mantenha a pasta** `projetos/images`, pois as imagens dos projetos ainda estão lá.

-----

### 📄 O Novo README.md (Completo e Profissional)

Agora que limpamos a casa, aqui está o `README.md` definitivo. Ele foi reescrito para refletir o status de **Sistema Web Completo**, destacando o Painel Administrativo, o Banco de Dados e a Arquitetura Híbrida.

Copie o código abaixo e substitua todo o conteúdo do seu arquivo `README.md`.

````markdown
# Sistema Web Institucional - Nexus Innova

<p align="center">
  <img src="images/captura-site.png" alt="Banner do Projeto Nexus Innova" width="1000"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Status-Concluído-success?style=for-the-badge" alt="Status Concluído">
  <img src="https://img.shields.io/badge/PHP-7.4%2B-blue?style=for-the-badge&logo=php" alt="PHP">
  <img src="https://img.shields.io/badge/MySQL-Database-orange?style=for-the-badge&logo=mysql" alt="MySQL">
</p>

## 📋 Índice

- [🎯 Sobre o Projeto](#-sobre-o-projeto)
- [🚀 Tecnologias Utilizadas](#-tecnologias-utilizadas)
- [🏗️ Arquitetura do Sistema](#️-arquitetura-do-sistema)
- [⚡ Funcionalidades](#-funcionalidades)
- [📂 Estrutura de Arquivos](#-estrutura-de-arquivos)
- [🛠️ Instalação e Execução](#️-instalação-e-execução)
- [🔐 Área Administrativa](#-área-administrativa)
- [🤝 Contribuindo](#-contribuindo)
- [📞 Contato](#-contato)

## 🎯 Sobre o Projeto

O **Nexus Innova** é uma plataforma digital desenvolvida como parte de um projeto de extensão da **Faculdade CDL**. O sistema simula a presença digital de uma empresa de tecnologia, servindo como laboratório prático para a aplicação de conhecimentos full-stack.

O projeto evoluiu de um site estático para um **Sistema Web Dinâmico**, integrando Front-End moderno com um Back-End robusto em PHP e MySQL, permitindo o gerenciamento de conteúdo e captação de leads em tempo real.

### Objetivos Acadêmicos Alcançados
- Desenvolvimento de **CRUD Completo** (Create, Read, Update, Delete).
- Implementação de sistema de **Login e Autenticação** seguro.
- Criação de **Páginas Dinâmicas** alimentadas por banco de dados.
- Integração de arquitetura híbrida (Static Pages + Server Side Rendering).

## 🚀 Tecnologias Utilizadas

### Back-End & Banco de Dados
- **PHP 8+**: Linguagem principal para lógica do servidor, autenticação e API.
- **MySQL**: Banco de dados relacional para armazenar projetos, usuários e contatos.
- **Apache**: Servidor web (via XAMPP/WAMP).

### Front-End
- **HTML5 & CSS3**: Estrutura semântica e estilização responsiva (Mobile-First).
- **JavaScript (Vanilla)**: Interatividade, consumo de API e validação de formulários.
- **AJAX/Fetch API**: Carregamento assíncrono de dados sem recarregar a página.

### Ferramentas & Bibliotecas
- **AOS Library**: Animações de scroll.
- **Font Awesome**: Ícones vetoriais.
- **Google Tag Manager/Analytics**: Monitoramento de tráfego.

## 🏗️ Arquitetura do Sistema

O projeto utiliza uma **Arquitetura Híbrida** para maximizar performance e SEO:

1.  **Páginas de Serviço (`.html`):** Estáticas para carregamento instantâneo e alta indexação em motores de busca (SEO).
2.  **Home e Blog (Client-Side Rendering):** O JavaScript consome uma API PHP (`api_projetos.php`) ou dados locais (`data.js`) para renderizar o conteúdo dinamicamente.
3.  **Detalhes do Projeto (Server-Side Rendering):** O arquivo `projeto_detalhe.php` gera o HTML no servidor baseado no ID do banco de dados, garantindo que o conteúdo esteja sempre atualizado.

## ⚡ Funcionalidades

### 🌍 Área Pública
- **Portfólio Dinâmico:** Listagem de projetos puxados diretamente do MySQL.
- **Páginas de Serviço:** Landing pages focadas em conversão com download de E-books.
- **Blog Técnico:** Sistema de artigos com busca em tempo real.
- **Formulários de Contato:** Envio de mensagens via AJAX com salvamento no banco.
- **Assistente Virtual:** Chatbot flutuante para pré-atendimento.

### 🔐 Área Administrativa (Restrita)
- **Login Seguro:** Autenticação com hash de senha (`password_verify`) e controle de sessão.
- **Gestão de Projetos (CRUD):**
    - **Adicionar:** Cadastrar novos cases com descrição, desafio, solução e resultados.
    - **Editar:** Alterar informações de projetos existentes.
    - **Excluir:** Remover projetos do portfólio.
- **Gestão de Leads:** Visualização de todos os contatos recebidos pelo site (Nome, E-mail, Telefone).

## 📂 Estrutura de Arquivos

```text
nexus-innova/
│   # --- FRONT-END (Páginas Públicas) ---
├── index.html              # Página Inicial (Consome API)
├── blog.html               # Página de Blog
├── bi-ux.html              # Serviço: BI e UX
├── full-stack.html         # Serviço: Full Stack
├── qa.html                 # Serviço: QA
├── suporte-sites.html      # Serviço: Suporte
├── suporte-juridico.html   # Serviço: Jurídico
├── automacao.html          # Serviço: Automação
│
│   # --- BACK-END (Lógica e Sistema) ---
├── db.php                  # Conexão com Banco de Dados
├── auth.php                # Processamento de Login
├── login.html              # Formulário de Login
├── logout.php              # Encerramento de Sessão
├── protect.php             # Middleware de Proteção de Rotas
├── admin.php               # Painel Administrativo (CRUD Completo)
├── api_projetos.php        # API JSON para o Front-end
├── projeto_detalhe.php     # Página Dinâmica de Projeto (SSR)
├── salvar_contato.php      # Processamento de Contatos
│
│   # --- ASSETS E RECURSOS ---
├── style.css               # Estilos Globais
├── script.js               # Lógica JavaScript Principal
├── data.js                 # Dados Estáticos (Blog/Equipe)
├── blog/                   # Template do Blog
├── projetos/               # Imagens dos Projetos
├── covers/                 # Capas dos E-books
└── documents/              # Arquivos PDF para Download
````

## 🛠️ Instalação e Execução

1.  **Clone o Repositório:**

    ```bash
    git clone [https://github.com/felipesalvim/projeto-nexus-innova-faculdade.git](https://github.com/felipesalvim/projeto-nexus-innova-faculdade.git)
    ```

2.  **Configure o Ambiente:**

      - Instale o **XAMPP** (ou similar).
      - Mova a pasta do projeto para `C:\xampp\htdocs\nexus-innova`.

3.  **Banco de Dados:**

      - Abra o phpMyAdmin (`http://localhost/phpmyadmin`).
      - Crie um banco chamado `nexus_innova_db`.
      - Importe o arquivo SQL (ou execute os comandos de criação das tabelas `usuarios`, `projetos`, `contatos_projetos`).

4.  **Acesse:**

      - Site: `http://localhost/nexus-innova`
      - Admin: `http://localhost/nexus-innova/login.html`

## 🔐 Área Administrativa

Para acessar o painel de controle e testar as funcionalidades de CRUD:

  - **URL:** `/login.html`
  - **Usuário Padrão:** `admin@nexus.com`
  - **Senha Padrão:** `123456`

## 🤝 Contribuindo

Este é um projeto acadêmico aberto a melhorias.

1.  Faça um **Fork** do projeto.
2.  Crie uma **Branch** (`git checkout -b feature/NovaFuncionalidade`).
3.  Faça o **Commit** (`git commit -m 'Adiciona nova funcionalidade'`).
4.  Faça o **Push** (`git push origin feature/NovaFuncionalidade`).
5.  Abra um **Pull Request**.

## 📞 Contato

**Equipe Nexus Innova**

  - **GitHub:** [felipesalvim](https://www.google.com/search?q=https://github.com/felipesalvim)
  - **E-mail:** contato@nexusinnova.com.br
  - **Instagram:** [@nexus\_innova](https://instagram.com/nexus_innova)

-----

*Desenvolvido com 💚 pela equipe Nexus Innova - Faculdade CDL*

```
```
