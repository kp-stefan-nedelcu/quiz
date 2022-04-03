
### #1 

```
// program to print a text 
let a = "hello";
const b = "world"

b = a

console.log(a)
console.log(b)
```

### #2 

```
// program to print a text 
let a = "hello";

function greet () {
    console.log(a);
}

greet();
```


### #3 
```
// program to show the change in global variable
let a = "hello";

function greet() {
    a = 3;
}

// before the function call
console.log(a);

//after the function call
greet();
console.log(a); // 3
```

### #4 
```
// program showing local scope of a variable
let a = "hello";

function greet() {
    let b = "World"
    console.log(a + b);
}

greet();
console.log(a + b); // error
```

### #5 
```
// program showing block-scoped concept
// global variable
let a = 'Hello';

function greet() {

    // local variable
    let b = 'World';

    console.log(a + ' ' + b);

    if (b == 'World') {

        // block-scoped variable
        let c = 'hello';

        console.log(a + ' ' + b + ' ' + c);
    }

    // variable c cannot be accessed here
    console.log(a + ' ' + b + ' ' + c);
}

greet();
```

### #6
```
// program to display a text using setTimeout method
function greet() {
    console.log('Hello world');
}

setTimeout(greet, 3000);
console.log('Hello guys');
```

### #7
```
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
```
// a promise
let promise = new Promise(function (resolve, reject) {
    setTimeout(function () {
    resolve('Promise resolved')}, 4000); 
});
let promise2 = new Promise(function (resolve, reject) {
    setTimeout(function () {
    resolve('Promise 2 resolved')}, 2000); 
});

// async function
async function asyncFunc() {

    // wait until the promise resolves 
    let result = await promise; 
    let result2 = await promise2;
    console.log(result);
    console.log(result2);
    console.log('hello');
}

// calling the async function
asyncFunc();
```

### #9

```
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

```
var a = 10;
var show = function(){
    console.log(a);
    var a = 20;
};
show();
```