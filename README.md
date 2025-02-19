# Math problems I solved with numerical methods

### Win Streak
Estimates the probability of achieving a winning streak in a binomial game, measures the execution time, then plots it. The classical description is exponential, and this solution does it dynamic to make it O(logn). In practise, I only manage to show the early parts of the logn so it looks O(n). Lesson learnt: O(logn) is in practise often simply O(n) in a slow program like Python and stack-overflows are horrible so avoid recursion.

### NP-Reduction

CASTING for a movie looks like the coloring problem if each edge is a scene and we only got two roles in each scene.
So I try that. Edges are scenes, and then, I don't think it matters which in order to create a reduction but,
I picked that nodes are roles and colors are specific actors.

The differences between the TV-casting problem and the Coloring problem are:
1. CASTING can't deal with monologues. However, these are automatically fixed in the coloring problem so I will
simply filter them out without causing a problem in the yes to yes equivelence. This will require me to re-index
the edges for the casting problem, so we do that starting from 1.

2. CASTING has two divas that can't cooperate. I will just filter that out as well by giving them roles immediatly
and then solving the problem. If I then only work with the rest of the possible actors the diva complexity doesn't
affect the rest of the problem.

Hence a TV-casting task reduced to the NP-hard coloring problem. This program solves such a problem. 

So:
edges = scenes
nodes = roles
colors = actors

And here is the reduction detailed in math:
https://docs.google.com/document/d/1uFP9dpM9Oza34r1YjZ0rV6NIeXD-UdWxXWjZNtIJeE4/edit
