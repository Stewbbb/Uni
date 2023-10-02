1. For each of these sentences indicate whether or not they are propositions:  
• The steak is cooked. This is a proposition
• I’m cooking the steak.  This is a proposition
• Is the steak cooked?  This is not a proposition
• This steak is not cooked. This is a proposition



2. Indicate whether the following argument is valid  
(a) If I burn the steak then I won’t be able to eat it  
(b) I haven’t eaten the steak  
(c) Therefore I must have burnt the steak

This is invalid because they could have not burned the steak but also not eaten it yet

3. assessed: Indicate whether the following argument is valid  
(a) If I burn the meal then I won’t be able to eat  
(b) If I don’t eat then I get cranky  
(c) Therefore if burn the meal then I get cranky

This is valid because they burn the meal therefore they cant eat it therefore they get cranky

4. Indicate whether the following argument is valid  
(a) We won’t be eating steak and fries  
(b) Therefore we won’t be eating fries

This is invalid because they could be eating fries on their own without steak

5. Consider the following language for arithmetic expressions that contains a nullary (arity 0) op-  
erator zero, a unary (arity 1) operator succ (successor), a unary operator pred (predecessor), a  
unary operator iszero (is-zero check), a ternary (arity 3) infix operator if-then-else, a nullary  
operator true, and a nullary operator false.  
• Define a BNF for this language. Your BNF should contain a single rule (of the form  
lhs ::= rhs1 | · · · | rhsn).  
• Indicate whether some expressions can be ambiguous.  
• Let e be an arithmetic expression. Using this grammar, write down another expression that  
returns zero if e is zero, and otherwise returns e’s predecessor. In addition, write down the  
parse tree corresponding to this expression.

exp ::= 0 | succ exp | pred exp | iszero exp | if exp then exp else exp | true | false

yes there is ambiguity because it doesn't say whether succ, pred and iszero is left or right associativity, if for example iszero is left associativity iszero exp would be exp iszero which would cause ambiguity
if exp then exp else exp iszero
this would cause a problem because it could be:
if exp then exp else (exp iszero)
(if exp then exp else exp) iszero
which would give different outputs

if iszero e then 0 else pred e

										IF THEN ELSE
										/	|	\
						iszero e     0       pred e


6. Some language also support “if-then” expressions where the infix “if-then” operator takes two  
arguments: a condition and a “then” branch.  
• Add an infix binary (arity 2) “if-then” operator to your language.  
• Indicate whether some expressions can be ambiguous.  
• In case some expressions are ambiguous, write down the parse trees corresponding to two  
different ways an ambiguous expression can be derived

exp ::= 0 | succ exp | pred exp | iszero exp | if exp then exp else exp | true | false | if exp then exp

as said before it is unclear whether the unary operators have right or left associativity

if they have left associativity then
if exp then exp iszero would be ambiguous:
let e be an arithmetic expression
if e then (e iszero)
(if e then e) iszero

						iszero
							|
						if then
							/ \
						 e   e

or 

				if then
				/     \
			e      e iszero



7. To use this language as part of a logical system, we can for example add an equality operator.  
• Add a new rule to your BNF for stating equalities between arithmetic expressions.  
• Define an axiom schema that states that “the expression that given an expression e, checks  
whether e is zero, and if it is returns zero, else returns e’s predecessor” is equal to “e’s  
predecessor”, and indicate which variables are metavariables in your axiom, if any.  
• Provide 2 different instances of this axiom

exp ::= 0 | succ exp | pred exp | iszero exp | if exp then exp else exp | true | false | if exp then exp
eq ::= exp = exp

if iszero e then 0 else pred e = pred e

e is a metavariable

instances:
e=0

0 = -1

e=5
4=4

1. Recover the decimal number from the following signed 8-bits binary representations  
• 00101011  
• 10011110  
• 10011000  
• 10000000

43
-30
-24
0


2. Transform the following decimal numbers into a signed 8-bits binary representation  
• 48  
• 23
• −25  
• −92

00110000
00010111
10011001
11011100


3. In binary, compute the following operations  
• 11010 + 11111  
• 10111 + 11110  
• 10000 − 1111
• 1101 × 101
- 11001
- 10101
- 00001
- 1000001

4. In Java, say that x, y and z are natural number variables, using 4 bytes to store a natural  
number. Currently, x is 2^31 + 5 and y is 2^31 + 2^30 + 5. After executing z = x + y, what is z?
z = 2^30 + 5


5. a. Y
	b. O



