
### #1 

```javascript
// program to print a text 
let a = "hello";
const b = "world"

b = a

console.log(a)
console.log(b)
```

### #2 

```javascript
// program to print a text 
let a = "hello";

function greet () {
    console.log(a);
}

greet();
```


### #3 
```javascript
let a = "hello";

function greet() {
    a = 3;
}

// before the function call
console.log(a);

//after the function call
greet();
console.log(a); 
```

### #4 
```javascript
let a = "hello";

function greet() {
    let b = "World"
    console.log(a + b);
}

greet();
console.log(a + b); 
```

### #5 
```javascript
let a = 'Hello';

function greet() {

    let b = 'World';

    console.log(a + ' ' + b);

    if (b == 'World') {

        let c = 'hello';

        console.log(a + ' ' + b + ' ' + c);
    }

    console.log(a + ' ' + b + ' ' + c);
}

greet();
```

### #6
```javascript
function greet() {
    console.log('Hello world');
}

setTimeout(greet, 3000);
console.log('Hello guys');
```

### #7
```javascript
let promise = new Promise(function (resolve, reject) {
    setTimeout(function () {
    resolve('Promise resolved 1')}, 4000); 
});

promise.then((res)=>{
    const secondPromise = new Promise(function (resolve, reject) {
        setTimeout(function () {
        resolve('Promise resolved 2')}, 1000); 
    });
    secondPromise.then((res2)=>{
      console.log(res)
      console.log(res2)
    })
    console.log(res)
})
```

### #8
```javascript

let promise = new Promise(function (resolve, reject) {
    setTimeout(function () {
    resolve('Promise resolved')}, 4000); 
});
let promise2 = new Promise(function (resolve, reject) {
    setTimeout(function () {
    resolve('Promise 2 resolved')}, 2000); 
});


async function asyncFunc() {

    let result = await promise; 
    let result2 = await promise2;
    console.log(result);
    console.log(result2);
    console.log('hello');
}


asyncFunc();
```

### #9

```javascript
const user = {
    name: 'John',
    location: {
        city: 'Berlin',
        country:'Germany'
    }
}

const copy = {...user};

copy.location.city = "Hamburg"
console.log('original: ', user.location);
console.log('Copy: ', copy.location);

```



### #10

```javascript
var a = 10;
var show = function(){
    console.log(a);
    var a = 20;
};
show();
```