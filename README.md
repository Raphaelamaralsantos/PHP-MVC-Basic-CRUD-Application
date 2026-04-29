# PHP MVC Basic CRUD Application

A simple MVC (Model-View-Controller) application built in pure PHP, demonstrating CRUD operations, user authentication, and MySQL database integration. Ideal for showcasing PHP fundamentals, object-oriented programming, and web development skills.

## Pré-requisitos

- **PHP**: Versão 7.0 ou superior (recomendado 8.x).
- **MySQL/MariaDB**: Para o banco de dados.
- **Composer**: Para gerenciar dependências (opcional, pois o `vendor/` já está incluído).
- **Servidor web**: Apache, Nginx ou o servidor embutido do PHP.

## Instalação

1. **Clone ou baixe o projeto**:
   - Baixe o arquivo ZIP ou clone o repositório para sua máquina.

2. **Instale as dependências** (se necessário):
   - Navegue até a pasta do projeto e execute:
     ```
     composer install
     ```
   - O `vendor/` já contém as dependências básicas, então isso pode não ser obrigatório.

3. **Configure o banco de dados**:
   - Crie um banco de dados MySQL (ex.: `front_mvc_php`).
   - Importe o arquivo `dump.sql` localizado na raiz do projeto para criar as tabelas e dados iniciais.
   - Edite o arquivo `App/Lib/Conexao.php` para ajustar as credenciais do banco (host, usuário, senha, nome do banco).

## Como executar

1. **Inicie o servidor**:
   - Abra o terminal na pasta do projeto.
   - Execute o servidor embutido do PHP:
     ```
     php -S localhost:8000
     ```
   - Alternativamente, configure um servidor web (ex.: Apache) e aponte o document root para a pasta do projeto.

2. **Acesse no navegador**:
   - Abra `http://localhost:8000` (ou a URL do seu servidor).
   - A página inicial será carregada, permitindo navegação entre as seções (home, usuários, clientes, fornecedores).

## Estrutura do Projeto

```
front-mvc-php-basico-main/
├── composer.json              # Configuração do Composer
├── dump.sql                   # Script SQL para criar o banco de dados
├── index.php                  # Ponto de entrada da aplicação
├── App/
│   ├── App.php                # Classe principal da aplicação
│   ├── Controllers/           # Controladores (lógica de negócio)
│   │   ├── Controller.php     # Classe base para controladores
│   │   ├── HomeController.php # Controlador da página inicial
│   │   ├── UsuarioController.php # Controlador de usuários
│   │   ├── ClienteController.php # Controlador de clientes
│   │   └── FornecedorController.php # Controlador de fornecedores
│   ├── Lib/                   # Bibliotecas auxiliares
│   │   ├── Conexao.php        # Classe para conexão com o banco
│   │   ├── Erro.php           # Tratamento de erros
│   │   └── Sessao.php         # Gerenciamento de sessões
│   ├── Models/                # Modelos (dados e regras de negócio)
│   │   ├── DAO/               # Data Access Objects
│   │   │   ├── BaseDAO.php    # Classe base para DAOs
│   │   │   ├── UsuarioDAO.php # DAO para usuários
│   │   │   ├── ClienteDao.php # DAO para clientes
│   │   │   └── FornecedorDao.php # DAO para fornecedores
│   │   └── Entidades/         # Entidades (representação dos dados)
│   │       ├── Usuario.php    # Entidade Usuário
│   │       ├── Cliente.php    # Entidade Cliente
│   │       └── Fornecedor.php # Entidade Fornecedor
│   └── Views/                 # Views (templates HTML)
│       ├── home/              # Página inicial
│       ├── usuario/           # Páginas de usuários (cadastro, editar, listar)
│       ├── cliente/           # Páginas de clientes
│       ├── Fornecedor/        # Páginas de fornecedores
│       ├── error/             # Páginas de erro (401, 404, 500)
│       └── layouts/           # Layouts compartilhados (header, footer, menu)
├── public/                    # Arquivos estáticos
│   ├── css/                   # Folhas de estilo (Bootstrap, custom)
│   └── js/                    # Scripts JavaScript (jQuery, validação)
└── vendor/                    # Dependências do Composer (autoload)
```

## Tecnologias Usadas

- **PHP**: Linguagem principal.
- **MySQL**: Banco de dados.
- **HTML/CSS/JavaScript**: Para as views e interface.
- **Bootstrap**: Framework CSS para responsividade.
- **jQuery**: Para interações JavaScript.
- **Composer**: Gerenciador de dependências.

## Funcionalidades

- **Página inicial**: Bem-vindo e navegação.
- **Usuários**: Cadastro, edição, listagem e autenticação básica.
- **Clientes**: Cadastro simples.
- **Fornecedores**: Cadastro simples.
- **Tratamento de erros**: Páginas para erros comuns (401, 404, 500).
- **Sessões**: Gerenciamento de login/logout.

## Contribuição

Este é um projeto de exemplo educacional. Sinta-se à vontade para modificar e melhorar. Para contribuições, crie um fork e envie um pull request.

## Licença

Este projeto é distribuído sob a licença MIT. Consulte o arquivo LICENSE para mais detalhes (se presente).

## Suporte

Se encontrar problemas, verifique:
- Logs de erro no terminal/servidor.
- Configurações do banco em `Conexao.php`.
- Compatibilidade da versão do PHP.

Para dúvidas, abra uma issue no repositório (se aplicável).

