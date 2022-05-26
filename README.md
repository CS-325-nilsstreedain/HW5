# HomeWork 5

1.  (7 pts) Let X and Y be two decision problems. Suppose we know that X reduces to Y in polynomial time. State whether the following statements are true or false and give a brief explanation. 
    - If Y is NP-complete then so is X.
    - If X is NP-complete then so is Y.
    - If Y is NP-complete and X is in NP then X is NP-complete.
    - If X is NP-complete and Y is in NP then Y is NP-complete.
    - If X is in P, then Y is in P.
    - If Y is in P, then X is in P.
    - X and Y can't both be in NP.

2. (3 pts) Two well-known NP-complete problems are 3-SAT and TSP, the Traveling Salesman Problem. The 2-SAT problem is a SAT variant in which each clause contains at most two literals.  2-SAT is known to have a polynomial-time algorithm.  State whether the following statements are true or false and give a brief explanation.
    - 3-SAT ≤p TSP.
    - If P != NP, then 3-SAT ≤p 2-SAT.
    - If TSP ≤p 2-SAT, then P = NP. 

3. (10 pts) A Hamiltonian path in a graph is a simple path that visits every vertex exactly once.  Show that HAM-PATH = { (G, u, v ): there is a Hamiltonian path from u to v in G }  is NP-complete.  You may use the fact that HAM-CYCLE is NP-complete.

4. (10 pts) K-COLOR.  Given a graph G = (V,E), a k-coloring is a function c: V -> {1, 2, ... , k} such that c(u) c(v) for every edge (u,v)  E.  In other words the number 1, 2, .., k represent the k colors and adjacent vertices must have different colors.  The decision problem K-COLOR asks if a graph can be colored with at most K colors.

The 3-COLOR decision problem is NP-complete by using a reduction from SAT. Use the fact that 3-COLOR is NP-complete to prove that 4-COLOR is NP-complete. 
