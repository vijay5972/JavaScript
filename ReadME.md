- Eveything in JS happens inside the Execution Context.
    - It has memory component(Variable Environmnet) --> Contains variables and functions as Key-Value pairs.
    - Code Component(Thread of Execution)--> Place where code is executed

- JS is s Synchronous single-threaded language.
- JavaScript uses the Event Loop + Callbacks + Promises + async/await to look asynchronous (non-blocking).

- At global level, this == window
- Js is a weakly typed language
- == Compares values only, not types. If the types are different, JS tries to convert one type to another (called type coercion) before comparing.
- === Compares both value and type. No type conversion happens.

- Lexical environmnet is the local memory along with the lexical environment of its parent.

- Let and Const 
    - Both are hoisted but will be in Temporal Dead Zone until initialized.
    - They will be allocated memory in 'Script' scope but not 'Global' scope like 'var'.
    - If you try to access it before initialization, it throws a 'ReferenceError'.
    - Referencing any random variable which doesn't exist also throws 'RefernceError: not defined'
    - You can't declare let and const with same variablenames again. It will throw a 'SyntaxError'. You cant do it separately inside a Block which will hoist them in nlock scope.
    - Const has to be declared and initialized at the same time. Or else will get 'SyntaxError'.
    - If you try to assign another value to const it throws 'TypeError'.
    - Const cannot be reassigned but for Objects/Arrays contents can change. Reassigned whole array is not possible.
    - If you want to truly freeze an object/array, use: Object.freeze(obj);


- let a=10;
  {
    var a=20; //throws error 'a' is already declared.
  }

  var a=10;
  {
    let a=20; // Works fine
  }

  let a=10;
  function x(){
    var a=20; //This is allowed, as var is function scope.
  }

  -Closures
    - 