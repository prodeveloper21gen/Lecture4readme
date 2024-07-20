# Lecture on Arrays and Array Methods in JavaScript

---

## Introduction to Arrays

Arrays are fundamental data structures in JavaScript used to store multiple values in a single variable. They are widely used because of their versatility and the variety of operations you can perform on them.
![image](https://github.com/user-attachments/assets/a8a64bfe-06e7-4467-b04b-40a0e5216f0d)

## Creating Arrays
![image](https://github.com/user-attachments/assets/ef755d8f-931b-4a4d-ba17-eeca53669eaf)

In JavaScript, arrays can be created using array literals `[]` or the `Array` constructor.

```javascript
// Array literal
let numbers = [1, 2, 3, 4, 5];

// Array constructor
let fruits = new Array('apple', 'banana', 'orange');
```

## Accessing Array Elements

Array elements are accessed using zero-based indexing.

```javascript
let fruits = ['apple', 'banana', 'orange'];
console.log(fruits[0]); // Output: 'apple'
```

## Array Properties and Methods

JavaScript provides a variety of built-in properties and methods to manipulate arrays efficiently.
![image](https://github.com/user-attachments/assets/39f8d2b2-2d6e-4e42-99b2-c732f7513c8f)

### Common Array Methods

1. **`push()` and `pop()`**:
   - `push()`: Adds one or more elements to the end of an array.
   - `pop()`: Removes the last element from an array and returns it.

   ```javascript
   let fruits = ['apple', 'banana', 'orange'];
   fruits.push('grape'); // ['apple', 'banana', 'orange', 'grape']
   fruits.pop(); // Removes 'grape'
   ```

2. **`shift()` and `unshift()`**:
   - `shift()`: Removes the first element from an array and returns it.
   - `unshift()`: Adds one or more elements to the beginning of an array.

   ```javascript
   let fruits = ['apple', 'banana', 'orange'];
   fruits.shift(); // Removes 'apple'
   fruits.unshift('grape'); // Adds 'grape' to the beginning
   ```

3. **`splice()`**:
   - Changes the contents of an array by removing or replacing existing elements and/or adding new elements.

   ```javascript
   let fruits = ['apple', 'banana', 'orange'];
   fruits.splice(1, 1, 'grape', 'kiwi'); // Removes 'banana', adds 'grape', 'kiwi'
   ```

4. **`slice()`**:
   - Returns a shallow copy of a portion of an array into a new array object.

   ```javascript
   let fruits = ['apple', 'banana', 'orange', 'grape', 'kiwi'];
   let citrus = fruits.slice(2); // ['orange', 'grape', 'kiwi']
   ```

5. **`concat()`**:
   - Returns a new array comprised of this array joined with other array(s) and/or value(s).

   ```javascript
   let fruits = ['apple', 'banana'];
   let moreFruits = ['orange', 'grape'];
   let allFruits = fruits.concat(moreFruits); // ['apple', 'banana', 'orange', 'grape']
   ```

6. **`forEach()`**:
   - Calls a function for each element in the array.

   ```javascript
   let fruits = ['apple', 'banana', 'orange'];
   fruits.forEach(function(fruit) {
       console.log(fruit);
   });
   ```

### Functional Array Methods

7. **`find()`**:
   - Returns the first element in the array that satisfies the provided testing function.

   ```javascript
   let numbers = [10, 20, 30, 40, 50];
   let found = numbers.find(function(number) {
       return number > 25;
   });
   console.log(found); // Output: 30
   ```

8. **`filter()`**:
   - Creates a new array with all elements that pass the test implemented by the provided function.

   ```javascript
   let numbers = [10, 20, 30, 40, 50];
   let filtered = numbers.filter(function(number) {
       return number > 25;
   });
   console.log(filtered); // Output: [30, 40, 50]
   ```

9. **`reduce()`**:
   - Executes a reducer function (that you provide) on each element of the array, resulting in a single output value.

   ```javascript
   let numbers = [1, 2, 3, 4, 5];
   let sum = numbers.reduce(function(accumulator, currentValue) {
       return accumulator + currentValue;
   }, 0);
   console.log(sum); // Output: 15
   ```
![image](https://github.com/user-attachments/assets/9cdfa1f1-bb2d-4b24-b693-c802bae471c0)

# 10. **Callback Functions**:
    - Many array methods such as `forEach`, `find`, `filter`, `reduce`, etc., accept callback functions as arguments.
    - Callback functions are functions passed as arguments to another function to be executed later.

    ```javascript
    let numbers = [1, 2, 3, 4, 5];
    numbers.forEach(function(number) {
        console.log(number * 2);
    });

    let filtered = numbers.filter(function(number) {
        return number > 2;
    });
    console.log(filtered); // Output: [3, 4, 5]
    ```
