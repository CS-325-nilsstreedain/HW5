# HomeWork 5

1.  (7 pts) Let X and Y be two decision problems. Suppose we know that X reduces to Y in polynomial time. State whether the following statements are true or false and give a brief explanation. 
- If Y is NP-complete then so is X.
```
False: Since X is not harder than Y, Y being NP-Complete does not determine X.
```
- If X is NP-complete then so is Y.
```
False: Since Y can be reduced to X but X cannot be reduced to Y, Y cannot be
NP-Complete
```
- If Y is NP-complete and X is in NP then X is NP-complete.
```
False: X being reducible to Y with Y NP-Complete doesn’t necessarily mean X is
NP-Complete
```
- If X is NP-complete and Y is in NP then Y is NP-complete.
```
True: Since X is not harder than Y and X is NP-Complete, meaning Y is al least
as hard as NP-Complete, and Y is NP, so Y is NP-Complete.
```
- If X is in P, then Y is in P.
```
False: Since X is not harder than Y, Y can be harder than X so Y is not
necessarily in P.
```
- If Y is in P, then X is in P.
```
True: Since X is not harder than Y, if Y is in P, then X will as well.
```
- X and Y can't both be in NP.
```
False: Both can be NP when X & Y are the same difficulty, or if Y is harder.
```

2. (3 pts) Two well-known NP-complete problems are 3-SAT and TSP, the Traveling Salesman Problem. The 2-SAT problem is a SAT variant in which each clause contains at most two literals.  2-SAT is known to have a polynomial-time algorithm.  State whether the following statements are true or false and give a brief explanation.
- 3-SAT ≤p TSP.
```
True: All NP problems can be solved in polynomial time if one can, TSP is NP and
3-SAT is NP-Complete so it can be solved in polynomial time.
```
- If P != NP, then 3-SAT ≤p 2-SAT.
```
False: If 3-SAT is NP-Complete and 3-SAT ≤p 2-SAT, then NP problems can be
reduced to 2-SAT. 2-SAT is polynomial, meaning that NP problems are polynomial
and P = NP which contradicts P ≠ NP
```
- If TSP ≤p 2-SAT, then P = NP. 
```
True: If TSP is NP-Complete and TSP ≤p 2-SAT, then NP problems can be reduced to
3-SAT ≤p 2-SAT. 2-SAT is polynomial, meaning that NP problems are polynomial and
P = NP.
```

3. (10 pts) A Hamiltonian path in a graph is a simple path that visits every vertex exactly once.  Show that HAM-PATH = { (G, u, v ): there is a Hamiltonian path from u to v in G }  is NP-complete.  You may use the fact that HAM-CYCLE is NP-complete.
```
Validating that there is a simple path visiting every vertex in a HAM-PATH
solution takes O(# of vertices) so HAM-PATH is NP. There will always be a
HAM-PATH in a graph with a HAM-CYCLE, but there may not be a HAM-CYCLE in a
graph with a HAM-PATH, meaning HAM-PATH is at least as hard as HAM-CYCLE.
Because of this and that HAM-CYCLE is NP-Complete, HAM-PATH is NP-Complete.
```

4. (10 pts) K-COLOR.  Given a graph G = (V,E), a k-coloring is a function c: V -> {1, 2, ... , k} such that c(u) c(v) for every edge (u,v)  E.  In other words the number 1, 2, .., k represent the k colors and adjacent vertices must have different colors.  The decision problem K-COLOR asks if a graph can be colored with at most K colors.
The 3-COLOR decision problem is NP-complete by using a reduction from SAT. Use the fact that 3-COLOR is NP-complete to prove that 4-COLOR is NP-complete. 
```
To prove 4-COLOR is NP-Complete, 4-COLOR must be both NP and NP-Hard.

1.  4-COLOR is NP because each edge can be checked whether the color on each of
it’s ends is different. When no edges have the same color, the graph is 4-COLOR.
Therefore, 4-COLOR is NP-Hard.

2. Next, 3-COLOR is NP because it is NP-Complete. 4-COLOR can be proved by
reducing 3-COLOR to 4-COLOR. The graph G can be reduced to graph G` where G is
3-COLOR and G` is 4-COLOR. G` can be created by adding a new vertex to G
connected to each vertex already in the graph. Because this vertex is connected
to all the others, it must be a new color so two colors are not next to each
other, therefore turning a 3-COLOR graph into a 4-COLOR graph. Meaning if G` is
4-COLOR, G just be 3-COLOR, proving that 4-COLOR is NP-Hard.

Because 4-COLOR is NP and NP-Hard, it is NP-Complete.
```
