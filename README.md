## JavaScript Quiz
The simple test for JavaScript developers:)

### Assignments & Labels & Blocks

```js
{ foo = 123 };
```

```js
var x = 8 | 1;
```

```js
a: b: c: d: e: f: g: 1, 2, 3, 4, 5;
```

```js
var num1 = 5;
var num2 = 10;

num1+++num2;
```

```js
{ foo: 'bar' };

{ 'foo': 'bar' };

({ 'foo': 'bar' });
```

```js
var y = 1, x = y = typeof x;
x;
```

```js
vars: var vars = vars;
```

```js
var x = [typeof x, typeof y][1];
typeof typeof x;
```

```js
var bar = 1,
    foo = {};

foo: {
    bar: 2;
    baz: ++bar;
};

foo.baz + foo.bar + bar;
```

```js
xxx: {
  console.log(111);
  break xxx;
  console.log(222);
};
```

```js
var foo = function bar() { return 23 };
typeof bar();
```

```js
{ break; 4; };
```

```js
(function tada(printTwo) {
  printing: {
     alert('one');
     if (!printTwo) break printing;
     alert('two');
  };
  alert('three');
})(true);
```

```js
var obj = {
  1: 'I love this wonderful language'
};

obj[1] == obj[[1]] == obj['1'];
```

```js
var x = [typeof 5, typeof null][1];
typeof typeof x;
```

### Semicolon

```js
var a = []
(new Date).getTime();
```

```js
function foo() {
  return 'Some string';
};

function bar() {
  return
      'Some string';
};

foo() == bar();
```

### Coercions & Comparisons

```js
!!~1;
```

```js
0 === -0;
```

```js
~~(-5.5);
```

```js
'3' - 2 === 1;
```

```js
'00' == 0;
```

```js
[2] == true;
```

```js
(0.2 + 0.4) / 1 == (0.1 + 0.2) * 2;
```

```js
'1' - - '1';
```

```js
'5' + + '6';
```

```js
1 + 2 + '3' == 1 + '2' + 3;
```

```js
[3 + NaN + true] + [10 / (8 * null) - 1];
```

```js
10 > 9 > 8 === true;
```

```js
1 + - + + + - + 1;
```

```js
typeof (null && false);
```

```js
'1' + 2 + '3' + 4;
```

```js
[1] == true;
```

```js
'1.0e0' == { valueOf: function() { return true } };
```

```js
'a' + + 'b';
```

```js
[4] * [4];
```

```js
++'52'.split('')[0];
```

```js
4 + 3 + 2 + '1';
```

```js
1 && 3;
```

```js
var x = 1;
if (function f() {}) {
  x += typeof f;
};

alert(x);
```

```js
01 - + - 02 - + - 03;
```

```js
1 || 'foo' && 0;

1 && 'foo' || 0;
```

```js
[true] == true;
```

```js
parseInt(null, 24) === 23;
```

```js
1/0 === 1/-0;
```

```js
null == 0;
```

```js
[1, 2, 3, 4, 5][0..toString.length];
```

```js
[1 , 1] == true;
[[1], [1]] == true;
```

```js
'3' > '12' === '03' > '12';
```

```js
0.1 + (0.2 + 0.3) == (0.1 + 0.2) + 0.3;
```

```js
parseFloat('\t\v\r12.34\n ');
```

```js
' \t\r\n' == 0;
```

```js
'foo'.split('') + [];
```

```js
parseInt(1/0, 19);
```

```js
({} + 'b' > {} + 'a');
```

```js
~~+'2.9'-1 == ('2.9' >> 0) - 1;
```

```js
[] + [] + 'foo'.split('');
```

```js
[[[[1]]]] == true;
```

```js
[] + {};

[] * {};
```

```js
{} + [];
```

```js
[] + [];
```

```js
[][[]];
```

```js
[4, 4] * [4, 4];
```

```js
{} === {};
```

```js
var foo = {};
foo === foo;
```

### Comma operator

```js
(1, 2, 3);
```

```js
var a = 0; 
var b = (a++, 99);
```

```js
(1, function(){})();
```

```js
if (9, 0) alert('ok');
```

```js
[true, false][+true, +false];
```

```js
var smth = (45, 87) > (195, 3) ? 'bar' : (54, 65) > (1, 0) ? '' : 'baz';
```

```js
alert('1', alert('2', alert('3')));
```

```js
var f = (function f() { return '1' }, function g() { return 2 })();
typeof f;
```

```js
[3, 4, 5, 6][1, 2];
```

```js
alert('2',
  foo = function (arg) {
    alert(arg)
  },
  foo('1')
),
foo('3');
```

### Scopes & Closures & Hoisting

```js
var x = 1;
{
  var x = 2;
}

alert(x);
```

```js
if (!('a' in window)) {
  var a = 1;
};

alert(a);
```

```js
function a(x) {
  return x * 2;
};

var a;
alert(a);
```

```js
var foo = 1;
function bar() {
  foo = 10;
  return;
  function foo() {};
};

bar();
alert(foo);
```

```js
x = 1;
(function() {
  return x;
  var x = 2;
})();
```

```js
var x = 5,
var o = {
  x: 10,
  doIt: function doIt() {
    var x = 20;
    setTimeout(function() {
        alert(this.x);
    }, 10);
  }
};

o.doIt();
```

```js
function a() {
  alert(this);
};

a.call(null);
```

```js
(function f() {
  function f() { return 1; }
  return f();
  function f() { return 2; }
})();
```

```js
for (var i = 0; i < 10; i++) {
  setTimeout(function() {
      alert(i);
  }, 100);
};
```

```js
var foo = 11;
function bar() {
  return foo;
  foo = 10;
  function foo() {};
  var foo = '12';
};

alert(typeof bar());
```

```js
var a = 1,
var b = function a(x) {
  x && a(--x);
};

alert(a);
```

```js
(function (x) {
  delete x;
  return x;
})(1);
```

```js
(function() {
  var foo = 'a';
  (function(foo) {
      foo = 'b';
  })(foo);
  return foo;
})();
```

```js
(function f(f) {
   return typeof f();
})(function() { return 1; });
```

### Properties

```js
{ foo: 1 }[0];
```

```js
Number.prototype.x = function() { return this === 123 };
Number(123).x();
```

```js
delete delete window.document;
```

```js
{ a: 1, b: 2 }[['b']];
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

alert('object: ' + obj);
```

```js
Object.prototype.toString.call();
```

```js
function foo() {};
delete foo.length;

alert(typeof foo.length);
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
};

var result = o < '9';

alert(o);
```

```js
'hello'.someProperty = 17;
'hello'.someProperty;
```

```js
var foo = {
  bar: function() { return this.baz },
  baz: 1
};
```

```js
var a = 1;
b = 1;

(function() {
  return (delete window.a) === (delete window.b);
})();
```

```js
var foo = {
  bar: function() { return this.baz },
  baz: 1
};
typeof (f = foo.bar);
```

```js
(function() {
  return (function (a, b) {}).length;
})();
```

```js
'Hello'[-1] == 'Hello'.charAt(-1);
```

```js
delete [].length;
```

```js
(function (foo) {
  return typeof foo.bar;
})({ foo: { bar: 1 } });
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
with ({a: 1}) {
  a = 2,
  b = 3
};

[window.a, window.b];
```

```js
with (function (x, undefined) {}) length;
```

### Built-in objects & Constructors & Methods

```js
new String('foo') === 'foo';
```

```js
Math.max(2, []);
```

```js
(function() {
  return typeof arguments;
})();
```

```js
new Array([], null, undefined, null) == ',,,';
```

```js
[NaN].indexOf(NaN);
```

```js
function foo(a, b) {
  arguments[1] = 2;
  alert(b);
};

foo(1);
```

```js
Math.pow(-0, -1);
```

```js
'foo' == new function() { return String('foo') };
```

```js
(function() {
  return arguments.toString();
})();
```

```js
RegExp.prototype.toString = function() { return this.source };

/3/-/2/;
```

```js
function b(x, y, a) {
  arguments[2] = 10;
  alert(a);
};

b(1, 2, 3);
```

```js
Math.pow(+0, -1);
```

```js
(function() {
    var foo = {};
    var bar = {};
    var map = {};

    map[foo] = 'foo';
    map[bar] = 'bar';

    return map[foo];
})();
```

```js
Array(2).join();
```

```js
var x = 0;
function foo() {
  x++;
  this.x = x;
  return foo;
};

var bar = new new foo;
alert(bar.x);
```

```js
Math.pow(2, 53) === (Math.pow(2, 53) + 1);
```

```js
Array(4).join('lol' - 2);
```

```js
if (new Boolean(false)) {
  alert('true');
};
```

```js
(function() {
  return Array(5).join(',').length;
})();
```

```js
Number(undefined);
```

```js
function f() { return f; }
new f() instanceof f;
```

```js
var x = function() {
  return arguments;
};

x() == x();
```

```js
function whatDoesItDo(num) {
  return Math.max(0, Math.min(10, num));
};
```

```js
Array.isArray({__proto__: Array.prototype });
```

```js
var s = new String('hello');
typeof 'hello';
typeof s;
```

```js
(1.22e-10).toFixed(2);
```

```js
var date = new Date('1999/12/31');
date == '1999/12/31';
```

```js
(function() {
  return Array(3).map(function (item) { return 'a' });
})();
```

```js
Math.max({}, 2);
```

```js
var s1 = new String('hello');
var s2 = new String('hello');
alert(s1 == s2);
alert(s1 === s2);
```

### Miscellaneous
```js
-9 % 7;
```

```js
alert(typeof typeof(typeof(undefined));
```

```js
/^.$/.test('');
/^..$/.test('');
```

```js
var x = 1;
if (function f() {}) {
  x += typeof f;
};

alert(x);
```

```js
(function() {
  return void (1 + 1);
})();
```

```js
var x1 = /[/ + 'javascript'[0] + '///';
x1;

var x2 = /\[/ + 'javascript'[0] + '///';
x2;
```

```js
(![]+[])[+[]]+(![]+[])[+!+[]]+([![]]+[][[]])[+!+[]+[+[]]]+(![]+[])[!+[]+!+[]];
```

```js
(function pewpew(Infinity, length, __proto__) {
  return [,,~0.[0|0]][pewpew.__proto__.length && Infinity, -~String(this).length >> __proto__] << (0. === .0) + Infinity;
}).apply(typeof pewpew, [,,2]);
```
