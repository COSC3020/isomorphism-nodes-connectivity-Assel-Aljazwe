[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/ppBU16qM)
# Isomorphism

Prove that if two graphs $A$ and $B$ have the same number of nodes and are
completely connected, they must be isomorphic. I have started with the formal
definition of isomorphism below. Add your answer to this markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$G_1=(V_1 , E_1)$ is isomorphic to $G_2 = (V_2, E_2)$ if there exists a
one-to-one and onto function (bijection) $f: V_1 \rightarrow V_2$ such that $(u,v)
\in E_1$ iff $(f(u),f(v)) \in E_2$.

# Proof:
## Proof by Contradiction: Complete Connectivity Implies Isomorphism

To prove that two completely connected graphs $A$ and $B$, each with the same number of nodes, are isomorphic, we can utilize a proof by contradiction based on the formal definition of graph isomorphism.

### Formal Definition of Isomorphism

Two graphs $G_1=(V_1, E_1)$ and $G_2=(V_2, E_2)$ are isomorphic if there exists a bijection $f: V_1 \rightarrow V_2$ such that for any pair of vertices $(u,v) \in E_1$, it is true that $(f(u),f(v)) \in E_2$, and vice versa.

### Assumption for Contradiction

Assume that two completely connected graphs $G_1$ and $G_2$, each with the same number of nodes, are not isomorphic despite having a bijection $f: V_1 \rightarrow V_2$.

### Analysis of the Assumption

- **Complete Connectivity**: By definition, in completely connected graphs (or complete graphs), there is an edge between every pair of distinct vertices. Therefore, for each graph with $n$ nodes, every node is connected to $n-1$ other nodes, resulting in $\frac{n(n-1)}{2}$ edges in total.

- **Identifying Contradiction**: Considering that both $G_1$ and $G_2$ are fully connected, and assuming a bijection $f$ exists; the nature of a fully connected graph implies that if there's a connection (edge) between two nodes $(u,v)$ in $G_1$, then there must be a matching connection between their counterparts $(f(u),f(v))$ in $G_2$. This is because in a fully connected graph, all nodes are linked to each other, which is true for both $G_1$ and $G_2$. 

  - **Why They Must Be Isomorphic**: This shows that the initial assumption of non-isomorphism contradicts the properties of complete connectivity and bijection. If two graphs are not isomorphic, it means you can't match up their nodes in a way that keeps all the connections between nodes the same in both graphs. The features of complete graphs and the definition of bijection ensure that the adjacency relationship is preserved (keeping connections between nodes the same when mapping from one graph to another), which is the primary condition for isomorphism.

### Conclusion

The assumption that two completely connected graphs with the same number of nodes are not isomorphic leads to a contradiction when considering the implications of complete connectivity and bijection. Therefore, such graphs must be isomorphic, proving that if two graphs have the same number of nodes and are completely connected, they inherently satisfy the conditions for isomorphism.

