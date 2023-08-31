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
- A = {
- A

Examples for Sets
- "Standard" Sets:
- Natural Numbers N =
- Integers Z =
- Positive Integers Z<sup>+</sup> = 
- Real Numbers R = 
- Rational Numbers Q =

- A = ∅ (empty/null set)
- A = {z}
    - Note: zE A, but z != {z}
- A = {{b, c}, {c, x, d}}
- A = {{x, y}}
  - Note: {x, y} E A, but {x, y} != {{x, y}}
- A

### Subsets
- A ⊆ B (A is a subset of B)
- A ⊆ B if and only if every element of A is also an element of B
