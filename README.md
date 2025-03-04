Projet de 4 eme année d'optimisation en python

**1 Preamble**

This project replicates a task assigned during a technical interview, as part of a recruitment
process for a major French company. The goal was to secure a position as a Research Engineer in
Data Science & Optimization. The task was given to the candidate four days before a technical
interview with the company’s expert panel. During this time, the candidate was expected to
familiarize themselves with the problem, define it formally, and develop effective solutions based
on AI algorithms.

The project mirrors the information and resources provided to the candidate, without adding
any additional elements beyond the original task description.

The question now is : Can you rise to the challenge of this recruitment phase and secure a position
at this prestigious French company by applying the knowledge and skills you’ve gained from the
AI algorithms course ?
1




**2 Problem Description**


A biscuit manufacturing factory is planning to produce a series of biscuits for Christmas. Using
the same roll of dough, the factory aims to create various biscuits of different sizes and shapes.
The goal is to maximize biscuit production from a single roll while ensuring the highest possible
profit.
To achieve this goal, we have the following information :

— The roll of dough has a predefined rectangular length, referred to as ’LENGTH’, representing a one-dimensional problem.

— The roll may contain irregularities, referred to as defects. Each defect has

— a position ‘x‘

— and a class, which could be one of several types (e.g., ’a’, ’b’, ’c’, ...).

— The factory aims to produce a set of biscuits. Each Biscuit can be produced an infinite
number of times, and has :

— a specific size (along the same dimension as the roll)

— a value (price)

— and a threshold for the maximum number of defects of each class it can contain (otherwise it cannot be marketed).
A solution is defined as an arrangement of biscuits along the dough roll. For an arrangement
(assignment) to be valid, it must satisfy the following conditions :

— Biscuits must be placed at integer positions.

— No overlapping of biscuits is allowed. For example, if you place a biscuit B1 of size 3 at
position ‘x=2‘, no other biscuit can be assigned to positions ‘x=3‘ or ‘x=4‘.

— Each biscuit placed must contain fewer defects (or an equal number) of each class than
its permitted thresholds. For instance, if biscuit B1 of size 3 is placed at ‘x=2‘, it covers
positions 2, 3 and 4. If there are 3 defects of class ’a’ in these positions, but B1’s threshold
for class ’a’ is a maximum of 2 defects, then the assignment is invalid.

— The total size of the assigned biscuits must not exceed the length of the dough roll.
The value of a solution is the sum of the individual values of the biscuits placed on the roll.
However, any portion of the dough roll without an assigned biscuit incurs a penalty of −1 per
position, reflecting the company’s loss from wasted material. This penalty is subtracted from the
overall value of the solution.


**Benchmark**

For this project, the following assumptions are made :
— The length of the roll of dough is set to 500 units.
— The roll has three classes of defects (’a’, ’b’, and ’c’). The set of defects and their positions
on the roll are available in the ’defects.csv’ file.
— The biscuit manufacturing factory aims to produce 4 types of biscuits :
— Biscuit 0 with a length of 4, a value of 3, and maximum allowed defects as {
′a
′
: 4,
′
b
′
:
2,
′
c
′
: 3}
— Biscuit 1 with a length of 8, a value of 12, and maximum allowed defects as {
′a
′
:
5,
′
b
′
: 4,
′
c
′
: 4}
— Biscuit 2 with a length of 2, a value of 1, and maximum allowed defects as {
′a
′
: 1,
′
b
′
:
2,
′
c
′
: 1}
— Biscuit 3 with a length of 5, a value of 8, and maximum allowed defects as {
′a
′
: 2,
′
b
′
:
3,
′
c
′
: 2}
