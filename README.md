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

### Objective

The goal is to prove that if two graphs, $\(A\)$ and $\(B\)$, are both fully connected (meaning every node connects to all others) and have the same number of nodes, they must be isomorphic.

### Formal Definition of Isomorphism

Two graphs $G_1=(V_1, E_1)$ and $G_2=(V_2, E_2)$ are isomorphic if there exists a bijection $f: V_1 \rightarrow V_2$ such that for any pair of vertices $(u,v) \in E_1$, it is true that $(f(u),f(v)) \in E_2$, and vice versa.

### Assuming the Opposite

We can start by assuming $\(G_1\)$ and $\(G_2\)$ are not isomorphic, despite being fully connected and having an equal number of nodes. This means we're saying there's no possible bijection between their nodes that keeps the connections intact.

### Understanding Full Connectivity

In fully connected graphs, every node connects to every other node. So, if there are $n$ nodes, each node connects to $n−1$ other nodes

### Finding the Contradiction

Given both $\(G_1\)$ and $\(G_2\)$ are fully connected with the same number of nodes $(n)$:

- Trying to pair any node from $G_1$ with any node from $\(G_2\)$ must maintain all connections due to the full connectivity. Every node has a connection with every other node, making mismatch impossible.
  
- This leads us to a contradiction of our initial assumption. Since both graphs are fully connected, with each node linked to every other, there's essentially only one pattern their connections can follow. This inherent property of full connectivity ensures the existence of a bijection $f$, a perfect one-to-one match between the nodes of $\(G_1\$ and $\(G_2\)$, that maintains this pattern. Our original assumption, doubting that such a bijection could exist, is contradicted by the nature of full connectivity. As it guarantees any bijection $f$ will keep the universal pattern of connections, clearly proving the graphs are isomorphic.

### Proving the Contradiction with a Mapping Example:
  
Imagine two fully connected graphs, $G_1$ and $G_2$, each with three nodes: $G_1$ has nodes $A$, $B$, and $C$, while $G_2$ has nodes $X$, $Y$, and $Z$. In a fully connected graph, every node is linked to every other node. So, in $G_1$, $A$ is connected to $B$ and $C, B$ is connected to $A$ and $C$, and $C$ is connected to $A$ and $B$. The same pattern of connectivity exists in $G_2$ among $X$, $Y$, and $Z$.

To establish a bijection $f$ for isomorphism, we pair each node in $G_1$ with a node in $G_2$. For example, let's say our mapping $f$ pairs them as follows: $f(A) = X$, $f(B) = Y$, and $f(C) = Z$.

Here's the crucial point: Because $G_1$ and $G_2$ are fully connected, the way we pair $A$, $B$, $C$ with $X$, $Y$, $Z$ will always preserve the complete connectivity and ensure that a bijection is inevitable. Any pairing will maintain the connectivity because, in both $G_1$ and $G_2$, every node is connected to every other node. So, when we map $A$ to $X$ (meaning $A$ corresponds to $X$), and since $A$ was connected to both $B$ and $C$, $X$ will similarly be connected to $Y$ and $Z$ in $G_2$, preserving the connectivity pattern. This preservation of connectivity holds true for every mapping we choose due to the complete connectivity of both graphs.

Through this example it becomes evident that the property of complete connectivity in both $G_1$ and $G_2$ not only simplifies the establishment of a bijection $f$ but also ensures its existence. Since every node in a fully connected graph is linked to every other node, any one-to-one pairing of vertices between $G_1$ and $G_2$ will naturally maintain all the required edge connections. This aspect of complete connectivity makes the preservation of bijection automatic, irrespective of how the vertices are paired.


## Conclusion

The assumption that two fully connected graphs with the same number of nodes could not be isomorphic contradicts the inherent property of full connectivity. This property guarantees that a bijection $f$ that preserves connectivity must exist, proving the two graphs are isomorphic. Thus, if two graphs are fully connected and have an equal number of nodes, they inherently satisfy the conditions for isomorphism, showing they share the same structural connectivity.


