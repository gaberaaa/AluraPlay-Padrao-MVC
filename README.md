# AluraPlay

Este é um sistema simples para gerenciar vídeos, desenvolvido em PHP utilizando o padrão MVC e MySQL.

## Requisitos

Antes de iniciar, certifique-se de ter os seguintes requisitos instalados:
- PHP 8.0 ou superior
- MySQL
- MySQL Workbench
- Composer
- Servidor Apache ou PHP embutido

## Instalação

1. Clone este repositório:
   ```bash
   git clone https://github.com/seuusuario/aluraplay.git
   cd aluraplay
   ```

2. Instale as dependências via Composer:
   ```bash
   composer install
   ```

3. Configure o banco de dados MySQL:
   - Crie um banco de dados chamado `aluraplay` no MySQL Workbench
   - Execute o seguinte comando SQL no MySQL Workbench:
     ```sql
     CREATE TABLE `videos` (
       `id` int NOT NULL AUTO_INCREMENT,
       `url` varchar(200) NOT NULL,
       `title` varchar(200) NOT NULL,
       PRIMARY KEY (`id`)
     );
     ```

4. Configure a conexão com o banco de dados no arquivo `conexao-bd.php`:
   ```php
   $pdo = new PDO('mysql:host=localhost;dbname=aluraplay', 'seu_usuario', 'sua_senha');
   ```

## Executando o Projeto

1. Inicie o servidor embutido do PHP:
   ```bash
   php -S localhost:8000 -t public
   ```

2. Acesse o sistema no navegador:
   ```
   http://localhost:8000
   ```

## Estrutura do Projeto

- `public/` - Contém os arquivos acessíveis ao público (index.php, CSS, imagens)
- `src/Controller/` - Contém os controladores da aplicação
- `src/Entity/` - Contém as entidades do sistema
- `src/Repository/` - Contém as classes de acesso ao banco de dados
- `views/` - Contém os arquivos de visualização (HTML e PHP)
- `config/` - Contém arquivos de configuração, como as rotas

## Tecnologias Utilizadas

- PHP
- MySQL
- MySQL Workbench
- Composer
- HTML/CSS

## Contribuição

Sinta-se à vontade para contribuir! Faça um fork do projeto e envie um pull request com melhorias.

## Licença

Este projeto está sob a licença MIT.

