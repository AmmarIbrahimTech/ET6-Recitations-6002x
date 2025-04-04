# Introduction to Dynamic Programming

## 📚 Optimization Problems: Making the Best Choice

In many real-life scenarios, we want to make the *best* decision — whether it's choosing which food to buy with limited calories or selecting the most valuable items to pack into a suitcase with weight restrictions.

This kind of problem is called an **optimization problem**, and they often have one key feature:  
> We want to **maximize** or **minimize** something (like value, calories, or cost), under certain constraints.

---

## 🛠 Brute Force: Try Everything (Literally)

A **brute-force algorithm** tries *every possible combination* of choices to find the best one. For example:

> 🍺 + 🍕 + 🍔 = 1 combo  
> 🍺 + 🍕 = another combo  
> 🍺 alone = another combo  
> ... and so on.

This works, but it's painfully slow when the number of items increases.

- If we have **n** items, brute force checks up to **2ⁿ** combinations.
- That means for 4 items, it checks 16; for 8, it checks 256 — and it explodes from there.

---

## 🌳 Visualizing Brute Force with a Decision Tree

We can draw out the brute-force approach as a **decision tree**:

- Each level of the tree represents a choice: _take_ or _don’t take_ an item.
- Each path down the tree is one combination of decisions.

### Example:

![Search Tree](tree.png)

You can quickly see that many **branches share subproblems** — we're solving the same smaller problems again and again.

---

## 💡 Enter Dynamic Programming

To fix the inefficiency, we use **Dynamic Programming (DP)** — a smarter strategy that:

- **Identifies overlapping subproblems** in the tree.
- **Stores (memoizes)** solutions to these subproblems.
- **Reuses** them instead of recomputing.

This saves **a massive amount of time**, especially for larger inputs.

---

## 🖼 Pictorial View: Why DP Works

The diagram below helps us visualize two key ideas behind DP:

![Overlapping Subproblems and Optimal Substructure](dp_structure.png)

### 🔹 Optimal Substructure (Left Side)
- Shows a **decision tree** breaking down a big problem into smaller subproblems.
- The full solution depends on the **optimal solutions to subparts**.

### 🔹 Overlapping Subproblems (Right Side)
- Highlights how the **same subproblems** are solved repeatedly in different paths.
- DP avoids this by **remembering and reusing results**.

---

## ✅ Why It Matters

With DP, we're not reinventing the wheel every time — we’re remembering past work to move faster and more efficiently. It's like having a cheat sheet for each subproblem — totally legal, and totally powerful!
