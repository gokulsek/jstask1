## **SECTION A: Technical Questions**

### **1. Difference between var, let, and const**

| Feature          | var                              | let           | const         |
| ---------------- | -------------------------------- | ------------- | ------------- |
| Scope            | Function-scoped                  | Block-scoped  | Block-scoped  |
| Redeclaration    | ✅ Allowed                        | ❌ Not allowed | ❌ Not allowed |
| Reinitialization | ✅ Allowed                        | ✅ Allowed     | ❌ Not allowed |
| Hoisting         | Yes (initialized as `undefined`) | Yes (TDZ)     | Yes (TDZ)     |

---

### **2. Which keyword allows redeclaration and why?**

**`var`** allows redeclaration because it does not enforce block scope and was designed in early JavaScript before strict scoping rules existed.

---

### **3. Which keyword allows reinitialization?**

**`var` and `let`** allow reinitialization because their values are mutable.

---

### **4. Which keyword does not allow redeclaration and reinitialization?**

**`const`** does not allow redeclaration or reinitialization because it is meant for fixed values.

---

### **5. Why should const be used for fixed values?**

Because `const` prevents accidental reassignment, improves code safety, and makes intent clear.

---

### **6. What error occurs when redeclaring a let variable?**

**SyntaxError:** Identifier has already been declared.

---

### **7. What error occurs when reassigning a const variable?**

**TypeError:** Assignment to constant variable.

---

### **8. Which keyword is preferred in modern JavaScript and why?**

**`let` and `const`** are preferred because they are block-scoped, safer, and prevent common bugs caused by `var`.

---

### **9. Can const be declared without initialization? Explain.**

**No.**
`const` must be initialized at declaration because its value cannot be assigned later.

---

### **10. When should var be avoided?**

`var` should be avoided in modern JavaScript because it can cause scope-related bugs due to function scoping and hoisting issues.

---

## **SECTION B: Code-Based Questions**

### **11. Predict the output**

```js
var a = 10;
a = 20;
var a = 30;
console.log(a);
```

 **Output:** `30`
**Reason:** `var` allows redeclaration and reinitialization.

---

### **12. Predict the output**

```js
let b = 5;
b = 15;
console.log(b);
```
 **Output:** `15`
**Reason:** `let` allows reinitialization.

---

### **13. Identify the error**

```js
let x = 10;
let x = 20;
```

 **Error:** SyntaxError (redeclaration of `let` variable)

---

### **14. Identify the error**

```js
const y = 50;
y = 100;
```

 **Error:** TypeError (cannot reassign a `const` variable)

---

### **15. Program using var to show redeclaration**

```js
var name = "Alice";
var name = "Bob";
console.log(name);
```

**Output:** `Bob`

---

### **16. Program using let to show reinitialization**

```js
let count = 1;
count = 2;
console.log(count);
```

**Output:** `2`

---

### **17. Program using const and explain why value cannot change**

```js
const PI = 3.14;
PI = 3.14159;
```

Error occurs because `const` variables cannot be reassigned after initialization.

---

### **18. Convert var to let where applicable**

```js
let age = 25;
age = 26;
console.log(age);
```

---

### **19. Convert var to const where applicable**

```js
const country = "India";
console.log(country);
```

---

### **20. Own example of var, let, and const**

```js
var city = "Delhi";      // can redeclare and reassign
let score = 90;          // can reassign but not redeclare
const passMark = 40;     // fixed value

score = 95;
city = "Mumbai";

console.log(city, score, passMark);


