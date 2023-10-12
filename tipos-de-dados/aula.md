# 7 Tipos de Dados

## Primitivos

- São imutáveis
- Todos são primitivos exceto os objetos

```javascript
var nome = 'letícia'; // string
var idade = 27; // number
var possuiFaculdade = false; // boolean
var time; // undefined, a definição fica em aberto
var comida = null; // null
var simbolo = Symbol() // symbol
var novoObjeto = {} // object
```

### Verificar tipo de Dado

`typeof` retorna o tipo de dado

```javascript
var nome = 'letícia';
console.log(typeof nome);
// retorna que é tipo string
```

## String

Somando string e concatenando as palavras

```javascript
var nome = 'letícia';
var sobrenome = 'amaral';
var nomeCompleto = nome + ' ' + sobrenome;
// retorna > letícia amaral
```

Somando números com strings, o resultado é sempre uma string.

```javascript
var gols = 1000;
var frase = 'Romário fez ' + gols + ' gols';
// retorna > Romário fez 1000 gols
```

## Aspas Duplas, Simples e Template String

```javascript
'JavaScript é "super" fácil'; // simples
"JavaScript é 'super' fácil"; // duplas
"JavaScript é \"super\" fácil"; // backslash
`JavaScript é "super" fácil`; // template string
"JavaScript é "super" fácil"; // inválido
```

### Template String

Passando expressões e/ou variáveis dentro de `${}`

```javascript
var gols = 1000;
var frase1 = 'Romário fez ' + gols + ' gols';
var frase2 = `Romário fez ${gols} gols`; // template string
```