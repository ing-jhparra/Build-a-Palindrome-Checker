Proyecto del curso [JavaScript Algorithms and Data Structures](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures-v8/) de la plataforma [FreeCodeCamp](https://www.freecodecamp.org/)

# El proyecto

# Build a Palindrome Checker

A palindrome is a word or phrase that can be read the same way forwards and backwards, ignoring punctuation, case, and spacing.

Note: You'll need to remove all non-alphanumeric characters (punctuation, spaces and symbols) and turn everything into the same case (lower or upper case) in order to check for palindromes.

###  Objective: 
Build an app that is functionally similar to https://palindrome-checker.freecodecamp.rocks.

### User Stories:

1. You should have an input element with an id of "text-input".
2. You should have a button element with an id of "check-btn".
3. You should have a div, span or p element with an id of "result".
4. When you click on the #check-btn element without entering a value into the #text-input element, an alert should appear with the text Please input a value.
5. When the #text-input element only contains the letter A and the #check-btn element is clicked, the #result element should contain the text A is a palindrome.
6. When the #text-input element contains the text eye and the #check-btn element is clicked, the #result element should contain the text eye is a palindrome.
7. When the #text-input element contains the text _eye and the #check-btn element is clicked, the #result element should contain the text _eye is a palindrome.
8. When the #text-input element contains the text race car and the #check-btn element is clicked, the #result element should contain the text race car is a palindrome.
9. When the #text-input element contains the text not a palindrome and the #check-btn element is clicked, the #result element should contain the text not a palindrome is not a palindrome.
10. When the #text-input element contains the text A man, a plan, a canal. Panama and the #check-btn element is clicked, the #result element should contain the text A man, a plan, a canal. Panama is a palindrome.
11. When the #text-input element contains the text never odd or even and the #check-btn element is clicked, the #result element should contain the text never odd or even is a palindrome.
12. When the #text-input element contains the text nope and the #check-btn element is clicked, the #result element should contain the text nope is not a palindrome.
13. When the #text-input element contains the text almostomla and the #check-btn element is clicked, the #result element should contain the text almostomla is not a palindrome.
14. When the #text-input element contains the text My age is 0, 0 si ega ym. and the #check-btn element is clicked, the #result element should contain the text My age is 0, 0 si ega ym. is a palindrome.
15. When the #text-input element contains the text 1 eye for of 1 eye. and the #check-btn element is clicked, the #result element should contain the text 1 eye for of 1 eye. is not a palindrome.
16. When the #text-input element contains the text 0_0 (: /-\ :) 0-0 and the #check-btn element is clicked, the #result element should contain the text 0_0 (: /-\ :) 0-0 is a palindrome.
17. When the #text-input element contains the text five|\_/|four and the #check-btn element is clicked, the #result element should contain the text five|\_/|four is not a palindrome.

    ## La función Javascript

    ```javascript
        const textInput = document.getElementById('text-input');
        const checkBtn = document.getElementById('check-btn');
        const result = document.getElementById('result');

        function esPalindrome(str) {
          
            // Limpiamos la entrada de signos de puntuación, espacios y simbolos y convertimos a minúsculas
            const strLimpio = str.replace(/[^a-zA-Z0-9]/g, '').toLowerCase();
            const strAlreves = strLimpio.split('').reverse().join('');

            return strLimpio === strAlreves;
        }

        function validarPalindrome() {
            
            // Eliminar espacios al inicio y final del texto
            const inputValue = textInput.value.trim();
            
            if (!inputValue) {
                alert('Introducir un valor...');
                return;
            }
            
            result.className = '';
            
            if (esPalindrome(inputValue)) {
                result.textContent = `${inputValue} es un palíndromo`;
                result.classList.add('palindrome');
            } else {
                result.textContent = `${inputValue} no es un palíndromo`;
                result.classList.add('not-palindrome');
            }
        }

        checkBtn.addEventListener('click', validarPalindrome);

        textInput.addEventListener('keypress', function(e) {
            if (e.key === 'Enter') {
                validarPalindrome();
            }
        });

        window.addEventListener('load', function() {
            textInput.focus();
        });
    ```


    La función JavaScript forma parte de una página HTML donde se muestra  el cálculo del promedio de calificaciones. La página incluye dos ejemplos prácticos de su ejecución con diferentes conjuntos de datos. El ejercicio puede verlo en linea dando clic [aquí](https://palindromo-snx.pages.dev/) y en este repositorio se encuentra incluido el código.

 ## El Autor

| [<img src="https://avatars.githubusercontent.com/u/123877201?v=4" width=115><br><sub>Jesus H. Parra B.</sub>](https://github.com/ing-jhparra)
| :---: |


