O _foreach_ é uma maneira de conseguir percorrer todos os dados de uma array se saber o tamanho dessa array (Explicação porca)

Na sintaxe do _foreach_ nos temos o valor que ele vai receber (nesse caso o array) e o valor que ele ira mostrar (nesse caso as informações desse array)

Exemplo(Codigo PHP):

```php
    $valorEntrada = $_GET['entrada'];
     // Pode ser as informações de uma pessoa. Exemplo: Pedro(nome); 16(idade); Itariri(cidade);
    $valorSeparado = explode(";", $valorEntrada);
    //Separando os valores através do ;(ponto e virgula)

    foreach ($valorSeparado as $value){
        echo "<br>"; //Quebra de linha
        echo $value;
    }

```

No _foreach_ apenas uma array pode ser utilizada, porém, caso você precise de utilizar outra array você pode criar um variavel que irá acrescentar toda vez que o loop for completado

Exemplo(Codigo PHP):

> Escreva um programa que receba o nome, a idade, a cidade e exiba na tela da seguinte forma:
> `Nome:` 'Nome da pessoa'
> `Idade:` 'Idade da pessoa'
> `Cidade:` 'Cidade da pessoa'

```php
    $valorEntrada = $_GET['entrada'];
     // Pode ser as informações de uma pessoa. Exemplo: Pedro(nome); 16(idade); Itariri(cidade);
    $valorSeparado = explode(";", $valorEntrada);
    //Separando os valores através do ;(ponto e virgula)
    $nomeDeCadaEntrada = ["Nome: ", "Idade: ", "Cidade: "];

    $n = 0; //Variavel que vai controlar o segundo Array(Pode ter qualquer nome)
    foreach($valorSeparado as $value){
        echo $nomeDeCadaEntrada[$n].$value;
        echo "<br>"; //Quebra de Linha
        $n++; //Incrementando a variavel que controla o segundo Array
    }

```
