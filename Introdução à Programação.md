# Introdução à Programação






## Instalação

https://code.visualstudio.com/ - VSCode, clique em Download for Windows e instale sem alterar nada

https://nodejs.org/en/download/ - NodeJS, clique em Windows Installer e instale sem alterar nada

<br>

## Extensões de arquivo / Formato de arquivo

Indicam o tipo de arquivo, é o que vem depois do `.` no nome dos arquivos. Na imagem abaixo, marcado em vermelho, vemos que há dois arquivos com extensão `.js` e outro arquivo com extensão `.txt`

![image-20220911205425774](/screenshots/image-20220911205425774.png)

Arquivos JavaScript têm extensão `.js` e são os que iremos trabalhar.

<br>

## Comandos terminal

`code .` abre o VSCode na pasta atual

`node nome_do_arquivo.js` roda o arquivo

<br>

## Comandos do VSCode

`CTRL + S`  - Salvar o arquivo atual

<br>

## Exibindo informações no console

Para exibir informações, escrever no console no nosso programa javascript usamos o `console.log()`. Dentro dos `()` colocamos as variáveis ou valores que queremos que seja exibido.

```js
console.log(123);
console.log('Maria');

let cidade = 'Rio de Janeiro';

console.log(cidade)
```

<br>

## Variáveis

Para criar uma variável usamos a palavra reservada `let` seguida do nome da variável. Depois colocamos um `=` e depois o valor daquela variável.

```js
let nome = 'João';

console.log(nome);
```

No exemplo acima criamos a variável chamada `nome` e o atribuímos o valor `'João'` para ela.

<br>

Podemos mudar o valor de uma variável já criada.

```js
let quantidadeDePontos = 20;

console.log(quantidadeDeDias);

quantidadeDeDias = 10;

console.log(quantidadeDeDias);
```

No exemplo acima criamos a variável `quantidadeDeDias` com o valor `20` e depois modificamos o valor dessa mesma variável para `10`.

<br>

## Constantes


Quando não queremos que um valor de uma variável não mude podemos criar uma constante.

Para criar uma constante escrevemos primeiro a palavra reservada `const` seguida do nome da constante. Depois coloca o `=` e o valor.

```js
const taxaDeJuros = 10;

console.log(taxaDeJuros);
```

<br>

No exemplo acima criamos uma constante chamada `taxaDeJuros` com o valor 10.

```js
const taxaDeJuros = 10;

taxaDeJuros = 20;

console.log(taxaDeJuros);
```

No exemplo acima criamos uma constante chamada `taxaDeJuros` com o valor 10 e depois tentamos mudar o valor dessa variável para 20. Ao tentar rodar esse programa, veremos um erro porque tentamos reatribuir o valor de um constante.


<br>


## Tipos Primitivos

### String

É o tipo texto.  Um valor do tipo texto está sempre entre aspas.

```js
let nome = 'João';
let cidade = 'Rio de Janeiro';
```

<br>

### Number

É o tipo de números. Pode ser inteiro, positivo, negativo, decimal.

```js
let idade = 30;
let taxaDeJuros = 0.12;
let temperatura = -5;
let saldo = 412345;
```

<br>

### Boolean

É tipo verdadeiro ou falso. Pode ser `true` para verdadeiro ou `false` para falso.

```js
let executado = true;
let premium = false;
```

<br>

### Undefined

Quando só damos um nome a uma variável e não colocamos o `=` depois dela. Ela terá o valor `undefined`, indefinido.

```js
let sobrenome;
```

No exemplo acima criamos a variável `sobrenome`, mas não demos um valor para ela. Logo essa variável será do tipo indefinido.

<br>

### Null

Quando queremos limpar o conteúdo de um variável colocamos o valor `null`. A variável passa a ser do tipo nula.

```js
let saldo = null;
```


<br>


## Tipos de referência

### Object

Um objeto é um tipo que agrupa variáveis relacionadas em um único lugar através de pares de **chave** e **valor**. Podemos pensar num objeto como uma variável que pode ter várias propriedades dentro de si. 

Para criar um objeto usamos as *chaves* `{}`

No caso abaixo temos a variável `pessoa` que é um objeto com as propriedades `nome`, `idade` e `estado`.

```js
let pessoa = {
  nome: 'Ronaldo',
  idade: 20,
  estado: 'Pernambuco'
}
```

`nome` é uma **chave** e `'Ronaldo'` é seu **valor**

`idade` é uma **chave** e `20` é seu **valor**

`estado` é uma **chave** e `'Pernambuco'` é seu **valor**

<br>

Podemos acessar cada propriedade de um objeto através do `.` seguido do nome da **chave**. Ou através de `['nomeDaChave']`. No exemplo abaixo acessamos a propriedade `estado` das duas formas:

```js
let pessoa = {
  nome: 'Heitor',
  idade: 26,
  estado: 'Pernambuco'
}

console.log(pessoa.estado);

console.log(pessoa['estado']);
```

<br>

### List / Array

Esse tipo contém uma lista de valores em um único lugar. Para criar uma lista usamos os *colchetes* `[]`

Podemos criar uma variável do tipo lista que contém nomes de produtos de uma lista de compras, por exemplo:

```js
let listaDeCompras = ['Maçã', 'Banana', 'Uva'];
```

A contagem dos elementos de uma lista começa sempre do `0`. Quando nos referimos à posição de uma lista estamos nos referindo ao **índice** (*index*). No nosso exemplo, `Maçã` está no índice 0 da lista `listaDeCompras`.

![image-20220911213419991](/screenshots/image-20220911213419991.png)

Para acessar elementos específicos de uma lista, primeiro escrevemos o nome da variável da lista e junto dela escrevemos o índice que queremos dentro de `[]`. Para o primeiro elemento escrevemos `listaDeCompras[0]`. Para o segundo elemento escrevemos `listaDeCompras[1]` e assim sucessivamente.

```js
console.log('Primeiro item ' + listaDeCompras[0]);

console.log('Terceiro item ' + listaDeCompras[2]);
```

<br>

### Function

