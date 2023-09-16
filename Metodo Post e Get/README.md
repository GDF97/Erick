Na ultima aula de pw o professor explicou como utiliza o metodo _POST_ e _GET_, e explicou a diferença, basicamente, esses dois metodos servem para pegar, ou receber informações de um formulario ou qualquer outro lugar, porém existe uma diferença.

No metodo _GET_ as informações + a variavel que guarda essas informações aparecem na url, isso pode dar uma brecha na segurança do site. Para usar o metodo get voce precisa "setar" uma variavel para recolher da url.
Na url ficaria +- desse jeito: `https://url.com?entrada=1`

> Esse `?` significa que o que tem na frente é uma variavel php e o `=` vai definir o valor dessa variavel.

Caso Você queira colocar mais de uma variavel na url e necessario colocar o `&`.
Com duas variaveis ficaria dese jeito: `https://url.com?entrada=1&nome=Pedro`

Exemplo(Codigo)

```php
    $valorentrada = $_GET['entrada'];
    $valornome = $_GET['nome'];
    //Vale lembrar que o valor que ta dentro do get é o nome da variavel que vai estar no url
    echo $valorentrada;
    echo '<br>';
    echo $valornome;
```

Com isso feito utilizando metodo _GET_ teremos isso:


https://github.com/GDF97/Erick/assets/117999512/95c25491-ee19-4e10-a75c-8ed5e28949d0


No metodo _POST_ as informações e as variaveis não aparecem no url sendo assim mais seguro

Exemplo(Codigo HTML):

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Sign In - Page</title>
  </head>
  <body>
    <!--
        A propriedade action deverá receber o nome do arquivo que irá pegar as informações
        Como a gente ta trabalhando com o metodo post a propriedade METHOD tem que ser igual a "POST"
    -->
    <form action="login.php" method="POST">
      <!--
            Dentro dos inputs temos a propriedade "name"
            ela vai servir para recuperarmos o valor dentro do input lá no PHP 
        -->
      <input type="text" id="username" name="username" />
      <input type="text" id="email" name="email" />
      <input type="password" id="password" name="password" />
      <button type="submit">Enviar</button>
    </form>
  </body>
</html>
```

Exemplo(Codigo PHP):

```php
    // A variavel pode ter qualquer nome
    //porem o nome dentro do POST tem que ser o nome da propriedade NAME do formulario
    $username = $_POST['username'];
    $email = $_POST['email'];
    $password = $_POST['password'];

    echo "Username: ".$username;
    echo "Email: ".$Email;
    echo "Password: ".$password;
```

Com isso feito utilizando metodo _POST_ teremos isso:


https://github.com/GDF97/Erick/assets/117999512/cfbaf963-3814-453e-af7a-7d1df28e4a63

