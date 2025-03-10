
![MapOS](https://raw.githubusercontent.com/RamonSilva20/mapos/master/assets/img/logo.png)

![version](https://img.shields.io/badge/version-4.9.0-blue.svg?longCache=true&style=flat-square)
![license](https://img.shields.io/badge/license-MIT-green.svg?longCache=true&style=flat-square)
![theme](https://img.shields.io/badge/theme-Matrix--Admin-lightgrey.svg?longCache=true&style=flat-square)
![issues](https://img.shields.io/github/issues/RamonSilva20/mapos.svg?longCache=true&style=flat-square)
![contributors](https://img.shields.io/github/contributors/RamonSilva20/mapos.svg?longCache=true&style=flat-square)
[![Codeac](https://static.codeac.io/badges/2-305440631.svg "Codeac")](https://app.codeac.io/github/jiritichy/mapos)

![Map-OS](https://raw.githubusercontent.com/RamonSilva20/mapos/master/docs/dashboard.png)

### [Instalação](Instalacao_xampp_windows.md)

1. Faça o download dos arquivos.
2. Extraia o pacote e copie para seu webserver.
3. Rode o comando `composer install --no-dev` a partir da raiz do projeto.
4. Acesse sua URL e inicie a instalação, é bem simples, basta preencher as informações no assistente de instalação **MAPOS**.
5. Configure o email de envio no arquivo email.php.
6. Configurar cron jobs para envio de e-mail:
    ##### Enviar emails pendentes a cada 2 minutos.
    - */2 * * * * php /var/www/index.php email/process
    ##### Enviar emails com falha a cada 5 minutos.
    - */5 * * * * php /var/www/index.php email/retry

    ##### Obs: O path até o index.php (/var/www/) deve ser configurado conforme o seu ambiente


### Instalação (Docker)

1. Faça o download dos arquivos.
2. Instale o [Docker](https://docs.docker.com/install/) e o [Docker Compose](https://docs.docker.com/compose/install/).
3. Entre na pasta `docker` no seu terminal e rode o comando `docker-compose up --force-recreate`.
4. Acesse a URL `http://localhost:8000/` no navegador e inicie a instalação.
5. Na etapa de configuração use as seguintes configurações:
```
1. Por favor, insira as informações da sua conexão de banco de dados.
Host: mysql
Usuário: mapos
Senha: mapos
Banco de Dados: mapos

2. Por favor, insira as informações para sua conta de administrador.
Configure do jeito que quiser.

3. Por favor, insira a URL.
URL: http://localhost:8000/
```
6. Configure o email de envio no arquivo email.php.

    ##### Obs: Cuide da pasta `docker/data`, onde é pasta que o mysql do docker salva os arquivos. Se for deletada você perderá seu banco de dados.
    ##### Obs2: O PhpMyAdmin também e instalado e pode ser acessado em `http://localhost:8080/`.

### Atualização

1. Faça o backup dos arquivos e do banco de dados;
2. Substitua os arquivos pelos da nova versão;
3. Rode o comando `composer install --no-dev` a partir da raiz do projeto.
4. Volte as configurações nos arquivos database.php e config.php;
5. Logue no sistema como administrador e navegue até Configurações -> Sistema e clique no botão `Atualizar Banco de Dados` para atualizar seu banco de dados. Obs.: Também é possível atualizar o banco de dados via terminal rodando o comando `php index.php tools migrate` a partir da raiz do projeto;
6. Pronto, sua atualização está concluída;

### Atualização (Docker)

1. Pare o docker de rodar;
2. Faça o backup dos arquivos e do banco de dados;
3. Substitua os arquivos pelos da nova versão;
4. Volte as configurações nos arquivos database.php e config.php;
5. Entre na pasta `docker` no seu terminal e rode o comando `docker-compose up --force-recreate`;
6. Logue no sistema como administrador e navegue até Configurações -> Sistema e clique no botão `Atualizar Banco de Dados` para atualizar seu banco de dados. Obs.: Também é possível atualizar o banco de dados via terminal rodando o comando `php index.php tools migrate` a partir da raiz do projeto;
7. Pronto, sua atualização está concluída;

### Atualização via sistema

1. Primeiro é necessário atualizar manualmente o sistema para a versão v4.4.0;
2. Quando estiver nessa versão é possível atualizar o sistema clicando no botão "Atualizar Mapos" em Sistema >> Configurações;
3. Serão baixados e atualizados todos os arquivos exceto: `config.php`, `database.php` e `email.php`;

### Comandos de terminal

Para listar todos os comandos de terminal disponíveis, basta executar o comando `php index.php tools` a partir da raiz do projeto, após feita todo o processo de instalação.

### Frameworks/Bibliotecas
* [bcit-ci/CodeIgniter](https://github.com/bcit-ci/CodeIgniter)
* [twbs/bootstrap](https://github.com/twbs/bootstrap)
* [jquery/jquery](https://github.com/jquery/jquery)
* [jquery/jquery-ui](https://github.com/jquery/jquery-ui)
* [mpdf/mpdf](https://github.com/mpdf/mpdf)
* [Matrix Admin](http://wrappixel.com/demos/free-admin-templates/matrix-admin/index.html)
* [filp/whoops](https://github.com/filp/whoops)

### Requerimentos
* PHP >= 7.2
* MySQL
* Composer

### Contribuidores
| [<img src="https://avatars.githubusercontent.com/Pr3d4dor?s=115"><br><sub>Gianluca Bine</sub>](https://github.com/Pr3d4dor) | [<img src="https://avatars.githubusercontent.com/Henrique-Miranda?s=115"><br><sub>Henrique Miranda</sub>](https://github.com/Henrique-Miranda) | [<img src="https://avatars.githubusercontent.com/mariolucasdev?s=115"><br><sub>Mário Lucas</sub>](https://github.com/mariolucasdev) | [<img src="https://avatars.githubusercontent.com/HelanAllysson?s=115"><br><sub>Helan Allysson</sub>](https://github.com/HelanAllysson) | [<img src="https://avatars.githubusercontent.com/KansasMyers?s=115"><br><sub>KansasMyers</sub>](https://github.com/KansasMyers)
|:-:|:-:|:-:|:-:|:-:|
| [<img src="https://avatars.githubusercontent.com/daniellbastos?s=115"><br><sub>Daniel Bastos</sub>](https://github.com/daniellbastos) | [<img src="https://avatars.githubusercontent.com/github?s=115"><br><sub>drelldeveloper</sub>](https://github.com/drelldeveloper) | [<img src="https://avatars.githubusercontent.com/fontebasso?s=115"><br><sub>Samuel Fontebasso</sub>](https://github.com/fontebasso) | [<img src="https://avatars.githubusercontent.com/marllonferreira?s=115"><br><sub>marllonferreira</sub>](https://github.com/marllonferreira) | [<img src="https://avatars.githubusercontent.com/rodrigo3d?s=115"><br><sub>Rodrigo Ribeiro</sub>](https://github.com/rodrigo3d)
| [<img src="https://avatars.githubusercontent.com/willph?s=115"><br><sub>Wilmerson</sub>](https://github.com/willph) | [<img src="https://avatars.githubusercontent.com/bulfaitelo?s=115"><br><sub>Thiago Rodrigues</sub>](https://github.com/bulfaitelo) | [<img src="https://avatars.githubusercontent.com/mvnp?s=115"><br><sub>Marcos Pereira</sub>](https://github.com/mvnp)| [<img src="https://avatars.githubusercontent.com/marcotuliomtb?s=115"><br><sub>Marcos</sub>](https://github.com/marcotuliomtb)| [<img src="https://avatars.githubusercontent.com/zanzoushio?s=115"><br><sub>ZanzouShio</sub>](https://github.com/ZanzouShio)


## Autor
| [<img src="https://avatars.githubusercontent.com/RamonSilva20?s=115"><br><sub>Ramon Silva</sub>](https://github.com/RamonSilva20) |
| :---: |
