<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

<!--<p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>-->


# AtalhoSETIC

AtalhoSetic como o próprio nome diz, tem por seu principal objetivo fornecer de forma simplificada Atalhos e Módulos para acesso rápido a rede interna da SETIC. Desenvolvido com Laravel por LmarDark.

- [Acesso Simplificado e Eficiente](#)
- [Conexão com LDAP](#)
- [Desenvolvimento com Laravel](#)
- [Customização e Modularidade](#como-fazer-a-criação-de-plugins).


## Como você configura um servidor de teste local

Para estar configurando a aplicação localmente, você deve instalar as seguintes ferramentas/extensões:
```
 - PHP 8.2
 - Composer
 - Extensões PHP necessárias:
   - ldap
   - dom
   - exif
   - ctype
   - FFI
   - fileinfo
   - ftp
   - gettext
   - iconv
   - phar
   - posix
   - readline
   - shmop
   - sockets
   - sysvmsg
   - sysvsem
   - sysvshm
   - tokenizer
   ```

Em seu terminal digite ```composer install```, para estar instalando todas as dependências.

Após isso apenas rodar o programa ```php artisan serve```.

## Como configurar para subir a aplicação no Docker

Para subir no docker você deve [instalar as extensões e ferramentas mencionadas acima](#como-você-configura-um-servidor-de-teste-local), porém além disso você deve instalar o Docker Engine para estar rodando a aplicação.

Depois de instalado as extensões, ferramentas e o Docker, apenas rodar os seguintes comandos:

**1** - ```docker compose up``` para subir o seu container.

**2.1** - Entre no container com o comando ```docker exec -it [id_do_container] sh```;

**2.2** - Executar como root se necessário ```docker exec -u -0 -it [id_do_container] sh```.

**3** - Por fim execute o comando ```chmod 777 -R .``` dentro da pasta */var/www/* para oferecer permissões de leitura, edição e execução para todos os usuários.

## Como fazer a criação de plugins?

Tendo acesso a este repositório, você pode estar criando seu módulo!

Abra seu Visual Code e faça o Módulo que desejar!

Observações:

- Permitido apenas *".blade.php"* e *".php"*.
- Tanto o Front(HTML/CSS/JS) quanto o Back-End(PHP) devem constar na mesma página.

### Como realizar a conexão de Banco de Dados

Requerimentos:
```
sqlite3
```

Segue exemplo prático:

```php
$databasePath = '../database/atalhosetic.sqlite';
$dsn = "sqlite:$databasePath"; 
$pdo = new PDO($dsn);
$pdo->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);

echo "Conexão bem-sucedida!";
```


### Como enviar um $_POST no .PHP

Segue exemplo prático:

```php
<?php
        $databasePath = '../database/atalhoseticDB.sqlite';
        //die($databasePath);
        $dsn = "sqlite:$databasePath";
        $pdo = new PDO($dsn);
        $pdo->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
        $csrfToken = csrf_token();
?>
```

Primeiro declare a variável $csrfToken no cabeçalho antes do "DOCTYPE".

Após isso insira o input do CSRF, segue exemplo:

```php
<form action="" method="POST">
    <input type="hidden" name="_token" value="<?php echo htmlspecialchars($csrfToken, ENT_QUOTES, 'UTF-8'); ?>">
    <input type="text" name="nome_name" placeholder="Nome" required>
    <input type="text" name="desc_name" placeholder="Descrição" required>
    <textarea id="textarea-id" name="code_name" placeholder="Code" required></textarea>
    <button type="submit">Enviar</button>
</form>
```


### Como programar tudo no mesmo arquivo?

Exemplo prático:
 - Em blade:

    ```blade
    @php
        $user = "Lucas";
        echo $user;
    @endphp
    
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Document</title>
    </head>
    <body>
        Hello, World!
    </body>
    </html>
    ```

- Em PHP:

    ```php
    <?php
        $user = "Lucas";
        echo $user;
    ?>

    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Document</title>
    </head>
    <body>
        Hello, World!
    </body>
    </html>
    ```

Segue documentação oficial do PHP e do BLADE para fins de aprendizado:

**PHP** - *https://www.php.net/manual/pt_BR/*

**BLADE** - *https://laravel-docs.readthedocs.io/en/latest/blade/*

Tendo terminado o seu módulo, você pode estar adicionando seu arquivo diretamente na aplicação indo em *"Admin"* depois em *"Módulos"*.


## Contribuidores

Obrigado por considerar contribuir com este projeto!
- Caio T.
- Lucas M.


## Melhorias ou vulnerabilidades

Caso encontre qualquer tipo de vulnerabilidade ou deseja fazer melhorias, fique a vontade para fazer a contribuição.


## License

 
