# CS-2813

## Logic

Logic is a system based on propositions
A proposition is a statement that is either true or false (not both)
We say that the truth value of a proposition is either true (T) or false (F)

### Statement/Proposition Game
- “Elephants are bigger than mice.”

Is this a statement? Yes

Is this a proposition? Yes

What is the truth value of the proposition? True

- “768 < 111”

Is this a statement? Yes

Is this a proposition? Yes

What is the truth value of the proposition? False

- “Please do not fall asleep in class”

Is this a statement? No, it is a request

Is this a proposition? No, only statements can be propositions

- “Y > 7”

Is this a statement? Yes

Is this a proposition? No

Its truth value depends on the value of y, but this value is not specified. We call this type of statement a propositional function or open sentence

- “Today is August 22 and 99 < 5”

Is this a statement? Yes

Is this a proposition? Yes

What is the truth value of the proposition? False

- “X < y if and only if y > x”

Is this a statement? Yes

Is this a proposition? Yes, because its truth value does not depend on specific values of x and y

What is the truth value of the proposition? True

### Combining Propositions

As we have seen in the previous examples, one or more propositions can be combined to form a single compound proposition
We formalize this by denoting propositions with letters such as p, q, r, and s, and introducing several logical operators/connectives

Logical Operators (Connectives) and Compound Propositions

- Negation (not): ¬ p (sometimes ~)
- Conjunction (and): p ⋀ q
- Disjunction (or): p ⋁ q
- Exclusive or: p ⊕ q
- Implication: p → q
- Biconditional: p ↔ q

## Logic Part II

### Truth Tables

Truth tables are tools that help us define logical operators

| P | ¬ P |
|---|---|
| T | T |  
| T | F |  
| F | T |  
| F | F |  

| P | Q | p ⋀ q |
|---|---|-------|
| T | T | T |
| T | F | F |
| F | T | F |
| F | F | F |

| P | Q | p ⋁ q |
|---|---|-------|
| T | T | T |
| T | F | T |
| F | T | T |
| F | F | F |

Truth tables can be used to show how these operators can combine propositions to compound propositions. They can also help determine if two propositions are logically equivalent by comparing their truth values based on the same truth values for p and q. 

### Implication (if-then)

| P | Q | p → q |
|---|---|-------|
| T | T | T |
| T | F | F |
| F | T | T |
| F | F | T |

Let p and q be propositions. The conditional statement p → q is the proposition "if p, then q." The conditional statement p → q is false when p is true and q is false, and true otherwise. In the conditional statement p → q, p is called the hypothesis (or antecedent or premise) and q is called the conclusion (or consequence). The statement p → q is called a conditional statement because p → q asserts that q is true on the condition that p holds. A conditional statement is also called an **implication.** Note that the statement p → q is true when both p and q are true and when p is false (no matter what truth value q has). **An implication is true exactly when the if-part is false or the then-part is true.** When evaluating an implication, the statement is primarily focused on what happens if p is true. If p is true, it implies q, meaning that q will be true. However, an implication doesn't mention what would happen if p were false so anytime p is false, the implication evaluates to true since there were no specifications on q's truth value if p were false. 

![image](https://github.com/TenHam3/CS-2813/assets/109705811/2ca52aec-33ad-4671-ad3b-16d8dcb4600c)

#### Converse, Inverse, and Contrapositive

- Converse: q → p
- Inverse: ¬p → ¬q
- Contrapositive: ¬q → ¬p

Ex: What are the contrapositive, converse, and inverse of the conditional statement: "The home team wins whenever it is raining?"

- Rewrite as an if-then statement
    - If it is raining, then the home team wins (p → q)
 
### Biconditional (if and only if)

| P | Q | p ↔ q |
|---|---|-------|
| T | T | T |
| T | F | F |
| F | T | F |
| F | F | T |

### Precedence of Logical Operators

![image](https://github.com/TenHam3/CS-2813/assets/109705811/8d532d0c-a35d-424c-9de2-7f8bbdd5e1aa)

### Logical Equivalance

![image](https://github.com/TenHam3/CS-2813/assets/109705811/ae7b897b-455d-401c-9e30-9ce30a120e2f)

![image](https://github.com/TenHam3/CS-2813/assets/109705811/0a2e9e02-6993-45a2-84d8-d6589eebe7ee)

### Tautologies and Contradictions

A **tautology** is a statement that is always true 
Ex: 
- R ⋁ (¬R)
- ¬(P ⋀ Q) ↔ (¬P) ⋁ (¬Q)
To denote equivalance, we use the symbol ≡ (Not an operator!)

A **contradiction** is a statement that is always false


The negation of any tautology is a contradiction, and the negation of any contradiction is a tautology

Ex: Show that ¬(p OR (¬p AND q)) and ¬p AND ¬q are logically equivalent by developing a series of logical equivalencies
- Solution: We can form a truth table
- Solution Strategy II: use the equivalence laws and equivalences from previous tables, one at a time, starting with ¬(p OR (¬p AND q)) and ending with ¬p AND ¬q

![image](https://github.com/TenHam3/CS-2813/assets/109705811/06b2a3af-828f-49c0-8335-dc6a13ff5c02)

### Propositional Functions

A propositional function (open sentence) is a statement involving one or more variables

Ex: x - 3 > 5

- Lets us call this propositional function P(x), where P is the predicate and x is the variable

What is the truth value of P(2)? False
What is the truth value of P(8)? False
What is the truth value of P(9)? True

- Let us consider the propositional function Q(x, y, z) as:
- $x + y = z$
- Here, Q is the predicate and x, y, and z are variables

#### Universal Quantification
Let P(x) be a propositional function. Universally quantified sentence: For all x in the universe of discourse (domain) P(x) is true.

Using the universal quantifier ∀: 
- ∀x P(x) "for all x P(x)" or "for every x P(x)"
- Note: ∀x P(x) is either true or false, so it is a proposition, not a propositional function

Ex: 
- S(x): x is an OU student
- G(x): x is a genius

What does ∀x (S(x) → G(x)) mean?
- "If x is a UMBC student, then x is a genius" or
- "All UMBC students are geniuses"

#### Existential Quantification
Existentially quantified setnece: There exists an x in the universe of discourse for which P(x) is true

Using the existential quantifier ∃:
∃x P(x) "There is an x such that P(x)" or "There is at least one x such that P(x)"
- Note: ∃x P(x) is either true or false, so it is a proposition, but no propositional function

Ex: 
- P(x): x is a OU professor
- G(x): x is a genius

What does ∃x (P(x) AND G(x)) mean? 
- "There is an x such that x is a UMBC professor and x is a genius" or
- "At least one UMBC professor is a genius"

Quantification Example
Let the universe of discourse be all real numbers. What does ∀x∃y (x + y = 320) mean?
- "For every x there exists a y so that x + y = 320"

- Is it true? Yes
- Is it true for the natural numbers? No

#### Disproof by Counterexample
- A counterexample to ∀x (Px) is an object c so that P(c) is false
- Statements such as ∀x (P(x) → Q(x)) can be disproved by simply providing a counterexample
  - Statement: "All birds can fly"
  - Disproved by counterexample: Penguin
 
#### Negation of Quantifiers
- ¬(∀x (Px)) is logically equivalent to ∃x (¬P(x)).
- ¬(∃x P(x)) is logically equivalent to ∀x (¬P(x)).

## Set Theory

Set: unordered collection of objects ("elements")
- a∈ A "a is an element of A"
- a∉ A "a is not an element of A"
- A = {a<sub>1</sub>, a<sub>2</sub>, ..., a<sub>n</sub>} "A contains..."
- Order of elements is meaningless
- It does not matter how often the same element is listed (when listing what elements are in the set, you only name each element once, no duplicates)

### Set Equality

Sets A and B are equal if and only if they contain exactly the same elements
Ex: 
- A = {9, 2, 7, -3}, B = {7, 9, -3, 2} A = B
- A = {dog, cat, horse}, B = {cat horse, squirrel, dog} A != B
- A = {dog, cat, horse}, B = {cat, horse, dog, dog} A = B

Examples for Sets
- "Standard" Sets:
- Natural Numbers **N** = {0, 1, 2, 3, ...}
- Integers **Z** = {-2, -1, 0, 1, 2, ...}
- Positive Integers **Z<sup>+</sup>** = {1, 2, 3, ...}
- Real Numbers **R** = {47.3, -12, $\pi$, ...}
- Rational Numbers **Q** = {1.5, 2.6, -3.8, 15, ...}

- A = ∅ (empty/null set)
- A = {z}
    - Note: z∈ A, but z ≠ {z}
- A = {{b, c}, {c, x, d}}
- A = {{x, y}}
  - Note: {x, y} ∈ A, but {x, y} ≠ {{x, y}}
- A = {x | P(x)} (set of all x such that P(x))
- A = {x | x∈ N AND x > 7} = {8, 9, 10, ...} (this is set builder notation)

### Subsets
- A ⊆ B (A is a subset of B)
- A ⊆ B if and only if every element of A is also an element of B
- We can formalize this as A ⊆ B ↔ ∀x(x∈A → x∈B)

#### Useful Rules for Subsets
- A = B ↔ (A ⊆ B) AND (B ⊆ A)
- (A ⊆ B) AND (B ⊆ C) → A ⊆ C
- ∅ ⊆ A for any set A
- A ⊆ A for any set A

#### Proper Subsets:
- A ⊂ B "A is a proper subset of B"

![image](https://github.com/TenHam3/CS-2813/assets/109705811/455c51e4-cbb8-46e6-8838-3faf62571401)

#### Cardinality of Sets
- If a set S contains n distinct elements, n∈ N, we call S a **finite set** with **cardinality n.**
Ex:
- A = {Mercedes, BMW, Porsche}, |A| = 3
- B = {1, {2, 3}, {4, 5}, 6} |B| = 4
- C = |C| = 0
- D = { x ∈ N | x <= 7000} |D| = 7001
- E = { x ∈ N | x > 7000} E is infinite

![image](https://github.com/TenHam3/CS-2813/assets/109705811/e4501707-1853-49ef-9600-7b7867fd1893)

- Since both sets have infinite elements, their cardinalities are infinity. However, even though it may seem that the first set would have twice the amount of elements as the second set, they actually have the same cardinality because you can match an element of the first set to the second set by multiplying it by two. This can continue for infinity so you can always have a one-to-one pairing with elements from both sets.

Cardinality of Finite Sets
- The cardinality of the set
- N<sub>k</sub> = {n | n ∈ N AND n < k} is k
- If there is a bijection between two sets, they have the same cardinality

#### The Power Set
- P(A) "Power set of A"
- P(A) = {B | B ⊆ A} (contains all subsets of A)
Ex:
- A = {x, y, z}
- P(A) = {∅, {x}, {y}, {z}, {x, y}, {x, z}, {y, z}, {x, y, z}}

- A = ∅
- P(A) = {∅}
- Note: |A| = 0, |P(A)| = 1

Cardinality of Power Sets:
- |P(A)| = 2<sup>|A|</sup>
- Imagine each element in A has an "on/off" switch
- Each possible switch configuration in A corresponds to one element in 2<sup>A</sup>

![image](https://github.com/TenHam3/CS-2813/assets/109705811/1b38b5fe-9b62-4ce9-91e6-1426f777bb0b)

#### Cartesian Product
- The ordered n-tuple (a<sub>1</sub>, a<sub>2</sub>, a<sub>3</sub>, ..., a<sub>n</sub>) is an ordered collection of objects
- Two ordered n-tuples (a<sub>1</sub>, a<sub>2</sub>, a<sub>3</sub>, ..., a<sub>n</sub>) and (b<sub>1</sub>, b<sub>2</sub>, b<sub>3</sub>, ..., b<sub>n</sub>) are equal if and only if they contain exactly the same elements in the same order, i.e. a<sub>i</sub> = b<sub>i</sub> for 1 <= i <= n. 
- The Cartesian Product of two sets is defined as:
- A X B = {(a, b) | a∈ A AND b∈ B} ≠ B X A
Ex: A = {x, y}, B = {a, b, c}
A X B = {(x, a), (x, b), (x, c), (y, a), (y, b), (y, c)}

![image](https://github.com/TenHam3/CS-2813/assets/109705811/22e3b43c-0c8f-4d2f-845e-5b94bc50712a)

Note that:
- A X ∅ = ∅
- ∅ X A = ∅
- For non-empty sets A and B: A ≠ B ↔ (A X B ≠ B X A)
- |A X B| = |A| * |B|

The Cartesian Product of two or more sets is defined as:
A<sub>1</sub> X A<sub>2</sub> X ... X A<sub>n</sub> = {(a<sub>1</sub>, a<sub>2</sub>, ..., a<sub>n</sub>) | a<sub>i</sub> ∈ A for 1 <= i <= n}

#### Set Operations
- Union: A ∪ B = {x | x∈ A OR x∈ B}
- Ex: A = {a, b}, B = {b, c, d}
    - A ∪ B = {a, b, c, d}
- Intersection: A ∩ B = {x | x∈ A AND x∈ B}
- Ex: A = {a, b}, B = {b, c, d}
    - A ∩ B = {b}

- Two sets are called disjoint if their intersection is empty, that is, they share no elements:
- A ∩ B = ∅
- The difference between two sets A and B contains exactly those elements of A that are not in B:
- A - B = {x | x∈ A AND x∉ B}
- Ex: A = {a, b}, B = {b, c, d}, A - B = {a}

The complement of a set A contains exactly those elements under consideration that are not in A:
- A<sup>c</sup> = U - A (can also be denoted with A with a bar/line over it)
- Ex: U = N, B = {250, 251, 252, ...}
    - $B<sup>c</sup> = {0, 1, 2, ..., 248, 249}

#### Set Identities

![image](https://github.com/TenHam3/CS-2813/assets/109705811/da2355c2-802c-4db5-afd7-8df3c13230e0)

#### Proving Set Equivalence

![image](https://github.com/TenHam3/CS-2813/assets/109705811/c42b7387-0232-4331-9d6a-baa1883b0572)

![image](https://github.com/TenHam3/CS-2813/assets/109705811/c85c588e-5c94-41da-824f-57c36ee663f2)

## Algorithms

An algorithm is a finite set of precise instructions for performing a computation or solving a problem

Properties of Algorithms:
- input from a specified set
- output from a specified set (solution)
- definiteness of every step in the computation
- correctness of output for every possible input
- finiteness of the number of calculation steps
- effectiveness of each calculation step
- generality for a class of problems

Ex: an algorithm that finds the maximum element in a finite sequence

Set the first element as the max and iterate through the entire data set comparing each element to the current max. If the current element is larger than the current max, assign it to the max.

![image](https://github.com/TenHam3/CS-2813/assets/109705811/3348a2f7-04ad-431c-b610-73e6f17d88fa)

Ex: a linear search algorithm, that is, an algorithm that linearly searches a sequence for a particular element.

Iterate through each element and compare the current element to the target value. If they are equal, the element is found and you return the position where it's located. If you iterate through all elements, the element is not in the data set and you return an invalid index. Since in the worst case scenario you have to iterate through n elements, the efficiency or time complexity of it can be described as O(n) or (c * n) (<- said as order of n).

![image](https://github.com/TenHam3/CS-2813/assets/109705811/ab40e027-f36f-4c4c-91b4-8598847fce71)

### Binary Search

![image](https://github.com/TenHam3/CS-2813/assets/109705811/0705cc71-57b2-46e8-99bd-d670eb565c40)

### Sorting Algorithms

Ordering a list of elements

#### Bubble Sort

The largest elements bubble their way to the top (end) of the array each iteration of the outer loop

![image](https://github.com/TenHam3/CS-2813/assets/109705811/efa48036-2af8-4838-b153-76aef44d8385)

## Functions

a **function** f from a set A to a set B is an **assignment** of **exactly one** element of B to each element of A
We write
- f(a) = b
- if b is the unique element of B assigned by the function f to the element a of A
- If if is a function from A to B, we write
- f: A->B
- (note: Here, "->" has nothing to do with if... then)

- If f: A->B, we say that A is the **domain** of f and B is the **codomain** of f
- If f(a) = b, we say that b is the **image** of a and a is the pre-image of b
- The **range** of f: A->B is the set of all images of elements of A
- We say that f: A->B **maps** A to B

Let us take a look at the function f: P->C with 
- P = {Linda, Max, Kathy, Peter}
- C = {Boston, New York, Hong Kong, Moscow}

- f(Linda) = Moscow
- f(Max) = Boston
- f(Kathy) = Hong Kong
- f(Peter) = New York
- Here, the range of f is C

Let us respecify f as follows:
- f(Linda) = Moscow
- f(Max) = Boston
- f(Kathy) = Hong Kong
- f(Peter) = Boston
- Is f still a function? Yes
- What is its range? {Moscow, Boston, Hong Kong}

Other ways to represent f:

![image](https://github.com/TenHam3/CS-2813/assets/109705811/54065781-ecba-44a4-b2ea-070ec8cf4751)


If the domain of our function f is large, it is convenient to specify f with a formula, e.g.:
- f: R->R
- f(x) = 2x
This leads to 
- f(1) = 2
- f(3) = 6
- f(-3) = -6

Let f1 and f2 be functions from A to R. Then the **sum** and the **product** of f1 and f2 are also functions from A to R defined by:
- (f1 + f2)(x) = f1(x) + f2(x)
- (f1f2)(x) = f1(x)f2(x)

![image](https://github.com/TenHam3/CS-2813/assets/109705811/d2224ed8-b3d5-4112-bd6f-791faeae0dd1)

We already know that the **range** of a function f: A->B is the set of all images of elements a∈A.

If we only regard a **subset** S⊆A, the set of all images of elements s∈S is called **image** of S
- We denote the image of S by f(S):
- f(S) = {f(s) | s∈S}

Let us look at the well known function: 
- f(Linda) = Moscow
- f(Max) = Boston
- f(Kathy) = Hong Kong
- f(Peter) = Boston

What is the image of S = {Linda, Max}?
- f(S) = {Moscow, Boston}

What is the image of S = {Max, Peter}
- f(S) = {Boston}

### Properties of Functions
A function f: A->B is said to be **one-to-one** (or **injective**) if and only if 
- ∀x, y∈A (f(x) = f(y) -> x = y)
- In other words, f is one-to-one if and only if it does not map two distinct elements of A onto the same element of B

A function f: A->B with A, B ⊆ R is called **strictly increasing** if
- ∀x, y∈A (x < y -> f(x) < f(y)) and **strictly decreasing** if
- ∀x, y∈A (x < y -> f(x) > f(y))
- Obviously, a function that is either strictly increasing or strictly decreasing is **one-to-one**

A function f: A->B is said to be **onto** (or **surjective**) if and only if for every element b∈B there is an element a∈A with f(a) = b
- In other words, f is onto if and only if its **range** is its **entire codomain**

A function f: A->B is a one-to-one correspondence, or a bijection, if and only if it is both one-to-one and onto
Obviously, if f is a bijection, and A and B are finite sets, then |A| = |B|
#### Inversion

An interesting property of bijections is that they have an inverse function

The inverse function of the bijection f: A->B is the function $f^{-1}$: B->A with $f^{-1}$(b) = a whenever f(a) = b

![image](https://github.com/TenHam3/CS-2813/assets/109705811/b8f231cd-e82f-4039-ba28-6dd796bfbb18)

#### Composition

The **composition** of two functions g: A->B and f: B->C denoted by f∘g, is defined by:
- (f∘g)(a) = f(g(a))
This means that
- first, function g is applied to element a∈A, mapping it onto an element of B,
- then the function f is applied to this element of B, mapping it onto an element of C
- Therefore, the composite function maps from A to C

The composite of a function and its inverse:
- ($f^{-1}$∘f)(x) = $f^{-1}$(f(x)) = x
- The composite of a function and its inverse is the **identity function** i(x) = x

