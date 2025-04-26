# Social Networks

## Basics

- Diameter of a graph is the largest distance between any two vertices.
- BFS is better to find the shortest distance in a social network between two nodes/vertices.
- There is a high probability to encounter a large community when:
  - average degree is 1.
  - edge probability is large enough.
- Adjacency-List is best for sparse graphs, and also easy to traverse the neighbors.

## NetworkX Library

- nx.Graph()
  - Creates a undirected graph.
- nx.DiGraph()
  - Creates a directed graph.
- nx.MultiGraph()
  - Creates a multigraph (a graph where two nodes can have multiple edges).

## Gephi

- Modularity is used to determine connectivity between communities.

## Algorithms and Models

### Page Rank Algorithm

- Pages that are linked to more often are more important.

#### Link Prediction

- Predicting what will the current page will link to next.
- Link Prediction is done with Jaccard Similarity Index.

### Grivan-Newman Algorithm

- Used to find communities in a graph.
- It works by removing edges from the graph and checking the connectivity of the graph.
- Monke see edge with high betweenness centrality, Monke remove it.

### Fatman Evolutionary Model

- A model that simulates the evolution of a social network.
- It is based on the idea that individuals in a social network are constantly forming and breaking connections with each other.
- The preferential attachment is driven by,
  - The degree of existing nodes.
  - The relative fitness of new nodes.

## Granovetter's Theory

- Weak ties are more important than strong ties.
- Strong ties are usually friends and family.
- Weak ties are acquaintances.
- We can get more information from weak ties than strong ties.

## Web Graph Model

- Nodes: Web Pages.
- Edges: Hyperlinks Between Pages.

## Closures

### Triad Closure

- When one person has two friends, it is highly likely that the other two become friends.

### Foci Closure

- When two people have a common activity, they are likely to become friends.

## Neighborhood Overlap

- Common neighbors that two nodes share.

## Bridge

- An edge connecting two components.

### Local Bridge

- Connects two nodes that have fewer or no connections between them or their neighbors.

### Structural Hole

- A gap between two components that aren't connected.
- Usually a BROKER helps in transfer of knowledge.

## Social Capital

- The resources that are available to an individual through their social network.
- It can be used to gain access to information, opportunities, and support.

## Embeddedness

- If stranger meets, NO
- If stranger already knew some of our friends, YES
- The degree to which a relationship is supported by other relationships.

## Betweenness Centrality

- The number of times a node acts as a bridge along the shortest path between two other nodes.
- It is used to find the most important nodes in a network.
- The formula is:

  $$
  Betweenness Centrality = \sum_{i \neq j} \frac{\sigma_{st}(v)}{\sigma_{st}}
  $$

  where:

  - $v$ is the node.
  - $\sigma_{st}$ is the number of shortest paths from node $s$ to node $t$.
  - $\sigma_{st}(v)$ is the number of shortest paths from node $s$ to node $t$ that pass through node $v$.

## Homophily Index

- The tendency of individuals to associate and bond with similar others.
- The formula is:

  $$
  Homophily Index = \frac{\text{No of similar connections}}{\text{Total connections}}
  $$

  where:

  - $i$ and $j$ are the nodes.
  - $\text{edges}$ is the number of edges between the two nodes.
  - $\text{degree}(i)$ is the degree of node $i$.
  - $\text{degree}(j)$ is the degree of node $j$.
