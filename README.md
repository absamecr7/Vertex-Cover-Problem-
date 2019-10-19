# Vertex-Cover-Problem-
  Python program implementation of vertex cover problem, using greedy approach.


**Description**

  Formally, a vertex-cover of an undirected graph G=(V,E) is a subset V′ of V such that if edge (u, v) is an edge of G, then u is in V′, or v is in V′, or both. The set V′ is said to "cover" the edges of G.
A minimum vertex cover is a vertex cover of smallest possible size. The vertex cover number, denoted by greek symbol "tau" is the size of a minimum vertex cover. 

Finding a smallest vertex cover is classical optimization problem and is an NP-hard problem. 


###Input:###

  An undirected graph G(V,E).
  ```
  graph = [[0, 1, 1, 0],
             [1, 0, 1, 1],
             [1, 1, 0, 1],
             [0, 1, 1, 0]]
  ```


###Algorithm:###

```
    Greedy approach to find vertex cover set:
      Greedy algorithm always takes the vertex with the highest degree, add it to the cover set, remove it from the graph, and repeats.
    
    def greedy(E, V)
      C = []
      while E not empty:
          select any edge with endpoints (u,v) from E
          add (u,v) to C
          remove all edges incident to u or v from E
      return C
      
    Basically, the algorithm works by finding a maximal matching in GG and adding at least one endpoint of each edge to the covering        set of vertices CC. The optimal answer will contain one vertex from each edge in the matching, but a suboptimal covering could          contain both endpoints from each edge, so the covering set CC could be as much as two times as big as the optimal answer. This          algorithm can be adapted to handle weighted graph
      
```


###Output:

  A vertex cover set(one in our case, although there can be many).
  ```
  [1, 2]
  ```
  
###Complexity: ###

  This is a polynomial time approximation algorithm (since it isn't guaranteed to return the optimal vertex cover) that runs                in O(V + E)O(V+E) time.


###Applications: ###

  Some problems that use ideas of vertex cover have additional and/or modified constraints compared to vertex cover. Travelling Salesman is a problem that uses a fairly straight-forward vertex cover approach.



  
