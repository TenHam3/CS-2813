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

### Tautologies and Contradictions

