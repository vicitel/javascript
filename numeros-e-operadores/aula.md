# Números e Operadores
## Números
```javascript
var idade = 27
var gols = 1000
var pi = 3.14 // usa-se ponto para decimal
var expoenciacao = 2e10 // retorna 2+10 zeros > 20000000000
```
## Operadores Aritméticos
```javascript
var soma = 100 + 50 // 150
var subtracao = 100 - 50 // 50
var multiplicacao = 100 * 2 // 200
var divisao = 100 / 2 // 50
var expoente = 2 ** 4 // 16
var modulo = 14 % 5 // 4
```
💡: atenção ao operador de Soma `+` pois quando usado em strings sua função é fazer **concatenação** dos dados!
```javascript
var exemplo = 'string' + 25
// retorna > string25
var exemplo2 = '100' + 50
// retorna > 10050
```
### Strings
```javascript
var soma = '100' + 50 // 10050
var subtracao = '100' - 50 // 50
var multiplicacao = '100' * 2 // 200
var divisao = 'comprei 10' / 2 // NaN (Not a Number)
```
💡: a operação acontece mas o resultado é *sempre* uma STRING
-  soma `+` concatena em uma string
-  subtração `-` e multiplicação `*` o resultado é uma string e não um número
- divisão `/` o resultado é um NaN (Not a Number)
	- é possível verificar se uma variável é NaN com a função `isNan()`
### NaN = Not a Number
```javascript
var numero = 80
var unidade = 'kg'
var peso = numero + unidade // 80kg > concatenação pois se trata da soma entre dois tipos de dados diferentes (um número e uma string)
var pesoPorDois = peso / 2 // NaN 
```
### A ordem importa
Da esquerda para a direita, começando por multiplicação e/ou divisão, depois vem a soma e/ou subtração.
```javascript
var total = 20 + 5 * 2
// 5 * 2 = 10 + 20 = 30
var total2 = (20 + 5) * 2
// 20 + 5 = 25 * 2 = 50
var total3 = 20 / 2 * 5
// 50
var total4 = 10 + 10 * 2 + 20 / 2
// 10 * 2 = 20 + 20 / 2 = 30 + 10 = 40
```
💡: os parênteses `()` priorizam uma expressão.
## Operadores Aritméticos Unários
```javascript
var incremento = 5
console.log(incremento++)
// retorna > 5
console.log(incremento)
// retorna > 6

var incremento2 = 5
console.log(++incremento2)
// retorna > 6
console.log(incremento)
// retorna > 6
```

```javascript
var decremento = 5
console.log(decremento++)
// retorna > 5
console.log(decremento)
// retorna > 4

var decremento2 = 5
console.log(++decremento2)
// retorna > 4
console.log(decremento2)
// retorna > 4
```
💡: a ordem dos sinais importa!

O `+` e `-` tenta transformar o valor seguinte em número
```javascript
var frase = 'Isso é um teste'
+frase // NaN
-frase // NaN

var idade = '27'
+idade // 27 (de string p/ número)
-idade // -27 (de string p/ número)
console.log(+idade + 5)
// retorna > 32, pois transformou a string em número

var possuiFaculdade = true
console.log(+possuiFaculdade)
// retorna > 1
```