1. It will print the number of iterations that the `for` loop made based on the length of `prices`. Since we passed in a list of length 3, the console with print 3.

---

2. Since `discountedPrice` is a `var` type variable, it will print the value of it. The last time `discountedPrice` was updated was in the last iteration of the `for` loop, which means it calculated the discount of the last price in the `prices` list. So we have `var discountedPrice = 300 * (1 - 0.5);`. That equals 150, so line 13 prints 150.

---

3. Similar to the last question, we need to find the last time `finalPrice` was updated. That also turns out to be within the for loop. So we have `finalPrice = Math.round(discountedPrice * 100) / 100;`. We know from the previous quesiton that `discountedPrice` is 150. So plugging that in we have `Math.round(150 * 100) / 100;`. Since 150 is whole we don't need to round and the 100s cancel. So at line 14, we print 150 also.

---

4. The function will return a new list of the original prices with the discount applied to each of them. So since our input is `[100, 200, 300], 0.5`, we would return `[50, 100, 150]`.

---

5. We will get an error because we defined our `for` loop with `let i = 0`, which means it can only be accessed within the `for` loop scope. 

---

6. Since `discountedPrice` was defined using `let`, it is only accesible within the `for` loop. So we get an error at line 13.

---

7. We're able to access `finalPrice` despite being defined with `let` because it was defined outside the `for` loop. This means that this line will print the same answer that we got for question 3, which is 150.

---

8. Despite using `let` instead of `var` to define the variables for this function, it still functions as one would expect. Thus, it returns the same thing as the funciton does in question 4, which is `[50, 100, 150]`.

---

9. At line 11 we get an error for the same reason as question 5. When the `for` loop was defined, we used `let i = 1`, so `i` is only accessible within the `for` loop.

---

10. At line 12, the console prints 3 since the length of `prices` is 3. There are no errors because we never tried to update the `const` variable length.

---

11. Despite `discounted` being defined as a `const` variable this time around, the function still returns as expected (even without `Math.round`). This is because even though`const` doesn't allow reassignment, it does allow for mutation. So in line 8 when we push a value into the array/list, we are not violating the properties of the `const` variable. So we return `[50, 100, 150]`.

---

12. - A. `student.name;`
    - B. `student['Grad Year'];`
    - C. `student.greeting();`
    - D. `student['Favorite Teacher'].name;`
    - E. `student.courseLoad[0];`

---

13. - A. `32` because integers map to their exact string representation
    - B. `1` because numeric conversions in mathematical expressions happen automatically
    - C. `3` since null is treated as a number, and it's number equivalent is `0`
    - D. `'3null'` null is treated as a string since `'3'` is a string, so they are concatenated
    - E. `4` true has a number value of 1
    - F. `0` false and null have number values of 0 
    - G. `'3undefined'` since `3` is a string `undefined` is converted to a string and concatenated
    - H. `NaN` since numeric conversion happened and `undefined` is `NaN` when converted

---

14. - A. `true` because different types are convert to numbers in a comparison and 2 > 1
    - B. `false` because strings are compared letter-by-letter and 2 > 1
    - C. `true` since the string '2' is converted to 2
    - D. `false` they are different types
    - E. `false` since true is 1 as an integer and comparisons of different types are converted to numbers
    - F. `true` since 2 becomes true as a Boolean

---

15. The `==` operator does an equality check after converting types. So if I compared `0 == false` that would be `true` since `false` as a number is `0`, and `0` as a boolean is `false`. However, if I were to use `===`, this is a strict equality check and does not do type conversions. So `0 === false` would be false because they are different types.

---

16. Check part2-question16.js.

---

17. The result of `modifyArray([1,2,3], doSomething)` is `[2, 4, 6]`. The function call on `modifyArray` takes us to that function first and then we call `doSomething` within the for loop. So everytime we're pushing something from the `array` in `modifyArray`, it goes to `doSomething` first which multiplies it by 2.

---

18. Check part2-question18.js.

---

19. The output is `1 4 3 2` each on their own line. This is because `setTimeout` runs the given function after the given delay. Since 1 is encountered first in the function `printNums` it is executed first. Then We have to wait 1 second to print 2. The reason 4 is printed before 3 even with a 0 delay is because `setTimeout` is set on a queue whereas line 5 is ran immediately. So lines 2 and 5 are run immediately in that order, then lines 4 and 3. That's why we get the order `1 4 3 2`.