## EX NO:07
## DATE:23.6.22
# <p align="center">Inferencing Propositional Logic Sentences

## AIM

To develop python code to inference propositional logic sentences to solve Wumpus World problem.

## THEORY
The Wumpus World's agent is an example of a knowledge-based agent that represents Knowledge representation, reasoning , and planning. A Knowledge-Based agent links general knowledge with current percepts to infer hidden characters of the current state before selecting actions.

## DESIGN STEPS
## STEP 1:
Importing required logical and utils files.

## STEP 2:
Defining a knowledge base class with functions on a python file.

## STEP 3:
creating a new knowledge base for agent, with a function called propKB().

## STEP 4:
Mentioning the labels in the wumpus game cell for location in the function of expressions.

## STEP 5:
Using wumpus_kb.tell() to define the environment of the wumpus game.

## STEP 6:
Using propositional Logic defines the possibility of agent's next move.

## STEP 7:
Using wumpus_kb.ask_if_true() to get the result based on TRUE value.

## PROGRAM
```python
from utils import *
from logic import *
char=['P','B','W','S']
abc=''
ind=[1,2,3,4]
for i in char:
    for x in ind:
        for y in ind:
            abc= abc+(str(i)+str(x)+str(y))+','
abc= abc[0:-1]
abc
wumpus_kb = PropKB()
P11, P12, P21, P22, P31, B11, B21 = expr('P11, P12, P21, P22, P31, B11, B21')
wumpus_kb.tell(B11 | '<=>' | ((P12 | P21)))
wumpus_kb.tell(B21 | '<=>' | ((P11 | P22 | P31)))
wumpus_kb.clauses
wumpus_kb.ask_if_true(~P22)
```

## OUTPUT:
### clauses
![image](https://user-images.githubusercontent.com/75235488/175973491-593b9b3f-5dad-460f-afd1-768dfec9e62f.png)

### check pit
![image](https://user-images.githubusercontent.com/75235488/175973840-f194470d-acea-42c7-9fcb-ddc25a4b3e17.png)

## RESULT
Thus, the developed agent can predict the next move in the wumpus game using propositional logic sentences .
