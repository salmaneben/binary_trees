# Binary Trees

A comprehensive C implementation of binary trees, binary search trees (BST), AVL trees, and binary heaps. This project implements various tree data structures and their operations, including insertion, deletion, traversal, and tree property validation.

## 📋 Table of Contents

- [Overview](#overview)
- [Data Structures](#data-structures)
- [Features](#features)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Function Reference](#function-reference)
- [Time Complexity](#time-complexity)
- [Testing](#testing)
- [Author](#author)

## 🔍 Overview

This project implements multiple tree data structures in C, following the ALX Software Engineering curriculum. Each implementation includes comprehensive functionality for creating, manipulating, and analyzing various types of binary trees.

### Key Concepts Covered
- Binary Trees fundamentals
- Tree traversal algorithms (preorder, inorder, postorder, levelorder)
- Binary Search Trees (BST)
- AVL Trees (self-balancing BST)
- Binary Heaps (Max Heap implementation)
- Tree rotations and balancing
- Tree properties validation

## 🏗️ Data Structures

### Binary Tree Node Structure
```c
struct binary_tree_s
{
    int n;                          /* Integer stored in the node */
    struct binary_tree_s *parent;   /* Pointer to the parent node */
    struct binary_tree_s *left;     /* Pointer to the left child node */
    struct binary_tree_s *right;    /* Pointer to the right child node */
};
```

### Type Definitions
- `binary_tree_t` - Basic binary tree
- `bst_t` - Binary Search Tree
- `avl_t` - AVL Tree (self-balancing BST)
- `heap_t` - Binary Heap

## ✨ Features

### Basic Binary Tree Operations
- ✅ Node creation and deletion
- ✅ Left and right insertion
- ✅ Tree traversal (preorder, inorder, postorder, level-order)
- ✅ Tree measurements (height, depth, size, leaves, nodes)
- ✅ Tree property checks (leaf, root, full, perfect, complete)
- ✅ Node relationships (sibling, uncle, ancestor)
- ✅ Tree rotations (left, right)

### Binary Search Tree (BST)
- ✅ BST validation
- ✅ Value insertion with BST property maintenance
- ✅ Value search
- ✅ Node removal
- ✅ Array to BST conversion

### AVL Tree (Self-Balancing BST)
- ✅ AVL property validation
- ✅ Balanced insertion with automatic rebalancing
- ✅ Node removal with rebalancing
- ✅ Array to AVL conversion
- ✅ Sorted array to AVL conversion

### Binary Heap (Max Heap)
- ✅ Heap property validation
- ✅ Value insertion maintaining heap structure
- ✅ Root extraction (max value)
- ✅ Array to heap conversion
- ✅ Heap to sorted array conversion

## 📁 Project Structure

```
binary_trees/
├── binary_trees.h              # Header file with all function prototypes
├── binary_tree_print.c         # Tree visualization utility
├── README.md                   # Project documentation
├── tests/                      # Test files directory
│   ├── 0-main.c               # Test for binary_tree_node
│   ├── 1-main.c               # Test for binary_tree_insert_left
│   └── ...                    # Additional test files
│
├── Basic Binary Tree Operations (0-18)
├── 0-binary_tree_node.c        # Create a binary tree node
├── 1-binary_tree_insert_left.c # Insert node as left child
├── 2-binary_tree_insert_right.c # Insert node as right child
├── 3-binary_tree_delete.c      # Delete entire tree
├── 4-binary_tree_is_leaf.c     # Check if node is leaf
├── 5-binary_tree_is_root.c     # Check if node is root
├── 6-binary_tree_preorder.c    # Preorder traversal
├── 7-binary_tree_inorder.c     # Inorder traversal
├── 8-binary_tree_postorder.c   # Postorder traversal
├── 9-binary_tree_height.c      # Calculate tree height
├── 10-binary_tree_depth.c      # Calculate node depth
├── 11-binary_tree_size.c       # Calculate tree size
├── 12-binary_tree_leaves.c     # Count leaf nodes
├── 13-binary_tree_nodes.c      # Count non-leaf nodes
├── 14-binary_tree_balance.c    # Calculate balance factor
├── 15-binary_tree_is_full.c    # Check if tree is full
├── 16-binary_tree_is_perfect.c # Check if tree is perfect
├── 17-binary_tree_sibling.c    # Find sibling node
├── 18-binary_tree_uncle.c      # Find uncle node
│
├── Advanced Binary Tree Operations (100-104)
├── 100-binary_trees_ancestor.c # Find lowest common ancestor
├── 101-binary_tree_levelorder.c # Level-order traversal
├── 102-binary_tree_is_complete.c # Check if tree is complete
├── 103-binary_tree_rotate_left.c # Left rotation
├── 104-binary_tree_rotate_right.c # Right rotation
│
├── Binary Search Tree Operations (110-115)
├── 110-binary_tree_is_bst.c    # Validate BST
├── 111-bst_insert.c            # Insert into BST
├── 112-array_to_bst.c          # Convert array to BST
├── 113-bst_search.c            # Search in BST
├── 114-bst_remove.c            # Remove from BST
├── 115-O                       # BST time complexities
│
├── AVL Tree Operations (120-125)
├── 120-binary_tree_is_avl.c    # Validate AVL tree
├── 121-avl_insert.c            # Insert into AVL tree
├── 122-array_to_avl.c          # Convert array to AVL
├── 123-avl_remove.c            # Remove from AVL tree
├── 124-sorted_array_to_avl.c   # Convert sorted array to AVL
├── 125-O                       # AVL time complexities
│
├── Binary Heap Operations (130-135)
├── 130-binary_tree_is_heap.c   # Validate binary heap
├── 131-heap_insert.c           # Insert into heap
├── 132-array_to_heap.c         # Convert array to heap
├── 133-heap_extract.c          # Extract max from heap
├── 134-heap_to_sorted_array.c  # Convert heap to sorted array
└── 135-O                       # Heap time complexities
```

## 🚀 Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/salmaneben/binary_trees.git
   cd binary_trees
   ```

2. **Compile the project:**
   ```bash
   gcc -Wall -Wextra -Werror -pedantic -std=gnu89 *.c -o binary_trees
   ```

3. **For individual function testing:**
   ```bash
   gcc -Wall -Wextra -Werror -pedantic -std=gnu89 binary_tree_print.c [function_file.c] tests/[test_file.c] -o test
   ./test
   ```

## 💡 Usage

### Basic Example - Creating and Printing a Binary Tree

```c
#include "binary_trees.h"

int main(void)
{
    binary_tree_t *root;

    /* Create root node */
    root = binary_tree_node(NULL, 98);
    
    /* Add children */
    root->left = binary_tree_node(root, 12);
    root->right = binary_tree_node(root, 402);
    
    /* Add more nodes */
    root->left->left = binary_tree_node(root->left, 6);
    root->left->right = binary_tree_node(root->left, 16);
    
    /* Print the tree */
    binary_tree_print(root);
    
    /* Clean up */
    binary_tree_delete(root);
    
    return (0);
}
```

### BST Example

```c
#include "binary_trees.h"

int main(void)
{
    bst_t *tree = NULL;
    int array[] = {79, 47, 68, 87, 84, 91, 21, 32, 34, 2, 20, 22, 98, 1, 62, 95};
    size_t n = sizeof(array) / sizeof(array[0]);

    /* Create BST from array */
    tree = array_to_bst(array, n);
    binary_tree_print(tree);

    /* Search for a value */
    bst_t *node = bst_search(tree, 32);
    if (node)
        printf("Found: %d\n", node->n);

    /* Insert new value */
    bst_insert(&tree, 55);
    binary_tree_print(tree);

    return (0);
}
```

## 📚 Function Reference

### Basic Binary Tree Operations

| Function | Description | Time Complexity |
|----------|-------------|-----------------|
| `binary_tree_node` | Creates a new binary tree node | O(1) |
| `binary_tree_insert_left` | Inserts node as left child | O(1) |
| `binary_tree_insert_right` | Inserts node as right child | O(1) |
| `binary_tree_delete` | Deletes entire binary tree | O(n) |
| `binary_tree_is_leaf` | Checks if node is a leaf | O(1) |
| `binary_tree_is_root` | Checks if node is root | O(1) |
| `binary_tree_preorder` | Preorder traversal | O(n) |
| `binary_tree_inorder` | Inorder traversal | O(n) |
| `binary_tree_postorder` | Postorder traversal | O(n) |
| `binary_tree_levelorder` | Level-order traversal | O(n) |
| `binary_tree_height` | Measures tree height | O(n) |
| `binary_tree_depth` | Measures node depth | O(n) |
| `binary_tree_size` | Counts total nodes | O(n) |
| `binary_tree_leaves` | Counts leaf nodes | O(n) |
| `binary_tree_nodes` | Counts non-leaf nodes | O(n) |
| `binary_tree_balance` | Calculates balance factor | O(n) |
| `binary_tree_is_full` | Checks if tree is full | O(n) |
| `binary_tree_is_perfect` | Checks if tree is perfect | O(n) |
| `binary_tree_is_complete` | Checks if tree is complete | O(n) |
| `binary_tree_sibling` | Finds sibling node | O(1) |
| `binary_tree_uncle` | Finds uncle node | O(1) |
| `binary_trees_ancestor` | Finds lowest common ancestor | O(n) |
| `binary_tree_rotate_left` | Performs left rotation | O(1) |
| `binary_tree_rotate_right` | Performs right rotation | O(1) |

### Binary Search Tree Operations

| Function | Description | Time Complexity |
|----------|-------------|-----------------|
| `binary_tree_is_bst` | Validates BST property | O(n) |
| `bst_insert` | Inserts value into BST | O(log n) average, O(n) worst |
| `bst_search` | Searches for value in BST | O(log n) average, O(n) worst |
| `bst_remove` | Removes value from BST | O(log n) average, O(n) worst |
| `array_to_bst` | Converts array to BST | O(n log n) |

### AVL Tree Operations

| Function | Description | Time Complexity |
|----------|-------------|-----------------|
| `binary_tree_is_avl` | Validates AVL property | O(n) |
| `avl_insert` | Inserts with auto-balancing | O(log n) |
| `avl_remove` | Removes with auto-balancing | O(log n) |
| `array_to_avl` | Converts array to AVL | O(n log n) |
| `sorted_array_to_avl` | Converts sorted array to AVL | O(n) |

### Binary Heap Operations

| Function | Description | Time Complexity |
|----------|-------------|-----------------|
| `binary_tree_is_heap` | Validates heap property | O(n) |
| `heap_insert` | Inserts into max heap | O(log n) |
| `heap_extract` | Extracts maximum value | O(log n) |
| `array_to_heap` | Converts array to heap | O(n) |
| `heap_to_sorted_array` | Converts heap to sorted array | O(n log n) |

## ⏱️ Time Complexity

### BST Operations (115-O)
- **Average case:** O(log n) for search, insert, delete
- **Worst case:** O(n) for unbalanced tree

### AVL Operations (125-O)
- **All cases:** O(log n) for search, insert, delete
- **Guaranteed balanced:** Always maintains O(log n) height

### Heap Operations (135-O)
- **Insert/Extract:** O(log n)
- **Build heap:** O(n)
- **Heap sort:** O(n log n)

## 🧪 Testing

The project includes comprehensive test files in the `tests/` directory:

```bash
# Test basic tree creation
gcc -Wall -Wextra -Werror -pedantic binary_tree_print.c 0-binary_tree_node.c tests/0-main.c -o 0-node
./0-node

# Test BST operations
gcc -Wall -Wextra -Werror -pedantic binary_tree_print.c 0-binary_tree_node.c 111-bst_insert.c tests/111-main.c -o 111-bst_insert
./111-bst_insert

# Test AVL operations
gcc -Wall -Wextra -Werror -pedantic binary_tree_print.c 0-binary_tree_node.c 121-avl_insert.c tests/121-main.c -o 121-avl_insert
./121-avl_insert
```

## 🛠️ Compilation Standards

This project follows strict C89 standards:
- **Compiler:** gcc
- **Flags:** `-Wall -Wextra -Werror -pedantic -std=gnu89`
- **Style:** Betty coding style
- **No global variables**
- **Maximum 5 functions per file**

## 📈 Learning Objectives

After completing this project, you should understand:

- ✅ What is a binary tree and how it differs from a Binary Search Tree
- ✅ Time complexity gains compared to linked lists
- ✅ Tree properties: depth, height, size
- ✅ Different traversal methods and their applications
- ✅ Types of binary trees: complete, full, perfect, balanced
- ✅ AVL trees and automatic balancing mechanisms
- ✅ Binary heaps and priority queue implementation

## 🔧 Requirements

- **Operating System:** Ubuntu 20.04 LTS
- **Compiler:** gcc 9.4.0 or later
- **Language Standard:** C89
- **Memory Management:** All malloc'd memory must be properly freed
- **Code Style:** Betty compliant

## 👨‍💻 Author

**Salman Eben**
- GitHub: [@salmaneben](https://github.com/salmaneben)
- Project: [binary_trees](https://github.com/salmaneben/binary_trees)

## 📄 License

This project is part of the ALX Software Engineering curriculum.

---

**Note:** This implementation follows the ALX project requirements and is designed for educational purposes. All functions are thoroughly tested and follow strict coding standards.
