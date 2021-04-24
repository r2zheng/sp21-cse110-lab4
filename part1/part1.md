## Part 1a
1. `values added: 20`
2. `final result: 20`
3. `values added: 20`
4. ReferenceError because variables declared with `let` does have block scope. Variable `result` is declared inside a block, so it is not visible outside the block.


## Part 1b
1. It prints: `3`. That is because the array of `prices` has `length=3`, which causes the variable `i` increases until it reaches `3`; also `i` is declared with `var`, so it is visible outside the for-loop. So after the for-loop, `console.log(i)` will print `3`.
2. It prints: `150`. At the last iteration of the for-loop, we have `i=2` and `prices[i]=300` and `discount=0.5`, for which `discountedPrice = prices[2] * (1 - discount) = 300 * 0.5=150`. Also, `discountedPrice` is declared with `var`, so it is visible outside the block. After the for-loop, `discountedPrice` is evetually assigned with `150`, so `console.log(discountedPrice)` will print `150`.
3. It prints: `150`. After the for-loop, we know that `discountedPrice=150` and `finalPrice` is assigned with `finalPrice = Math.round(discountedPrice * 100) / 100`, so `finalPrice = 150`. Therefore, `console.log(finalPrice)` will print `150`.
4. This function will return an array: `[50, 100, 150]`. The function calculates `discountedPrice` for each element of input `prices`, rounds the `discountedPrice`, and pushes each rounded value into the array `discounted`. This code calculates the discounted prices for `[100, 200,300]` by multiplying each element with `(1-discount) = 0.5` in the for-loop, so the output result from `discounted` is `[50, 100, 150]`.
5. ReferenceError because variable `i` declared with `let` does have block scope. So `i` is not visible outside the for-loop.
6. ReferenceError because variable `discountedPrice` declared with `let` does have block scope. So `discountedPrice` is not visible outside the block of the for-loop.
7. It prints: `150`. `finalPrice` is declared with `let`, but `console.log(finalPrice)` calls `finalPrice` in the same block, so it is visible. After the for-loop, we know that `discountedPrice=150` and `finalPrice` is assigned with `finalPrice = Math.round(discountedPrice * 100) / 100`, so `finalPrice = 150`. Therefore, `console.log(finalPrice)` will print `150`.
8. This function will return an array: `[50, 100, 150]`. The function calculates `discountedPrice` for each element of input `prices`, rounds the `discountedPrice`, and pushes each rounded value into the array `discounted`. This code calculates the discounted prices for `[100, 200,300]` by multiplying each element with `(1-discount) = 0.5` in the for-loop, so the output result from `discounted` is `[50, 100, 150]`.
9. ReferenceError because variable `i` declared with `let` does have block scope. So `i` is not visible outside the for-loop.
10. It prints: `3`. When we called `discountPrices`, `prices` is assigned with the array `[100,200,300]`, which has length `3`. So `prices.length=3`. `const` variable `length` is assigned with `prices.length` during its initial assignment, so `length` is correctly assigned with `length=3`. Therefore, `console.log(length)` will print `3`.
11. This function will return an array: `[50, 100, 150]`. Even though `discounted` is a `const` variable, but the values inside the const array can be changed (although `discounted` cannot reference to a new array). The function calculates `discountedPrice` for each element of input `prices`, and pushes each value into the array `discounted`. This code calculates the discounted prices for `[100, 200,300]` by multiplying each element with `(1-discount) = 0.5` in the for-loop, so the output result from `discounted` is `[50, 100, 150]`.
12. A. student.name
    B. student['Grad Year']
    C. student.greeting()
    D. student['Favorite Teacher'].name
    E. student.courseLoad[0]
13. A . `'3' + 2 = '32'` since integer `2` maps to its exact string representation.
    B. `'3' - 2 = 1` since string `'3'` converts to number `3`.
    C. `3 + null = 3` since `null` converts to number `0`.
    D. `'3'+null = '3null'` since `null` maps to the string `'null'`.
    E. `true + 3 = 4` since `true` maps to number `1`.
    F. `false + null = 0` since both `false` and `null` maps to numbers `0`.
    G. `'3' + undefined = '3undefined'` since `undefined` maps to the string `'undefined'`.
    H. `'3' - undefined = NaN` since `undefined` converts to `NaN` after numeric conversion.
14. A. `'2' > 1` is `true` since string `'2'` converts to number `2`.
    B. `'2' < '12'` is `false` since strings are compared letter-by-letter, and the first letters `'2' < '1'` returns `false`.
    C. `2 == '2'` is `true` since string `'2'` converts to number `2`.
    D. `2 === '2'` is `false` since number `2` and string `'2'` are of different types, which causes the strict equality returns `false`.
    E. `true == 2` is `false` since `true` converts to number `1`.
    F. `true === Boolean(2)` is `true` since `Boolean(2)` converts to boolean `true`, and `true === true` returns `true` since two values have the same type with the same value.
15. Regular equality `==` checks the equality with type conversion. However, `===` is the strict equality, which checks the equality without type conversion, so it returns `false` when two values are of different types. Also, `null == undefined` returns `true`, but `null === undefined` returns `false` since they are of different types.
16. Answered in `part1b-question16.js`.
17. It will return array `[2, 4, 6]`. In the for-loop of the `modifyArray`, it runs `callback` for each element of the input `array` and pushes the output of `callback` to `newArr`. The input `array` is `[1,2,3]` and callback is assigned with the function `doSomething` which multiplies the input number by 2. So `modifyArray` multiplies each element in `[1,2,3]` by `2` and pushes the results in `newArr`. So the returned array `newArr` should be `[2,4,6]`.
18. Answered in `part1b-question18.js`.
19. It will prints:
    ```
    1
    4
    3
    2
    ```
    `console.log(1)` is done at first. The `setTimeout` will cause `console.log(2)` to be delayed after 1 second (enough time for the next two lines to be done), and `console.log(3)` to be delayed just after its next line `console.log(4)` is done.
