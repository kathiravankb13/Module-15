# Ex. No: 15B - Build a Binary Search Tree Using Built-in Function

## AIM:
To write a Python program to build a binary search tree using a built-in function.

---

## ALGORITHM:

1. **Start the program.**
2. Define `_build_bst_from_sorted_values(sorted_values)` to recursively build a binary search tree (BST) from a sorted list.
3. Define `left_subtree(l)` to print the left subtree of the BST.
4. Take user input for the number of elements and store the values in a list `a`.
5. Sort the list and pass it to `_build_bst_from_sorted_values()` to construct the BST.
6. Print the postorder traversal of the BST.
7. Call `left_subtree(l)` to print the left subtree.
8. Check whether the tree is a binary search tree using the `is_bst` property.
9. **End the program.**

---

## PROGRAM:

```
from binarytree import Node
def _build_bst_from_sorted_values(l):
    if len(l) == 0:
        return None
    mid = len(l)//2
    root = Node(l[mid])
    root.left = _build_bst_from_sorted_values(l[:mid])
    root.right = _build_bst_from_sorted_values(l[mid+1:])
    return (root)
    
b = int(input())
a = []
for i in range(b):
    s = int(input())
    a.append(s)
k = _build_bst_from_sorted_values(sorted(a))
print(k.postorder)
print(k.is_bst)

```

## OUTPUT
![image](https://github.com/user-attachments/assets/468befb5-0d2a-43ef-a903-de63b677c1e8)

## RESULT
Thus the Python program to build a binary search tree using a built-in function is verified successfully.
