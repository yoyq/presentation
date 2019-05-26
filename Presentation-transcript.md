### Presentation transcript

Hello my name is Dima Garkusha and today we're going to cover **callbacks promises and async await**.  
First of all these are all ways to deal with asynchronous data.  
Operations in javascript traditionally are synchronous and calling from top to bottom but what if you want some async 
operations for example fetch data from server or make some operations after few second.  
Here comes callbacks promises and async await.  

### Callbacks

**Callback** is a function that passed to another function. You can find all callbacks in most JavaScript code.  
For example set interval so here we have set interval and here we have our callback. Or for example array methods also uses callbacks.  
For example here you have array and here we used map method with our callback. Callback functions also can be named
and used in another functions so here we have function greeting, introduction. We call function introduction with first
name second name and our callback function greeting.  

#### Callback hell 
Multiple functions can be created independently and used as callback functions. This create multi-level functions.  
When we have multiple async functions we create some pyramids of callbacks for example here.  

Callback hell solution is promises. 

### Promises

A **promise** is an object and used to handle the asynchronous result of an operation. Promise makes handling asynchronous code
easier and more readable. For example here we can compare a callbacks and promises. We have helpful function calcValue we have our
promise with resolved value two here we get our value two and call calcValue function with that value. Here we return four
and here our value will be four and so on. As we see with promise we have improved readability and better error handling.  

Promise have **three states**:
- **pending** - this is the initial state of the promise
- **fulfilled** - this means the specified operation was completed
- **rejected** - the operation did not complete

#### Creating a promise

The promise object is created using the **new keyword**. So here we create our promise. This function is called an **executor function**.
When the promise is created the executor function runs automatically. Here we create the promise we have here value.
If our value more than 0.5 we resolve them else we reject.

#### Promises chaining

Using a promise that has been created is relatively straightforward. We chain then and catch to our promise.
So here our promise then here we chain it with then if our promise resolved we get that value here or if rejected here.
Also when we call then we return a promise so we can chain that promise. For example we create a promise and resolve it with
value one after one second here we get first result our result one and return result two (one multiply by two).
Here you have that value and so on. 

#### Handle errors in promises

If our promise rejected we can handle error with **then** and call our error handling function with **second parameter**
or we can use **catch** and our error handling function. So we create here our promise and if our promise rejected
we catch error here.

#### Finally in promises

Just like this finally in a regular try catch there is finally in promises. The call **finally** is always runs when the promise
is settled be it resolved or rejected. Finally is a good handler for performing cleanup for example stopping our loading indicator.
So here we create our promise here we have finally which log that our promise ready.

#### Promise methods

Promise have **four static methods**:
- promise resolve
- promise reject
- promise all
- promise race

#### Promise resolved

Here we can find syntax **promise resolve**. The promise resolve method is used when we already have a value but would like to have
it wrapped into a promise.

#### Promise reject

Here we can find syntax. **Promise reject** rarely used in real code.

#### Promise all

Here we can find syntax. **Promise all** takes an array of promises and return a new promise. The new promise resolves
when all listed promises are settled and has an array of their results. If any of the promises is rejected promise all
immediately rejects with that error.

#### Promise race

Here we can find syntax. Similar to promise all **promise race** takes an iterable of promises but instead of waiting
for all of them to finish it waits for the first result or error.

### async/await

#### async functions

An **async** function is a modification to the syntax used in writing promises you can call it syntactic sugar over
promises. It only makes writing promises easier. So here we can compare promises and async await. Here we have
our helpful function, we have async function and we call our helpful function with value two await for result
so here we have value four and so on. When we create async functions our code looks more like synchronous code.

#### Create async functions

Async functions are created by **prepending the word async before the function**. So here we create async function.
Or here we create async arrow function. Also **async functions always returns a promise**. If the function returns a
value the promise will be resolved with that value but if the function rejects the value our promise is rejected with that value.
So here we have our async function and here we return value, so we resolve our function with value one and here we get them.

#### Await

**Await** is only used with an async functions. **The keyword await** makes javascript wait until that promise settles and
returns it's result. So here we have async function here we have promise and we resolve them after one second.
Here we use the keyword await and wait when our promise will be resolved or rejected. Here we have our result.

#### Error handling in async functions

If a promise resolves normally then await promise returns the result but in case of a rejection it throws the error.
We can catch that error using **try catch**. So here we have async function we have try and we try to fetch some data from url.
If here we have some error we can catch them here in that block.

### That's all thank you for your attention, bye!
