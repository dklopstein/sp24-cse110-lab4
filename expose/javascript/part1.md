1. Line 9 prints "values added: 20". 

2. Line 13 prints "final result: 20".

3. Line 9 prints "values added: 20". 

4. Line 13 returns an error because using the `let` keyword defines our variable, result, in **block scope**. This means it can only be seen within the conditional `if`, so when we try to reference it outside of that we get an error.

5. Line 9 returns an error because we used the keyword `const`, which means it is an unchanging variable. So when line 7 is run, we're trying to reassign an unchanging variable to a new value, which is why we get an error.

6. Since `const` is like `let` because it has block scope, even if we got to line 13, we would get an error. This is because, for the same reason as question 4, result is not defined outside of the `if` conditional.