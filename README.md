## CS472-Homework-05-Async
## Coding Exercise 01
Implement the code for `Meditation` class. The `start()` method prints a countdown every 1 second. To be used as follows:
```typescript
const morning_meditation = new Meditation(5);
morning_meditation.start();
console.log(`Start meditation`);

// Start meditation
// 5
// 4
// 3
// 2
// 1
// Jay Guru Dev
```

## Coding Exercise 02
Change `isPrime` function below to run asynchronously using Promise.  
* if the input is prime number, the promise resolves with `{ prime: true }`.  
* if the input is not a prime number, it rejects with `{ prime: false }`.  
```typescript
const isPrime = (n: number) => {
    for (let i = 2, s = Math.sqrt(n); i <= s; i++)
        if (n % i === 0) return false;
    return n > 1;
};
```
When you finish, test using the code below:
```typescript
console.log('start');
isPrime(7)
    .then(console.log)
    .catch(console.error);
console.log('end');

// start
// end
// { prime: true }
```
Make changes to the provided test and use `async`/`await` instead of `.then()` and `.catch()`

## Coding Exercise 03
Write an IIFE that fetch recipes from `https://dummyjson.com/recipes` and print to the console a list of recipe names.  
Make sure you [type the response](https://transform.tools/json-to-typescript). 
