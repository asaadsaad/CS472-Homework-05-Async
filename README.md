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
Using Fetch API, write functions that implement the following CRUD operations on the products API from `https://dummyjson.com/products`:
* Get all products: `get_products(skip: number = 0, limit: number = 30)` Print list of product titles only, with pagination (30 products each page). Use [limit and skip](https://dummyjson.com/docs/products#products-limit_skip) query parameters.
* Get a single product: `get_product(id: number)` Print JSON with `{title, description, category, price}`.
* Add a new product: `add_product(product: Partial<Product>)` return `{ok: boolean}`
* Update a product title: `update_product_title(id: number, new_title: string)` return `{ok: boolean}`
* Delete a product: `delete_product(id: number)` return `{ok: boolean}`
  
Make sure you [type the response](https://transform.tools/json-to-typescript). 
