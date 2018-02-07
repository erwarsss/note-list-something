# note-list-something

## Functional Programming

adalah sebuah teknik pemrograman yang meminimalkan perubahan pada data utama (`immutable data`), serta menggunakan `pure function`

#### Using Higher Order Function - Reduce
here is example reduce using different style of code:
```javascript
var orders = [
    { amount: 200 },
    { amount: 150 },
    { amount: 250 },
    { amount: 120 },
    { amount: 50 }
]

//using reduce
var totalAmount = orders.reduce(function(sum, order) {
    return sum + order.amount
}, 0)

//using arrow function
var totalAmount = orders.reduce((sum, order) => {
    return sum + order.amount
}, 0)

var totalAmount = orders.reduce((sum, order) =>
    sum + order.amount
, 0)

var totalAmount = orders.reduce((sum, order) => sum + order.amount, 0)

//using loop
var totalAmount = 0
for (var i = 0; i < orders.length; i++) {
    totalAmount += orders[i].amount
}
console.log(totalAmount)
```

`pure function` adalah `function` :
1. memberikan input 5 dan akan selalu mengembalikan output 5
2. dan tidak mempunyai `side-effect`


## Callback

callback adalah function yang di jadikan parameter


```javascript
function sumberData() {
  var num = [{num: 2}, {num: 1}, {num: 5}]
  return num
}

function pengolahan(callback) {
  callback.map(x => {
  return x.num
  })
}

pengolahan(sumberData)
//it will log: 2 1 5
```

# Recursion

recursion adalah sebuah function yang memanggil function itu sendiri

example:
```javascript

function countDown(numb) {
  if (numb === 0) {
    return
  }
  console.log(numb)
  countDown(numb - 1)
}

countDown(10)

```
