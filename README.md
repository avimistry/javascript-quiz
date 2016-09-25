# javascript-quiz
**Simple:) test for javascript developers**

```js
{ foo: 'bar' } // ..?

{ 'foo': 'bar' } // ..?

({ 'foo': 'bar' }) // ..?
```

```js
{ foo = 123 }
```

```js
vars: var vars = vars;
```

```js
var x = 1;
{
  var x = 2;
}
alert(x);
```

```js
"1" - - "1";
```

```js
'3' - 2 === 1;
```

```js
var a = []
(new Date).getTime()
```

```js
{} === {};
```

```js
var foo = {};
foo === foo;
```

```js
new String('foo') === 'foo';
new Number(10) === 10;
```

```js
typeof (null && false);
typeof (null && []);
```

```js
10 > 9 > 8 === true;
```

```js
new Array([], null, undefined, null) == ',,,';
```

```js
'1.0e0' == { valueOf: function() { return true; } };
```

```js
Object.prototype.toString.call();
Object.prototype.toString.call([]);
Object.prototype.toString.call({});
Object.prototype.toString.call(true);
Object.prototype.toString.call(null);
```

```js
if ( !('a' in window) ) {
var a = 1;
}
alert(a);
```

```js
'foo'.split('') + []
```

```js
'foo' == new function(){ return String('foo'); };
```

```js
{ break; 4; }
```

```js
RegExp.prototype.toString = function() { return this.source };

/3/-/2/; // ..?
```

```js
delete [].length;
```

```js
x = 1; (function() {
  return x;
  var x = 2;
}())
```

```js
Array(2).join();
```

```js
Number.prototype.x = function() { return this === 123; };
n(123).x();
```

```js
({} + 'b' > {} + 'a');
```

```js
[1,2,3,4,5][0..toString.length];
```

```js
(function(){}());
```

```js
{ a: { b:2 } };
```

```js
{ a: 1, b: 2 }[['b']];
```

```js
a: b: c: d: e: f: g: 1, 2, 3, 4, 5;
```

```js
++'52'.split('')[0];
```

```js
[true, false][+true, +false];
```

```js
{ foo: 1 }[0];
```

```js
(1, 2, 3)
```

```js
function a(x) {
  return x * 2;
}
var a;
alert(a);
```

```js
var x = 0;
function foo() {
  x++;
  this.x = x;
  return foo;
}

var bar = new new foo;
console.log(bar.x);
```

```js
var a = 1,
    b = function a(x) {
      x && a(--x);
    };
alert(a);
```

```js
function foo(a, b) {
  arguments[1] = 2;
  alert(b);
}
foo(1);
```

```js
function b(x, y, a) {
  arguments[2] = 10;
  alert(a);
}
b(1, 2, 3);
```

```js
function a() {
  alert(this);
}
a.call(null);
```

```js
(function(){
  return typeof arguments;
})();
```

```js
var f = function g() { return 23; }
typeof g();
```

```js
(function (x) {
  delete x;
  return x;
})(1); // 1
```

```js
var y = 1, x = y = typeof x;
x;
```

```js
(function f(f) {
   return typeof f();
})(function() { return 1; });
```

```js
var foo = {
  bar: function() { return this.baz; }
  baz: 1
};

(function() {
  return typeof arguments[0]();
})(foo.bar);
```

```js
var foo = {
  bar: function() { return this.baz; }
  baz: 1
};
typeof  (f = foo.bar);
```

```js
var f = (function f() { return '1'; }, function g() {return 2; })();
typeof f;
```

```js
var x = 1;
if ( function f() {} ) {
  x += typeof f;
}
x;
```

```js
var x = [typeof x, typeof y][1];
typeof typeof x;
```

```js
(function (foo) {
  return typeof foo.bar;
})({ foo: { bar: 1 } });
```

```js
(function f() {
  function f() { return 1; }
  return f();
  function f() { return 2; }
})();
```

```js
function f() { return f; }
new f() instanceof f;
```

```js
var x = 5,
    o = { x: 10,
          doIt: function doIt() {
                  var x = 20;
                  setTimeout( function() {
                      alert(this.x);
                  }, 10);
          }
     };
o.doIt();
```

```js
var o = {
          x: 8,
          valueOf: function() {
            return this.x + 2;
          },
          toString: function() {
            return this.x.toString();
          }
        },
        result = o < '9';
alert(o);
```

```js
function foo() {
  return 'Как правило, на этом срезаются новички';
}

function bar() {
  return
      'Как правило, на этом срезаются новички';
}

foo();
bar();
```

```js
var o = {
          b: function() {
                alert(this === o);
              }
        };
o['b']();
```

```js
for(var i = 0; i < 10; i++) {
  setTimeout(function() {
       alert(i);
  }, 100);
}
```

```js
function isEven(arg) {
  if (arg % 2 == 0) return 1;
  return undefined;
}
if (isEven(3) == false) {
  alert('ба, нечетное число!');
}
```

```js
var obj = {
            toString: function() {
              return '[object MyObject]';
            },
            valueOf: function() {
              return 17;
            }
          };
'object: ' + obj;
```

```js
'hello'.someProperty = 17;
'hello'.someProperty;
```

```js
var s = new String('hello');
typeof 'hello';
typeof s;
```

```js
var x1 = /[/ + 'javascript'[0] + '///';
// Answer: /[\/ + 'javascript'[0] + '/

var x2 = /\[/ + 'javascript'[0] + '///';
// Answer: /\[/j///
```

```js
'Hello'[-1];
'Hello'.charAt(-1);
```

```js
if ( new Boolean (false) ) alert('true') // ..?
```

```js
if(false) {
  function x() { a = 1 }
}

x();
```

```js
with({a: 1}) {
  a = 2,
  b = 3
}

[window.a, window.b];
```

```js
with (function (x, undefined) {}) length;
```

```js
new Promise( function() {}).then( function() { throw 'err' })

setTimeout( function() { 'no Error:)'}, 1000);
```

```js
(function pewpew(Infinity, length, __proto__) {
  return [,,~0.[0|0]][pewpew.__proto__.length && Infinity, -~String(this).length >> __proto__] << (0. === .0) + Infinity;
}).apply(typeof pewpew, [,,2]);
```

http://perfectionkills.com/javascript-quiz-es6/
