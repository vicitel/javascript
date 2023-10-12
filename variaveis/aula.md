# Variáveis

Responsáveis por guardar dados na memória.

Iniciar com a palavra `var`, `let` ou `const`

```javascript
var nome = 'letícia';
let idade = 27;
const possuiFaculdade = false;
```

Evitam repetições (DRY - Don't repeat yourself)

```javascript
var preco = 20;
var totalComprado = 5;
var precoTotal = preco * totalComprado;
// retorna 100
```

## Sintaxe

Palavra chave `var` seguida do nome, sinal de igual e o valor

```javascript
var nome = 'letícia'
var idade = 27
var possuiFaculdade = false
```

## Vírgula

Utilize a vírgula para criar mais de uma variável, sem repetir a palavra chave `var`

```javascript
var nome = 'letícia',
    idade = 27,
    possuiFaculdade = false
```

## Sem valor declarado

Pode declarar ela e não atribuir valor inicialmente

```javascript
var precoAplicativo
// retorna undefined
```

## Nome

- Os nomes podem iniciar com $, _, ou letras

Podem conter números mas não inciar com eles

- Case sensitive

nome é diferente de Nome

- Se atentar as palavras reservadas
- Camel case

É comum nomearmos iniciando com minuscula e as proximas palavras com a primeira maiuscula: exemploDeCamelCase

```javascript
// inválidos
var $nome
var function
var 1possuiFaculdade

// válido
var $selecionar
var _nome
var possuiFaculdadeNoExterior
```

## Declarar

Erro ao tentar utilizar uma variável que não foi declarada

```javascript
console.log(nome);
// retorna > nome is not defined
```

## Hoisting

```javascript
console.log(nome)
var nome = 'letícia'
// retorna > undefined

var profissao = 'estudante'
console.log(profissao)
// retorna > estudante
```

## Mudar o valor atribuido

É possível mudar os valores atribuídos a variáveis declaradas com `var` e `let`. Porém, não é possível modificar valores das declaradas com `const`

```javascript
var idade = 27
idade = 28

let preco = 50
preco = 25

const possuiFaculdade = false
possuiFaculdade = true
// retorna um erro
```