The grammar of a language often defined using Backus Naur Form (BNF)

BNFs allow context free grammars, rules are independent of context

arity of a symbol is the number of arguments it takes
Fixity of a terminal symbol is where it occurs in arguments:
infix: in middle of arguments
prefix: before arguments
postfix: after arguments


An expression derived from a BNF can be seen as a tree
abstract sytax tree
exp ::=num|exp + exp|exp x exp
		+
	+		2
0		1


Is it (0+1)+2
Or 0+(1+2)

define associativity of terminal symbols
top is left associativity bottom is right

With 0+1x2

Fix precedence
x has higher precedence => 0+(1x2)

Implication is right associativity:
P->(Q->R)

In general an expression of language is only terminal symbols
Non terminal symbols can be used to generalise facts about logic



