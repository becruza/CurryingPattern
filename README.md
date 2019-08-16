# Patrón de diseño funcional - Currying
## ¿En qué consiste?
Currificar una función que recibe n parámetros (Arity) convierte la función en una que sólo recibe un parámetro.
Veamos en qué consiste con este ejemplo:

```javascript
var divisible = function (mod, num) {
    return num % mod;
}
 
 
//Este función es equivalente a la de arriba
//divisible currificada
var divisibleCurry = function (mod) {
   return function (num) {
       return num % mod;
   }
} 
```

Una vez currificada la función podemos usarla para generar funciones que un parámetro en común.
```Javascript
//Función para verificar paridad de un número
const mod2 = divisibleCurry(2);

//Función original
console.log(divisble(2,8)); //0

//Función currificada
console.log(divisibleCurry(2)(8)); //0

//Función currificada con parámetro mod = 2
console.log(mod2(8));
```

##Referencias:
- https://www.nypl.org/blog/2016/12/06/currying-functions
- https://yeisondaza.com/currying-en-javascript-funciones-con-superpoderes
- https://wsvincent.com/javascript-currying/
