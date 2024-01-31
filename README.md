![image](https://github.com/gebre-a/binary_trees/assets/138770113/5ad2b9ee-7812-4474-a816-191d63ae6393)

# **Table of Contents**
- [**Learning Objectives**](#learning-objectives)
- [**Requirements**](#requirements)
- [**More Info Data structures**](#more-info-data-structures)
-  [**Lists of tasks and solutions**](#list)
      - [**Task 0 New node**](#task-0-new-node)
      - [**Task 1 Insert left**](#task-1-insert-left)
      - [**Task 2 Insert right**](#task-2-insert-right)
      - [**Task 3 Delete**](#task-3-delete)
      - [**Task 4 Is leaf**](#task-4-is-leaf)
      - [**Task 5 Is root**](#task-5-is-root)
      - [**Task 6 Pre-order traversal**](#task-6-pre-order-traversal)
      - [**Task 7 In-order traversal**](#task-7-in-order-traversal)
      - [**Task 8 Post-order traversal**](#task-8-post-order-traversal)
      - [**Task 9 Height**](#task-9-height)
      - [**Task 10 Depth**](#task-10-depth)
      - [**Task 11 Size**](#task-11-size)
      - [**Task 12 Leaves**](#task-12-leaves)
      - [**Task 13 Nodes**](#task-13-nodes)
      - [**Task 14 Balance factor**](#task-14-balance-factor)
      - [**Task 15 Is full**](#task-15-is-full)
      - [**Task 16 Is perfect**](#task-16-is-perfect)
      - [**Task 17 Sibling**](#task-17-sibling)
      - [**Task 18 Uncle**](#task-18-uncle)
- [**Resources: Read or watch**](#resources:-read-or-watch)












## [**Learning Objectives**] <a name="learning-objectives"></a>

At the end of this project, you are expected to be able to explain to anyone, without the help of Google:
~~~
General
What is a binary tree
What is the difference between a binary tree and a Binary Search Tree
What is the possible gain in terms of time complexity compared to linked lists
What are the depth, the height, the size of a binary tree
What are the different traversal methods to go through a binary tree
What is a complete, a full, a perfect, a balanced binary tree
~~~

## [**Requirements**] <a name="requirements"></a>

General
~~~
Allowed editors: vi, vim, emacs
All your files will be compiled on Ubuntu 20.04 LTS using gcc, using the options -Wall -Werror -Wextra -pedantic -std=gnu89
All your files should end with a new line
A README.md file, at the root of the folder of the project, is mandatory
Your code should use the Betty style. It will be checked using betty-style.pl and betty-doc.pl
You are not allowed to use global variables
No more than 5 functions per file
You are allowed to use the standard library
In the following examples, the main.c files are shown as examples. You can use them to test your functions, but you don’t have to push them to your repo (if you do we won’t take them into account). We will use our own main.c files at compilation. Our main.c files might be different from the one shown in the examples
The prototypes of all your functions should be included in your header file called binary_trees.h
Don’t forget to push your header file
All your header files should be include guarded
~~~
GitHub
~~~
There should be one project repository per group. If you clone/fork/whatever a project repository with the same name before the second deadline, you risk a 0% score.
~~~
## [**More Info Data structures**] <a name="more-info-data-structures"></a>

Please use the following data structures and types for binary trees. Don’t forget to include them in your header file.
~~~
Basic Binary Tree
/**
 * struct binary_tree_s - Binary tree node
 *
 * @n: Integer stored in the node
 * @parent: Pointer to the parent node
 * @left: Pointer to the left child node
 * @right: Pointer to the right child node
 */
struct binary_tree_s
{
    int n;
    struct binary_tree_s *parent;
    struct binary_tree_s *left;
    struct binary_tree_s *right;
};

typedef struct binary_tree_s binary_tree_t;
~~~
Binary Search Tree
> typedef struct binary_tree_s bst_t;
AVL Tree
> typedef struct binary_tree_s avl_t;
Max Binary Heap
> typedef struct binary_tree_s heap_t;

Note: For tasks 0 to 23 (included), you have to deal with simple binary trees. They are not BSTs, thus they don’t follow any kind of rule.

Print function
To match the examples in the tasks, you are given this function
> This function is used only for visualization purposes. You don’t have to push it to your repo. It may not be used during the correction

## [**Lists of tasks and solutions**] <a name="list"></a>

## [**Task 0 New node**] <a name="task-0-new-node"></a> ................................... [Go to answer](0-binary_tree_node.c)
~~~
Write a function that creates a binary tree node

Prototype: binary_tree_t *binary_tree_node(binary_tree_t *parent, int value);
Where parent is a pointer to the parent node of the node to create
And value is the value to put in the new node
When created, a node does not have any child
Your function must return a pointer to the new node, or NULL on failure
~~~
## [**Task 1 Insert left**] <a name="task-1-insert-left"></a> ............................[Go to answer](1-binary_tree_insert_left.c)
~~~
Write a function that inserts a node as the left-child of another node

Prototype: binary_tree_t *binary_tree_insert_left(binary_tree_t *parent, int value);
Where parent is a pointer to the node to insert the left-child in
And value is the value to store in the new node
Your function must return a pointer to the created node, or NULL on failure or if parent is NULL
If parent already has a left-child, the new node must take its place, and the old left-child must be set as the left-child of the new node.
~~~
## [**Task 2 Insert right**] <a name="task-2-insert-right"></a>  ............................[Go to answer](2-binary_tree_insert_right.c)
~~~
Write a function that inserts a node as the right-child of another node

Prototype: binary_tree_t *binary_tree_insert_right(binary_tree_t *parent, int value);
Where parent is a pointer to the node to insert the right-child in
And value is the value to store in the new node
Your function must return a pointer to the created node, or NULL on failure or if parent is NULL
If parent already has a right-child, the new node must take its place, and the old right-child must be set as the right-child of the new node.
~~~
##  [**Task 3 Delete**] <a name="task-3-delete"></a>  ............................[Go to answer](3-binary_tree_delete.c)
~~~
Write a function that deletes an entire binary tree

Prototype: void binary_tree_delete(binary_tree_t *tree);
Where tree is a pointer to the root node of the tree to delete
If tree is NULL, do nothing
~~~
## [**Task 4 Is leaf**] <a name="task-4-is-leaf"></a>  ............................[Go to answer](4-binary_tree_is_leaf.c)
~~~
Write a function that checks if a node is a leaf

Prototype: int binary_tree_is_leaf(const binary_tree_t *node);
Where node is a pointer to the node to check
Your function must return 1 if node is a leaf, otherwise 0
If node is NULL, return 0
~~~
## [**Task 5 Is root**] <a name="task-5-is-root"></a>  ............................[Go to answer](5-binary_tree_is_root.c)
~~~
Write a function that checks if a given node is a root

Prototype: int binary_tree_is_root(const binary_tree_t *node);
Where node is a pointer to the node to check
Your function must return 1 if node is a root, otherwise 0
If node is NULL, return 0
~~~
## [**Task 6 Pre-order traversal**] <a name="task-6-pre-order-traversal"></a>  ............................[Go to answer](6-binary_tree_preorder.c)
~~~
Write a function that goes through a binary tree using pre-order traversal

Prototype: void binary_tree_preorder(const binary_tree_t *tree, void (*func)(int));
Where tree is a pointer to the root node of the tree to traverse
And func is a pointer to a function to call for each node. The value in the node must be passed as a parameter to this function.
If tree or func is NULL, do nothing
~~~
## [**Task 7 In-order traversal**] <a name="task-7-in-order-traversal"></a>  ............................[Go to answer](7-binary_tree_inorder.c)
~~~
Write a function that goes through a binary tree using in-order traversal

Prototype: void binary_tree_inorder(const binary_tree_t *tree, void (*func)(int));
Where tree is a pointer to the root node of the tree to traverse
And func is a pointer to a function to call for each node. The value in the node must be passed as a parameter to this function.
If tree or func is NULL, do nothing
~~~
##  [**Task 8 Post-order traversal**] <a name="task-8-post-order-traversal"><a/>  ............................[Go to answer](8-binary_tree_postorder.c)
~~~
Write a function that goes through a binary tree using post-order traversal

Prototype: void binary_tree_postorder(const binary_tree_t *tree, void (*func)(int));
Where tree is a pointer to the root node of the tree to traverse
And func is a pointer to a function to call for each node. The value in the node must be passed as a parameter to this function.
If tree or func is NULL, do nothing
~~~
## [**Task 9 Height**] <a name="task-9-height"></a>  ............................[Go to answer](9-binary_tree_height.c)
~~~
Write a function that measures the height of a binary tree

Prototype: size_t binary_tree_height(const binary_tree_t *tree);
Where tree is a pointer to the root node of the tree to measure the height.
If tree is NULL, your function must return 0
~~~
## [**Task 10 Depth**] <a name="task-10-depth"></a>  ............................[Go to answer](10-binary_tree_depth.c)
~~~
Write a function that measures the depth of a node in a binary tree

Prototype: size_t binary_tree_depth(const binary_tree_t *tree);
Where tree is a pointer to the node to measure the depth
If tree is NULL, your function must return 0
~~~
## [**Task 11 Size**] <a name="task-11-size"></a>  ............................[Go to answer](11-binary_tree_size.c)
~~~
Write a function that measures the size of a binary tree

Prototype: size_t binary_tree_size(const binary_tree_t *tree);
Where tree is a pointer to the root node of the tree to measure the size
If tree is NULL, the function must return 0
~~~
## [**Task 12 Leaves**] <a name="task-12-leaves"></a>  ............................[Go to answer](12-binary_tree_leaves.c)
~~~
Write a function that counts the leaves in a binary tree

Prototype: size_t binary_tree_leaves(const binary_tree_t *tree);
Where tree is a pointer to the root node of the tree to count the number of leaves
If tree is NULL, the function must return 0
A NULL pointer is not a leaf
~~~
## [**Task 13 Nodes**] <a name="task-13-nodes"></a>  ............................[Go to answer](13-binary_tree_nodes.c)
~~~
Write a function that counts the nodes with at least 1 child in a binary tree

Prototype: size_t binary_tree_nodes(const binary_tree_t *tree);
Where tree is a pointer to the root node of the tree to count the number of nodes
If tree is NULL, the function must return 0
A NULL pointer is not a node
~~~
## [**Task 14 Balance factor**] <a name="task-14-balance-factor"></a>  ............................[Go to answer](14-binary_tree_balance.c)
~~~
Write a function that measures the balance factor of a binary tree

Prototype: int binary_tree_balance(const binary_tree_t *tree);
Where tree is a pointer to the root node of the tree to measure the balance factor
If tree is NULL, return 0
~~~
## [**Task 15 Is full**] <a name="task-15-is-full"></a>  ............................[Go to answer](15-binary_tree_is_full.c)
~~~
Write a function that checks if a binary tree is full

Prototype: int binary_tree_is_full(const binary_tree_t *tree);
Where tree is a pointer to the root node of the tree to check
If tree is NULL, your function must return 0
~~~
## [**Task 16 Is perfect**] <a name="task-16-is-perfect"></a>  ............................[Go to answer](16-binary_tree_is_perfect.c)
~~~
Write a function that checks if a binary tree is perfect

Prototype: int binary_tree_is_perfect(const binary_tree_t *tree);
Where tree is a pointer to the root node of the tree to check
If tree is NULL, your function must return 0
~~~
## [**Task 17 Sibling**] <a name="task-17-sibling"></a>  ............................[Go to answer](17-binary_tree_sibling.c)
~~~
Write a function that finds the sibling of a node

Prototype: binary_tree_t *binary_tree_sibling(binary_tree_t *node);
Where node is a pointer to the node to find the sibling
Your function must return a pointer to the sibling node
If node is NULL or the parent is NULL, return NULL
If node has no sibling, return NULL
~~~
## [**Task 18 Uncle**] <a name="task-18-uncle"></a>  ............................[Go to answer](18-binary_tree_uncle.c)
~~~
Write a function that finds the uncle of a node

Prototype: binary_tree_t *binary_tree_uncle(binary_tree_t *node);
Where node is a pointer to the node to find the uncle
Your function must return a pointer to the uncle node
If node is NULL, return NULL
If node has no uncle, return NULL
~~~

## [**Resources: Read or watch**] <a name="resources:-read-or-watch"></a>
[Binary tree](https://intranet.alxswe.com/rltoken/1F2x42-8vUbOmU4L1C1KMg)
[Data Structure and Algorithms - Tree](https://intranet.alxswe.com/rltoken/QmcTMCkQyrgMjrqoWxYdhw)
[Tree Traversal](https://intranet.alxswe.com/rltoken/z6ZaXr_RxwE5nTHAUx_dfQ)
[Binary Search Tree](https://intranet.alxswe.com/rltoken/qO5dBlMnYJzbaWG3xVpcnQ)
[Data structures: Binary Tree](https://intranet.alxswe.com/rltoken/BeyJ2gjlE7_djwRiDyeHig)



