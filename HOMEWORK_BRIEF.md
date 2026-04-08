# Weekly Coding #5: Moonlight Museum Tree Guide

**Topic:** Trees, Traversals, and BST Basics  
**Course:** Data Structures (Python 3.11+)  
**Due:** Friday, 2026-04-10, 23:59 KST  
**Repo structure:**

```text
src/challenges.py
tests/test_challenges.py
README.md
```

## Story
The **Moonlight Museum** is building a small software tool to organize its exhibits.

The museum uses **trees** in two different ways:

1. A **category tree** stores exhibit sections such as `Museum`, `History`, and `Science`.
2. A **binary search tree (BST)** stores exhibit ID numbers so the museum can search and add IDs efficiently.

Your job is to finish the core tree functions in `src/challenges.py`.

---

## Learning targets
This assignment gives evidence for:

- **S1 — Python + Testing Fundamentals**
- **S3 — Big-O Reasoning**
- **S10 — Trees + Traversals + BST Basics**

To reach **Meets (M)**, your work should correctly implement:
- tree traversals
- BST search
- BST insert
- clear README complexity notes
- edge-case thinking

---

## Rules
- Python **3.11+**
- **stdlib only**
- notebooks are allowed for practice, but **not graded**
- graded files are:
  - `src/challenges.py`
  - `tests/test_challenges.py`
  - `README.md`

---

## Your tasks
Implement these functions in `src/challenges.py`.

### 1) `preorder_values(root)`
Return a list of node values in **preorder**.

Preorder order:
- node
- left
- right

### 2) `inorder_values(root)`
Return a list of node values in **inorder**.

Inorder order:
- left
- node
- right

### 3) `postorder_values(root)`
Return a list of node values in **postorder**.

Postorder order:
- left
- right
- node

### 4) `bst_contains(root, target)`
Return `True` if `target` is in the BST. Otherwise return `False`.

### 5) `bst_insert(root, value)`
Insert `value` into the BST and return the root of the tree.

Use this duplicate rule:
- if the value is already in the tree, **do not add a duplicate**

---

## Provided helper
You are given a `TreeNode` class. Use it. Do not replace it with a different structure.

---

## Expected behavior

### Traversals
If the tree is empty, traversal functions should return an empty list.

### BST search
If the tree is empty, `bst_contains` should return `False`.

### BST insert
If the tree is empty, `bst_insert` should create and return a new root node.

---

## Example tree for traversal thinking

```text
        Museum
       /      \
 History      Science
   /   \          \
Art   Maps      Space
```

For this tree:

- Preorder: `Museum, History, Art, Maps, Science, Space`
- Inorder: `Art, History, Maps, Museum, Science, Space`
- Postorder: `Art, Maps, History, Space, Science, Museum`

---

## Example BST for search/insert thinking

```text
        40
       /  \
     20    60
    / \    / \
  10  30  50  70
```

- `bst_contains(root, 50)` should return `True`
- `bst_contains(root, 25)` should return `False`
- inserting `65` should place it as the left child of `70`

---

## README requirements
Your `README.md` must include these sections:

### Summary
3–6 lines explaining what your code does.

### Approach
Short bullet points describing how you implemented the functions.

### Complexity
For each public function, give:
- time complexity
- space complexity
- 1–3 lines of explanation

### Edge-case checklist
Use checkboxes and mention what your code does for cases like:
- empty tree
- single-node tree
- missing target in BST
- duplicate insert value

### Assistance & Sources
Include:
- AI used? (Y/N)
- what it helped with
- any outside sources

---

## Submission checklist
Before you submit:

- [ ] `src/challenges.py` runs without syntax errors
- [ ] `pytest -q` passes
- [ ] `README.md` is filled in, not left as blank template text
- [ ] complexity explanations are included
- [ ] edge cases are mentioned clearly
- [ ] your code is pushed to the correct repo

---

## Hints
- A tree traversal usually has:
  - a **base case** for `None`
  - a **recursive case** that combines results
- BST search does **not** need to visit every node
- BST insert should follow the BST rule until it finds an empty place
- For this assignment, duplicates should be ignored

---

## Complexity reminder
You should be able to explain ideas like these in your README:

- traversal visits every node once
- BST search is often faster than searching a regular binary tree
- tree shape affects BST performance

Be specific. Do not write only `O(n)` or `O(log n)` with no explanation.

---

## Academic integrity
You may discuss ideas and debugging with classmates, but you may not share code.
If you use AI or outside help, record it honestly in the README.
