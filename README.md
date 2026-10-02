## Loops

**What a loop does**

A loop repeats a block of code multiple times, instead of writing the same line over and over. Anytime you need to "do this for every item" or "repeat until a condition is met," that's a loop.

**`for` loop — most common, when you know how many times to repeat**

```jsx
for (let i = 0; i < 5; i++) {
  console.log(i);
}
// prints 0, 1, 2, 3, 4
```

Three parts, separated by `;`:

- `let i = 0` — initialization, runs once at the start
- `i < 5` — condition, checked before every loop; loop continues while this is true
- `i++` — update, runs after every loop iteration**Tracing through it manually (helps it click)**

```
i = 0 → 0 < 5? yes → print 0 → i becomes 1
i = 1 → 1 < 5? yes → print 1 → i becomes 2
...
i = 5 → 5 < 5? no  → loop stops
```

---

**`while` loop — when you don't know exactly how many times in advance**

```jsx
let i = 0;

while (i < 5) {
  console.log(i);
  i++;
}
```

Same output as the `for` loop above, just structured differentlyCondition is checked first — if it's false right away, the loop body never runs.

**`do...while` — runs the body at least once**

```jsx
let i = 0;

do {
  console.log(i);
  i++;
} while (i < 5);
```

Difference from `while`: the condition is checked *after* the body runs, so it always executes at least once, even if the condition is false from the start

---

---

**`break` — exit a loop early**

```jsx
for (let i = 0; i < 10; i++) {
  if (i === 5) {
    break;
  }
  console.log(i);
}
// prints 0, 1, 2, 3, 4 — stops completely once i is 5
```

**`continue` — skip just this iteration, keep looping**

```jsx
for (let i = 0; i < 5; i++) {
  if (i === 2) {
    continue;
  }
  console.log(i);
}
``````jsx
// prints 0, 1, 3, 4 — skips 2, but keeps going
```

---

**Nested loops**

```jsx
for (let i = 1; i <= 3; i++) {
  for (let j = 1; j <= 3; j++) {
    console.log(i, j);
  }
}
```

A loop inside another loop — the inner loop completes fully for every single iteration of the outer loop. Common for grid-like patterns, multiplication tables, comparing pairs of items.

**Common mistakes**

- Infinite loops — forgetting `i++`, or writing a condition that never becomes false

```jsx
// infinite loop — i never changes
for (let i = 0; i < 5;) {
  console.log(i);
}
```

- Off-by-one errors — using `<=` when `<` was meant, looping one time too many or too few
- Using `for...in` on an array instead of `for...of` — technically works but gives indices as strings, not the values, and isn't the intended use
- Confusing `break` (stops the whole loop) with `continue` (skips just one iteration)

**Small practice task**

```jsx
// 1. Print numbers 1 to 10 using a for loop
// 2. Print only even numbers from 1 to 20 using continue
// 3. Use a while loop to print a countdown from 10 to 1
// 4. Loop through this array using for...of and print each value:
let colors = ["red", "green", "blue"];
// 5. Loop through this object using for...in:
let student = { name: "Riya", age: 21, course: "MCA" };
// 6. Use a nested loop to print a 3x3 grid of "i,j" pairs
```# Day-23
js 3 loop
