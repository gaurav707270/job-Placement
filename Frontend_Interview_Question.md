# 🚀 Interactive Frontend Developer Interview Practice

## 🎯 How to Use This

For every question:

1. **Read the question**
2. Try answering it yourself in **30–60 seconds**
3. Click/think through the **Expected Answer**
4. Check the **Follow-up Question**
5. Rate yourself:

   * 🟢 Easy
   * 🟡 Need Practice
   * 🔴 Don't Know

---

# 🟢 LEVEL 1 — Frontend Fundamentals

### Q1. What is frontend development?

**💡 Try answering before reading the answer.**

<details>
<summary>👉 Show Answer</summary>

Frontend development is the development of the part of a website or web application that users directly interact with.

It mainly uses:

* HTML → Structure
* CSS → Styling
* JavaScript → Behavior
* React/Next.js → Component-based application development

**Example:**

A login page containing inputs, buttons, animations, and validation is frontend development.

</details>

**🔥 Follow-up:**
What happens when a user clicks the Login button?

---

### Q2. What skills are required for a frontend developer?

<details>
<summary>👉 Show Answer</summary>

Important skills include:

* HTML
* CSS
* JavaScript
* Responsive design
* Git/GitHub
* REST APIs
* React/Next.js
* Browser DevTools
* Accessibility
* Performance optimization
* Basic SEO

</details>

**🔥 Follow-up:**
Which of these skills are you strongest in?

---

### Q3. Frontend vs Backend?

| Frontend       | Backend                 |
| -------------- | ----------------------- |
| User interface | Server logic            |
| HTML/CSS/JS    | Node.js/PHP/Python/Java |
| Browser        | Server                  |
| UI interaction | Database/API            |
| Client-side    | Server-side             |

**🔥 Interview Challenge:**
Explain this using an **e-commerce website example**.

---

### Q4. What is responsive web design?

<details>
<summary>👉 Show Answer</summary>

Responsive design means creating a website that automatically adapts to different screen sizes such as:

* Mobile
* Tablet
* Laptop
* Desktop

Common techniques include:

```css
@media (max-width: 768px) {
    .container {
        width: 100%;
    }
}
```

</details>

**🔥 Follow-up:**
How would you make a navbar responsive?

---

# 🟡 LEVEL 2 — HTML Challenge

## HTML Rapid Fire ⚡

### Q5. What is semantic HTML?

**Answer:**

Semantic elements describe their meaning.

Examples:

```html
<header>
<nav>
<main>
<section>
<article>
<footer>
```

**Why use them?**

* Better SEO
* Better accessibility
* Better code readability

**🔥 Follow-up:**
Why would you use `<article>` instead of `<div>`?

---

### Q6. `<div>` vs `<span>`

| `<div>`                  | `<span>`                |
| ------------------------ | ----------------------- |
| Block-level              | Inline                  |
| Usually creates new line | Doesn't create new line |
| Large sections           | Small text/content      |

---

### Q7. Why is `alt` important?

```html
<img src="profile.jpg" alt="User profile photo">
```

The `alt` attribute:

* Helps screen readers
* Improves accessibility
* Provides fallback text
* Can help image SEO

**🔥 Interview Trap:**
Should `alt` contain `"image of..."`?

Usually, no. The image role is already understood by assistive technology.

---

# 🔵 LEVEL 3 — CSS Battle

## CSS Questions

### Q8. Explain the CSS Box Model.

The box model consists of:

```text
┌──────────────────────┐
│       Margin         │
│  ┌────────────────┐  │
│  │     Border     │  │
│  │ ┌────────────┐ │  │
│  │ │  Padding   │ │  │
│  │ │ ┌────────┐ │ │  │
│  │ │ │Content │ │ │  │
│  │ │ └────────┘ │ │  │
│  │ └────────────┘ │  │
│  └────────────────┘  │
└──────────────────────┘
```

**🔥 Follow-up:**
What does this do?

```css
box-sizing: border-box;
```

---

### Q9. Flexbox vs Grid

**Flexbox:** Best for one-dimensional layouts.

```css
display: flex;
```

**Grid:** Best for two-dimensional layouts.

```css
display: grid;
```

**Interview Challenge:**

> You need a dashboard with sidebar + header + content + cards. Which would you use?

**Expected:** Usually CSS Grid for the overall layout, with Flexbox inside individual components where appropriate.

---

### Q10. `display: none` vs `visibility: hidden`

```css
display: none;
```

Removes the element from the layout.

```css
visibility: hidden;
```

Hides the element but normally keeps its layout space.

**🔥 Follow-up:**
How is `opacity: 0` different?

---

# 🟣 LEVEL 4 — JavaScript Interview

## JavaScript Rapid Fire

### Q11. `var`, `let`, `const`

|           | var      | let   | const |
| --------- | -------- | ----- | ----- |
| Scope     | Function | Block | Block |
| Reassign  | ✅        | ✅     | ❌     |
| Redeclare | ✅        | ❌     | ❌     |
| Modern JS | Avoid    | ✅     | ✅     |

**🔥 Interview Challenge**

What happens?

```js
const user = {
    name: "Sachin"
};

user.name = "Rahul";
```

Can you change the property?

**Answer:** Yes. `const` prevents reassignment of the variable itself; it does not make the object immutable.

---

### Q12. What is a closure?

A closure occurs when an inner function remembers variables from its outer function even after the outer function has finished executing.

```js
function counter() {
    let count = 0;

    return function () {
        count++;
        return count;
    };
}

const increment = counter();

increment(); // 1
increment(); // 2
```

**🔥 Follow-up:**
Where are closures useful in real applications?

---

### Q13. `==` vs `===`

```js
5 == "5"   // true
5 === "5"  // false
```

`==` performs type conversion.

`===` checks both value and type.

**Interview recommendation:** Prefer `===` unless you intentionally need loose equality.

---

### Q14. `map()` vs `filter()` vs `reduce()`

```js
map()
```

Transforms every item.

```js
filter()
```

Returns matching items.

```js
reduce()
```

Combines values into one result.

**Challenge:**

```js
const numbers = [1, 2, 3, 4, 5];
```

Create:

```text
[2, 4, 6, 8, 10]
```

Expected:

```js
numbers.map(num => num * 2);
```

---

# ⚛️ LEVEL 5 — React Interview

## React Fundamentals

### Q15. What is React?

React is a JavaScript library for building user interfaces using reusable components.

Core concepts include:

* Components
* JSX
* Props
* State
* Hooks
* Events
* Conditional rendering
* Lists
* Context
* Routing

**🔥 Follow-up:**
Why do companies use React instead of writing everything with vanilla JavaScript?

---

### Q16. What is JSX?

JSX allows us to write HTML-like syntax inside JavaScript.

```jsx
const element = <h1>Hello World</h1>;
```

JSX is transformed into JavaScript during the build process.

---

### Q17. Props vs State

| Props                  | State                 |
| ---------------------- | --------------------- |
| Passed by parent       | Managed by component  |
| Read-only              | Can change            |
| Used for communication | Used for dynamic data |

Example:

```jsx
<User name="Sachin" />
```

`name` is a prop.

---

### Q18. What is `useState()`?

`useState()` allows a functional component to store and update state.

```jsx
const [count, setCount] = useState(0);
```

Update:

```jsx
setCount(count + 1);
```

**🔥 Follow-up:**
Why shouldn't you directly do this?

```js
count = count + 1;
```

---

### Q19. What is `useEffect()`?

`useEffect()` is used for side effects such as:

* API calls
* Event listeners
* Timers
* Subscriptions
* Synchronizing with external systems

Example:

```jsx
useEffect(() => {
    fetchUsers();
}, []);
```

**🔥 Interview Trap:**
What does `[]` mean?

It means the effect does not re-run because of component state/prop dependencies; on the client it runs after the initial mount.

---

# 🛍️ LEVEL 6 — Shopify Interview

### Q20. What is Shopify?

Shopify is an e-commerce platform that allows businesses to create and operate online stores.

Developers commonly work with:

* Liquid
* HTML
* CSS
* JavaScript
* Shopify themes
* Sections
* Blocks
* Snippets
* Metafields

---

### Q21. What is Shopify Liquid?

Liquid is Shopify's templating language.

Example:

```liquid
{{ product.title }}
```

Conditional:

```liquid
{% if product.available %}
    <button>Add to Cart</button>
{% endif %}
```

---

### Q22. Sections vs Snippets

**Sections**

Reusable/customizable theme components that can be configured through the Shopify theme editor.

**Snippets**

Small reusable Liquid code components.

Example:

```liquid
{% render 'product-card' %}
```

**🔥 Follow-up:**
When would you create a snippet instead of a section?

---

### Q23. What are Shopify metafields?

Metafields allow additional custom data to be stored against Shopify resources.

Examples:

```text
Product → Material
Product → Size Guide
Product → Brand
Product → Custom Specification
```

---

# 🟠 LEVEL 7 — WordPress Interview

### Q24. What is WordPress?

WordPress is an open-source content management system used for websites, blogs, business sites, and e-commerce through extensions such as WooCommerce.

---

### Q25. Theme vs Plugin

**Theme**

Controls the appearance and presentation.

**Plugin**

Adds functionality.

Example:

```text
Theme → Website design
Plugin → Contact form
Plugin → SEO
Plugin → E-commerce
```

---

### Q26. Parent Theme vs Child Theme

A child theme inherits functionality/styles from a parent theme and allows customizations without directly modifying the parent theme.

**🔥 Interview Challenge:**
Why is modifying the parent theme directly risky?

---

# ⚔️ LEVEL 8 — React vs Shopify vs WordPress

## Scenario-Based Questions

### Q27. Client wants a small business website.

Which would you choose?

**Possible answer:**

WordPress can be a strong choice because it provides:

* Fast development
* CMS functionality
* Large ecosystem
* Easy content management

---

### Q28. Client wants a large custom web application.

Which would you choose?

React/Next.js can be appropriate because developers have greater control over application architecture and UI behavior.

---

### Q29. Client wants an online store quickly.

Shopify can be a strong choice because it provides:

* Store infrastructure
* Product management
* Checkout
* Payments integrations
* Theme system
* App ecosystem

---

### Q30. Which requires more custom development?

A highly customized React application generally requires more development work than a standard Shopify/WordPress implementation.

But the correct choice depends on requirements.

---

# 🔥 LEVEL 9 — Real Interview Scenarios

## Scenario 1 — API Problem

> Your React application is calling an API, but the browser returns `401 Unauthorized`. What will you check?

### Expected approach

1. Check API URL
2. Check HTTP method
3. Check authentication token/cookie
4. Check request headers
5. Check CORS
6. Check backend authentication middleware
7. Check browser Network tab
8. Check backend logs

---

## Scenario 2 — React Page Is Slow

> Your React dashboard takes 5 seconds to load. What do you do?

### Expected approach

Check:

* Network requests
* Bundle size
* Large images
* Unnecessary API calls
* Component re-renders
* Expensive calculations
* Lazy loading
* Caching
* Code splitting

---

## Scenario 3 — Mobile UI Broken

> Desktop looks perfect but mobile is broken.

What do you check?

```text
Responsive CSS
↓
Viewport
↓
Media queries
↓
Flex/Grid
↓
Fixed widths
↓
Overflow
↓
Images
↓
Typography
```

---

# 🎤 LEVEL 10 — HR + Technical Questions

### Q31. Tell me about yourself.

Your answer should follow:

```text
Introduction
↓
Education
↓
Technical skills
↓
Projects
↓
Strengths
↓
Career goal
```

**Target duration:** 60–90 seconds.

---

### Q32. Why did you choose React?

A strong answer should mention:

* Component architecture
* Reusability
* Ecosystem
* State management
* Developer productivity
* Industry adoption

Avoid saying only:

> "Because React is popular."

---

### Q33. Tell me about your project.

Use:

```text
Problem
↓
Solution
↓
Technology
↓
Your contribution
↓
Challenge
↓
How you solved it
↓
Result
```

---

# 🧠 LEVEL 11 — Interview Traps

### Q34. Is React a framework?

**Good answer:**

React is primarily a JavaScript library for building user interfaces. Frameworks such as Next.js build additional application capabilities around React.

---

### Q35. Is JavaScript the same as Java?

**No.**

They are different programming languages with different ecosystems and use cases.

---

### Q36. Does `const` make an object immutable?

**No.**

```js
const user = {
    name: "Sachin"
};

user.name = "Rahul";
```

This is allowed.

To prevent mutations, additional techniques such as `Object.freeze()` or immutable update patterns can be used.

---

# ⚡ LEVEL 12 — 30-Second Rapid Fire

Answer each in **30 seconds or less**.

| #  | Question                  |
| -- | ------------------------- |
| 1  | What is DOM?              |
| 2  | What is BOM?              |
| 3  | What is closure?          |
| 4  | What is hoisting?         |
| 5  | What is callback?         |
| 6  | What is Promise?          |
| 7  | What is async/await?      |
| 8  | What is REST API?         |
| 9  | What is JSON?             |
| 10 | What is CORS?             |
| 11 | What is JWT?              |
| 12 | What is localStorage?     |
| 13 | What is sessionStorage?   |
| 14 | What is event delegation? |
| 15 | What is debouncing?       |
| 16 | What is throttling?       |
| 17 | What is Virtual DOM?      |
| 18 | What is reconciliation?   |
| 19 | What is prop drilling?    |
| 20 | What is Context API?      |

---

# 🏆 Final Mock Interview

## Round 1 — Fundamentals

**Interviewer:** What is frontend development?

**You:** Answer in 30–60 seconds.

---

## Round 2 — JavaScript

**Interviewer:** Explain closures with a real-world example.

---

## Round 3 — React

**Interviewer:** Explain the difference between props and state.

---

## Round 4 — API

**Interviewer:** How would you connect a React frontend with a Node.js backend?

---

## Round 5 — Shopify

**Interviewer:** How would you create a customizable Shopify section?

---

## Round 6 — WordPress

**Interviewer:** How would you customize a WordPress theme without directly modifying the parent theme?

---

## Round 7 — Scenario

**Interviewer:** Your website works on Chrome but breaks on Safari. How would you debug it?

---

## Round 8 — Project

**Interviewer:** Explain one project you have built from beginning to end.

---

# 📊 Self-Evaluation

After the mock interview, score yourself:

| Skill           | Score |
| --------------- | ----: |
| HTML            |   /10 |
| CSS             |   /10 |
| JavaScript      |   /10 |
| React           |   /10 |
| APIs            |   /10 |
| Shopify         |   /10 |
| WordPress       |   /10 |
| Git/GitHub      |   /10 |
| Problem Solving |   /10 |
| Communication   |   /10 |

### Score

**80–100:** 🟢 Interview Ready
**60–79:** 🟡 Good — Practice weak areas
**40–59:** 🟠 Need more preparation
**Below 40:** 🔴 Build fundamentals first

---

# 🚀 Final Challenge

Don't memorize answers.

For every technical question, try this structure:

**Definition → Why → Example → Real-world use → Follow-up**

Example:

> **What is React?**

**Definition:** React is a JavaScript library for building user interfaces.

**Why:** It allows developers to build reusable component-based interfaces.

**Example:** A dashboard can be divided into Navbar, Sidebar, Cards and Tables.

**Real-world:** E-commerce, banking dashboards, admin panels, SaaS applications.

**Follow-up:** How does React update the UI efficiently?
